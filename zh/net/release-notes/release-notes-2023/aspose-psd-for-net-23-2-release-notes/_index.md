---
title: Aspose.PSD的.NET 23.2版 - 发行说明
type: docs
weight: 110
url: /zh/net/aspose-psd-for-net-23-2-release-notes/
---

{{% alert color="primary" %}}

本页面包含了[Aspose.PSD的.NET 23.2版](https://www.nuget.org/packages/Aspose.PSD/)的发行说明

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-1359|重新设计文本呈现以改善文本定位、呈现和支持|增强功能|
|PSDNET-1270|添加通过公共API处理翘曲效果的能力|功能|
|PSDNET-1391|在段落设置中添加支持自底向上和自顶向下的行距模式|功能|
|PSDNET-912|更改TextLayer PSD的字体和颜色|错误|
|PSDNET-1022|在测试TextUpdateTests时文本导出不正确，文本丢失|错误|
|PSDNET-1221|在调整较大PSD图像大小后，额外小的文本丢失|错误|
|PSDNET-1301|Aspose.Psd for .NET的textLayer.UpdateText()以不同数据集的随机方式将“ -”（破折号）打印为下划线|错误|
|PSDNET-1379|从PSD导出到PDF时ResolutionSettings不适用|错误|

## **公共API更改**
# **已添加的API:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.AllowWarpRepaint
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.NoBreak
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.PosterizeLayer.Levels
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- T:Aspose.PSD.FileFormats.Psd.LeadingType
- F:Aspose.PSD.FileFormats.Psd.LeadingType.BottomToBottom
- F:Aspose.PSD.FileFormats.Psd.LeadingType.TopToTop

# **已移除的API:**
- T:Aspose.PSD.FileFormats.Psd.LeadingMode
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Auto
- F:Aspose.PSD.FileFormats.Psd.LeadingMode.Manual

## **使用示例:**

**PSDNET-912. 更改TextLayer PSD的字体和颜色**

{{< highlight csharp >}}
string fontsFolder = "Fonts";
string srcFile = "M1PDTT26052021001.psd";
string outputPsd = "result.psd";
string outputPng = "result.png";

FontSettings.SetFontsFolder(fontsFolder);

using (var image = (PsdImage)Image.Load(srcFile))
{
    TextLayer nameLayer = (TextLayer)image.Layers[9];
    var textPortion = nameLayer.TextData.Items[0];

    textPortion.Text = "MODESTO SR";
    textPortion.Style.FontName = FontSettings.GetAdobeFontName("Fugaz One");
    textPortion.Style.FillColor = Color.Red;

    nameLayer.TextData.UpdateLayerData();

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1022. 在测试TextUpdateTests中文本导出不正确，文本丢失**

{{< highlight csharp >}}
string srcFile = "ComplexKerningExample.psd";
string outputPsd = "TextUpdateComplexKerningExample_.psd";
string outputPng = "TextUpdateComplexKerningExample_.png";

using (var image = (PsdImage)Image.Load(srcFile))
{
    for (int i = 0; i < image.Layers.Length; i++)
    {
        var layer = image.Layers[i] as TextLayer;

        if (layer != null)
        {
            layer.UpdateText("Text is updated");
        }
    }

    image.Save(outputPsd);
    image.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1221. 在调整较大PSD图像大小后，额外小的文本丢失**

{{< highlight csharp >}}
string src = "textTest.psd";
string output = "output.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Resize(30, 30);

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1270. 添加通过公共API处理翘曲效果的能力**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string pngWarpedExport = "warped.png";
string psdWarpedExport = "warpFile.psd";

var warpLoadOptions = new PsdLoadOptions() { AllowWarpRepaint = true };

using (var image = (PsdImage)Image.Load(sourceFile, warpLoadOptions))
{
    image.Save(pngWarpedExport, new PngOptions());
    image.Save(psdWarpedExport, new PsdOptions());
}
{{< /highlight >}}

**PSDNET-1301. Aspose.Psd for .NET的textLayer.UpdateText()以不同数据集的随机方式将“ -”（破折号）打印为下划线**

{{< highlight csharp >}}
string src = "TEST_PSD_FILE.PSD";
string output = "OUTPUTIMAGE.jpg";

using (PsdImage psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers.Where(x => x.IsVisible))
    {
        if (layer is TextLayer)
        {
            TextLayer textLayer = layer as TextLayer;
            switch (layer.Name.Trim().ToUpper())
            {
                case "NAME":
                    textLayer.UpdateText("MR. JACK SMITH");
                    break;
                case "IDNO":
                    textLayer.UpdateText("OFF-022/GRP - 016");
                    break;
                case "DESIGNATION":
                    textLayer.UpdateText("OFFICER-001");
                    break;
                case "BLOODGROUP":
                    textLayer.UpdateText("AB-");
                    break;
                case "ADDRESS":
                    textLayer.UpdateText("BLOCK-A, STREET-7, APPT NO - 047, SECTOR-024");
                    break;
                case "PERMADDRESS":
                    textLayer.UpdateText("HOUSE NO - 42, LANE -025, PALM GREENS VIEW HOUSING SOCIETY, SECTOR - 45");
                    break;
            }
        }
    }

    psdImage.Save(output, new JpegOptions());
}
{{< /highlight >}}

**PSDNET-1379. ResolutionSettings在从PSD到PDF的导出中不起作用**

{{< highlight csharp >}}
string input = "Datensatz 1.psd";
string output = "Datensatz 1.pdf";

using (var image = Image.Load(input, new PsdLoadOptions()))
{
    ResolutionSetting resolutionSetting = new ResolutionSetting(300, 300);

    image.Save(output, new PdfOptions()
    {
        ResolutionSettings = resolutionSetting
    });
}
{{< /highlight >}}

**PSDNET-1391. 在段落设置中添加支持自底向上和自顶向下的行距模式**

{{< highlight csharp >}}
string input = "leadingMode.psd";
string output = "output_leadingMode.png";

using (var psdImage = (PsdImage)Image.Load(input, new PsdLoadOptions()))
{
    IText text1 = ((TextLayer)psdImage.Layers[1]).TextData;
    foreach (var textPortion in text1.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.TopToTop; // 更改LeadingType的值   
    }
    text1.Items[8].Text = "TopToTop";
    text1.Items[8].Style.FillColor = Color.ForestGreen;
    text1.UpdateLayerData();

    IText text2 = ((TextLayer)psdImage.Layers[2]).TextData;
    foreach (var textPortion in text2.Items)
    {
        textPortion.Paragraph.LeadingType = LeadingType.BottomToBottom; // 更改LeadingType的值   
    }
    text2.Items[8].Text = "BottomToBottom";
    text2.Items[8].Style.FillColor = Color.ForestGreen;
    text2.UpdateLayerData();

    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}
