---
title: Gegevensverwerking
type: docs
weight: 50
url: /nl/gegevensverwerking-ruw/
---

## **Gegevensverwerking**
Om de prestaties van de Aspose.PSD API te verbeteren, hebben we een methode voor ruwe gegevensverwerking geïntroduceerd met versie 2.4.0. De ruwe gegevensverwerking wordt nu intern gebruikt en heeft een externe API, zodat deze van buiten de bibliotheek kan worden gebruikt om de algehele prestaties te verbeteren. Soms kan de verwerking wat lastig zijn en uitleg vereisen. Ruwe gegevensverwerking is momenteel alleen beschikbaar voor het BMP-formaat.

Om ontwikkelaars te helpen de beste prestaties te behalen, biedt de Aspose.PSD API een ruwe gegevensverwerkingssysteem met een externe API voor aanpassing. Ontwikkelaars roepen de [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) en [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) methodefamilie aan om ruwe gegevensverwerking te gebruiken. Deze methoden vereisen ook dat het gewenste ruwe gegevensformaat wordt ingesteld met behulp van de [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings) klasse. De RawDataSettings-klasse stelt ontwikkelaars in staat om elk ruwe gegevensformaat te specificeren. Voor de beste prestaties moet je echter het ruwe gegevensformaat gebruiken waarin de gegevens zijn opgeslagen. De RawDataSettings gedefinieerd in de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) klasse helpt bij het bepalen van het ruwe [gegevensformaat](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings/properties/pixeldataformat) van de afbeelding. Wanneer je de RawDataSettings-instantie doorgeeft aan de LoadRawData-methode, worden de gegevens geretourneerd zoals ze zijn, zonder enige conversie toegepast, en dit kan de prestaties verbeteren. Aan de andere kant moet je letten op alle mogelijke lay-outs van ruwe gegevensindeling, wat soms wat ingewikkeld kan zijn.

