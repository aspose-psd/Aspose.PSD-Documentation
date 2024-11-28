---
title: Java 使用 Aspose.PSD 中的组图层示例
weight: 100
type: docs
description: 通过 Java 使用 PSD 文件的组图层
keywords: [图层组, 组图层, 将图层添加到组, psd api, java, 代码示例]
url: zh/java/psd-group-layer/
---

## **概述**

在 Aspose.PSD 中利用组图层可以有效地管理和组织 PSD 图像中的图层。组图层，也称为文件夹图层，使您能够整合多个图层并集体应用变换或效果。

首先，使用 PsdImage.create() 方法创建一个新的 PSD 图像。然后，通过 PsdImage 对象的 addLayerGroup 方法初始化一个新的 LayerGroup 对象。为组图层提供所需的名称（"Folder"），指定插入索引（0），并设置一个指示其可见性的布尔标志（True）。

随后，创建两个 Layer 对象，并使用 setDisplayName 方法设置它们的显示名称。使用 addLayer 方法将这些图层添加到组图层中。

要访问组内的图层，请利用 LayerGroup 对象的 layers 属性。确认组中第一个和第二个图层的显示名称分别为 "Layer 1" 和 "Layer 2"。

一旦您操作了组图层，使用 PsdImage 对象的 save 方法保存修改后的 PSD 图像。

这是一个基本示例，帮助您熟悉使用 Aspose.PSD 中的组图层。该库提供了大量用于在 PSD 图像中操作和转换图层的高级功能。有关关于利用组图层和库的其他功能的详细信息和示例，请参阅 Aspose.PSD for Java 文档。

要在 Aspose.PSD for Java 中使用组图层，请使用 LayerGroup 类。下面是一个代码片段，演示如何创建一个组图层，将图层添加到其中，并保存修改后的 PSD 图像。

请参考提供的完整示例。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-group-layer.java" >}}
