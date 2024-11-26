---
title: Afbeeldingen van TIFF-bestanden bewerken
type: docs
weight: 50
url: /nl/net/afbeeldingen-van-tiff-bestanden-bewerken/
---

## **Frames toevoegen met verschillende instellingen**
TIFF is een zeer flexibel formaat en het staat toe dat verschillende frames worden toegevoegd, met verschillende afmetingen, compressie en andere instellingen. Aspose.PSD API's stellen u in staat om elk TIFF-frame van elk formaat toe te voegen, wat helpt bij het maken van complexe documenten. Als er een vereiste is om de frames aan te passen tijdens het toevoegproces om ze allemaal gelijk te maken, volg dan de onderstaande stappen:

- Maak een nieuw leeg frame met de gewenste opties of kopieer het bramframe met de opgegeven uitvoeropties met behulp van de CreateFrameFrom-methode.
- Wijzig de grootte van het bramframe/afbeelding naar de gewenste afmetingen met behulp van de Resize-methode.
- Voeg de pixels van het bramframe/afbeelding toe aan het nieuwe frame.
- Voeg het nieuwe frame toe aan de uitvoertiff-afbeelding.

## **Lagen van PSD-afbeelding exporteren naar Multi Page Tiff-indeling**
Soms moet u lagen van PSD-afbeeldingen exporteren naar de Multi-page TIFF-indeling. Dit artikel zal demonstreren hoe we deze taak kunnen uitvoeren met behulp van Aspose.PSD voor .NET API. Eerst laden we de PSD-afbeelding vanaf de schijf. Vervolgens zullen we itereren over de lagen van de PSD-afbeelding en TiffFrame maken van de overeenkomstige lagen. Ten slotte slaan we de resulterende Tiff-afbeelding op in één bestand op de schijf.

## **TiffOptsies Configuratie**

Ontwikkelaars kunnen verschillende eigenschappen van de [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)-klasse aanpassen om de gewenste resultaten te verkrijgen. In dit document zullen we ons richten op 4 hoofdeigenschappen die de kenmerken van de resulterende afbeelding beheersen.

Deze eigenschappen worden hieronder vermeld.

