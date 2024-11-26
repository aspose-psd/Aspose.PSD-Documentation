---
title: Aspose.PSD for .NET 24.1 - 发布说明
type: docs
weight: 120
url: /zh/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

此页面包含了 [Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明。

{{% /alert %}}

| **关键字**   | **摘要**                                                                                       | **类别**    |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI 格式] 增加了对多页 AI 图像的基本处理                                                     |   功能      |
| PSDNET-718  | 文本变形效果不适用于文本                                                                      |     缺陷     |
| PSDNET-1620 | 特定文件中蒙版的呈现不正确                                                                    |     缺陷     |
| PSDNET-1855 | 在 Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor 处引发 NullReferenceException | 缺陷     |
| PSDNET-1883 | [AI 格式] 修复了 AiExporterUtils 中的内存使用                                              |     缺陷     |



## **公共 API 更改**
# **新增的 API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **已移除的 API:**
- 无


## **使用示例:**

**PSDNET-718. 文本变形效果不适用于文本**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. 特定文件中蒙版的呈现不正确**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI 格式] 增加了对多页 AI 图像的基本处理**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// 加载 AI 图像。
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // 默认情况下，ActivePageIndex 为 0。
    // 因此，如果您保存 AI 图像而不更改此属性，则将呈现并保存第一页。
    image.Save(firstPageOutputPng, new PngOptions());

    // 将活动页索引更改为第二页。
    image.ActivePageIndex = 1;

    // 将 AI 图像的第二页保存为 PNG 图像。
    image.Save(secondPageOutputPng, new PngOptions());

    // 将活动页索引更改为第三页。
    image.ActivePageIndex = 2;

    // 将 AI 图像的第三页保存为 PNG 图像。
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. 在 Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor 处引发 NullReferenceException**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI 格式] 修复了 AiExporterUtils 中的内存使用**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// 加载 AI 图像。
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // 将 AI 图像的第一页保存为 PNG 图像。
    image.Save(firstPageOutputPng, new PngOptions());

    // 将活动页索引更改为第二页。
    image.ActivePageIndex = 1;

    // 将 AI 图像的第二页保存为 PNG 图像。
    image.Save(secondPageOutputPng, new PngOptions());

    // 将活动页索引更改为第三页。
    image.ActivePageIndex = 2;

    // 将 AI 图像的第三页保存为 PNG 图像。
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("内存使用过大。实际为 " + memoryUsed + "，期望为 " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
