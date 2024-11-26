---
title: Het Bewerken van JPEG Afbeeldingen
type: docs
weight: 20
url: /nl/java/het-bewerken-van-jpeg-afbeeldingen/
---

## **Het Gebruik van de ExifData Klasse om JPEG EXIF Tags te Lezen en te Wijzigen**


Bijna alle digitale camera's (inclusief smartphones), scanners en andere systemen die afbeeldingen verwerken, slaan afbeeldingen op met EXIF (Exchangeable Image File) informatie. Camera-instellingen en scène-informatie worden door de camera in het afbeeldingsbestand opgenomen. EXIF-gegevens bevatten ook zaken als sluiter-snelheid, datum en tijd van het nemen van een foto, brandpuntsafstand, belichtingscompensatie, belichtingsmetingpatroon en of er een flitser is gebruikt. Aspose.Imaging API's hebben het mogelijk gemaakt om op een zeer eenvoudige en simpele manier de EXIF-informatie uit een gegeven afbeelding te extraheren. Ontwikkelaars kunnen ook EXIF-gegevens naar de afbeeldingen schrijven of de bestaande informatie wijzigen volgens hun behoefte. Aspose.Imaging heeft de ExifData klasse geleverd voor het lezen, schrijven en wijzigen van de EXIF-gegevens, terwijl de Aspose.PSD.Exif.Enums namespace de relevante enumeraties bevat die in het proces worden gebruikt.
### **Het Lezen van de EXIF-Gegevens**
Aspose.PSD API's bieden middelen om EXIF-gegevens uit een gegeven afbeelding te lezen. De onderstaande stappen illustreren het gebruik van de ExifData klasse om de EXIF-informatie uit een afbeelding te lezen.

- Laad een PSD-afbeelding met behulp van de factory-methode Load.
- Zoek de JPEG-miniatuur onder de PSD-bronnen.
- Haal een instantie van de ExifData klasse op.

Haal de benodigde informatie op en schrijf deze naar de console.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Als alternatief kunnen ontwikkelaars ook de specifieke informatie ophalen met behulp van de volgende code snippet.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Het Schrijven en Wijzigen van EXIF-Gegevens**
Met behulp van de Aspose.PSD API's kunnen ontwikkelaars nieuwe EXIF-informatie schrijven en bestaande EXIF-gegevens van een afbeelding wijzigen. Beide processen (Schrijven & Wijzigen) vereisen het laden van een afbeelding en het ophalen van de EXIF-gegevens in een instantie van de ExifData klasse. Vervolgens kan men toegang krijgen tot de eigenschappen die door de ExifData klasse worden blootgesteld om ze naar behoren in te stellen. Let op: afbeeldingen voor manipulatie moeten JPEG- of TIFF-afbeeldingen zijn die meestal PSD-thumbnails zijn. Een voorbeeldcode om het gebruik te demonstreren is als volgt:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Het Extraheren van Miniaturen uit PSD-Bronnen**
Miniaturen zijn verkleinde versies van afbeeldingen die worden gebruikt om een ​​belangrijk deel van de afbeelding weer te geven in plaats van het volledige kader. Sommige afbeeldingsbestanden (vooral die zijn gemaakt met een digitale camera) hebben een miniatuurafbeelding ingesloten in het bestand. De Aspose.PSD API biedt u de mogelijkheid om PSD-bronminiaturen te extraheren en deze apart op schijf op te slaan. De miniaturenbronnen bevatten de eigenschap ExifData.Thumbnail die de miniaturendata kan ophalen. Het onderstaande codevoorbeeld demonstreert hoe deze eigenschap te gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Gebruik de hierboven besproken aanpak om de miniatuur naar andere ondersteunde bestandsindelingen op te slaan. Als u de miniatuurgegevens wilt exporteren naar andere afbeeldingsindelingen zoals BMP en PNG, gebruik dan andere exportopties voor afbeeldingen.
### **Het Extraheren van Miniaturen uit JFIF-Segementen**
Het is ook mogelijk om miniaturen te extraheren uit het ExifData- of JFIF-segment van PSD-miniatuurbronnen. De volgende code laat zien hoe het extractieproces van miniaturen uit JFIF- of ExifData-segment moet worden uitgevoerd:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Gebruik de hierboven besproken aanpak om de miniatuur naar andere ondersteunde bestandsindelingen op te slaan. Als u de miniatuurgegevens wilt exporteren naar andere afbeeldingsindelingen zoals BMP en PNG, gebruik dan andere exportopties voor afbeeldingen.
### **Een Miniatuur Toevoegen aan het JFIF-Segment**
Het onderstaande codevoorbeeld toont hoe de eigenschap JFIF.Thumbnail kan worden gebruikt om een miniatuurafbeelding toe te voegen aan het JFIF-segment van een geladen PSD-afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Miniatuurafbeeldingen met andere segmentgegevens mogen niet meer dan 65.545 bytes innemen vanwege de JPEG-formaatspecificaties. In gevallen waarbij grote afbeeldingen als miniatuur moeten worden ingesteld, kan er een uitzondering optreden.


