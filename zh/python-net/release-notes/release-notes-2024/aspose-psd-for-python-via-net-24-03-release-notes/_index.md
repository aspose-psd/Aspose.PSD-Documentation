---
title: Aspose.PSD for Python via .NET 24.3 - 发布说明
type: docs
weight: 10
url: /zh/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

本页包含了[Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/)的发布说明。

{{% /alert %}}

| **关键**      | **摘要**                                            | **类别**    |
|:-------------|:------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI格式] 减少大型多页AI图像的加载时间          | 增强       |
| PSDPYTHON-45 | 由8位转换为16位的PSD文件变得无法阅读              |     错误   |
| PSDPYTHON-46 | 由8位转换为32位的PSD文件变得无法阅读              |     错误   |
| PSDPYTHON-47 | [AI格式] 修复AI文件中的Short Curve渲染         |     错误   |



## **公共API更改**
# **已添加的API：**
- 无

# **已删除的API：**
- 无


## **使用示例：**

**PSDPYTHON-42. [AI格式] 减少大型多页AI图像的加载时间**

{{< highlight python >}}
   # 无示例
{{< /highlight >}}

**PSDPYTHON-45. 由8位转换为16位的PSD文件变得无法阅读**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # 正确
                pass
            else:
                raise Exception("错误的全局资源，第一个资源应为Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. 由8位转换为32位的PSD文件变得无法阅读**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # 正确
                pass
            else:
                raise Exception("错误的全局资源，第一个资源应为Lr32Resource")
{{< /highlight >}}


**PSDPYTHON-47. [AI格式] 修复AI文件中的Short Curve渲染**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
