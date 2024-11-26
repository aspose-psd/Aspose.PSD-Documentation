---
title: Gegevensverwerking van ruwe data
type: docs
weight: 70
url: /nl/java/raw-data-processing/
---

## **Gegevensverwerking van ruwe data**
Om de prestaties van de Aspose.PSD API te verbeteren hebben we een methode voor gegevensverwerking van ruwe data geïntroduceerd met versie 2.4.0. De gegevensverwerking van ruwe data wordt nu intern gebruikt en heeft een externe API zodat het van buiten de bibliotheek kan worden gebruikt om de algehele prestaties te verbeteren. Soms kan de verwerking wat ingewikkeld zijn en uitleg nodig hebben. Gegevensverwerking van ruwe data is momenteel alleen beschikbaar voor het BMP-formaat.

Om ontwikkelaars te helpen om de beste prestaties te behalen, biedt de Aspose.PSD API een gegevensverwerkingssysteem van ruwe data met een externe API voor aanpassingen. Ontwikkelaars roepen de LoadRawData- en SaveRawData-methoden aan om de gegevensverwerking van ruwe data te gebruiken. Deze methoden vereisen ook dat het gewenste formaat van ruwe data wordt ingesteld met behulp van de RawDataSettings-klasse. De RawDataSettings-klasse stelt ontwikkelaars in staat om elk formaat van ruwe data te specificeren. Echter, om de beste prestaties te bereiken moet je het ruwe dataformaat gebruiken waarin de data is opgeslagen. De RawDataSettings gedefinieerd in de RasterImage-klasse helpen bij het bepalen van het ruwe dataformaat van de afbeelding. Wanneer je een instantie van RawDataSettings doorgeeft aan de LoadRawData-methode, wordt de data teruggegeven zoals het is, zonder enige conversie toegepast en dit kan de prestaties verbeteren. Aan de andere kant, moet je zorgen voor alle mogelijke lay-outs van ruwe dataformaten die soms een beetje ingewikkeld kunnen zijn.

Om het verwerkingsproces te vereenvoudigen, tegen een prestatieverlies, kun je het gewenste RawDataSettings specificeren door de klasse te instantiëren en te initialiseren met de gewenste ruwe data-instellingen. Er zijn gevallen waarin het niet mogelijk is om de ruwe data terug te sturen in het gespecificeerde formaat (bijvoorbeeld conversie van CMYK-kleurruimte naar RGB is niet beschikbaar in versie 2.4.0). Bovendien kunnen er zich situaties voordoen waarbij gegevensverwerking van ruwe data helemaal niet beschikbaar is voor een bepaald afbeeldingsformaat. Om te bepalen of je de familie van LoadRawData- en SaveRawData-methoden kunt gebruiken, moet je de eigenschap IsRawDataAvailable raadplegen.
### **Inzicht**
Voor het RGB-pixeldataformaat zijn er geïndexeerde (palet-gebaseerde) en op RGB gebaseerde ruwe dataformaten beschikbaar. Geïndexeerde ruwe dataformaten bevatten paletvermeldingen in het bereik van 0..(2 ^ bis count - 1). De geïndexeerde ruwe dataformaten zijn 1, 2, 4 en 8 bits per pixel. De rest zijn op RGB gebaseerde ruwe dataformaten. Bij het laden van ruwe data, zorg ervoor dat er voldoende bytes beschikbaar zijn om de data te laden, anders wordt er een passende uitzondering gegenereerd. Je kunt eenvoudig de grootte van de byte-array schatten door de regelgrootte te vermenigvuldigen met het aantal benodigde regels. De regelgrootte kan variëren en is afhankelijk van het ruwe dataopslagformaat.

Om de beste prestaties te behalen, gebruik altijd een regelgrootte van ruwe data gelijk aan de waarde van de RasterImage.RawLineSize-eigenschap. Soms kan het nodig zijn om extra opvulling aan de ruwe datarijen toe te voegen, of verminderen, in welk geval een andere regelgrootte kan worden gebruikt. Als een subset van een afbeeldingsomgrenzingsrechthoek vereist is, houd dan rekening met de bitverschuivingen die kunnen optreden voor geïndexeerde RGB-pixelformaten. Stel bijvoorbeeld dat je een afbeelding hebt met de afmetingen van 100x100 pixels en een ruw dataformaat van 1 bit per pixel. Je wilt een rechthoek met ruwe data laden met de locatie (7,0) en afmetingen (2,1), of met andere woorden, je wilt 2 pixels ontvangen vanaf x=7 en y=0. In dit geval zou je de volgende gegevenslay-out moeten ontvangen:




