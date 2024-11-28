---
title: Aspose.PSD for .NET 24.6 - 发行说明
type: 文档
weight: 70
url: /zh/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明。

{{% /alert %}}

| **关键字**   | **摘要**                                                                             | **类别**     |
|:------------|:-------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | 实现渐变映射图层的支持                                                                               | 功能       |
| PSDNET-1670 | 【AI 格式】添加对 AI 格式的 XPacket 元数据的支持                                                                               | 功能       |
| PSDNET-1831 | 实现 Inflate、Squeeze 和 Twist 类型的变形                                                                               | 功能       |
| PSDNET-1653 | 在带有艺术板图层的文件中，RGB 和 Lab 模式不能包含少于 3 个通道和多于 4 个通道                                                                               | Bug       |
| PSDNET-1775 | 处理区域顶部必须为正数。(参数'areaToProcess')在处理特定文件时                                                                               | Bug       |
| PSDNET-2052 | 保存后，扩展到画布图像被裁剪。数据丢失但预览内容正确                                                                               | Bug       |

## **公共 API 更改**
# **已添加的 API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **已移除的 API:**
- 无

## **用法示例:**

**PSDNET-1450. 实现渐变映射图层的支持**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "gradient_map_src.psd");
string outputFile = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(sourceFile))
{
    // 添加渐变映射调整图层。
    GradientMapLayer layer = im.AddGradientMapAdjustmentLayer();
    layer.GradientSettings.Reverse = true;

    im.Save(outputFile);
}

// 检查保存的更改
using (PsdImage im = (PsdImage)Image.Load(outputFile))
{
    GradientMapLayer gradientMapLayer = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientSettings = (GradientFillSettings)gradientMapLayer.GradientSettings;

    AssertAreEqual(0.0, gradientSettings.Angle);
    AssertAreEqual((short)4096, gradientSettings.Interpolation);
    AssertAreEqual(true, gradientSettings.Reverse);
    AssertAreEqual(false, gradientSettings.AlignWithLayer);
    AssertAreEqual(false, gradientSettings.Dither);
    AssertAreEqual(GradientType.Linear, gradientSettings.GradientType);
    AssertAreEqual(100, gradientSettings.Scale);
    AssertAreEqual(0.0, gradientSettings.HorizontalOffset);
    AssertAreEqual(0.0, gradientSettings.VerticalOffset);
    AssertAreEqual("Custom", gradientSettings.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objects are not equal.");
    }
}
{{< /highlight >}}

**PSDNET-1670. 【AI 格式】添加对 AI 格式的 XPacket 元数据的支持**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objects are not equal.");
    }
}

void AssertIsNotNull(object testObject)
{
    if (testObject == null)
    {
        throw new Exception("Test object are null.");
    }
}

string creatorToolKey = ":CreatorTool";
string nPagesKey = "xmpTPg:NPages";
string unitKey = "stDim:unit";
string heightKey = "stDim:h";
string widthKey = "stDim:w";

string expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string expectedNPages = "1";
string expectedUnit = "Pixels";
double expectedHeight = 768;
double expectedWidth = 1366;

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Xmp Metadata was added.
    var xmpMetaData = image.XmpData;

    AssertIsNotNull(xmpMetaData);

    // No we can get access to Xmp Packages of AI files.
    var basicPackage = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = xmpMetaData.Packages[4];

    // And we have access to the content of these packages.
    var creatorTool = basicPackage[creatorToolKey].ToString();
    var nPages = package[nPagesKey];
    var unit = package[unitKey];
    var height = double.Parse(package[heightKey].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(package[widthKey].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, expectedCreatorTool);
    AssertAreEqual(nPages, expectedNPages);
    AssertAreEqual(unit, expectedUnit);
    AssertAreEqual(height, expectedHeight);
    AssertAreEqual(width, expectedWidth);
}
{{< /highlight >}}
