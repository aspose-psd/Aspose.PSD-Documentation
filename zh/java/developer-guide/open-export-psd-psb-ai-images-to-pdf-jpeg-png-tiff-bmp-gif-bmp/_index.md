---
title: 打开PSD、PSB和AI文件并将其导出为PDF、PNG、TIFF、GIF、BMP、JPEG
weight: 100
type: docs
description: 示例PSD、PSB和AI文件导出到其他格式
keywords: [打开psd, 打开ai, 打开psb, 导出为png, 导出为pdf, 导出为jpeg, 导出为tiff, psd api, java, 代码示例]
url: zh/java/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **概述**
要使用Java将PSD、PSB和AI文件转换为不同格式，您可以利用Aspose.PSD库。以下是涉及的步骤的概述：

- 从Aspose.PSD库中导入必要的类和模块。

- 为不同格式（如PNG、PDF、TIFF、JPEG、BMP、JPEG2000、GIF、PSB和PSD）定义各种选项。

- 创建一个将文件扩展名映射到其各自保存选项的字典。

- 使用PsdImage.load()加载PSD文件并通过格式字典迭代，以将图像保存为每种所需格式。

- 类似地，使用AiImage.load()加载AI文件并通过格式字典迭代，以将图像保存为每种所需格式。

请确保为源PSD和AI文件提供正确的文件路径。
这是使用Aspose.PSD为Java将PSD、PSB和AI文件转换为各种格式的一般过程。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.java" >}}
