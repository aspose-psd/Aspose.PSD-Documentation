---
title: 使用Aspose.PSD为Python中的组图层示例
weight: 100
type: docs
description: 通过Python使用PSD文件的组图层
keywords: [图层组, 组图层, 添加图层到组, psd api, python, 代码示例]
url: zh/python-net/psd-group-layer/
---

## **概述**

在Aspose.PSD为Python中使用组图层是一个强大的功能，它允许您组织和操作PSD图像中的图层。组图层，也称为文件夹图层，提供了一种将多个图层组合在一起并对整个组应用变换或效果的方式。

在本示例中，我们首先使用PsdImage.create方法创建一个新的PSD图像。然后，我们使用PsdImage对象的add_layer_group方法创建一个新的LayerGroup对象。我们提供组图层的名称（"Folder"），应插入的索引（0）以及一个布尔标志，指示组图层是否可见（True）。

接下来，我们创建两个Layer对象，并使用display_name属性设置它们的显示名称。我们使用add_layer方法将这些图层添加到组图层中。

最后，我们可以通过LayerGroup对象的layers属性访问组内的图层。在示例中，我们断言组内第一个和第二个图层的显示名称分别为"Layer 1"和"Layer 2"。

在处理完组图层后，我们可以使用PsdImage对象的save方法保存修改后的PSD图像。

这只是一个基本示例，帮助您开始使用Aspose.PSD为Python处理组图层。该库提供了许多高级功能，用于操纵和转换PSD图像中的图层。您可以参考Aspose.PSD为Python文档，了解有关处理组图层和库其他功能的更多详细信息和示例。

要在Aspose.PSD为Python中使用组图层，您可以使用LayerGroup类。以下是一个代码片段示例，演示如何创建组图层，向其中添加图层并保存修改后的PSD图像。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-group-layer.py" >}}
