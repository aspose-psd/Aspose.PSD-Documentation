---
title: 使用Python打开PSD、PSB和AI文件，并将其导出为PDF、PNG、TIFF、GIF、BMP、JPEG
weight: 100
type: docs
description: 示例PSD、PSB和AI文件导出到其他格式
keywords: [打开psd，打开ai，打开psb，导出到png，导出到pdf，导出到jpeg，导出到tiff，psd api，python，代码示例]
url: zh/python-net/open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **概述**
要将PSD、PSB和AI文件转换为不同格式，您可以使用Python中的Aspose.PSD库。该库提供了各种选项和设置，可自定义转换过程。

首先，您需要从Aspose.PSD库导入必要的类和模块。确保在运行代码之前已安装该库。

在此代码中，我们为不同格式定义了各种选项，例如PNG、PDF、TIFF、JPEG、BMP、JPEG2000、GIF、PSB和PSD。这些选项允许您根据需求自定义输出文件。

接下来，我们定义了一个格式字典，将文件扩展名映射到它们各自的保存选项。

要将PSD文件转换为其他格式，需要使用PsdImage.load()加载PSD文件，然后遍历格式字典。对于每种格式，指定输出文件名，并使用image.save()方法保存图像。

类似地，要将AI文件转换为其他格式，需要使用AiImage.load()加载AI文件，并遍历格式字典。指定输出文件名，并使用image.save()方法保存图像。

请确保为源PSD和AI文件提供正确的文件路径。

就是这样！您现在可以使用此代码使用Aspose.PSD为Python将PSD、PSB和AI文件转换为各种格式。

请检查完整示例。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
