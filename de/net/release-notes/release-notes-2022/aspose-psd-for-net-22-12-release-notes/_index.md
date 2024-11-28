---
title: Aspose.PSD für .NET 22.12 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-fuer-net-22-12-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- In dieser Version wurde ein Regression mit dem 16-Bit-Export behoben.

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1336|Fügen Sie die bearbeitbare TextOrientation-Eigenschaft dem IText-Interface hinzu|Funktion|
|PSDNET-725|Das Ändern der Größe der angegebenen PSD-Datei mit einer Ebenenmaske erzeugt eine falsche Maske|Fehler|
|PSDNET-1277|Fügen Sie die Möglichkeit hinzu, eine Maske für 16 Bilder zu speichern und zu laden|Fehler|
|PSDNET-1281|Fehlerhafte Transparenz beim Speichern eines 16-Bit-Bildes als 16- oder 8-Bit-Bild|Fehler|
|PSDNET-1375|Korrigieren Sie CMYK in 16-Bit-Farbe|Fehler|


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Entfernte APIs:**
- Keine


## **Beispiele für die Verwendung:**

**PSDNET-725. Das Ändern der Größe der angegebenen PSD-Datei mit einer Ebenenmaske erzeugt eine falsche Maske**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Es öffnet die Ausgangs-PSD-Datei
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Es ändert die Größe 
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Es öffnet eine neu skalierte PSD-Datei
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Es rendert zu PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Fügen Sie die Möglichkeit hinzu, eine Maske für 16 Bilder zu speichern und zu laden**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Optionen ermöglichen das Speichern von 16-Bit-Farben
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Die PSD-Datei wird mit Transparenz gespeichert
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281.Fehlerhafte Transparenz beim Speichern eines 16-Bit-Bildes in ein 16- oder 8-Bit-Bild**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// Die 16-Bit-Farbpsd-Datei (mit Transparenz) wird geöffnet und als 16-Bit-Farbe gespeichert
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Die als 16-Bit-Farbe gespeicherte PSD-Datei wird in eine PNG-Datei mit Transparenz gerendert
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Fügen Sie die bearbeitbare TextOrientation-Eigenschaft dem IText-Interface hinzu**

{{< highlight csharp >}}
// Der folgende Code zeigt die Möglichkeit, die neue TextOrientation-Eigenschaft zu bearbeiten.
// Dies beeinträchtigt die Wiedergabe im Moment nicht, sondern ermöglicht nur die Bearbeitung des Eigenschaftswerts.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Korrektes Lesen
    }
    else
    {
        throw new Exception("Falsches Lesen des Eigenschaftswerts für TextOrientation");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Korrektes Lesen
    }
    else
    {
        throw new Exception("Falsches Lesen des Eigenschaftswerts für TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Korrigieren Sie CMYK in 16-Bit-Farbe**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Es setzt Konvertierungsoptionen
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Es konvertiert und speichert
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Es öffnet die konvertierte Datei und rendert sie zu PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
