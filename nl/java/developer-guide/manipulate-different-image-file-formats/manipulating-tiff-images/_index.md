---
title: Het manipuleren van TIFF-afbeeldingen
type: docs
weight: 40
url: /nl/java/het-manipuleren-van-tiff-afbeeldingen/
---

## **Frames toevoegen met verschillende instellingen**
TIFF is een zeer flexibel formaat en het staat toe dat verschillende frames worden toegevoegd, met verschillende afmetingen, compressie en andere instellingen. Aspose.PSD API's stellen u in staat om elk TIFF-frame van elke grootte toe te voegen, wat helpt bij het maken van complexe documenten. Als er een vereiste is om de frames aan te passen tijdens het toevoegen om ze allemaal gelijk te maken, voer dan de volgende stappen uit:

- Maak een nieuw leeg frame aan met de gewenste opties of kopieer het bronframe met de opgegeven uitvoeropties met behulp van de methode CreateFrameFrom.
- Wijzig de grootte van het bronframe/afbeelding naar de gewenste afmetingen met behulp van de methode Resize.
- Voeg de pixels van het bronframe/afbeelding toe aan het nieuwe frame.
- Voeg het nieuwe frame toe aan de uitvoertafbeelding in TIFF-indeling.

## **Lagen van PSD-afbeelding exporteren naar multi-page TIFF-bestandsindeling**
Soms moet u lagen van PSD-afbeeldingen exporteren naar de multi-page TIFF-bestandsindeling. In dit artikel wordt gedemonstreerd hoe we deze taak kunnen uitvoeren met behulp van de Aspose.PSD voor Java API. Eerst zullen we de PSD-afbeelding laden vanaf de schijf. Vervolgens zullen we itereren over de lagen van de PSD-afbeelding en TiffFrame maken van overeenkomstige lagen. Tot slot slaan we het resulterende TIFF-afbeelding op in één bestand op de schijf.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}

## **TiffOptions-configuratie**
Ontwikkelaars kunnen verschillende eigenschappen van de TiffOptions-klasse aanpassen om de gewenste resultaten te verkrijgen. In dit document richten we ons op 4 hoofdeigenschappen die de attributen van de resulterende afbeelding beheersen.

Deze eigenschappen worden hieronder vermeld.

1. ` `TiffOptions.Photometric
2. TiffOptions.Compressie
3. TiffOptions.BitsPerSample
4. TiffOptions.Voorspeller

Telkens wanneer we een lege TiffOptions-structuur initialiseren, wordt elke optie ingesteld op de standaardwaarde, bijvoorbeeld compressie is ingesteld op Geen, BitsPerSample is ingesteld op 1 en Photometric is ingesteld als MinIsWhite. Opslaan in dit formaat maakt de uiteindelijke afbeelding zwart-wit en dit is verwacht gedrag voor deze optiescombinatie. Om de gekleurde resultaten te verkrijgen, moet u alle bovengenoemde eigenschappen instellen op waarden die overeenkomen met de gewenste kleurruimte, of u kunt de TiffOptions-structuur initialiseren met vooraf gedefinieerde instellingen zoals later in dit artikel wordt besproken. Hieronder wordt een tabel beschreven die de verwachte parameterwaarden toont die u kunt instellen om de gewenste resultaten te bereiken. Let op, u moet alle 4 kolommen instellen via TiffOptions om een geladen/gemaakte afbeelding op te slaan in TIFF-bestandsindeling.

|` `**TiffOptions.Photometric**|**TiffOptions.Compressie**|**TiffOptions.BitsPerSample**|**TiffOptions.Voorspeller**|
| :- | :- | :- | :- |
|Palet|min./ongecomprimeerd|1/4/8/16 (palet, kleurmodus) enkel kanaal|Geen|
|min. wit/min. zwart|min./ongecomprimeerd|1/4/8/16 (grijsschaalmodus) enkel kanaal|Geen|
|Palet|min./ongecomprimeerd|8 (palet, kleurmodus) enkel kanaal|Horizontaal (meer compressie bereikt voor LZW met dezelfde patronen)|
|min. wit/min. zwart|min./ongecomprimeerd|8 (grijsschaalmodus) enkel kanaal|Horizontaal (meer compressie bereikt voor LZW met dezelfde patronen)|
|RGB|min./ongecomprimeerd|[8,8,8] (3 RGB-kanalen)|Geen/Horizontaal|
|RGB|min./ongecomprimeerd|[8,8,8,8] (3 RGB-kanalen en aanvullend alfa-kanaal kan worden ingesteld via TiffOptions.AlphaStorage) Eigenlijk wordt elke toegevoegde kanalen tellen ondersteund, maar elk kanaal moet een grootte hebben van 8 bit zoals [8,8,8,8,8,8]|Geen/Horizontaal|
Alle 4 eigenschappen moeten worden ingesteld via TiffOptions om een afbeeldingsindeling op te slaan in Tiff-indeling. Bij het gebruiken van verschillende combinaties kunnen sommige kijkers (inclusief de Windows Photo Viewer) weigeren om de resulterende afbeelding weer te geven vanwege de beperkte ondersteuning die ze bieden. In dat geval moet u een andere viewer kiezen voor uw tests.
### **Vooraf gedefinieerde instellingen voor TiffOptions-klasse**
Om de gebruikers te vergemakkelijken en foutieve configuratie van de TiffOptions-instantie te voorkomen, heeft de Aspose.PSD voor Java API een andere constructor blootgelegd die een parameter van het type TiffExpectedFormat accepteert. Op basis van de geselecteerde waarde uit de TiffExpectedFormat-enumeratie configureert de API automatisch alle verplichte eigenschappen voor de TiffOptions-instantie om de gewenste resultaten te produceren. Voordat we doorgaan met de voorbeeldcode, volgt hier de lijst van de TiffExpectedFormat-velden en hun details voor een beter begrip van het gebruik.

