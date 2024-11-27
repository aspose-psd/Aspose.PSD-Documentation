---
title: Aspose.PSD für .NET 20.3 - Versionshinweise
type: docs
weight: 100
url: /de/net/aspose-psd-fur-net-20-3-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-188|Unterstützung von .Net Core|Feature|
|PSDNET-523|Konvertierung von Adobe Illustrator-Dateien in PDFs|Feature|
|PSDNET-212|Hinzufügen der Möglichkeit, verschiedene Stile in einer Textebene zu rendern|Feature|
|PSDNET-144|Unterstützung von Black and White Adjustment Layer|Feature|
|PSDNET-233|Hinzufügen der Unterstützung für den Export von AI-Format (Version 8) in andere Formate|Feature|
|PSDNET-540|Unterstützung der Verarbeitung des PassThrough-Überblendungsmodus (nur für Layergruppen verwendet)|Feature|
|PSDNET-539|Ausnahme: Bildladefehler beim Laden eines Bildes mit leerem Unicode Alpha Names-Ressourcen|Bug|
|PSDNET-541|Falsche Ausgabe nach Ändern der Sichtbarkeit einer Layer-Gruppe|Bug|
|PSDNET-516|Ausnahme beim Laden des PSD-Bildes: Der Farbbereich (DropShadow Resource) muss 3 Farbkomponenten für RGB oder 4 Farbkomponenten für CMYK enthalten|Bug|
|PSDNET-536|Ausnahme, wenn versucht wird, auf neu erstellter Ebene zu zeichnen, wenn die einfache Version des Konstruktors verwendet wird|Bug|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **Entfernte APIs:**
- None

## **Anwendungsbeispiele:**
**PSDNET-523. Konvertierung von Adobe Illustrator-Dateien in PDFs**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Hinzufügen der Möglichkeit, verschiedene Stile in einer Textebene zu rendern**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // bearbeiten des Textstils "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // bearbeiten des Textstils "2\r"

    newPortions[2].Style.FauxBold = true; // bearbeiten des Textstils "Bold"

    newPortions[3].Style.FauxItalic = true; // bearbeiten des Textstils "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // bearbeiten des Textstils "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // bearbeiten des Textstils "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Hinzufügen der Unterstützung für den Export von AI-Format (Version 8) in andere Formate**

{{< highlight java >}}

 // Beispiel für den Export einer AI-Datei in PSD- und PNG-Format

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Unterstützung der Verarbeitung des PassThrough-Überblendungsmodus (nur für Layergruppen verwendet).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Ausgabe" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Es gibt keine 23. Ebene.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "Die 23. Ebene ist keine Layer-Gruppe.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Der Name der 23. Ebene ist nicht 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Die AdjustmentGroup-Ebene sollte den Überblendungsmodus 'Pass Through' haben.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("AusgabeApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalAusgabeApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Aktualisierung des Textebenen-Textes führt zu einer Ausnahme**

{{< highlight java >}}

 // Aktualisierung des Textebenen-Textes führt zu einer Ausnahme

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_geändert.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Speichern des PSD-Bildes nach der RotateFlip-Operation erzeugt eine beschädigte Datei, die nicht geöffnet werden kann.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Sollte ohne Ausnahmen ausgeführt werden

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd))

{

    // Nichts tun

}

{{< /highlight >}}

**PSDNET-539. Ausnahme: Bildladefehler beim Laden eines Bildes mit leerem Unicode Alpha Names Resource**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Hier sollten keine Ausnahmen auftreten

{

    // nichts tun

}

{{< /highlight >}}

**PSDNET-541. Falsche Ausgabe nach Ändern der Sichtbarkeit einer Layer-Gruppe**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// Änderungen in den Ebenennamen vornehmen und speichern

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Alles innerhalb einer Gruppe ausschalten

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Ausnahme beim Laden des PSD-Bildes: Der Farbbereich (DropShadow Resource) muss 3 Farbkomponenten für RGB oder 4 Farbkomponenten für CMYK enthalten**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Hier sollten keine Ausnahmen auftreten

{

    // nichts tun

}

{{< /highlight >}}

**PSDNET-536. Ausnahme, wenn versucht wird, auf einer neu erstellten Ebene zu zeichnen, wenn die einfache Version des Konstruktors verwendet wird**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // Zeichnen eines Rechtecks mit dem Stiftwerkzeug

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // Zeichnen eines weiteren Rechtecks mit Solid Brush in Blauer Farbe

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