![todo:image_alt_text](raw-data-processing_1.png)

Dit betekent dat je 2 bytes ontvangt waarbij de eerste byte 7 ongewenste pixels bevat, dan 1 gewenste pixel, en de tweede byte bevat 1 gewenste pixel en dan 7 ongewenste. Je zou je afvragen waarom we geen gegevensverschuiving hebben uitgevoerd en die 2 pixels in één byte hebben geplaatst? Het antwoord is eenvoudig: om de prestaties hoog te houden. Alle interne verwerking wordt typisch uitgevoerd met alle data beginnend vanaf de eerste pixel en eindigend met de laatste beschikbare pixel. Er zijn zelden situaties wanneer een subset van pixels nodig is. Bovendien hebben we geen idee hoe die pixels naderhand zullen worden verwerkt, dus een verschuiving zou de prestaties verminderen en de code onnodig complex maken. Schat altijd het juiste bit in (je hoeft niet het juiste byte te bepalen omdat de data altijd wordt geleverd met het eerste byte gevuld) waar de gevraagde pixels zullen beginnen. Om het juiste bit te berekenen kan een eenvoudige formule worden gebruikt: (rect.Left * bitsCount) % 8.
### **Omzetting van geïndexeerde RGB-kleuren**
Om de hoogst mogelijke prestaties te behalen, gebruik altijd dezelfde bron- en bestemmingsruwe data-instellingen, pixelformaten en regelgroottes. Soms moet je echter wellicht gegevensconversie uitvoeren. Bijvoorbeeld, je kunt een RGB-afbeelding met 1 bit per pixel laden en deze opslaan met 2 bits per pixel, of een 4-bits RGB-afbeelding laden en de kleurbereik verlagen naar 2 bits per pixel. In beide gevallen moet er een kleurconversie worden toegepast. Het omzetten van geïndexeerde RGB-afbeeldingen kan soms ingewikkeld zijn en kan niet worden uitgevoerd zonder enkele toegepaste instellingen. We moeten bepalen hoe het bronkleurbereik is gemapt naar de doelkleurruimte. Om deze taak te volbrengen hebben we verschillende modi:

- Palet mapping (DitheringMethods.PaletteConversion)
- Ruwe data mapping (DitheringMethods.PaletteIgnore)
- Aangepaste conversie (DitheringMethods.CustomConverter)

Bij het gebruik van paletconversie probeert de bronkleurruimte zo goed mogelijk overeen te komen met de doelkleurruimte. Laten we bijvoorbeeld aannemen dat we een 4-bits afbeelding hebben met de volgende kleuren:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

De bronafbeelding ziet er als volgt uit:




![todo:image_alt_text](raw-data-processing_2.png)

En we zetten de 4-bits afbeelding om naar de 1-bits afbeelding met de volgende gedefinieerde paletkleuren:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Bij de paletconversiemodus leest de converter de bronkleur en bepaalt het doelindex met behulp van de GetNearestColorIndex-methode van het doelpalet. De eigenschapswaarde RasterImage.RawFallbackIndex wordt gebruikt in het geval dat de GetNearestColorIndex-methode van het palet een index buiten bereik geeft. Dit zet de bronkleuren om naar de dichtstbijzijnde doelkleuren in termen van intensiteitswaarden. De doelafbeelding komt zo dicht mogelijk overeen met de bronafbeelding. Je kunt het volgende resultaat zien:




![todo:image_alt_text](raw-data-processing_3.png)

Bij de 'ruwe data mapping' modus wordt een ander scenario gebruikt. Het bron- en doelpalet worden eenvoudig genegeerd en de bronindexes worden gemapt naar de doelindexes. Wanneer een waarde wordt gevonden die niet kan worden gemapt naar het doelbereik (bij het verlagen van het aantal bits), wordt de eigenschapswaarde RasterImage.RawFallbackIndex gebruikt. De waarde is standaard 0 en zal worden gemapt naar de eerste kleur in het doelpalet. Als deze eigenschapswaarde buiten het doelbereik ligt, wordt er een gepaste uitzondering gegenereerd. Dit leidt tot minder voorspelbare resultaten die worden getoond op de volgende afbeelding:




![todo:image_alt_text](raw-data-processing_4.png)

