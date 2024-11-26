---
title: Het manipuleren van JPEG-afbeeldingen
type: docs
weight: 30
url: /nl/net/het-manipuleren-van-jpeg-afbeeldingen/
---

## **Het gebruiken van de ExifData-Klasse voor het Lezen en Wijzigen van Jpeg EXIF-Tags**
Bijna alle digitale camera's (inclusief smartphones), scanners en andere systemen die afbeeldingen verwerken, slaan afbeeldingen op met EXIF (Exchangeable Image File) informatie. Camera-instellingen en scène-informatie worden door de camera in het afbeeldingsbestand opgenomen. EXIF-gegevens bevatten ook informatie zoals sluitertijd, datum en tijd van het maken van een foto, brandpuntsafstand, belichtingscompensatie, belichtingsmeting en of er een flits is gebruikt. Aspose.Imaging API's hebben het mogelijk gemaakt om op een zeer eenvoudige en eenvoudige manier de EXIF-informatie uit een gegeven afbeelding uit te pakken. Ontwikkelaars kunnen ook EXIF-gegevens naar de afbeeldingen schrijven of de bestaande informatie wijzigen volgens hun vereisten. Aspose.PSD heeft de [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) klasse geleverd voor het lezen, schrijven en wijzigen van de EXIF-gegevens, terwijl de [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) namespace de relevante enumeraties bevat die worden gebruikt in het proces.
### **EXIF-gegevens lezen**
Aspose.PSD API's bieden middelen om EXIF-gegevens uit een gegeven afbeelding te lezen. De hieronder verstrekte stappen illustreren het gebruik van de ExifData-klasse om de EXIF-informatie uit een afbeelding te lezen.

- Laad het PSD-afbeelding met behulp van de factory methode Load.
- Zoek de Jpeg-miniatuur tussen de PSD-bronnen.
- Pak een instantie van de ExifData-klasse uit.

Haal de benodigde informatie op en schrijf deze naar de console.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Ontwikkelaars kunnen ook de specifieke informatie krijgen met behulp van de volgende codefragment.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **EXIF-gegevens schrijven & wijzigen**
Met behulp van Aspose.PSD API's kunnen ontwikkelaars nieuwe EXIF-informatie schrijven en bestaande EXIF-gegevens van een afbeelding wijzigen. Beide processen (schrijven & wijzigen) vereisen het laden van een afbeelding en het verkrijgen van de EXIF-gegevens in een instantie van de ExifData-klasse. Vervolgens kan men de eigenschappen benaderen die worden blootgesteld door de ExifData-klasse om ze dienovereenkomstig in te stellen. Let op dat afbeeldingen voor manipulatie Jpeg- of Tiff-afbeeldingen moeten zijn die meestal PSD-miniaturen zijn. Een voorbeeldcode om het gebruik te demonstreren is als volgt:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Thumbnail Extractie uit PSD-bronnen**
Thumbnails zijn verkleinde versies van afbeeldingen die worden gebruikt om een belangrijk deel van de afbeelding weer te geven in plaats van het volledige kader. Sommige afbeeldingsbestanden (vooral die zijn genomen met een digitale camera) bevatten een miniaturenafbeelding in het bestand. Aspose.PSD API stelt je in staat om PSD-bronminiaturen te extraheren en deze apart op schijf op te slaan. Thumbnail-bronnen bevatten de eigenschap ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) die de miniaturafoto's kunnen ophalen. Het onderstaande codefragment toont hoe je het kunt gebruiken.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Gebruik de hierboven besproken aanpak om de thumbnail naar andere ondersteunde bestandsindelingen op te slaan. Als je de miniaturendata wilt exporteren naar andere afbeeldingsindelingen zoals BMP & PNG, gebruik dan andere opties voor afbeeldingsexport.
### **Thumbnail Extractie uit JFIF-segmenten**
Het is ook mogelijk om miniaturen te extraheren uit de ExifData- of JFIF-segmenten van PSD-miniatuurbronnen. De volgende code toont hoe je de miniaturendata uit het JFIF- of ExifData-segment kunt extraheren:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Gebruik de hierboven besproken aanpak om de thumbnail naar andere ondersteunde bestandsindelingen op te slaan. Als je de miniaturendata wilt exporteren naar andere afbeeldingsindelingen zoals BMP & PNG, gebruik dan andere opties voor afbeeldingsexport.
### **Een Thumbnail toevoegen aan het JFIF-segment**
Het onderstaande codefragment toont hoe je de JFIF.Thumbnail-eigenschap kunt gebruiken om een miniatuurafbeelding toe te voegen aan het JFIF-segment van een geladen PSD-afbeelding.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Thumbnailafbeeldingen met andere segmentgegevens mogen niet meer dan 65.545 bytes bevatten vanwege de JPEG specificaties. In gevallen waarbij grote afbeeldingen als thumbnail moeten worden ingesteld, kan een uitzondering optreden.


