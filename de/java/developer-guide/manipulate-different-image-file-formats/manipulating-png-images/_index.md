---
title: Manipulieren von PNG-Bildern
type: docs
weight: 30
url: /de/java/manipulieren-von-png-bildern/
---

## **Transparenz für PNG-Bilder festlegen**
Einer der Vorteile des Speicherns von Bildern im PNG-Format ist, dass PNG einen transparenten Hintergrund haben kann. Aspose.PSD für Java bietet die Möglichkeit, die Transparenz für die Klassen PngImage & RasterImage anzugeben, wie im folgenden Abschnitt dargestellt. Die Aspose.PSD für Java-API kann verwendet werden, um bei der Erstellung neuer PNG-Bilder oder bei der Konvertierung vorhandener Bilder in das PNG-Format eine beliebige Farbe als transparent festzulegen. Zu diesem Zweck hat die Aspose.PSD für Java-API die Eigenschaft TransparentColor und die Enumeration PngColorType freigegeben, die festgelegt werden kann, um eine Farbe als transparent im PNG-Bild zu rendern. Der folgende Codeausschnitt zeigt, wie ein vorhandenes PSD-Bild in ein PNG-Bild konvertiert wird, indem der gewünschte Farbe als transparent angegeben wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Auflösung für PNG-Bilder festlegen**
Aspose.PSD für Java bietet die Klasse ResolutionSetting, die verwendet werden kann, um die Auflösung für alle Bildformate einschließlich PNG festzulegen. Dieser Artikel zeigt die Verwendung der Aspose.PSD für Java-API, um die horizontalen und vertikalen Auflösungsparameter für das PNG-Bildformat festzulegen. Der folgende Codeausschnitt lädt ein vorhandenes PSD-Bild und konvertiert es auch in das PNG-Format, wobei die Auflösung geändert wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Komprimieren von PNG-Dateien**
Das Portable Network Graphic (PNG) ist ein verlustfreies Komprimierungsformat zum Übertragen eines Bitmaps über Netzwerke. Wenn Sie ein Bild in einem Programm als PNG-Datei speichern, werden Sie möglicherweise aufgefordert, einen Komprimierungsgrad in einem Bereich von 0 bis zu einem Maximalgrad zu wählen. Durch das Festlegen dieses Werts wird die Dateigröße tatsächlich komprimiert, ohne dass die Bildqualität verringert wird. Dieser Artikel beschreibt, wie Sie mit den Aspose.PSD-APIs die Größe der PNG-Datei steuern können. Mit den Aspose.PSD-APIs können Sie die Kompressionsstufen für das PNG-Dateiformat mithilfe der Klasse PngOptions festlegen, die eine Eigenschaft CompressionLevel vom Typ int hat. Diese Eigenschaft akzeptiert einen Wert von 0 bis 9, wobei 9 die maximale Kompression ist. Der folgende Codeausschnitt zeigt, wie die Kompressionsstufen mit der Aspose.PSD für Java-API festgelegt werden.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Festlegen der Farbtiefe für PNG-Bilder**
Die Farbtiefe in der Bildverarbeitung ist die Anzahl der Bits, die verwendet werden, um die Farbe eines einzelnen Pixels in einem Bitmapbild anzugeben. Wie alle anderen Bitmapformate wird auch die Farbtiefe von PNG in Bit angegeben, z. B. 1 Bit (2 Farben), 2 Bit (4 Farben), 4 Bit (16 Farben) und 8 Bit (256 Farben). Die Aspose.PSD für Java-API kann verwendet werden, um die Farbtiefe für PNG-Bilder mithilfe der Eigenschaft BitDepth der Klasse PngOptions festzulegen. Derzeit kann die Eigenschaft BitDepth auf 1, 2, 4 oder 8 Bits für Grauskalen- und indizierte Farbtypen festgelegt werden. Für alle anderen Farbtypen werden nur 8 Bits unterstützt. Der folgende Codeausschnitt zeigt, wie die Farbtiefe für ein PNG-Bild festgelegt wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Filtermethoden auf PNG-Bilder anwenden**
Aspose.PSD für Java bietet die Enumeration PngFilterType, die verwendet werden kann, um den Filtertyp für PNG-Bilder festzulegen. Der folgende Codeausschnitt zeigt, wie ein Filter auf ein vorhandenes PSD-Datei zu PNG-Bild angewendet wird, indem PngFilterType verwendet wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Ändern der Hintergrundfarbe eines transparenten PNG-Bildes**
PNG-Formatbilder können einen transparenten Hintergrund haben. Aspose.PSD für Java bietet die Möglichkeit, die Hintergrundfarbe eines PNG-Bildes mit transparentem Hintergrund zu ändern. Mit der Aspose.PSD für Java-API kann die Farbe eines transparenten PNG-Bildes festgelegt/geändert werden. Der folgende Codeausschnitt zeigt, wie die Hintergrundfarbe eines transparenten PNG-Bildes festgelegt/geändert wird.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