1. [TiffOptsies.Photometrisch](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptsies.Compressie](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptsies.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptsies.Voorspeller](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Elke optie wordt ingesteld op de standaardwaarde wanneer een lege TiffOptions-structuur wordt geïnitialiseerd, bijvoorbeeld compressie is ingesteld op Geen, BitsPerSample is ingesteld op 1 en Photometrisch op MinIsWhite. Opslaan in dit formaat maakt de uiteindelijke afbeelding zwart-wit en dit is het verwachte gedrag voor dergelijke optiecombinaties. Voor gekleurde resultaten moeten alle bovengenoemde eigenschappen worden ingesteld op waarden die overeenkomen met de gewenste kleurruimte of u kunt de TiffOptions-structuur initialiseren met vooraf gedefinieerde instellingen zoals later in dit artikel besproken. Hieronder vindt u een tabel die de verwachte parameterwaarden beschrijft die u kunt instellen om de gewenste resultaten te bereiken. Let op, u moet alle 4 kolommen instellen via TiffOptions om een geladen/gemaakte afbeelding op te slaan in TIFF-indeling.

|**TiffOptsies.Photometrisch**|**TiffOptsies.Compressie**|**TiffOptsies.BitsPerSample**|**TiffOptsies.Voorspeller**|
| :- | :- | :- | :- |
|Palet|LZW/Ongecomprimeerd|1/4/8/16 (palet, kleurenmodus) alleen enkelvoudig kanaal|Geen|
|MinIsWhite/MinIsBlack|LZW/Ongecomprimeerd|1/4/8/16 (grijstintenmodus) enkel kanaal|Geen|
|Palet|LZW/Ongecomprimeerd|8 (palet, kleurenmodus) enkel kanaal|Horizontaal (meer compressie bereikt voor LZW dezelfde patronen)|
|MinIsWhite/MinIsBlack|LZW/Ongecomprimeerd|8 (grijstintenmodus) enkel kanaal|Horizontaal (meer compressie bereikt voor LZW dezelfde patronen)|
|RGB|LZW/Ongecomprimeerd|[8,8,8] (3 RGB-kanalen)|Geen/Verticaal|
|RGB|LZW/Ongecomprimeerd|[8,8,8,8] (3 RGB-kanalen en een aanvullend alfakanaal kan worden ingesteld via TiffOptions.AlphaStorage) Eigenlijk wordt elke extra aantal kanalen ondersteund maar elk kanaal moet een grootte van 8 bits hebben zoals [8,8,8,8,8,8]|Geen/Verticaal|
Alle 4 eigenschappen moeten worden ingesteld via TiffOptions om een afbeelding in Tiff-indeling op te slaan. Bij gebruik van verschillende combinaties kunnen sommige weergaven (inclusief de Windows Photo Viewer) weigeren om de resulterende afbeelding weer te geven vanwege de beperkte ondersteuning die ze bieden. In dat geval kunt u een andere viewer kiezen voor uw testen.

### **Vooraf gedefinieerde instellingen voor TiffOptsies Klasse**
Om gebruikers te faciliteren en foutieve configuratie van de TiffOptions-instantie te voorkomen, heeft de Aspose.PSD voor .NET API een andere constructor blootgesteld die een parameter van het type [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat) accepteert. Op basis van de geselecteerde waarde uit de TiffExpectedFormat-enumeratie configureert de API automatisch alle verplichte eigenschappen voor de TiffOptions-instantie om de gewenste resultaten te produceren. Voordat we naar de voorbeeldcode gaan, hier is de lijst van de velden van TiffExpectedFormat en hun details voor een beter begrip van het gebruik.

- TiffExpectedFormat.Default: Het instellen van het veld op Standaard gedraagt zich net als de standaardconstructor van de TiffOptions-klasse met geen compressie en BitsPerPixel ingesteld op 1 om een zwart-witresultaat te produceren. Het wordt aanbevolen om dit veld te gebruiken wanneer andere specifieke eigenschappen van het formaat handmatig moeten worden ingesteld volgens de gewenste resultaten.
- TiffExpectedFormat.TiffCcitRle: Specifiek voor RLE-codering bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit) TIFF-indeling.
- TiffExpectedFormat.TiffCcittFax3: Specifiek voor CCITT Fax3-codering bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit) TIFF-indeling.
- TiffExpectedFormat.TiffCcittFax4: Specifiek voor CCITT Fax4-codering bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit) TIFF-indeling.
- TiffExpectedFormat.TiffDeflateBW: Specifiek voor Deflate-compressie bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit) TIFF-indeling.
- TiffExpectedFormat.TiffDeflateRGB: Specifiek voor Deflate-compressie bij het opslaan van het resultaat in RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffJpegRGB: Specifiek voor Jpeg-compressie bij het opslaan van het resultaat in RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffJpegYCBCR: Specifiek voor Deflate-compressie bij het opslaan van het resultaat in YCBCR (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffLzwBW: Specifiek voor LZW-compressie bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit) TIFF-indeling.
- TiffExpectedFormat.TiffLzwRGB: Specifiek voor LZW-compressie bij het opslaan van het resultaat in RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffLzwRGBA: Specifiek voor LZW-compressie bij het opslaan van het resultaat in RGBA (kleur met transparantie) TIFF-indeling.
- TiffExpectedFormat.TiffNoCompressionBW: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffNoCompressionRGB: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in RGB (kleur).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in RGBA (kleur met transparantie).

De volgende codefragmenten lichten het gebruik van TiffExpectedFormat-velden toe bij het maken van een instantie van de TiffOptions-klasse.

## **Ondersteuning voor Deflate- en Adobe Deflate-compressie**
Het TIFF (Tagged Image File Format) bestandsformaat ondersteunt verschillende soorten compressie, waarbij het compressietype wordt opgeslagen als een tag (een geheel getal) in het bestand. Een van dergelijke compressiemethoden is Adobe Deflate (voorheen bekend als Deflate). Aspose.PSD voor .NET API ondersteunt deze compressiemethode voor het exporteren en maken van TIFF-afbeeldingen.
### **Afbeelding opslaan in TIFF met Deflate-compressie**
Het converteren van de geladen afbeeldingen naar TIFF met Deflate/Adobe Deflate-compressie is eenvoudig zoals hieronder beschreven.
### **TiffImage maken met Adobe Deflate-compressie**
Het hieronder verstrekte voorbeeld laat het gebruik van Aspose.PSD voor .NET API zien om een afbeelding vanaf nul te maken met behulp van de Adobe Deflate-compressiemethode.
### **TIFF-afbeeldingen comprimeren**
Aspose.PSD voor .NET API kan worden gebruikt om PSD-afbeeldingen naar TIFF-afbeeldingsindeling te converteren en zelfs de compressie van de resulterende TIFF-afbeelding te wijzigen. De API kan ook worden gebruikt om verschillende afbeeldingen als frames in een TIFF-afbeelding op te slaan voor archiveringsdoeleinden terwijl de afbeeldingen worden gecomprimeerd naar de kleinste gegevensgrootte. De beeldcompressie moet in elk geval worden uitgevoerd door de bron-dataset te verkleinen, ongeacht het gebruikte compressiealgoritme. Om de beste compressieverhouding te bereiken, kunnen we geïndexeerde kleurruimten gebruiken. Het onderstaande codefragment voert de beste compressie uit met slechts 16 geïndexeerde kleuren en het LZW-compressiealgoritme, hoewel de bronskleuren iets vertekend zijn.
