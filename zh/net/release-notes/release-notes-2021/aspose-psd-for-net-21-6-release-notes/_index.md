---
title: Aspose.PSD for .NET 21.6 - 发行说明
type: docs
weight: 70
url: /zh/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}}

本页面包含 [Aspose.PSD for .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/) 的发行说明

{{% /alert %}}

|**关键**|**摘要**|**类别**|
| :- | :- | :- |
|PSDNET-546|群组的裁剪蒙版在渲染时不正确|错误|
|PSDNET-547|图层组的常规或矢量蒙版在渲染时被忽略|错误|
|PSDNET-647|保存时禁用矢量图层蒙版的 PSD 图像启用了矢量蒙版|错误|
|PSDNET-786|创建文本图层时，文本长度超过 255 个字符会导致异常|错误|
|PSDNET-900|无法在 Linux 上渲染文本图层的文本|增强功能|

## **公共 API 更改**
# **新增的 API:**
- 无

# **已移除的 API:**
- 无

## **用法示例：**

**PSDNET-546. 群组的裁剪蒙版在渲染时不正确**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. 图层组的常规或矢量蒙版在渲染时被忽略**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. 保存时禁用矢量图层蒙版的 PSD 图像启用了矢量蒙版**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. 创建文本图层时，文本长度超过 255 个字符会导致异常**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
