---
title: PSD 图层
type: docs
weight: 70
url: /zh/net/psd-layer/
---

## **概述**
Adobe® Photoshop® PSD 图层是图形处理中最好的概念之一。图层包含有关像素的信息，可以有不同数量的通道。

在 Photoshop 文档中，图层资源是图层的一个最重要部分。您可以在我们的文档中找到受支持的[图层资源](/psd/zh/net/list-of-psd-layer-resources/)的完整列表。

您可以在以下截屏中找到用于操纵图层的用户界面：

![todo:image_alt_text](psd-layer_1.png)

但是，Aspose.PSD专注于通过[C#](/psd/zh/net/home/)和[Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home)对 PSD 图层进行编程操纵。

附加文档可以在本文中找到：[操纵图像](/psd/zh/net/manipulating-images-html/)。所有操作可以在 PSD 预览和图层中进行处理，您可以在 [Aspose.PSD 位图图像 API 参考](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)中找到更多信息。
## **可用的 PSD 图层 API**
- 图层效果
- 图层常见属性
- 图层元数据
## **通过 C# 编辑图层的示例**
### **添加新图层**
如果您想要在打开的[PSD 文件](/psd/zh/net/psd-file/)中添加一个空白图层，可以使用以下代码。

使用 API 向 PSD 文件添加新图层

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}
### **从 Jpeg、Png、Gif、Ai、Tiff、Bmp 文件添加新图层**
任何[支持的格式的文件](/psd/zh/net/supported-file-formats/)都可以作为一个新图层添加到您的图像中。但您无法直接加载它。

您可以使用下面的代码从流中添加新的 PSD 图层，该流是来自任何受支持格式的文件

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
### **合并所有图层或图层组**
如果您不希望向用户提供可编辑的 PSD 文件，这将非常有用。此外，您可以通过 API 识别文件是否已被合并。

PSD 文件的图层合并：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
