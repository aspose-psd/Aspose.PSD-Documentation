---
title: Aspose.PSD for .NET 23.8 - 发行说明
type: docs
weight: 50
url: /zh/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}}

| **关键**     | **摘要**                                                                                                  | **类别** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | 添加新的变形类型（Flag）| 功能 |
| PSDNET-1621 | 添加新的变形类型：arc up, arc down, sphere | 功能 |
| PSDNET-1682 |实现新方法 PsdImage.AddPosterizeAdjustmentLayer 用于添加新的海报化图层 | 功能 |
| PSDNET-913  | 仅打开和保存时丢失的 PSD 信息 | 错误     |
| PSDNET-1352 | 图像加载失败 | 错误     |
| PSDNET-1553 | 图像加载失败：无法将类型 UnknownStructure 转换为类型 DescriptorStructure | 错误     |
| PSDNET-1631 | 在第三方库中更改的文件损坏 PSD 文件，但可以在 Photoshop 中打开 | 错误     |


## **公共 API 变更**
# **添加的 API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **已移除的 API:**
- 无


## **用法示例:**

**PSDNET-913. 仅打开和保存时丢失的 PSD 信息**

{{< highlight csharp >}}
string src = "原始文件.psd";
string outputPsd = "out_原始文件.psd";
string outputPng = "out_原始文件.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. 图像加载失败**

{{< highlight csharp >}}
string srcFile1 = "test_text.psd";
string srcFile2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. 图像加载失败：无法将类型 UnknownStructure 转换为类型 DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // 应该正确加载
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. 在第三方库中更改的文件损坏 PSD 文件，但可以在 Photoshop 中打开**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "export.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. 添加新的变形类型（Flag）**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. 添加新的变形类型：arc up, arc down, sphere**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ArcUpper_export.png";
string outputFileArcLower = "ArcLower_export.png";
string outputFileBulge = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. 实现新方法 PsdImage.AddPosterizeAdjustmentLayer 用于添加新的海报化图层**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// 检查保存的更改
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "对象不相等。");
    }
}
{{< /highlight >}}
