---
title: Manipulation von JPEG-Bildern
type: docs
weight: 30
url: /de/net/manipulation-von-jpeg-bildern/
---

## **Verwendung der ExifData-Klasse zum Lesen und Ändern von Jpeg-EXIF-Tags**
Fast alle Digitalkameras (einschließlich Smartphones), Scanner und andere Systeme, die Bilder verarbeiten, speichern Bilder mit EXIF (Austauschbare Bilddatei) Informationen. Kameradaten und Szeneninformationen werden von der Kamera in die Bilddatei aufgezeichnet. EXIF-Daten enthalten auch Verschlusszeit, Datum und Uhrzeit, zu der ein Foto aufgenommen wurde, Brennweite, Belichtungskorrektur, Messmuster und ob ein Blitz verwendet wurde. Die Aspose.Imaging-APIs haben es ermöglicht, die EXIF-Informationen aus einem bestimmten Bild sehr einfach und unkompliziert zu extrahieren. Entwickler können auch EXIF-Daten in die Bilder schreiben oder die vorhandenen Informationen gemäß ihren Anforderungen ändern. Aspose.PSD hat die [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) Klasse zum Lesen, Schreiben und Modifizieren der EXIF-Daten bereitgestellt, während der [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) Namensraum die relevanten Enumerationen enthält, die im Prozess verwendet werden.
### **Lesen von EXIF-Daten**
Aspose.PSD-APIs bieten die Möglichkeit, EXIF-Daten aus einem bestimmten Bild zu lesen. Die unten angegebenen Schritte veranschaulichen die Verwendung der ExifData-Klasse zum Lesen der EXIF-Informationen aus einem Bild.

- Laden Sie das PSD-Bild mit der Factory-Methode Load.
- Suchen Sie das Jpeg-Vorschaubild unter den PSD-Ressourcen.
- Extrahieren Sie eine Instanz der ExifData-Klasse.

Holen Sie sich die benötigten Informationen und schreiben Sie sie in die Konsole.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternativ können Entwickler auch die spezifischen Informationen mit folgendem Code-Snippet abrufen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Schreiben & Ändern von EXIF-Daten**
Mit Hilfe der Aspose.PSD-APIs können Entwickler neue EXIF-Informationen schreiben und vorhandene EXIF-Daten eines Bildes ändern. Beide Prozesse (Schreiben & Ändern) erfordern das Laden eines Bildes und das Abrufen der EXIF-Daten in eine Instanz der ExifData-Klasse. Anschließend können die von der ExifData-Klasse bereitgestellten Eigenschaften verwendet werden, um sie entsprechend einzustellen. Beachten Sie, dass Bilder für die Manipulation Jpeg- oder Tiff-Bilder sein sollten, die normalerweise PSD-Vorschaubilder sind. Ein Beispielcode zur Veranschaulichung der Verwendung ist wie folgt:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Extrahieren von Miniaturansichten aus PSD-Ressourcen**
Miniaturansichten sind verkleinerte Versionen von Bildern, die verwendet werden, um einen bedeutenden Teil des Bildes anstelle des gesamten Rahmens anzuzeigen. Einige Bilddateien (insbesondere die mit einer Digitalkamera aufgenommenen) enthalten ein Miniaturbild, das in der Datei eingebettet ist. Die Aspose.PSD-API ermöglicht es Ihnen, PSD-Ressourcenminiaturansichten zu extrahieren und sie separat auf der Festplatte zu speichern. Miniaturressourcen enthalten die Eigenschaft [Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) von ExifData, die die Miniaturdaten abrufen kann. Das unten bereitgestellte Code-Snippet zeigt, wie man es verwendet.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Verwenden Sie den oben diskutierten Ansatz, um die Miniatur in andere unterstützte Dateiformate zu speichern. Wenn Sie die Miniaturdaten in andere Bildformate wie BMP und PNG exportieren möchten, verwenden Sie bitte andere Bildexportoptionen.
### **Extrahieren von Miniaturansichten aus JFIF-Segmenten**
Es ist auch möglich, Miniaturansichten aus dem ExifData- oder JFIF-Segment von PSD-Thumbnail-Ressourcen zu extrahieren. Der folgende Code zeigt, wie die Extraktion von Miniaturdaten aus dem JFIF- oder ExifData-Segment durchgeführt wird:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Verwenden Sie den oben diskutierten Ansatz, um die Miniatur in andere unterstützte Dateiformate zu speichern. Wenn Sie die Miniaturdaten in andere Bildformate wie BMP und PNG exportieren möchten, verwenden Sie bitte andere Bildexportoptionen.
### **Hinzufügen von Miniaturbildern zum JFIF-Segment**
Das folgende Code-Snippet zeigt, wie die JFIF. Thumbnail-Eigenschaft verwendet wird, um einem geladenen PSD-Bild ein Miniaturbild im JFIF-Segment hinzuzufügen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Miniaturbilder mit anderen Segmentdaten dürfen aufgrund der Spezifikationen des JPEG-Formats nicht mehr als 65.545 Bytes einnehmen. In Fällen, in denen große Bilder als Miniatur festgelegt werden sollen, kann eine Ausnahme auftreten.


