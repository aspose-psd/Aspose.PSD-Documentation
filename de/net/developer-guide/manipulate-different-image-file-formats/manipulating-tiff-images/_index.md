---
title: Manipulation von TIFF-Bildern
type: docs
weight: 50
url: /de/net/manipulation-von-tiff-bildern/
---

## **Rahmen hinzufügen mit unterschiedlichen Einstellungen**
TIFF ist ein sehr flexibles Format, das es ermöglicht, verschiedene Rahmen mit unterschiedlichen Abmessungen, Kompressionen und anderen Einstellungen hinzuzufügen. Aspose.PSD APIs ermöglichen es Ihnen, jeden TIFF-Rahmen beliebiger Größe hinzuzufügen, was bei der Erstellung komplexer Dokumente hilft. Wenn es erforderlich ist, die Rahmen während des Hinzufügens anzupassen, um sie alle gleich zu machen, führen Sie die folgenden Schritte aus:

- Erstellen Sie einen neuen leeren Rahmen mit den gewünschten Optionen oder kopieren Sie den Quellrahmen mit den angegebenen Ausgabesettings mithilfe der Methode CreateFrameFrom.
- Ändern Sie die Größe des Quellrahmens/ -bildes auf die gewünschten Abmessungen mithilfe der Resize-Methode.
- Fügen Sie die Pixel des Quellrahmens/-bildes dem neuen Rahmen hinzu.
- Fügen Sie den neuen Rahmen dem Ausgabe-TIFF-Bild hinzu.

## **Export von Ebenen eines PSD-Bildes im Multi-Page-Tiff-Dateiformat**
Manchmal müssen Sie Ebenen eines PSD-Bildes im Multi-Page-TIFF-Dateiformat exportieren. Dieser Artikel zeigt, wie Sie diese Aufgabe mithilfe der Aspose.PSD für .NET API ausführen können. Zunächst laden wir das PSD-Bild von der Festplatte. Dann werden wir über die Ebenen des PSD-Bildes iterieren und ein TiffFrame aus den entsprechenden Ebenen erstellen. Schließlich speichern wir das resultierende Tiff-Bild in einer einzelnen Datei auf der Festplatte.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **TiffOptions Konfiguration**
Entwickler können verschiedene Eigenschaften der Klasse TiffOptions einstellen, um die gewünschten Ergebnisse zu erzielen. In diesem Dokument konzentrieren wir uns auf 4 Hauptattribute, die die attributiven Eigenschaften des resultierenden Bilds steuern.

Diese Eigenschaften sind nachstehend aufgeführt.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Wenn wir eine leere TiffOptions-Struktur initialisieren, wird jede Option auf ihren Standardwert gesetzt. Beispielsweise wird die Kompression auf None gesetzt, BitsPerSample als 1 und Photometric als MinIsWhite. Beim Speichern in diesem Format wird das Endbild schwarz-weiß und dies ist das erwartete Verhalten für diese Optionskombination. Um farbige Ergebnisse zu erzielen, müssen alle oben genannten Eigenschaften auf Werte gesetzt werden, die dem gewünschten Farbraum entsprechen, oder Sie können die TiffOptions-Struktur mit vordefinierten Einstellungen initialisieren, wie später in diesem Artikel erläutert. Im Folgenden ist eine Tabelle beschrieben, die die erwarteten Parameterwerte enthält, die Sie setzen können, um die gewünschten Ergebnisse zu erzielen. Bitte beachten Sie, dass Sie alle 4 Spalten durch TiffOptions setzen sollten, um ein beliebiges geladenes/erstelltes Bild im TIFF-Format zu speichern.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Unkomprimiert|1/4/8/16 (Palette, Farbmodus) nur einzelner Kanal|None|
|MinIsWhite/MinIsBlack|LZW/Unkomprimiert|1/4/8/16 (Graustufenmodus) nur einzelner Kanal|None|
|Palette|LZW/Unkomprimiert|8 (Palette, Farbmodus) nur einzelner Kanal|Horizontal (mehr Kompression für LZW bei gleichen Mustern)| 
|MinIsWhite/MinIsBlack|LZW/Unkomprimiert|8 (Graustufenmodus) nur einzelner Kanal|Horizontal (mehr Kompression für LZW bei gleichen Mustern)| 
|RGB|LZW/Unkomprimiert|[8,8,8] (3 RGB-Kanäle)|None/Horizontal|
|RGB|LZW/Unkomprimiert|[8,8,8,8] (3 RGB-Kanäle und zusätzlicher Alphakanal kann über TiffOptions.AlphaStorage eingestellt werden) Tatsächlich wird jede zusätzliche Anzahl von Kanälen unterstützt, aber jeder Kanal muss eine Größe von 8 Bit haben, wie [8,8,8,8,8,8]|None/Horizontal|

Alle 4 Eigenschaften sollten durch TiffOptions gesetzt werden, um ein Bild in Tiff-Format zu speichern. Bei Verwendung unterschiedlicher Kombinationen können einige Viewer (einschließlich des Windows-Fotoanzeigers) die resultierende Abbildung möglicherweise nicht richtig wiedergeben, aufgrund der begrenzten Unterstützung, die sie bieten. Wählen Sie in einem solchen Fall bitte einen anderen Viewer für Ihre Tests aus.

