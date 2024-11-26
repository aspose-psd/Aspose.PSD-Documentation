---
title: Aspose.PSD for C# 中使用分组图层的示例
weight: 100
type: docs
description: 通过 C# 使用 PSD 文件的 Group Layer
keywords: [层组, 分组层, 将层添加到组, psd api, C#, csharp, 代码示例]
url: zh/net/psd-group-layer/
---

## 概述

在 Aspose.PSD for C# 中，分组图层允许有效地组织和操作 PSD 文件中的图层。通过使用文件夹图层，您可以将多个图层分组在一起，并对整个组应用变换或效果。

该示例演示了使用 `PsdImage.Create` 创建新的 PSD 图像。然后，使用 `PsdImage` 对象的 `AddLayerGroup` 创建一个新的 `LayerGroup` 对象。分组图层命名为 "Folder"，插入到索引 0，并设置为可见状态。

接下来，创建两个 `Layer` 对象，并设置它们的 `DisplayName` 属性。使用 `AddLayer` 将这些图层添加到组图层中。

可以通过 `LayerGroup` 对象的 `Layers` 属性访问组内的图层。示例断言组中的第一个和第二个图层显示名称分别为 "Layer 1" 和 "Layer 2"。

在修改组图层后，使用 `PsdImage` 对象的 `Save` 方法保存更新后的 PSD 图像。

这个基本示例介绍了如何使用 Aspose.PSD for C# 中的分组图层。该库提供了高级功能，用于操作和转换 PSD 文件中的图层。有关更详细的示例和功能，请参阅 Aspose.PSD for C# 文档。

以下是一个示例代码，演示了如何在 Aspose.PSD for C# 中使用分组图层：

## 示例

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

有关更详细的信息和示例，请访问[Aspose.PSD for C# 文档](https://docs.aspose.com/psd/net/)。
