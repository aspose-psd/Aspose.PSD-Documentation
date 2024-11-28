---
title: Bilder konvertieren
type: docs
weight: 20
url: /de/net/bilder-konvertieren/
---

## **Bilder in Schwarzweiß und Graustufen umwandeln**
Manchmal müssen farbige Bilder für Druck- oder Archivierungszwecke in Schwarzweiß oder Graustufen umgewandelt werden. Dieser Artikel zeigt die Verwendung der Aspose.PSD für die .NET-API, um dies mit zwei unten aufgeführten Methoden zu erreichen.

- Binarisierung
- Grauskalierung
### **Binarisierung**
Um das Konzept der Binarisierung zu verstehen, ist es wichtig, ein Binärbild zu definieren; das ist ein digitales Bild, das für jeden Pixel nur zwei mögliche Werte haben kann. Normalerweise werden für ein Binärbild die beiden Farben Schwarz und Weiß verwendet, obwohl jede beliebige Farbe verwendet werden kann. Binarisierung ist der Prozess der Umwandlung eines Bildes in schwarz-weiß, was bedeutet, dass jeder Pixel als ein einzelnes Bit (0 oder 1) gespeichert wird, wobei 0 das Fehlen von Farbe bedeutet und 1 das Vorhandensein von Farbe. Die Aspose.PSD für .NET-API unterstützt derzeit zwei Binarisierungsmethoden.
#### **Binarisierung mit festem Schwellenwert**
Der folgende Code-Ausschnitt zeigt, wie der feste Schwellenwert binarisiert angewendet werden kann.
  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarisierung mit Otsu-Schwellenwert**
Der folgende Code-Ausschnitt zeigt, wie die Otsu-Schwellenwert binarisierte auf ein Bild angewendet wird.
  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Grauskalierung**
Grauskalierung ist der Prozess der Umwandlung eines kontinuierlichen Tonbildes in ein Bild mit diskreten Grautönen. Der folgende Codeausschnitt zeigt, wie die Grauskalierung verwendet wird.
  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **GIF-Bildschichten in TIFF-Bild umwandeln**
