---
title: Manipulation von JPEG-Bildern
type: docs
weight: 20
url: /de/java/manipulation-von-jpeg-bildern/
---

## **Verwendung der ExifData-Klasse zum Lesen und Ändern von JPEG-EXIF-Tags**

Fast alle Digitalkameras (einschließlich Smartphones), Scanner und andere Systeme, die Bilder verarbeiten, speichern Bilder mit EXIF (Exchangeable Image File) -Informationen. Kameradaten und Szeneninformationen werden von der Kamera in die Bilddatei aufgenommen. Die EXIF-Daten enthalten auch Verschlusszeit, Datum und Uhrzeit der Aufnahme eines Fotos, Brennweite, Belichtungskorrektur, Messmuster und ob ein Blitz verwendet wurde. Die Aspose.Imaging APIs haben es ermöglicht, die EXIF-Informationen aus einem gegebenen Bild auf sehr einfache und einfache Weise zu extrahieren. Entwickler können auch EXIF-Daten zu den Bildern schreiben oder die vorhandenen Informationen je nach Bedarf ändern. Aspose.Imaging hat die Klasse ExifData zum Lesen, Schreiben und Modifizieren der EXIF-Daten bereitgestellt, während der Namensraum Aspose.PSD.Exif.Enums die relevanten Enumerationen enthält, die im Prozess verwendet werden.
### **Lesen von EXIF-Daten**
Die Aspose.PSD APIs bieten Möglichkeiten, EXIF-Daten aus einem gegebenen Bild zu lesen. Die unten angegebenen Schritte veranschaulichen die Verwendung der ExifData-Klasse, um die EXIF-Informationen aus einem Bild zu lesen.

- Laden Sie das PSD-Bild mit der Factory-Methode Load.
- Suchen Sie das JPEG-Thumbnail unter den PSD-Ressourcen.
- Extrahiere eine Instanz der ExifData-Klasse.

Holen Sie sich die erforderlichen Informationen und geben Sie sie auf der Konsole aus.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Alternativ können Entwickler die spezifischen Informationen auch mit folgendem Code-Schnipsel abrufen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}


### **Schreiben und Ändern von EXIF-Daten**
Mit den Aspose.PSD APIs können Entwickler neue EXIF-Informationen schreiben und vorhandene EXIF-Daten eines Bildes ändern. Beide Prozesse (Schreiben & Ändern) erfordern das Laden eines Bildes und das Abrufen der EXIF-Daten in einer Instanz der ExifData-Klasse. Dann kann man auf die von der ExifData-Klasse bereitgestellten Eigenschaften zugreifen und sie entsprechend setzen. Beachten Sie bitte, dass Bilder, die manipuliert werden sollen, JPEG- oder TIFF-Bilder sein sollten, die normalerweise PSD-Vorschaubilder sind. Der Beispielcode zur Demonstration der Verwendung lautet wie folgt:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}


## **Extrahieren von Miniaturansichten aus PSD-Ressourcen**
Miniaturansichten sind verkleinerte Versionen von Bildern, die verwendet werden, um einen wesentlichen Teil des Bildes anzuzeigen, anstatt den gesamten Rahmen. Einige Bilddateien (insbesondere diejenigen, die mit einer Digitalkamera aufgenommen wurden) enthalten ein Miniaturbild im Bild. Aspose.PSD API ermöglicht es Ihnen, PSD-Ressourcenminiaturen zu extrahieren und separat auf der Festplatte zu speichern. Die Thumbnail-Ressourcen enthalten die ExifData.Thumbnail-Eigenschaft, die die Miniaturdaten abrufen kann. Der unten bereitgestellte Code-Ausschnitt zeigt, wie es verwendet wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Verwenden Sie den oben diskutierten Ansatz, um die Miniatur in andere unterstützte Dateiformate zu speichern. Wenn Sie Miniaturdaten in andere Bildformate wie BMP & PNG exportieren möchten, verwenden Sie bitte andere Bildexportoptionen.


