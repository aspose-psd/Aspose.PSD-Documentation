---
title: Aspose.PSD עבור .NET 23.9 - רשימות השחרור
type: docs
weight: 40
url: /he/net/aspose-psd-for-net-23-9-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את רשימות השחרור עבור [Aspose.PSD עבור .NET 23.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                                                                                | **קטגוריה** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1638 | ליישום יצירת מסכים עבור שכבות התאמה חדשות                                                                       | תכונה |
| PSDNET-1654 | הוספת תמיכה בשכבות מקופלות מבולטות כאופציית מיזוג קבוצה                                                               | תכונה |
| PSDNET-1194 | קובץ PSD במצב צבע 16 ביטים לא מחיל מסך לשכבות התאמה                                                    | באג     |
| PSDNET-1235 | הצגת סולמים שגויה בשכבת טקסט                                                                          | באג     |
| PSDNET-1559 | אי אפשרות לעדכן סגנונות בשכבות הטקסט                                                                        | באג     |
| PSDNET-1583 | לאחר ייצוא קובץ PSD עם CMYK מתרסקים הצבעים ב- PSD המיוצא                                                      | באג     |
| PSDNET-1619 | קובץ PSB ספציפי זורק חריגה "המלבן אינו מכיל אזור עיבוד משותף"                                           | באג     |
| PSDNET-1648 | כשל בטעינת התמונה. OverflowException: פעולת חשבון גרמה להתמרה                                                | באג     |


## **שינויים ציבוריים ב- API**
# **APIs מוספים:**
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


# **APIs הוסרו:**
- אף אחד


## **דוגמאות שימוש:**

**PSDNET-1638. ליישום יצירת מסכים עבור שכבות התאמה חדשות**

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
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1654. הוספת תמיכה בשכבות מקופלות מבולטות כאופציית מיזוג קבוצה**

{{< highlight csharp >}}
string sourceFile = "example_source.psd";
string outputPsd = "example_output.psd";
string outputPng = "example_output.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Layers[1].BlendClippedElements = false;
    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1194. קובץ PSD במצב צבע 16 ביטים לא מחיל מסך לשכבות התאמה**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string outputPng = "current.png";

using (var image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1235. הצגת סולמים שגויה בשכבת טקסט**

{{< highlight csharp >}}
string file = "file1.psd";
string output = "output_1235.png";

using (var psdImage = (PsdImage)Image.Load(file))
{
    foreach (var layer in psdImage.Layers)
    if (layer is TextLayer textLayer)
    textLayer.TextData.UpdateLayerData();

    var imageOptions = new PsdOptions(psdImage);
    psdImage.Save(output, imageOptions);
}
{{< /highlight >}}

**PSDNET-1559. אי אפשרות לעדכן סגנונות בשכבות הטקסט**

{{< highlight csharp >}}
string sourceFile = "Example_FontSize.psd";
string outputFile = "output_Example_FontSize.psd";

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

    var textItems2 = l2.TextData.ProducePortions(new string[] { "text layer 1", "text layer 22" }, l2.TextData.Items[0].Style, l2.TextData.Items[0].Paragraph);

    foreach (var item in textItems2)
    {
        l2.TextData.AddPortion(item);
    }

    l1.TextData.UpdateLayerData();
    l2.TextData.UpdateLayerData();

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1583. לאחר ייצוא קובץ PSD עם CMYK מתרסקים הצבעים ב- PSD המיוצא**

{{< highlight csharp >}}
string sourceFile = "canyon.psd";
string outputFilePng = "output_canyon.png";

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

**PSDNET-1619. קובץ PSB ספציפי זורק חריגה "המלבן אינו מכיל אזור עיבוד משותף"**

{{< highlight csharp >}}
var input = "1619_src.psb";
var output = "1619_output.png";
using (PsdImage img = (PsdImage)Image.Load(input, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(output,
    new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1648. כשל בטעינת התמונה. OverflowException: פעולת חשבון גרמה להתמרה**

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
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}