### **Vordefinierte Einstellungen für die TiffOptions-Klasse**
Um den Benutzern die Konfiguration zu erleichtern und die Fehlkonfiguration der TiffOptions-Instanz zu vermeiden, hat die Aspose.PSD für .NET API einen weiteren Konstruktor freigegeben, der ein Parameter vom Typ [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat) akzeptiert. Basierend auf dem ausgewählten Wert aus der TiffExpectedFormat-Enumeration konfiguriert die API automatisch alle obligatorischen Eigenschaften für die TiffOptions-Instanz, um die gewünschten Ergebnisse zu erzielen. Bevor wir zum Beispielcode übergehen, hier ist die Liste der TiffExpectedFormat-Felder und ihre Details, um das Verständnis für die Verwendung zu verbessern.

- TiffExpectedFormat.Default: Wenn das Feld auf Standard gesetzt ist, ähnelt es dem Standardkonstruktor der TiffOptions-Klasse ohne Kompression und BitsPerPixel auf 1 gesetzt, um ein Schwarz-Weiß-Ergebnis zu erzielen. Es wird empfohlen, dieses Feld zu verwenden, wenn andere formatbezogene Eigenschaften manuell entsprechend den gewünschten Ergebnissen eingestellt werden sollen.
- TiffExpectedFormat.TiffCcitRle: Spezifisch für RLE-Kodierung beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß) TIFF-Format.
- TiffExpectedFormat.TiffCcittFax3: Spezifisch für CCITT Fax3-Kodierung beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß) TIFF-Format.
- TiffExpectedFormat.TiffCcittFax4: Spezifisch für CCITT Fax4-Kodierung beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß) TIFF-Format.
- TiffExpectedFormat.TiffDeflateBW: Spezifisch für Deflate-Kompression beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß) TIFF-Format.
- TiffExpectedFormat.TiffDeflateRGB: Spezifisch für Deflate-Kompression beim Speichern des Ergebnisses im RGB (Farb-) TIFF-Format.
- TiffExpectedFormat.TiffJpegRGB: Spezifisch für JPEG-Kompression beim Speichern des Ergebnisses im RGB (Farb-) TIFF-Format.
- TiffExpectedFormat.TiffJpegYCBCR: Spezifisch für Deflate-Kompression beim Speichern des Ergebnisses im YCBCR (Farb-) TIFF-Format.
- TiffExpectedFormat.TiffLzwBW: Spezifisch für LZW-Kompression beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß) TIFF-Format.
- TiffExpectedFormat.TiffLzwRGB: Spezifisch für LZW-Kompression beim Speichern des Ergebnisses im RGB (Farb-) TIFF-Format.
- TiffExpectedFormat.TiffLzwRGBA: Spezifisch für LZW-Kompression beim Speichern des Ergebnisses im RGBA (Farbe mit Transparenz) TIFF-Format.
- TiffExpectedFormat.TiffNoCompressionBW: Spezifisch für unkomprimiertes TIFF-Format beim Speichern des Ergebnisses im 1 BitsPerPixel (Schwarz-Weiß).
- TiffExpectedFormat.TiffNoCompressionRGB: Spezifisch für unkomprimiertes TIFF-Format beim Speichern des Ergebnisses im RGB (Farbe).
- TiffExpectedFormat.TiffNoCompressionRGBA: Spezifisch für unkomprimiertes TIFF-Format beim Speichern des Ergebnisses im RGBA (Farbe mit Transparenz).

Der folgende Code-Ausschnitt erläutert die Verwendung der TiffExpectedFormat-Felder bei der Erstellung einer Instanz der TiffOptions-Klasse.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **Unterstützung für Deflate- und Adobe Deflate-Kompression**
Das TIFF (Tagged Image File Format) unterstützt verschiedene Arten der Kompression, wobei der Kompressionstyp als Tag (ein Integer-Wert) in der Datei gespeichert wird. Eine solche Kompressionsmethode ist Adobe Deflate (früher bekannt als Deflate). Die Aspose.PSD für .NET API unterstützt diese Kompressionsmethode beim Exportieren und Erstellen von TIFF-Bildern.
### **Speichern eines Bildes in TIFF mit Deflate-Kompression**
Das Konvertieren der geladenen Bilder in TIFF mit Deflate-/Adobe-Deflate-Kompression ist einfach wie folgt.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Erstellen eines TiffImage mit Adobe-Deflate-Kompression**
Das folgende Beispiel zeigt, wie die Aspose.PSD für .NET API verwendet wird, um ein Bild von Grund auf neu zu erstellen, wobei die Adobe-Deflate-Komprimierungsmethode verwendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Komprimierung von TIFF-Bildern**
Die Aspose.PSD für .NET API kann verwendet werden, um PSD-Bilder in das TIFF-Bildformat zu konvertieren und sogar die Kompression des resultierenden TIFF-Bildes zu ändern. Die API kann auch verwendet werden, um verschiedene Bilder als Rahmen in einem TIFF-Bild zu archivieren und dabei die Bilder auf kleinstmögliche Dateigröße zu komprimieren. Die Bildkompression sollte in jedem Fall durch Verringerung der Quelldatengröße erfolgen, unabhängig vom verwendeten Kompressionsalgorithmus. Um das beste Kompressionsverhältnis zu erzielen, können indizierte Farbräume verwendet werden. Der folgende Codeausschnitt erzielt die beste Kompression mit nur 16 indizierten Farben und dem LZW-Komprimierungsalgorithmus, wobei die Quellfarben leichter gerastert sind.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
