---
title: Aspose.PSD for Java 21.6 - 发行说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} 本页面包含 [Aspose.PSD for Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) 的发行说明 {{% /alert %}}

|**关键字**|**摘要**|**类别**|
| :- | :- | :- |
|PSDJAVA-351|组内的裁剪蒙版渲染不正确|错误|
|PSDJAVA-352|图层组的常规或矢量蒙版在渲染时被忽略|错误|
|PSDJAVA-353|在保存时禁用矢量图层蒙版的 PSD 图像启用矢量蒙版|错误|
|PSDJAVA-354|创建长度超过 255 个字符的 TextLayer 时出现异常|错误|

# **公共 API 更改**
# **已添加的 API:**
- 无

# **已移除的 API:**
- 无

# **使用示例:**

**PSDJAVA-351. 组内的裁剪蒙版渲染不正确**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. 图层组的常规或矢量蒙版在渲染时被忽略**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. 在保存时禁用矢量图层蒙版的 PSD 图像启用矢量蒙版**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. 创建长度超过 255 个字符的 TextLayer 时出现异常**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