### **Extrahieren von Miniaturansichten aus JFIF-Segmenten**
Es ist auch möglich, Miniaturansichten aus dem ExifData- oder JFIF-Segment von PSD-Thumbnail-Ressourcen zu extrahieren. Der folgende Code zeigt, wie die Extraktion von Miniaturdaten aus dem JFIF- oder ExifData-Segment durchgeführt wird:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Verwenden Sie den oben diskutierten Ansatz, um die Miniatur in andere unterstützte Dateiformate zu speichern. Wenn Sie Miniaturdaten in andere Bildformate wie BMP & PNG exportieren möchten, verwenden Sie bitte andere Bildexportoptionen.
### **Thumbnail zum JFIF-Segment hinzufügen**
Der folgende Codeausschnitt zeigt, wie Sie die JFIF.Thumbnail-Eigenschaft verwenden, um ein Miniaturbild zum JFIF-Segment eines geladenen PSD-Bildes hinzuzufügen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}


Miniaturbilder mit anderen Segmentdaten dürfen aufgrund der JPEG-Formatspezifikationen nicht mehr als 65.545 Bytes einnehmen. In Fällen, in denen große Bilder als Miniaturbild festgelegt werden sollen, kann es zu Ausnahmen kommen.


### **Thumbnail zum EXIF-Segment hinzufügen**
Der folgende Codeausschnitt zeigt, wie Sie die ExifData.Thumbnail-Eigenschaft verwenden, um ein Miniaturbild zum EXIF-Segment eines geladenen PSD-Bildes hinzuzufügen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}


In diesem Fall kann die Aspose.PSD-API die Größe des Miniaturbildes nicht schätzen, aber sie kann die Größe des gesamten EXIF-Datensegments überprüfen. Diese darf nicht größer als 65.535 Bytes sein.
## **Verwendung der JpegExifData-Klasse zum Lesen und Ändern von JPEG-EXIF-Tags**
Aspose.PSD APIs bieten die JpegExifData-Klasse, die exklusiv für JPEG-Bildformate entwickelt wurde, um EXIF-Informationen abzurufen und zu aktualisieren. Dieser Artikel zeigt die Verwendung der JpegExifData-Klasse zur Erreichung desselben. Die Aspose.PSD.Exif.JpegExifData-Klasse fungiert als EXIF-Datencontainer für JPEG-Bilder und bietet Mittel zum Abrufen standardmäßiger JPEG-EXIF-Tags, wie im Folgenden dargestellt:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

### **Vollständige Liste der EXIF-Tags**
Der obige Codeausschnitt liest einige EXIF-Tags mithilfe der von der Aspose.PSD.Exif.JpegExifData-Klasse bereitgestellten Eigenschaften. Eine vollständige Liste dieser Eigenschaften finden Sie hier. Der folgende Code liest alle EXIF-Tags mithilfe der System.Reflection.PropertyInfo-Klasse.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}

## **Automatische Korrektur der Ausrichtung von JPEG-Bildern**
Fotos können mit einer Kamera gedreht werden um 90°, 180°, 270° oder gar nicht (normale Ausrichtung). Die meisten Digitalkameras speichern die Ausrichtungsinformationen zusammen mit den Bilddaten als EXIF-Tags der JPEG-Bilder. Diese Informationen können verwendet werden, um die automatische Drehung der Bilder zur Korrektur der Ausrichtung durchzuführen. Aspose.PSD APIs bieten die AutoRotate-Methode für die JpegImage-Klasse, um die Ausrichtung von JPEG-Bildern automatisch zu korrigieren. Hier erfahren Sie, wie Sie die AutoRotate-Methode mit der Aspose.PSD für die Java-API verwenden können.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}

## **Unterstützung für JPEG-LS mit CMYK und YCCK**
Aspose.PSD für die Java-API bietet Unterstützung für CMYK- und YCCK-Farbmodelle mit JPEG-LS. Der folgende Codeausschnitt zeigt, wie Sie diese Unterstützung für JPEG-LS verwenden können.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}

## **Unterstützung für 2-7 Bits pro Sample in JPEG-LS-Bildern**
Aspose.PSD für die Java-API bietet Unterstützung für 2-7 Bits pro Sample JPEG-LS-Bilder. Der folgende Codeausschnitt zeigt, wie Sie diese Unterstützung für JPEG-LS verwenden können.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}

## **Festlegen von ColorType und CompressionType für JPEG-Bilder**
Aspose.PSD für die Java-API bietet Unterstützung für Color Type und Compression Type, und setzt sie auf Graustufen und progressiv für JPEG-Bilder. Der folgende Codeausschnitt zeigt, wie Sie diese Unterstützung verwenden können.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}