### **Een Thumbnail toevoegen aan het EXIF-segment**
Het onderstaande codefragment demonstreert hoe je de ExifData.Thumbnail-eigenschap kunt gebruiken om een miniatuurafbeelding toe te voegen aan het EXIF-segment van een geladen PSD-afbeelding.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

In dit geval kan de Aspose.PSD API de grootte van de thumbnailafbeelding niet schatten, maar kan het de grootte van het hele EXIF-gegevenssegment controleren. Dit kan niet groter zijn dan 65.535 bytes.
## **Het Gebruiken van de JpegExifData-Klasse voor het Lezen en Wijzigen van Jpeg EXIF-Tags**
Aspose.PSD API's bieden [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) klasse die exclusief is voor Jpeg-afbeeldingsindelingen om EXIF-informatie op te halen & bij te werken. Dit artikel demonstreert het gebruik van de JpegExifData-klasse om hetzelfde te bereiken. De Aspose.PSD.Exif.JpegExifData-klasse fungeert als EXIF-datacontainer voor Jpeg-afbeeldingen en biedt middelen om standaard Jpeg EXIF-tags op te halen zoals hieronder gedemonstreerd:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Volledige Lijst van EXIF-Tags**
Het bovenstaande codefragment leest een paar EXIF-tags met behulp van de eigenschappen die worden aangeboden door de Aspose.PSD.Exif.JpegExifData-klasse. De volledige lijst van deze eigenschappen is beschikbaar hier. De volgende code zal alle EXIF-tags lezen met behulp van de [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) klasse.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Automatische Correctie van de Oriëntatie van JPEG-Afbeeldingen**


Foto's kunnen worden genomen met een camera die 90°, 180°, 270°, of geen (normale oriëntatie) is gedraaid. De meeste digitale camera's slaan de oriëntatie informatie op samen met de afbeeldingsgegevens als EXIF-tags van de JEPG-afbeeldingen. Deze informatie kan worden gebruikt om de automatische rotatie op de afbeeldingen uit te voeren om de oriëntatie te corrigeren. Aspose.PSD API's bieden de AutoRotate-methode voor de JpegImage-klasse om de oriëntatie van JPEG-afbeeldingen automatisch te corrigeren. Zo kun je de AutoRotate-methode gebruiken met de Aspose.PSD voor .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Ondersteuning voor JPEG-LS met CMYK en YCCK**


De Aspose.PSD voor .NET API biedt ondersteuning voor CMYK en YCCK klemodellen met JPEG-LS. Het onderstaande codefragment laat zien hoe je die ondersteuning voor JPEG-LS kunt gebruiken.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Ondersteuning voor 2-7 bits per monster in JPEG-LS-afbeeldingen**


De Aspose.PSD voor .NET API biedt ondersteuning voor 2-7 bits per monster JPEG-LS-afbeeldingen. Het onderstaande codefragment laat zien hoe je die ondersteuning voor JPEG-LS kunt gebruiken.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Instellen van ColorType en CompressionType voor JPEG-afbeeldingen**


Aspose.PSD voor .NET API biedt ondersteuning voor Color Type en Compression Type en stelt deze in als grijswaarden en progressief voor JPEG-afbeeldingen. Het onderstaande codefragment toont hoe je die ondersteuning kunt gebruiken.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





Het onderstaande codefragment toont hoe je de ExifData.Thumbnail-eigenschap kunt gebruiken om een miniatuurafbeelding toe te voegen aan het EXIF-segment van een geladen PSD-afbeelding.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

In dit geval kan de Aspose.PSD API de grootte van de thumbnailafbeelding niet schatten, maar kan het de grootte van het hele EXIF-gegevenssegment controleren. Dit kan niet groter zijn dan 65.535 bytes.
