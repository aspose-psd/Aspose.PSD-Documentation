---
title: Aspose.PSD für .NET 22.11 - Versionshinweise
type: docs
weight: 20
url: /de/net/aspose-psd-fuer-net-22-11-versionshinweise/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Diese Version weist eine Regression im Fall von 16-Bit-Exporten auf, daher empfehlen wir Vorsicht bei der Verwendung dieses Features in dieser Version.
Bitte aktualisieren Sie Aspose.PSD nicht auf 22.9-22.11, wenn die Verarbeitung von 16-Bit-Bildern Ihre Hauptfunktionalität ist.

Wir arbeiten an Lösungen für diese Probleme.

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-1320|Sehr große PSB-Dateien können nicht exportiert werden|Verbesserung|
|PSDNET-659|Das Zentrum des radialen Farbverlaufs ist beweglich|Feature|
|PSDNET-1330|Nicht unterstützte ZipWithoutPrediction-Komprimierungsmethode für bestimmte Dateien|Feature|
|PSDNET-735|Nach Verwendung einer Transformationsmethode nur für eine Ebene hat die gespeicherte Ebene eine falsche Begrenzung|Fehler|
|PSDNET-1234|Ausnahme beim Laden eines PSD-Bildes mit Muster|Fehler|
|PSDNET-1244|Bildexport fehlgeschlagen (IndexOutOfRangeException) beim Speichern einer PSD-Datei mit chinesischen Symbolen|Fehler|
|PSDNET-1303|Zeitachsen-Aktivbild wendet sich inkorrekt an|Fehler|
|PSDNET-1307|Regression 22.7: Falsche Darstellung von Text mit arabischen Zeichen|Fehler|
|PSDNET-1321|Vektormaske auf der Gruppenebene funktioniert inkorrekt. Das Endbild hat ein schwarzes Loch, sollte es aber nicht haben|Fehler|


## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Entfernte APIs:**
- Keine


## **Beispielanwendungen:**

**PSDNET-659. Das Zentrum des radialen Farbverlaufs ist beweglich**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // Aktualisieren des Versatzpunkts
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Nach Verwendung einer Transformationsmethode nur für eine Ebene hat die gespeicherte Ebene eine falsche Begrenzung**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // Es setzt die neue Größe der Textebene
    const int NeueBreite = 250;
    const int NeueHöhe = 250;

    // Es legt fest, wie die Resize-Funktion die Ebene ändern wird (Standardwert)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Neue Größenänderung für Textebene hier verwenden
    // Nicht nur die Ebene, sondern auch die Transformationsmatrix der Textebene wird geändert
    textLayer.Resize(NeueBreite, NeueHöhe, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // Grund für den Unterschied ist eine andere Standard-Schriftart
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // Alles ist in Ordnung
    }
    else
    {
        throw new Exception("Positionsangabe ist falsch");
    }
}
{{< /highlight >}}

**PSDNET-1234. Ausnahme beim Laden eines PSD-Bildes mit Muster**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. Bildexport fehlgeschlagen (IndexOutOfRangeException) beim Speichern einer PSD-Datei mit chinesischen Symbolen**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // Hier sollte keine Ausnahme auftreten.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame wendet sich inkorrekt an**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. Regression 22.7: Falsche Darstellung von Text mit arabischen Zeichen**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Sehr große PSB-Dateien können nicht exportiert werden**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Vektormaske auf der Gruppenebene funktioniert inkorrekt. Das Endbild hat ein schwarzes Loch, sollte es aber nicht haben**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. Nicht unterstützte ZipWithoutPrediction-Komprimierungsmethode für bestimmte Dateien**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
