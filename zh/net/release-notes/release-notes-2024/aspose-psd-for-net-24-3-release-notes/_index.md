---
title: Aspose.PSD for .NET 24.3 - 发行说明
type: docs
weight: 100
url: /zh/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

此页面包含 [Aspose.PSD for .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}}

| **关键**     | **摘要**                                                          | **类别** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI 格式] 减少大多页 AI 图像的加载时间         |     增强功能     |
| PSDNET-1905 | 从 8 位转换为 16 位后的 PSD 文件变得无法读取 |     Bug     |
| PSDNET-1906 | 从 8 位转换为 32 位后的 PSD 文件变得无法读取 |     Bug     |
| PSDNET-1921 | [AI 格式] 修复 AI 文件中短曲线的渲染                 |     Bug     |

## **公共 API 更改**
# **新增的 API:**
- 无

# **移除的 API:**
- 无

## **使用示例：**

**PSDNET-1905. 从 8 位转换为 16 位后的 PSD 文件变得无法读取**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Wrong global resource, the first resource should be Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. 从 8 位转换为 32 位后的 PSD 文件变得无法读取**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Wrong global resource, the first resource should be Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI 格式] 修复 AI 文件中短曲线的渲染**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
