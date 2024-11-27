---
title: Manipulating PNG-Bilder
type: docs
weight: 40
url: /de/net/manipulating-png-bilder/
---

## **Transparenz für PNG-Bilder festlegen**
Einer der Vorteile beim Speichern von Bildern im PNG-Format ist, dass PNG einen transparenten Hintergrund haben kann. Aspose.PSD für .NET bietet die Möglichkeit, die Transparenz für die PNG-Bilder und Rasterbilder festzulegen, wie im folgenden Abschnitt demonstriert wird. Die Aspose.PSD für .NET-API kann verwendet werden, um beim Erstellen neuer PNG-Bilder oder beim Konvertieren vorhandener Bilder in das PNG-Format eine beliebige Farbe als transparent festzulegen. Zu diesem Zweck hat die Aspose.PSD für .NET-API die Eigenschaft [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) und die Aufzählung [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) freigelegt, die festgelegt werden können, um eine beliebige Farbe als transparent im PNG-Bild zu rendern. Der unten bereitgestellte Code zeigt, wie ein vorhandenes PSD-Bild in ein PNG-Bild konvertiert wird, wobei die gewünschte Farbe als transparent festgelegt ist.
 
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}

## **Auflösung für PNG-Bilder festlegen**
Aspose.PSD für .NET stellt die ResolutionSetting-Klasse bereit, die verwendet werden kann, um die Auflösung für alle Bildformate einschließlich PNG festzulegen. Dieser Artikel demonstriert die Verwendung der Aspose.PSD für .NET-API, um die horizontalen und vertikalen Auflösungsparameter für das PNG-Bildformat festzulegen. Der folgende Codeausschnitt lädt ein vorhandenes PSD-Bild, konvertiert es in das PNG-Format und ändert auch die Auflösung.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}

## **Komprimieren von PNG-Dateien**
Das Portable Network Graphics (PNG) ist ein verlustfreies Komprimierungsformat für die Übertragung eines Bitmaps über Netzwerke. Wenn Sie ein Bild in einem Programm als PNG-Datei speichern, können Sie aufgefordert werden, einen Kompressionsgrad in einem Bereich von 0 bis zu einem Maximalwert zu wählen. Durch Festlegen dieses Werts wird die Dateigröße tatsächlich komprimiert, ohne die Bildqualität zu verringern. Dieser Artikel beschreibt, wie Aspose.PSD-APIs es Ihnen ermöglichen, die Größe von PNG-Dateien zu kontrollieren. Die Aspose.PSD-APIs können verwendet werden, um die Kompressionsstufen des PNG-Dateiformats mithilfe der PngOptions-Klasse festzulegen, die eine Ganzzahl [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) Eigenschaft hat. Diese Eigenschaft akzeptiert einen Wert von 0 bis 9, wobei 9 die maximale Kompression ist. Der unten bereitgestellte Code zeigt, wie die Kompressionsstufen mit der Aspose.PSD für .NET-API festgelegt werden können.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}

## **Bit-Tiefe für PNG-Bilder festlegen**
Die Bit-Tiefe in der Bildgebung ist die Anzahl der Bits, die zur Anzeige der Farbe eines einzelnen Pixels in einem Bitmap-Bild verwendet werden. Wie alle anderen Bitmap-Formate wird auch die PNG-Farbentiefe in Bit dargestellt, wie z.B. 1-Bit (2 Farben), 2-Bit (4 Farben), 4-Bit (16 Farben) und 8-Bit (256 Farben). Aspose.PSD für .NET-API kann verwendet werden, um die Bit-Tiefe für PNG-Bilder mit der Eigenschaft [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) festzulegen, die von der PngOptions-Klasse freigelegt wird. Aktuell kann die BitDepth-Eigenschaft auf 1, 2, 4 oder 8 Bits für Graustufen- und indizierte Farbtypen festgelegt werden. Für alle anderen Farbtypen werden nur 8 Bits unterstützt. Der unten bereitgestellte Code zeigt, wie die Bit-Tiefe für ein PNG-Bild festgelegt werden kann.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}

## **Anwendung von Filtermethoden auf PNG-Bilder**
Die Bit-Tiefe in der Bildgebung ist die Anzahl der Bits, die zur Anzeige der Farbe eines einzelnen Pixels in einem Bitmap-Bild verwendet werden. Wie alle anderen Bitmap-Formate wird auch die PNG-Farbentiefe in Bit dargestellt, wie z.B. 1-Bit (2 Farben), 2-Bit (4 Farben), 4-Bit (16 Farben) und 8-Bit (256 Farben). Aspose.PSD für .NET-API kann verwendet werden, um die Bit-Tiefe für PNG-Bilder mit der von der PngOptions-Klasse freigelegten BitDepth-Eigenschaft festzulegen. Aktuell kann die BitDepth-Eigenschaft auf 1, 2, 4 oder 8 Bits für Graustufen- und indizierte Farbtypen festgelegt werden. Für alle anderen Farbtypen werden nur 8 Bits unterstützt. Der folgende Codeausschnitt zeigt, wie die Bit-Tiefe für ein PNG-Bild festgelegt werden kann.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}

## **Ändern der Hintergrundfarbe eines transparenten PNG-Bildes**
PNG-Formatbilder können einen transparenten Hintergrund haben. Aspose.PSD für .NET bietet die Möglichkeit, die Hintergrundfarbe eines PNG-Bildes mit transparentem Hintergrund zu ändern. Die Aspose.PSD für .NET-API kann verwendet werden, um die Farbe eines transparenten PNG-Bildes zu setzen/ändern. Der unten bereitgestellte Code zeigt, wie die Hintergrundfarbe eines transparenten PNG-Bildes gesetzt/geändert werden kann.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
