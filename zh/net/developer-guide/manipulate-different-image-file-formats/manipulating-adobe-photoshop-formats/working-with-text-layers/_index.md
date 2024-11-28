---
title: 处理文本图层
type: docs
weight: 170
url: /zh/net/working-with-text-layers/
---

## **添加文本图层**
Aspose.PSD for .NET 允许您在 PSD 文件中添加文本图层。在 PSD 文件中添加文本图层的步骤如下：

- 使用 Image 类公开的 [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) 工厂方法将 PSD 文件加载为图像
- 调用 [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) 方法，该方法接受文本和 [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle) 类的实例
- 保存结果

以下代码片段向您展示在 PSD 文件中添加文本图层的方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **设置文本图层位置**
Aspose.PSD for .NET 允许您设置 PSD 文件中文本图层的位置。在 PSD 文件中设置文本图层位置的步骤如下：

- 使用 Image 类公开的 Load 工厂方法加载 PSD 文件作为图像
- 在指定文本层的左侧和顶部位置时调用 AddTextLayer 方法
- 保存结果

以下代码片段向您展示在 PSD 文件中设置文本图层位置的方法

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}
## **从文本图层获取文本属性**
使用 Aspose.PSD for .NET，您可以获取并更新 PSD 文本图层中不同部分的文本属性。本文演示如何获取文本图层的段落、样式和文本属性并对其进行更新。

下面的代码片段显示了如何实现此要求。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


以下示例演示了开发人员如何使用 [Aspose.PSD for .NET](https://products.aspose.com/psd/net) 从 [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) 获取不同文本部分的文本格式。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}
## **更新 PSD 文件中的文本图层**
Aspose.PSD for .NET 允许您操作 PSD 文件中文本图层中的文本。请使用 Aspose.PSD.FileFormats.Psd.Layers.TextLayer 类更新 PSD 图层中的文本。以下代码片段加载一个 PSD 文件，访问文本图层，更新文本并使用 [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index) 方法将 PSD 文件另存为新名称。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **运行时支持文本图层**
本文展示了如何为 PSD 图像在运行时添加文本图层。下面提供了代码片段。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