De paletconversiemodus is een nauwkeurigere oplossing voor het kleurenprobleem, maar het duurt ook iets langer om te voltooien omdat er berekeningen moeten worden uitgevoerd om de juiste paletmapping te schatten. (Er is over het algemeen een zeer klein prestatieverschil tussen de twee methoden.) Aan de andere kant presteert de raw mapping-modus een beetje sneller en kan worden gebruikt voor ruwere kleurconversie wanneer exacte kleurmapping niet zo belangrijk is. Bijvoorbeeld, er zijn gevallen waarin het bronkleurpalet wordt ingekort en veilig kan worden omgezet naar minder bit-tellingen omdat de extra bits toch niet zijn gebruikt.

Om een van deze benaderingen te gebruiken, gebruik de RawDitheringMethod-eigenschap van de RasterImage-klasse. Standaard staat deze ingesteld op de paletconversiemethode om de beste resultaten te behalen. Je kunt deze eigenschap wijzigen voordat elke conversie plaatsvindt (bijvoorbeeld bij het opslaan van een afbeelding naar een stream). Let op dat de palet-ignore en palet conversie-ditheringmethoden niet worden toegepast als je een afbeelding hebt geladen en een deel van de originele pixeldata hebt herschreven, aangezien de nieuwe gegevens in de cache worden opgeslagen en de cache de gegevens in het maximale beschikbare formaat 32ARGB bewaart (zoals vanaf versie 2.4.0, kan onderhevig zijn aan verandering). Dit formaat wordt gebruikt om problemen te overwinnen met mogelijke verschillende kleurbereiken voor geladen en opgeslagen afbeeldingen. Bovendien worden de paletignore- en paletconversie-ditheringmethoden genegeerd wanneer een afbeelding in RGB-modus wordt geladen en wordt geconverteerd naar geïndexeerde modus of vice versa.
### **Aangepaste Kleurconverters**
Soms is het niet voldoende om de standaardbenadering voor kleurconversie te gebruiken. Mogelijk wilt u een aangepast algoritme gebruiken om volledige vrijheid te hebben bij het gebruik van kleurconversieroutines. Wanneer de bron- en doelafbeeldingspixelformaten beide geïndexeerde RGB-formaten zijn, kan een eenvoudigere interface, IIndexedColorConverter, worden gebruikt. Stel de RasterImage.RawIndexedColorConverter-eigenschap in op een instantie van de IIndexedColorConverter-interface en gebruik de waarde DitheringMethods.CustomConverter voor de RawDitheringMethod-eigenschapswaarde. Wanneer deze combinatie wordt toegepast, gaat elke geïndexeerde kleurconversie via die gespecificeerde IIndexedColorConverter-instantie. De aangepaste geïndexeerde kleurconverter heeft de volgende methode gedefinieerd:

{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}

De FillIndexedtoIndexedMap-methode wordt aangeroepen wanneer conversie vereist is van geïndexeerde RGB-afbeelding naar geïndexeerde RGB-afbeeldingsformaat (wanneer een van de 1, 2, 4 of 8 bit-tellingen naar elkaar worden omgezet). De maparray heeft de lengte van alle mogelijke ingangen van het bronformaat. Je moet dat array vullen om de mapping van de bronkleurpaletinvoer naar de doelkleurpaletinvoer te maken. Zorg ervoor dat de doelinvoerwaarde in het bereik van 0..(bitsteller - 1) ligt, anders wordt er een passende uitzondering gegenereerd.

Als de vereiste is om een meer aangepast kleurconversiescenario uit te voeren, moet de RasterImage.RawCustomColorConverter-eigenschap worden ingesteld op een instantie van de IColorConverter-interface. De RawCustomColorConverter-eigenschap vervangt altijd de RawIndexedColorConverter-eigenschap als beide zijn ingesteld en er zal in dat geval geen geïndexeerde kleurconverter worden gebruikt. De IColorConverter heeft een enkele methode:

{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}

De Convert-methode wordt elke keer aangeroepen wanneer kleurconversie nodig is. De methode ontvangt de bronruwe data in het bronformaat en heeft een uitvoerbuffer om de kleur geconverteerd naar de bestemming te ontvangen. De doelbuffer moet voldoende zijn om de geconverteerde data te ontvangen (als de interfaceoproep intern door de Aspose.PSD-bibliotheek wordt gemaakt) en moet de geconverteerde ruwe data bevatten bij het retourneren van de methode. De Convert-methode kan meerdere keren worden aangeroepen totdat de hele brondata is verwerkt.