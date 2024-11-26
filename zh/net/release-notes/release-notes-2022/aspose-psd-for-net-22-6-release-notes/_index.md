---
title: Aspose.PSD for .NET 22.6 - 发布说明
type: docs
weight: 70
url: /zh/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/) 的发布说明

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-940|创建用于获取不同文件中类似图层的唯一哈希的 API|增强功能|
|PSDNET-678|在图层顺序更改时，使用模式的 FillLayer 渲染不正确的 Bug|错误|
|PSDNET-1125|在加载特定采用 CMYK 颜色模式的 PSD 文件时发生异常|错误|


## **公共 API 更改**
# **已添加的 API:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **已删除的 API:**
- 无


## **用法示例:**

**PSDNET-678. 在图层顺序更改时，使用模式的 FillLayer 渲染不正确**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. 创建用于获取不同文件中类似图层的唯一哈希的 API**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // 代码已省略
}
{{< /highlight >}}

**PSDNET-1125. 在加载特定采用 CMYK 颜色模式的 PSD 文件时发生异常**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}