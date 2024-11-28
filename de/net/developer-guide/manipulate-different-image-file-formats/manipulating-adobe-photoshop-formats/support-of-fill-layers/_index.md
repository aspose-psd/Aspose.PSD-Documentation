---
title: Unterstützung von Füllschichten
type: docs
weight: 90
url: /de/net/support-of-fill-layers/
---


## **Füllschichten mit Musterfüllung**
Dieser Artikel zeigt, wie die [PSD](https://wiki.fileformat.com/image/psd/) Schicht mit einer Musterfüllung gefüllt wird. Ein Muster ist ein Bild, eine Farbe, ein Schatten oder eine Linie, die verwendet wird, um einen Bereich eines Bildes zu füllen. Verwenden Sie die Aspose.PSD.FileFormats.Psd.Layers.FillLayer, um ein Muster in die PSD-Schicht einzufügen. Die folgenden Codeschnipsel laden eine PSD-Datei, greifen auf die [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)-Klasse zu und setzen das Muster mithilfe der [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) Eigenschaften.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Hier ist ein weiteres Beispiel, das zeigt, wie [Aspose.PSD](https://products.aspose.com/psd/net) das Muster mit Hilfe von [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) und [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) rendert.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Füllschichten mit Verlaufsfüllung**
Dieser Artikel zeigt die Verwendung von Verlaufsfüllung für das Füllen der PSD-Schicht. Aspose.PSD APIs haben effiziente und benutzerfreundliche Methoden für die Erreichung dieses Ziels bereitgestellt. Aspose.PSD hat die Klassen [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) und [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) freigelegt, um einen Verlaufseffekt in eine Schicht einzufügen.

`Die Schritte zum Füllen [der PSD](https://wiki.fileformat.com/image/psd/)-Schicht mit einer Verlaufsfüllung sind so einfach wie unten aufgeführt:

- Laden Sie eine PSD-Datei als Bild unter Verwendung der Factory-Methode [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) der durch die [Image](https://reference.aspose.com/net/psd/aspose.psd/image) Klasse bereitgestellt wird.
- Setzen Sie Einstellungseigenschaften des [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) Objekts.
- Erstellen Sie eine Liste von [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) mit den erforderlichen Farben und Positionen der Farbe.
- Erstellen Sie eine Liste von Transparenzpunkten mit erforderlicher Deckkraft und Position des Transparenzpunkts.
- Rufen Sie die Methode [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) auf.
- Speichern Sie die Ergebnisse.



Der folgende Code-Schnipsel zeigt Ihnen, wie Sie der PSD-Schicht eine Verlaufsfüllung hinzufügen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Hier ist ein weiteres Beispiel, das die Verwendung einer [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** Eigenschaft zeigt, um die PSD-Schicht mit einer Verlaufsfüllung zu füllen. Aspose.PSD unterstützt die folgenden Verlaufstypen durch die GradientType-Enumeration:

- **GradientType.Linear:**       Bei einem linearen Verlauf wechselt die Farbe von der Startfarbe zur Endfarbe in einer geraden Linie.
- **GradientType.Radial:**       Bei einem radialen Verlauf verteilen sich die Farben vom Startpunkt in einem kreisförmigen Muster.
- **GradientType.Angle:**        Bei einem Winkelverlauf verläuft die Farbe gegen den Uhrzeigersinn um den Startpunkt.
- **GradientType.Reflected:** Bei einem gespiegelten Verlauf wird die Farbe auf beiden Seiten des Startpunkts gespiegelt.
- **GradientType.Diamond:**   Der Diamantverlauf erzeugt eine Diamantform vom Startpunkt aus.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Unterstützung der Skaleneigenschaft für Verlaufs-Füllschicht**
Dieser Artikel zeigt, wie die FillLayer mit Verlaufs-Füllung mithilfe von Aspose.PSD für .NET skaliert werden kann. Zu diesem Zweck wurde eine neue Eigenschaft [**Skala**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) in [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings) hinzugefügt.

Im Folgenden wird die Code-Demonstration gezeigt, die zeigt, wie die **Skala**-Eigenschaft verwendet wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Füllung von Schichten mit Farbenfüllung**
Dieser Artikel zeigt, wie die [PSD](https://wiki.fileformat.com/image/psd/)-Schicht mit Farbe gefüllt wird. Verwenden Sie die [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)-Klasse, um Farbe in die PSD-Schicht einzufügen. Der folgende Code-Schnipsel lädt eine PSD-Datei, greift auf die Fill-Schichtklasse zu und setzt die Farbe mit der [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) Eigenschaft.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}

