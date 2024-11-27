---
title: Aspose.PSD für .NET 23.9 - Versionshinweise
type: docs
weight: 40
url: /de/net/aspose-psd-fuer-net-23-9-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Schlüssel** | **Zusammenfassung** | **Kategorie** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | Implementieren des Erstellens einer Maske für neue Anpassungsebenen | Feature |
| PSDNET-1654 | Hinzufügen der Unterstützung von Nicht abgeschnittenen Ebenen als Gruppenmischungsoption | Feature |
| PSDNET-1194 | PSD-Datei im 16-Bit-Farbbereich wendet keine Maske auf Anpassungsebenen an | Fehler |
| PSDNET-1235 | Falsche Darstellung von Klammern in der Textebene | Fehler |
| PSDNET-1559 | Kann Styles in den Textebenen nicht aktualisieren | Fehler |
| PSDNET-1583 | Nach dem Exportieren einer PSD-Datei mit CMYK brechen die Farben in der exportierten PSD-Datei | Fehler |
| PSDNET-1619 | Spezifische PSB-Datei wirft die Ausnahme "Das Rechteck hat keinen gemeinsamen Bearbeitungsbereich" | Fehler |
| PSDNET-1648 | Bildladefehler. OverflowException: Arithmetischer Vorgang führte zu einem Überlauf | Fehler |


## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Layer.BlendClippedElements
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.CustomFontHandler.CustomFontData.#ctor(System.String,System.Byte[])
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontName
- P:Aspose.PSD.CustomFontHandler.CustomFontData.FontData
- P:Aspose.PSD.FontSettings.GetSystemAlternativeFont
- P:Aspose.PSD.Graphics.PaintableImageOptions
- P:Aspose.PSD.Image.UsePalette
- M:Aspose.PSD.Region.Equals(System.Object)
- M:Aspose.PSD.Region.GetHashCode
- P:Aspose.PSD.StringFormat.CustomCharIdent
- M:Aspose.PSD.StringFormat.Equals(System.Object)
- M:Aspose.PSD.StringFormat.GetHashCode
- F:Aspose.PSD.StringFormatFlags.ExactAlignment

# **Entfernte APIs:**
- Keine

## **Beispiele für die Verwendung:**

**PSDNET-1638. Implementieren des Erstellens einer Maske für neue Anpassungsebenen**

{{< highlight csharp >}}
string srcFile = "zendeya_BW.psd";
string dstFile = "zendeya_BW_out.psd";

using (var im = (PsdImage)Image.Load(srcFile))
{
    im.AddBlackWhiteAdjustmentLayer();

    im.Save(dstFile);
}

using (var im = (PsdImage)Image.Load(dstFile))
{
    Layer layer = im.Layers[1];

    AssertAreEqual((ushort)5, layer.ChannelsCount);
    AssertAreEqual((short)-2, layer.ChannelInformation[4].ChannelID);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objekte sind nicht gleich.");
    }
}
{{< /highlight >}}

**PSDNET-1654. Hinzufügen der Unterstützung von Nicht abgeschnittenen Ebenen als Gruppenmischungsoption**

{{< highlight csharp >}}
string sourceFile = "beispiel_quelle.psd";
string outputPsd = "beispiel_ausgabe.psd";
string outputPng = "beispiel_ausgabe.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. PSD-Datei im 16-Bit-Farbbereich wendet keine Maske auf Anpassungsebenen an**

{{< highlight csharp >}}
string sourceFile = "quelle.psd";
string outputPng = "aktuell.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. Falsche Darstellung von Klammern in der Textebene**

{{< highlight csharp >}}
string file = "datei1.psd";
string output = "ausgabe_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. Kann Styles in den Textebenen nicht aktualisieren**

{{< highlight csharp >}}
string sourceFile = "Beispiel_Schriftgröße.psd";
string outputFile = "ausgabe_Beispiel_Schriftgröße.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var l1 = (TextLayer)psdImage.Layers[4];
    var l2 = (TextLayer)psdImage.Layers[5];

    var textItems1 = l1.TextData.ProducePortions(new string[] { "text1", "text2" }, l1.TextData.Items[0].Style, l1.TextData.Items[0].Paragraph);

    l1.TextData.RemovePortion(0);
    foreach (var item in textItems1)
    {
        l1.TextData.AddPortion(item);
    }

    var textItems2 = l2.TextData.ProducePortions(new string[] { "Textebene 1", "Textebene 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. Nach dem Exportieren einer PSD-Datei mit CMYK brechen die Farben in der exportierten PSD-Datei**

{{< highlight csharp >}}
string sourceFile = "canyon.psd";
string outputFilePng = "ausgabe_canyon.png";

using (var outputStream = new MemoryStream())
{
    using (var psdImage = (PsdImage)Image.Load(sourceFile))
    {
        psdImage.Save(outputStream);
    }

    outputStream.Position = 0;
    using (var psdImage = (PsdImage)Image.Load(outputStream))
    {
        psdImage.Save(outputFilePng, new PngOptions());
    }
}
{{< /highlight >}}


**PSDNET-1619. Spezifische PSB-Datei wirft die Ausnahme "Das Rechteck hat keinen gemeinsamen Bearbeitungsbereich"**

{{< highlight csharp >}}
var input = "1619_quelle.psb";
var output = "1619_ausgabe.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. Bildladefehler. OverflowException: Arithmetischer Vorgang führte zu einem Überlauf**

{{< highlight csharp >}}
string sourceFile = "9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

using (PsdImage im = (PsdImage)PsdImage.Load(sourceFile))
{
    Layer layer = im.Layers[28];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    AssertAreEqual("自定", grdmResource.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objekte sind nicht gleich.");
    }
}
{{< /highlight >}}
