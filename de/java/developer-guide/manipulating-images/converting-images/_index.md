---
title: Konvertierung von Bildern
type: docs
weight: 20
url: /de/java/konvertierung-von-bildern/
---

## **Konvertierung von Bildern in Schwarz-Weiß und Graustufen**
Manchmal müssen farbige Bilder für Druck- oder Archivierungszwecke in Schwarz-Weiß oder Graustufen umgewandelt werden. Dieser Artikel demonstriert die Verwendung der Aspose.PSD für Java-API, um dies mit zwei unten beschriebenen Methoden zu erreichen.

- Binarisierung
- Grauskalierung
### **Binarisierung**
Um das Konzept der Binarisierung zu verstehen, ist es wichtig, ein Binärbild zu definieren; das ist ein digitales Bild, das für jeden Pixel nur zwei mögliche Werte haben kann. Normalerweise werden die beiden Farben, die für ein Binärbild verwendet werden, schwarz und weiß verwendet, obwohl jede beliebige Kombination von zwei Farben verwendet werden kann. Binarisierung ist der Prozess, ein Bild in Bi-Level umzuwandeln, was bedeutet, dass jeder Pixel als ein einzelnes Bit (0 oder 1) gespeichert wird, wobei 0 das Fehlen von Farbe bedeutet und 1 das Vorhandensein von Farbe. Die Aspose.PSD für Java-API unterstützt derzeit zwei Binarisierungsmethoden.
#### **Binarisierung mit festem Schwellenwert**
Der folgende Codeteil zeigt, wie die Binarisierung mit festem Schwellenwert auf ein Bild angewendet werden kann.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-BinarisierungMitFestemSchwellenwert-BinarisierungMitFestemSchwellenwert.java" >}}
#### **Binarisierung mit Otsu-Schwellenwert**
Der folgende Codeteil zeigt, wie die Binarisierung mit Otsu-Schwellenwert auf ein Bild angewendet werden kann.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-BinarisierungMitOtsuSchwellenwert-BinarisierungMitOtsuSchwellenwert.java" >}}
### **Grauskalierung**
Die Grauskalierung ist der Prozess der Umwandlung eines kontinuierlichen Bildes in ein Bild mit diskreten Graustufen. Der folgende Codeteil zeigt, wie die Grauskalierung verwendet wird.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-Grauskalierung-Grauskalierung.java" >}}
## **GIF-Bildschichten in TIFF-Bild konvertieren**
Manchmal ist es erforderlich, Schichten eines PSD-Bildes in ein anderes Rasterbildformat zu extrahieren und zu konvertieren, um eine Anwendungsanforderung zu erfüllen. Die Aspose.PSD-API unterstützt die Funktion zum Extrahieren und Konvertieren von Schichten eines PSD-Bildes in ein anderes Rasterbildformat. Zunächst werden wir eine Instanz des Bildes erstellen und das PSD-Bild von der lokalen Festplatte laden, dann werden wir jede Schicht im Schichtenobjekt durchlaufen. Danach werden wir den Block in ein TIFF-Bild umwandeln. Der folgende Codeteil zeigt, wie man PSD-Bildschichten in TIFF-Bilder konvertiert.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-GIFBildschichtenZuTIFF-GIFBildschichtenZuTIFF.java" >}}
## **Konvertierung von CMYK-PSD in CMYK-TIFF**
Mit Aspose.PSD für Java können Entwickler eine CMYK-PSD-Datei in das CMYK-Tiff-Format konvertieren. Dieser Artikel zeigt, wie man mit Aspose.PSD CMYK-PSD-Dateien in das CMYK-TIFF-Format exportiert/konvertiert. Mit Aspose.PSD für Java können Sie PSD-Bilder laden und dann verschiedene Eigenschaften mit der TiffOptions-Klasse festlegen und das Bild speichern oder exportieren. Der folgende Codeteil zeigt, wie man dieses Feature verwendet.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-CMYKPSDzuCMYKTiff-CMYKPSDzuCMYKTiff.java" >}}
## **Export von Bildern**
Zusätzlich zu einer Vielzahl von Bildverarbeitungsroutinen bietet Aspose.PSD spezialisierte Klassen, um PSD-Dateiformate in andere Formate zu konvertieren. Mit dieser Bibliothek ist die Konvertierung von PSD-Bildern sehr einfach und intuitiv. Im Folgenden sind einige spezialisierte Klassen für diesen Zweck im ImageOptions-Namespace aufgeführt.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Es ist einfach, PSD-Bilder mit der Aspose.PSD für Java-API zu exportieren. Alles, was Sie benötigen, ist ein Objekt der entsprechenden Klasse des ImageOptions-Namespace. Durch die Verwendung dieser Klassen können Sie jedes Bild, das mit Aspose.PSD für Java erstellt, bearbeitet oder einfach geladen wurde, problemlos in jedes unterstützte Format exportieren.
## **Kombinieren von Bildern**
Dieses Beispiel verwendet die Graphics-Klasse und zeigt, wie zwei oder mehr Bilder zu einem einzelnen vollständigen Bild kombiniert werden können. Zur Veranschaulichung der Operation erstellt das Beispiel ein neues PsdImage und zeichnet Bilder auf der Leinwandfläche mithilfe der von der Graphics-Klasse bereitgestellten Draw Image-Methode. Mit der Graphics-Klasse können zwei oder mehr Bilder so kombiniert werden, dass das resultierende Bild wie ein vollständiges Bild ohne Zwischenräume zwischen den Bildteilen und ohne Seiten aussieht. Die Größe der Leinwand muss der Größe des resultierenden Bildes entsprechen. Im Folgenden ist das Codebeispiel aufgeführt, das zeigt, wie die Draw Image-Methode der Graphics-Klasse verwendet wird, um Bilder in einem Bild zu kombinieren.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenUndFormatierenVonBildern-KombinierenVonBildern-KombinierenVonBildern.java" >}}
## **Bilder erweitern und zuschneiden**
Die Aspose.PSD-API ermöglicht es Ihnen, ein Bild während des Bildkonvertierungsprozesses zu erweitern oder zuzuschneiden. Der Entwickler muss ein Rechteck mit X- und Y-Koordinaten erstellen und die Breite und Höhe des Rechteckkastens angeben. Die X-, Y- und Breite-, Höhe-Werte des Rechtecks werden die Erweiterung oder den Zuschnitt des geladenen Bildes darstellen. Wenn erforderlich, das Bild während der Bildkonvertierung zu erweitern oder zu zuschneiden, führen Sie die folgenden Schritte aus:

