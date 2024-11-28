---
title: Aspose.PSD for .NET 22.11 - 发行说明
type: docs
weight: 20
url: /zh/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明。

{{% /alert %}}

{{% alert color="warning" %}}

- 该版本在处理16位导出时存在回归问题，因此我们建议在使用此版本中谨慎使用此功能。
如果16位图像处理是您的主要功能，请不要将 Aspose.PSD 升级到 22.9-22.11。

我们正在努力解决这些问题。

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-1320|无法导出极大的 PSB 文件|增强功能|
|PSDNET-659|使径向渐变的中心可移动|特性|
|PSDNET-1330|对于特定文件不支持 ZipWithoutPrediction 压缩方法|特性|
|PSDNET-735|仅对图层使用变换方法后，保存的图层边界框不正确|错误|
|PSDNET-1234|加载具有图案的 PSD 图像时出现异常|错误|
|PSDNET-1244|保存具有中文标志的 PSD 文件时图像导出失败 (IndexOutOfRangeException)|错误|
|PSDNET-1303|TimeLine ActiveFrame 应用不正确|错误|
|PSDNET-1307|回归 22.7: 文本渲染出现问题|错误|
|PSDNET-1321|组图层上的矢量蒙版工作不正确。最终图像有黑洞但不应有|错误|

## **公共 API 更改**
# **新增的 API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)

# **已移除的 API:**
- 无

## **用法示例:**

**PSDNET-659. 使径向渐变的中心可移动**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // 更新偏移点
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. 仅对图层使用变换方法后，保存的图层边界框不正确**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // 设置文本图层的新大小
    const int NewWidth = 250;
    const int NewHeight = 250;

    // 设置调整函数将如何调整图层的机制（默认值）
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // 使用新的调整方式调整文本图层
    // 不仅图层本身，文本图层的转换矩阵也会发生变化
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // 位置点不同的原因是默认字体不同
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // 一切正常
    }
    else
    {
        throw new Exception("位置点错误");
    }
}
{{< /highlight >}}

**PSDNET-1234. 加载具有图案的 PSD 图像时出现异常**

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

**PSDNET-1244. 保存具有中文标志的 PSD 文件时图像导出失败 (IndexOutOfRangeException)**

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

    // 这里不应该有异常。
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame 应用不正确**

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

**PSDNET-1307. 回归 22.7: 文本渲染出现问题**

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

**PSDNET-1320. 无法导出极大的 PSB 文件**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. 组图层上的矢量蒙版工作不正确。最终图像有黑洞但不应有**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. 对于特定文件不支持 ZipWithoutPrediction 压缩方法**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