- TiffExpectedFormat.Standaard: Het instellen van het veld op Standaard gedraagt zich vergelijkbaar met de standaard constructor van de TiffOptions-klasse zonder compressie en BitsPerPixel ingesteld op 1 om een zwart-witresultaat te produceren. Het wordt aangeraden dit veld te gebruiken wanneer andere formaatspecifieke eigenschappen handmatig moeten worden ingesteld volgens de gewenste resultaten.
- TiffExpectedFormat.TiffCcitRle: Specifiek voor RLE-encodering bij het opslaan van het resultaat in een TIFF-indeling met 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffCcittFax3: Specifiek voor CCITT Fax3-codering bij het opslaan van het resultaat in een TIFF-indeling met 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffCcittFax4: Specifiek voor CCITT Fax4-codering bij het opslaan van het resultaat in een TIFF-indeling met 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffDeflateBW: Specifiek voor Deflate-compressie bij het opslaan van het resultaat in een TIFF-indeling met 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffDeflateRGB: Specifiek voor Deflate-compressie bij het opslaan van het resultaat in een RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffJpegRGB: Specifiek voor Jpeg-compressie bij het opslaan van het resultaat in een RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffJpegYCBCR: Specifiek voor Jpeg-compressie bij het opslaan van het resultaat in een YCBCR (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffLzwBW: Specifiek voor LZW-compressie bij het opslaan van het resultaat in een TIFF-indeling met 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffLzwRGB: Specifiek voor LZW-compressie bij het opslaan van het resultaat in een RGB (kleur) TIFF-indeling.
- TiffExpectedFormat.TiffLzwRGBA: Specifiek voor LZW-compressie bij het opslaan van het resultaat in een RGBA (kleur met transparantie) TIFF-indeling.
- TiffExpectedFormat.TiffGeenCompressieBW: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in 1 BitsPerPixel (zwart-wit).
- TiffExpectedFormat.TiffGeenCompressieRGB: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in RGB (kleur).
- TiffExpectedFormat.TiffGeenCompressieRGBA: Specifiek voor ongecomprimeerde TIFF-indeling bij het opslaan van het resultaat in RGBA (kleur met transparantie).

De volgende codefragment verduidelijkt het gebruik van de velden TiffExpectedFormat bij het maken van een instantie van de TiffOptions-klasse.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}

## **Ondersteuning voor Deflate- en Adobe Deflate-compressie**
Het TIFF (Tagged Image File Format) bestandsformaat ondersteunt verschillende soorten compressie, waarbij het compressietype als tag (een geheel getal) in het bestand wordt opgeslagen. Een van dergelijke compressiemethoden is Adobe Deflate (voorheen bekend als Deflate). De Aspose.PSD voor Java API ondersteunt deze compressiemethode voor het exporteren en creëren van TIFF-afbeeldingen.
### **Afbeelding opslaan in TIFF met Deflate-compressie**
Het omzetten van geladen afbeeldingen naar TIFF met Deflate/Adobe Deflate-compressie is eenvoudig zoals hieronder beschreven.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Het maken van een TiffImage met Adobe Deflate-compressie**
Het onderstaande voorbeeld toont het gebruik van de Aspose.PSD voor Java API om een afbeelding vanaf nul te maken met behulp van de Adobe Deflate-compressiemethode.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Comprimeren van TIFF-afbeeldingen**
De Aspose.PSD voor Java API kan worden gebruikt om PSD-afbeeldingen om te zetten naar TIFF-afbeeldingsformaat en zelfs de compressie van de resulterende TIFF-afbeelding te wijzigen. De API kan ook worden gebruikt om verschillende afbeeldingen als frames in een TIFF-afbeelding op te slaan voor archiveringsdoeleinden terwijl de afbeeldingen worden gecomprimeerd tot de kleinste gegevensgrootte. De beeldcompressie moet in elk geval worden uitgevoerd door de bron-gegevensgrootte te verkleinen, ongeacht het gebruikte compressiealgoritme. Om de beste compressieverhouding te bereiken, kunnen we geïndexeerde kleurruimten gebruiken. Het onderstaande codefragment voert de beste compressie uit door slechts 16 geïndexeerde kleuren te gebruiken en het LZW-compressiealgoritme toe te passen, hoewel de bronkleuren licht zijn geüniformeerd.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