1. Eine Instanz der RasterImage-Klasse erstellen und das vorhandene Bild laden.
1. Eine Instanz der ImageOptions-Klasse erstellen.
1. Eine Instanz der Rectangle-Klasse erstellen und die X-, Y- und Breite-, Höhe-Werte des Rechtecks initialisieren.
1. Die Save-Methode der RasterImage-Klasse aufrufen und dabei den Ausgabedateinamen, die Bildoptionen und das Rechteckobjekt als Parameter übergeben.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenUndFormatierenVonBildern-ErweiternUndZuschneidenVonBildern-ErweiternUndZuschneidenVonBildern.java" >}}
## **XMP-Daten in Bildern lesen und schreiben**
XMP (Extensible Metadata Platform) ist ein ISO-Standard. XMP standardisiert ein Datenschema, ein Serialisierungsformat und Kernattribute zur Definition und Verarbeitung von erweiterbaren Metadaten. Es gibt auch Richtlinien für das Einbetten von XMP-Informationen in beliebte Bilder wie JPEG, ohne deren Lesbarkeit durch Anwendungen zu beeinträchtigen, die XMP nicht unterstützen. Mit der Aspose.PSD für Java-API können Entwickler XMP-Metadaten in Bilder lesen oder schreiben. Dieser Artikel zeigt, wie XMP-Metadaten aus einem Bild gelesen und XMP-Metadaten in Bilder geschrieben werden können.
### **XMP-Metadaten erstellen, schreiben und aus Datei lesen**
Mit Hilfe des XMP-Namensraums kann ein Entwickler ein XMP-Metadatenobjekt erstellen und es in ein Bild schreiben. Der folgende Codeteil zeigt, wie die im XMP-Namensraum enthaltenen XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage und DublinCorePackage-Pakete verwendet werden.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-ZeichnenUndFormatierenVonBildern-XMPMetadatenErstellen-XMPMetadatenErstellen.java" >}}
## **Bilder in einer Umgebung mit mehreren Threads exportieren**
Aspose.PSD für Java unterstützt jetzt die Konvertierung von Bildern in einer Umgebung mit mehreren Threads. Aspose.PSD für Java gewährleistet die optimierte Leistung der Operationen während der Ausführung des Codes in einer multithreaded Umgebung. Alle Klassen für Bildoptionen (z.B. BmpOptions, TiffOptions, JpegOptions, usw.) in Aspose.PSD für Java implementieren das IDisposable-Interface. Daher ist es ein Muss, dass der Entwickler das Objekt der Bildoptionenklasse ordnungsgemäß entsorgt, falls die Source-Eigenschaft festgelegt ist. Im folgenden Codeteil wird diese Funktionalität demonstriert.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-BilderExportierenInMultithread-Umgebung-BilderExportierenInMultithread-Umgebung.java" >}}



Aspose.PSD unterstützt jetzt die SyncRoot-Eigenschaft bei der Arbeit in einer Multi-Thread-Umgebung. Entwickler können diese Eigenschaft verwenden, um den Zugriff auf den Quellstrom zu synchronisieren. Der folgende Codeteil zeigt, wie die SyncRoot-Eigenschaft verwendet werden kann.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Beispiele-src-main-java-com-aspose-psd-Beispiele-Konvertierung-SyncRoot-SyncRoot.java" >}}