### **Een Miniatuur Toevoegen aan het EXIF-Segment**
Het onderstaande codevoorbeeld laat zien hoe de eigenschap ExifData.Thumbnail kan worden gebruikt om een miniatuurafbeelding toe te voegen aan het EXIF-segment van een geladen PSD-afbeelding.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

In dit geval kan de Aspose.PSD API niet de grootte van de miniatuurafbeelding schatten, maar het kan wel de grootte van het gehele EXIF-gegevenssegment controleren. Dit mag niet groter zijn dan 65.535 bytes.
## **Het Gebruik van de JpegExifData Klasse om JPEG EXIF Tags te Lezen en te Wijzigen**
Aspose.PSD API's bieden de JpegExifData klasse die exclusief is voor JPEG afbeeldingsformaten om EXIF-informatie op te halen en bij te werken. Dit artikel demonstreert het gebruik van de JpegExifData klasse om hetzelfde te bereiken. De Aspose.PSD.Exif.JpegExifData klasse dient als EXIF-gegevenscontainer voor JPEG-afbeeldingen, en biedt middelen om standaard JPEG EXIF-tags op te halen en bij te werken zoals hieronder gedemonstreerd:




{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Volledige Lijst van EXIF Tags**
Het bovenstaande codevoorbeeld leest enkele EXIF Tags met behulp van de eigenschappen aangeboden door de Aspose.PSD.Exif.JpegExifData klasse. Een volledige lijst van deze eigenschappen is hier beschikbaar. Met de volgende code worden alle EXIF-tags gelezen met behulp van de System.Reflection.PropertyInfo klasse.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-as-pse-exphn-o-n-to-con-ge-PEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Automatische Correctie van de Oriëntatie van JPEG Afbeeldingen**
Foto's kunnen worden genomen met een cameras die zijn gedraaid op 90°, 180°, 270°, of normaal (geen draaiing). De meeste digitale camera's slaan de oriëntatie-informatie op samen met de beeldgegevens als EXIF-tags van de JPEG-afbeeldingen. Deze informatie kan worden gebruikt om de automatische rotatie van de afbeeldingen uit te voeren om de oriëntatie te corrigeren. Aspose.PSD API's bieden de AutoRotate methode voor de JpegImage klasse om de oriëntatie van JPEG-afbeeldingen automatisch te corrigeren. Hier is hoe u de AutoRotate methode kunt gebruiken met de Aspose.PSD voor Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Ondersteuning voor JPEG-LS met CMYK en YCCK**
De Aspose.PSD voor Java API biedt ondersteuning voor CMYK en YCCK kle modellen met JPEG-LS. Het onderstaande codevoorbeeld demonstreert hoe u deze ondersteuning voor JPEG-LS kunt gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-as-pse-exphn-o-n-to-con-ge-PEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Ondersteuning voor 2-7 bits per monster in JPEG-LS afbeeldingen**
Aspose.PSD voor Java API biedt ondersteuning voor 2-7 bits per monster in JPEG-LS afbeeldingen. Het onderstaande codevoorbeeld demonstreert hoe u deze ondersteuning voor JPEG-LS kunt gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-as-pse-exphn-o-n-to-con-ge-PEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Het Instellen van ColorType en CompressionType voor JPEG-afbeeldingen**



Aspose.PSD voor de Java API biedt ondersteuning voor Color Type en Compression Type en stelt deze in als grijswaarden en progressief voor JPEG-afbeeldingen. Het onderstaande codevoorbeeld demonstreert hoe u deze ondersteuning kunt gebruiken.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-as-pse-exphn-o-n-to-con-ge-PEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}


