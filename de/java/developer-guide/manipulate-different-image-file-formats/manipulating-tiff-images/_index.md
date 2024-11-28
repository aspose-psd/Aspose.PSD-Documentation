---
title: Manipulation von TIFF-Bildern
type: docs
weight: 40
url: /de/java/manipulating-tiff-images/
---

## **Rahmen mit verschiedenen Einstellungen hinzufügen**
TIFF ist ein sehr flexibles Format und ermöglicht das Hinzufügen von verschiedenen Rahmen mit unterschiedlichen Dimensionen, Kompressionen und anderen Einstellungen. Die Aspose.PSD-APIs ermöglichen es Ihnen, beliebige TIFF-Rahmen beliebiger Größe hinzuzufügen, was bei der Erstellung komplexer Dokumente hilft. Wenn es erforderlich ist, die Rahmen während des Hinzufügens anzupassen, um sie alle gleich zu machen, führen Sie die folgenden Schritte aus:

- Erstellen Sie einen neuen leeren Rahmen mit den gewünschten Optionen oder kopieren Sie den Quellrahmen mit den angegebenen Ausgabeoptionen mithilfe der CreateFrameFrom-Methode.
- Ändern Sie die Größe des Quellrahmens/-bildes auf die gewünschten Abmessungen mithilfe der Resize-Methode.
- Fügen Sie die Pixel des Quellrahmens/-bildes dem neuen Rahmen hinzu.
- Fügen Sie den neuen Rahmen dem Ausgabe-TIFF-Bild hinzu.

## **Ebenen eines PSD-Bildes in das Dateiformat Multi-Page TIFF exportieren**
Manchmal müssen PSD-Bildebenen in das Dateiformat Multi-Page TIFF exportiert werden. Dieser Artikel zeigt, wie diese Aufgabe mithilfe der Aspose.PSD for Java-API ausgeführt werden kann. Zunächst laden wir das PSD-Bild von der Festplatte. Dann iterieren wir über die PSD-Bildebenen und erstellen aus den entsprechenden Ebenen TiffFrame. Schließlich speichern wir das resultierende TIFF-Bild in einer einzigen Datei auf der Festplatte.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}

## **Konfiguration der TiffOptions**
Entwickler können verschiedene Eigenschaften der Tiffoptions-Klasse anpassen, um die gewünschten Ergebnisse zu erzielen. In diesem Dokument konzentrieren wir uns auf 4 Haupt-Eigenschaften, die die Attribute des resultierenden Bildes steuern.

Diese Eigenschaften sind nachfolgend aufgeführt.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Beim Initialisieren einer leeren Tiffoptions-Struktur ist jede Option auf ihren Standardwert gesetzt, beispielsweise ist die Kompression auf "None" gesetzt, BitsPerSample ist auf 1 und Photometric auf MinIsWhite. Das Speichern in diesem Format macht das Endbild schwarz-weiß, und dies ist das erwartete Verhalten für eine solche Kombination von Optionen. Um die farbigen Ergebnisse zu erhalten, müssen alle oben genannten Eigenschaften auf Werte eingestellt werden, die dem gewünschten Farbraum entsprechen, oder Sie können die Tiffoptions-Struktur mit vordefinierten Einstellungen initialisieren, wie später in diesem Artikel diskutiert. Im Folgenden finden Sie eine Tabelle, die die erwarteten Parameterwerte beschreibt, die Sie einstellen können, um die gewünschten Ergebnisse zu erzielen. Bitte beachten Sie, dass Sie alle 4 Spalten durch Tiffoptions einstellen sollten, um irgendwelche geladenen/erstellten Bilder im TIFF-Dateiformat zu speichern.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (Palette, Farbmodus) jeweils nur ein Kanal|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (Graustufenmodus) jeweils nur ein Kanal|None|
|Palette|LZW/Uncompressed|8 (Palette, Farbmodus) jeweils nur ein Kanal|Horizontal (mehr Kompression für LZW bei gleichen Mustern)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (Graustufenmodus) jeweils nur ein Kanal|Horizontal (mehr Kompression für LZW bei gleichen Mustern)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB-Kanäle)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB-Kanäle und zusätzlicher Alphakanal kann durch TiffOptions.AlphaStorage festgelegt werden) Tatsächlich wird jede zusätzliche Kanalanzahl unterstützt, aber jeder Kanal muss eine Größe von 8 Bit haben, z.B. [8,8,8,8,8,8]|None/Horizontal|
Alle 4 Eigenschaften sollten über TiffOptions eingestellt werden, um jedes Bildformat in das Tiff-Format zu speichern. Bei Verwendung unterschiedlicher Kombinationen können einige Viewer (einschließlich des Windows-Fotoanzeigeprogramms) möglicherweise die resultierenden Bilder nicht anzeigen, da sie nur eine begrenzte Unterstützung bieten. In einem solchen Fall wählen Sie bitte einen anderen Viewer für Ihre Tests aus.
### **Vordefinierte Einstellungen für die TiffOptions-Klasse**
Um den Benutzern die Arbeit zu erleichtern und die Fehlkonfiguration der Tiffoptions-Instanz zu vermeiden, hat die Aspose.PSD for Java API einen weiteren Konstruktor freigegeben, der einen Parameter vom Typ TiffExpectedFormat akzeptiert. Basierend auf dem ausgewählten Wert aus der TiffExpectedFormat-Aufzählung konfiguriert die API automatisch alle obligatorischen Eigenschaften für die Tiffoptions-Instanz, um die gewünschten Ergebnisse zu erzielen. Bevor wir zum Beispielcode übergehen, hier ist die Liste der TiffExpectedFormat-Felder und deren Details zur besseren Verständnis der Verwendung.

- TiffExpectedFormat.Default: Das Setzen des Felds auf Default verhält sich ähnlich wie der Standardkonstruktor der Tiffoptions-Klasse, ohne Kompression und BitsPerPixel auf 1 festzulegen, um ein schwarz-weißes Ergebnis zu erzielen. Es wird empfohlen, dieses Feld zu verwenden, wenn andere formatbezogene Eigenschaften manuell gemäß den gewünschten Ergebnissen eingestellt werden sollen.
- TiffExpectedFormat.TiffCcitRle: Spezifisch für die RLE-Kodierung, während das Ergebnis im 1 BitsPerPixel (schwarz-weiß) TIFF-Format gespeichert wird.
- (Weiterer Text wurde übersetzt und aus Gründen der Zeichenbeschränkung abgebrochen)