Om het verwerkingsproces te vereenvoudigen, ten koste van een prestatieverlies, kun je de gewenste RawDataSettings specificeren door de klasse te instantiëren en initialiseren met de gewenste ruwe gegevensinstellingen. Er zijn gevallen waarin het niet mogelijk is om de ruwe gegevens in het gespecificeerde formaat terug te geven (bijvoorbeeld conversie van CMYK-kleurenspace naar RGB is niet beschikbaar in versie 2.4.0). Bovendien kunnen er situaties zijn waarin ruwe gegevensverwerking helemaal niet beschikbaar is voor een afbeeldingsformaat. Om te bepalen of je de LoadRawData- en SaveRawData-methodenfamilie kunt gebruiken, moet je de [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable) eigenschap raadplegen.
### **Inzicht**
Voor RGB [pixelgegevensformaat](https://reference.aspose.com/psd/net/aspose.psd/pixeldataformat) zijn geïndexeerde (paletgebaseerde) en op RGB gebaseerde ruwe gegevensformaten beschikbaar. Geïndexeerde ruwe gegevensformaten bevatten paletvermelding indexen in het bereik van 0..(2^bis count - 1). De geïndexeerde ruwe gegevensformaten zijn 1, 2, 4 en 8 bits per pixel. De rest zijn op RGB gebaseerde ruwe gegevensformaten. Bij het laden van ruwe gegevens moet je ervoor zorgen dat er voldoende bytes beschikbaar zijn om de gegevens te laden, anders wordt er een passende uitzondering gegenereerd. Je kunt eenvoudig de grootte van de byte-array schatten door de lijngrootte te vermenigvuldigen met het aantal benodigde regels. De lijngrootte kan variëren en is afhankelijk van het ruwe gegevensopslagformaat.

Om de beste prestaties te bereiken, gebruik je altijd een ruwe gegevenslijngrootte gelijk aan de [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize) eigenschapswaarde. Soms moet je echter extra vullingen aan de ruwe gegevensrijen toevoegen of verminderen, en in dat geval kan een andere lijngrootte worden gebruikt. Als een subset van een afbeeldingskader vereist is, houd dan rekening met de bitverschuivingen die kunnen optreden voor geïndexeerde RGB-pixelformaten. Bijvoorbeeld, laten we aannemen dat een afbeelding afmetingen heeft van 100x100 pixels en een ruwe gegevensindeling van 1 bit per pixel. Je wilt een ruw gegevensrechthoek laden met de locatie (7,0) en afmetingen (2,1), of met andere woorden, je hebt 2 pixels nodig die beginnen bij x=7 en y=0. In dit geval zou je de volgende gegevensindeling moeten krijgen:



![todo:image_alt_text](ruwe-gegevensverwerking_1.png)

Dit betekent dat je 2 bytes ontvangt waarbij de eerste byte 7 ongewenste pixels bevat, dan 1 gewenste pixel, en de tweede byte bevat 1 gewenste pixel en vervolgens 7 ongewenste pixels. Misschien vraag je je af waarom we geen gegevensverschuiving hebben uitgevoerd en die 2 pixels in een enkele byte hebben geplaatst? Het antwoord is simpel: om de prestaties hoog te houden. Alle interne verwerking gebeurt meestal met alle gegevens die beginnen bij de eerste pixel en eindigen bij de laatste beschikbare pixel. Er zijn zeldzame situaties waarin een subset van pixels vereist is. Bovendien hebben we geen idee hoe die pixels daarna zullen worden verwerkt, dus een verschuiving zal de prestaties verlagen en de code onnodig complex maken. Schat altijd de juiste bit (het is niet nodig om de juiste byte te bepalen aangezien de gegevens altijd komt met de eerste byte gevuld) waar de gevraagde pixels zullen beginnen. Om de juiste bit te berekenen kan een eenvoudige formule worden gebruikt: (rect.Linker * bitsCount) % 8.
### **Geïndexeerde RGB Kleurconversie**
Om de best mogelijke prestaties te behalen, gebruik altijd dezelfde bron- en doelruwe gegevensinstellingen, pixelindelingen en lijngroottes. Soms moet je echter gegevensconversie uitvoeren. Bijvoorbeeld, je kunt een RGB-afbeelding met 1 bit per pixel laden en opslaan met 2 bits per pixel, of je kunt een 4-bit RGB-afbeelding laden en de kleurbereik ervan verlagen naar 2 bits per pixel. In beide gevallen moet een kleurconversie worden toegepast. Het converteren van geïndexeerde RGB-afbeeldingen kan soms lastig zijn en kan niet worden uitgevoerd zonder bepaalde instellingen toe te passen. We moeten bepalen hoe het kleurenbereik van de bron wordt gekoppeld aan de doelkleurruimte. Om deze taak uit te voeren hebben we verschillende [modi](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods):

- Paletkoppeling (DitheringMethods.PaletteConversion)
- Ruwe gegevenskoppeling (DitheringMethods.PaletteIgnore)
- Aangepaste conversie (DitheringMethods.CustomConverter)

Bij het gebruik van paletconversie probeert de bronkleurruimte zo nauwkeurig mogelijk overeen te komen met de doelkleurruimte. Laten we bijvoorbeeld aannemen dat we een 4-bits afbeelding hebben met de volgende kleuren:
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



![todo:image_alt_text](ruwe-gegevensverwerking_2.png)

En we converteren de 4-bits afbeelding naar de 1-bits afbeelding met de volgende gedefinieerde paletkleuren:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

Bij paletconversie leest de converter de bronkleur en bepaalt de doelindex door de methode [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) van de doelpalet te gebruiken. De waarde van de eigenschap [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) wordt gebruikt in het geval de methode GetNearestColorIndex van de palet een index geeft die buiten bereik is. Hierdoor worden de bronkleuren omgezet naar de dichtstbijzijnde doelkleuren in termen van intensiteitswaarden. Je kunt het volgende resultaat zien:


![todo:image_alt_text](ruwe-gegevensverwerking_3.png)

Bij ruwe gegevenskoppeling wordt een ander scenario gebruikt. De bron- en doelkleurpaletten worden eenvoudig genegeerd en de bronindexen worden toegewezen aan doelindexen. Wanneer een waarde wordt gevonden die niet kan worden toegewezen aan het doelbereik (bij verlaging van het aantal bits), wordt de waarde van de RasterImage.RawFallbackIndex-eigenschap gebruikt. De standaardwaarde is 0 en wordt toegewezen aan de eerste kleur in het doelpalet. Als de waarde van deze eigenschap buiten het doelbereik ligt, wordt er een passende uitzondering gegenereerd. Dit leidt tot minder voorspelbare resultaten, zoals te zien is op de volgende afbeelding:


![todo:image_alt_text](ruwe-gegevensverwerking_4.png)

De paletconversiemodus is een meer juiste oplossing voor het kleurtoewijzingsprobleem, maar het kost ook iets meer tijd om te voltooien, omdat berekeningen moeten worden uitgevoerd om de juiste paletten te schatten. (Typisch is er een zeer klein prestatieverschil tussen de twee methoden.) Aan de andere kant voert de ruwe koppelingsmodus iets sneller uit en kan worden gebruikt voor ruwere kleurconversie wanneer exacte kleurtoewijzing niet zo belangrijk is. Bijvoorbeeld zijn er gevallen waarin het bronkleurpalet is bijgesneden en veilig kan worden geconverteerd naar minder bit-tellingen aangezien de extra bits toch niet zijn gebruikt.

Om een van deze benaderingen te gebruiken, gebruik je de RasterImage klasse RawDitheringMethod eigenschap. Standaard is deze ingesteld op de paletconversiemethode om de beste resultaten te bereiken. Je kunt deze eigenschap wijzigen voordat enige conversie plaatsvindt (bijvoorbeeld bij het opslaan van een afbeelding naar een stream). Houd er rekening mee dat de palet ignore en paletconversie dithering-methoden niet worden toegepast als je een afbeelding hebt geladen en sommige van de oorspronkelijke pixelgegevens hebt herschreven, aangezien de nieuwe gegevens in de cache worden geplaatst en de cache de gegevens in het maximale beschikbare formaat 32ARGB opslaat (vanaf 2.4.0, onderhevig aan verandering). Dit formaat wordt gebruikt om problemen met mogelijke verschillende kleurbereiken voor geladen en opgeslagen afbeeldingen te overwinnen. Verder worden de ignore en conversiemodi voor palet dithering genegeerd wanneer een afbeelding in RGB-modus is geladen en geconverteerd naar geïndexeerde modus of vice versa.
### **Aangepaste Kleurconversies**
Soms is het niet voldoende om de standaard benadering voor kleurconversie te gebruiken. Je wilt misschien een aangepast algoritme gebruiken voor volledige vrijheid bij het gebruik van kleurconversieroutines. Wanneer de bron- en doelafbeeldingspixelindelingen beide geïndexeerde RGB-indelingen zijn, kan een eenvoudigere interface, [IIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/iindexedcolorconverter), worden gebruikt. Je moet de [RasterImage.RawIndexedColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawindexedcolorconverter) eigenschap instellen op een instantie van de IIndexedColorConverter-interface en de [DitheringMethods](https://reference.aspose.com/psd/net/aspose.psd/ditheringmethods).CustomConverter gebruiken voor de RawDitheringMethod eigenschapswaarde. Wanneer deze combinatie wordt toegepast, gaat elke geïndexeerde kleurenconversie via die gespecificeerde IIndexedColorConverter-instantie. De aangepaste geïndexeerde kleurenconversie heeft de volgende methode gedefinieerd:



{{< highlight java >}}

 void FillIndexedtoIndexedMap(byte[] map, PixelDataFormat sourceFormat, PixelDataFormat destFormat);

{{< /highlight >}}



De FillIndexedtoIndexedMap-methode wordt aangeroepen wanneer conversie vereist is van geïndexeerde RGB-afbeelding naar geïndexeerde RGB-afbeeldingsindeling (wanneer een van de bits count 1, 2, 4 of 8 bits wordt geconverteerd naar elkaar). De kaartarray heeft de lengte van alle mogelijke invoergegevensindelingen tellen. Je moet die array vullen om de mapping van de invoer kleurpaletvermelding naar de doelpaletvermelding te laten plaatsvinden. Let erop dat de waarde van de doelindex in het bereik van 0..(bits count - 1) moet liggen, anders wordt er een passende uitzondering gegenereerd.

Als de vereiste is om een meer aangepast kleurconversiescenario uit te voeren, moet de [RasterImage.RawCustomColorConverter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawcustomcolorconverter) eigenschap worden ingesteld op een instantie van de [IColorConverter](https://reference.aspose.com/psd/net/aspose.psd/icolorconverter) interface. De RawCustomColorConverter eigenschap overschrijft altijd de RawIndexedColorConverter eigenschap als beide zijn ingesteld en een geïndexeerde kleurconverter wordt in een dergelijk geval niet gebruikt. De IColorConverter heeft een enkele methode:



{{< highlight java >}}

 int Convert(PixelDataFormat sourceFormat, byte[] data, int offset, int bitStart, int samplesCount, int linesCount, PixelDataFormat destFormat, byte[] outputData, int outputOffset); 

{{< /highlight >}}


De Convert-methode wordt elke keer aangeroepen wanneer kleurconversie vereist is. De methode ontvangt de bronruwe gegevens in de bronindeling en heeft een uitvoerbuffer om de kleurindeling omgezet naar de bestemming te ontvangen. De doelbuffer moet voldoende zijn om de geconverteerde gegevens te ontvangen (als de interface-oproep intern door de Aspose.PSD-bibliotheek wordt gemaakt) en moet de geconverteerde ruwe gegevens bevatten bij de terugkeer van de methode. De Convert-methode kan meerdere keren worden aang