Manchmal ist es erforderlich, Ebenen eines PSD-Bildes in ein anderes Rasterbildformat zu extrahieren und umzuwandeln, um den Anforderungen einer Anwendung gerecht zu werden. Die Aspose.PSD-API unterstützt das Extrahieren und Umwandeln von Ebenen eines PSD-Bildes in ein anderes Rasterbildformat. Zunächst werden wir eine Instanz des Bildes erstellen und das PSD-Bild von der lokalen Festplatte laden, dann werden wir jede Ebene im Layer-Eigenschaft iterieren. Dann werden wir den Block in ein TIFF-Bild umwandeln. Der folgende Codeausschnitt zeigt, wie PSD-Bildebenen in TIFF-Bilder konvertiert werden.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Konvertieren von CMYK-PSD in CMYK-TIFF**
Mit Aspose.PSD für .NET können Entwickler eine CMYK-PSD-Datei in das CMYK-Tiff-Format konvertieren. Dieser Artikel zeigt, wie eine CMYK-PSD-Datei ins CMYK-Tiff-Format exportiert/konvertiert werden kann mit Aspose.PSD. Mit Aspose.PSD für .NET können Sie PSD-Bilder laden und verschiedene Eigenschaften mit der [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)-Klasse einstellen und das Bild speichern oder exportieren. Der folgende Codeausschnitt zeigt, wie dies erreicht werden kann.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Bilder exportieren**
Neben einem umfangreichen Satz von Bildverarbeitungsroutinen bietet Aspose.PSD spezialisierte Klassen zum Konvertieren von PSD-Dateiformaten in andere Formate. Mit dieser Bibliothek ist die Konvertierung von PSD-Bildern sehr einfach und intuitiv. Hier sind einige spezialisierte Klassen für diesen Zweck im [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)-Namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Es ist einfach, PSD-Bilder mit der Aspose.PSD für die .NET-API zu exportieren. Alles was Sie brauchen, ist ein Objekt der entsprechenden Klasse aus dem [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)-Namespace. Mit diesen Klassen können Sie jedes Bild, das mit Aspose.PSD für .NET erstellt, bearbeitet oder einfach geladen wurde, leicht in ein beliebiges unterstütztes Format exportieren.
## **Bilder kombinieren**
Dieses Beispiel verwendet die Graphics-Klasse und zeigt, wie zwei oder mehr Bilder zu einem einzigen vollständigen Bild kombiniert werden können. Zur Veranschaulichung erstellt das Beispiel ein neues PsdImage und zeichnet Bilder auf der Leinwandfläche unter Verwendung der von der Graphics-Klasse bereitgestellten Draw-Image-Methode. Mit der Graphics-Klasse können zwei oder mehr Bilder so kombiniert werden, dass das resultierende Bild wie ein vollständiges Bild aussieht, ohne Platz zwischen den Bildteilen und ohne Seiten. Die Leinwandgröße muss der Größe des resultierenden Bildes entsprechen. Im Folgenden ist die Code-Demonstration, die zeigt, wie die [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index)-Methode der [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-Klasse verwendet wird, um Bilder zu kombinieren.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Bilder erweitern und zuschneiden**
Aspose.PSD API ermöglicht es Ihnen, ein Bild während des Bildkonvertierungsprozesses zu erweitern oder zuzuschneiden. Der Entwickler muss ein Rechteck mit X- und Y-Koordinaten erstellen und die Breite und Höhe der Rechteckbox angeben. Die X-, Y- und Breite-, Höhe des Rechtecks geben die Erweiterung oder das Zuschneiden des geladenen Bildes an. Wenn erforderlich, das Bild während der Bildkonvertierung zu erweitern oder zuzuschneiden, führen Sie folgende Schritte aus:

1. Erstellen Sie eine Instanz der [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)-Klasse und laden Sie das vorhandene Bild.
1. Erstellen Sie eine Instanz der ImageOption-Klasse.
1. Erstellen Sie eine Instanz der [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle)-Klasse und initialisieren Sie die X,Y- und Breite-, Höhe des Rechtecks
1. Rufen Sie die [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index)-Methode der RasterImage-Klasse auf, wobei Ausgabedateiname, Bilddateioptionen und das Rechteckobjekt als Parameter übergeben werden.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **XMP-Daten in Bilder schreiben und lesen**
XMP (Extensible Metadata Platform) ist ein ISO-Standard. XMP standardisiert ein Datenmodell, ein Serialisierungsformat und Kern-Eigenschaften für die Definition und Verarbeitung von erweiterbaren Metadaten. Es gibt auch Richtlinien dafür, wie XMP-Informationen in ein beliebtes Bild wie JPEG eingebettet werden können, ohne die Lesbarkeit durch Anwendungen zu beeinträchtigen, die XMP nicht unterstützen. Mit der Aspose.PSD für .NET-API können Entwickler XMP-Metadaten in Bilder einlesen oder schreiben. Dieser Artikel zeigt, wie XMP-Metadaten aus einem Bild gelesen und in Bilder geschrieben werden können.
### **Erstellen von XMP-Metadaten, Schreiben und Lesen aus Datei**
Mit Hilfe des Xmp-Namespaces kann der Entwickler ein XMP-Metadatenobjekt erstellen und es in ein Bild schreiben. Der folgende Code-Ausschnitt zeigt, wie die im [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp)-Namespace enthaltenen XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage und DublinCorePackage-Pakete verwendet werden.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Bilder in einer Mehrfadenumgebung exportieren**
Aspose.PSD für .NET unterstützt jetzt das Konvertieren von Bildern in einer mehrfädigen Umgebung. Aspose.PSD für .NET gewährleistet eine optimierte Leistung von Operationen während der Ausführung von Code in einer mehrfädigen Umgebung. Alle [Bildoption](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)-Klassen (z. B. BmpOptions, TiffOptions, JpegOptions usw.) in Aspose.PSD für .NET implementieren das IDisposable-Interface. Daher ist es erforderlich, dass der Entwickler das Objekt der Bildoptionenklasse ordnungsgemäß freigibt, falls die Source-Eigenschaft gesetzt ist. Der folgende Code-Ausschnitt zeigt die Funktionalität.


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD unterstützt jetzt die SyncRoot-Eigenschaft bei der Arbeit in einer mehrfädigen Umgebung. Der Entwickler kann diese Eigenschaft verwenden, um auf den Quellstrom zuzugreifen. Der folgende Code-Ausschnitt zeigt, wie die SyncRoot-Eigenschaft verwendet werden kann.  


  

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
