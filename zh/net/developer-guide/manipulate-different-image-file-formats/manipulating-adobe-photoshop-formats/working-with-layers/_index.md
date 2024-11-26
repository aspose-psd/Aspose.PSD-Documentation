---
title: Working with Layers
type: docs
weight: 150
url: /zh/net/working-with-layers/
---

## **创建图层组**
图层组由一个或多个图层组成，有助于组织相似或相关的图层。使用 Aspose.PSD for .NET，您可以创建一个图层组。为此，在 **[PsdImage ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** 类中添加了一个新方法 **[AddLayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** 来添加图层组。

创建图层组的步骤如下：

- 使用指定的宽度、高度和图像选项创建一个图像实例。
- 使用指定的组名和索引创建一个 **[LayerGroup](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup)**。
- 创建一个 Layer 类的实例并将 PSD 图像分配给它。
- 使用 LayerGroup 类公开的 AddLayer 方法将创建的图层添加到图层组中。
- 保存结果。

以下代码片段演示了如何创建图层组。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **重命名图层**
您可以使用任何您喜欢的名称，但是通常的做法是使用该图层上对象或元素的一般描述。本文演示了如何使用 Aspose.PSD for .NET 更改图层的名称。为此，在 Layer 类中添加了一个新属性 **[DisplayName](https://reference.aspose.com/net/aspose.psd.fileformats.psd/layers/layer/properties/displayname)** 以正确显示图层名称。已经观察到，当 Photoshop 使用 **[Name](https://reference.aspose.com/net/aspose.psd.fileformats.psd/layers/layer/properties/name)** 属性保存图层名称时，韩文字符会以 ASCII 中的字节 63'?' 存储。因此，如果您想正确显示图层名称，请使用 **DisplayName** 属性，因为 **Name** 属性不支持韩文字符。

以下代码示例显示了如何重命名一个图层。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}


## **支持链接图层**
链接图层类似于对图层进行分组。如果您将两个或多个图层链接在一起，那么您可以对这些链接的图层进行某些更改。例如，如果您对一个图层应用变换，则所有其他链接的图层也会应用这些变换。本文演示了如何使用 [Aspose.PSD](https://products.aspose.com/psd) 获取和取消链接的图层。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