### **Hinzufügen von Miniaturbildern zum EXIF-Segment**
Das folgende Code-Snippet zeigt, wie die Eigenschaft ExifData.Thumbnail verwendet wird, um einem geladenen PSD-Bild ein Miniaturbild im EXIF-Segment hinzuzufügen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


In diesem Fall kann die Aspose.PSD-API die Größe des Miniaturbilds nicht schätzen, kann jedoch die Größe des gesamten EXIF-Datensegments überprüfen. Dies darf nicht größer als 65.535 Bytes sein.
## **Verwendung der JpegExifData-Klasse zum Lesen und Ändern von Jpeg-EXIF-Tags**
Die Aspose.PSD-APIs bieten die [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) Klasse, die ausschließlich für Jpeg-Bildformate gedacht ist, um EXIF-Informationen abzurufen und zu aktualisieren. Dieser Artikel demonstriert die Verwendung der JpegExifData-Klasse, um dasselbe zu erreichen. Die Aspose.PSD.Exif.JpegExifData-Klasse dient als EXIF-Datencontainer für Jpeg-Bilder und bietet Mittel, um standardmäßige Jpeg-EXIF-Tags abzurufen, wie unten dargestellt:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Vollständige Liste der EXIF-Tags**
Das obige Code-Snippet liest einige EXIF-Tags mithilfe der von der Aspose.PSD.Exif.JpegExifData-Klasse angebotenen Eigenschaften. Die vollständige Liste dieser Eigenschaften ist hier verfügbar. Der folgende Code liest alle EXIF-Tags mithilfe der [System.Reflection.PropertyInfo](https://docs.microsoft.com/de-de/dotnet/api/system.reflection.propertyinfo?view=net-5.0) Klasse.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Automatische Korrektur der Ausrichtung von JPEG-Bildern**


Fotos können mit einer Kamera gedreht werden um 90°, 180°, 270° oder normal ausgerichtet sein. Die meisten Digitalkameras speichern die Ausrichtungsinformationen zusammen mit den Bilddaten als EXIF-Tags der JEPG-Bilder. Diese Informationen können verwendet werden, um die automatische Drehung der Bilder zur Korrektur der Ausrichtung durchzuführen. Aspose.PSD-APIs bieten die AutoRotate-Methode für die JpegImage-Klasse, um die Ausrichtung von JPEG-Bildern automatisch zu korrigieren. So können Sie die AutoRotate-Methode mit der Aspose.PSD for .NET-API verwenden.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Unterstützung für JPEG-LS mit CMYK- und YCCK-Farbräumen**


Aspose.PSD for .NET-API bietet Unterstützung für die Farbmodelle CMYK und YCCK mit JPEG-LS. Das folgende Code-Snippet zeigt, wie Sie diese Unterstützung für JPEG-LS nutzen können.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Unterstützung für 2-7 Bits pro Sample in JPEG-LS-Bildern**


Aspose.PSD for .NET-API bietet Unterstützung für 2-7 Bits pro Sample in JPEG-LS-Bildern. Das folgende Code-Snippet zeigt, wie Sie diese Unterstützung für JPEG-LS nutzen können.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Festlegen des Farbtyps und des Kompressionstyps für JPEG-Bilder**




Aspose.PSD for .NET-API bietet Unterstützung für den Farbtyp und den Kompressionstyp und setzt sie auf Graustufen und progressiv für JPEG-Bilder. Das folgende Code-Snippet zeigt, wie Sie diese Unterstützung nutzen können.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}




Der folgende Code zeigt, wie die ExifData.Thumbnail-Eigenschaft verwendet wird, um einem geladenen PSD-Bild ein Miniaturbild im EXIF-Segment hinzuzufügen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


In diesem Fall kann die Aspose.PSD-API die Größe des Miniaturbilds nicht schätzen, kann jedoch die Größe des gesamten EXIF-Datensegments überprüfen. Dies darf nicht größer als 65.535 Bytes sein.
