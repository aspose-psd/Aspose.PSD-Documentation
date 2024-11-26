---
title: 操作Adobe Photoshop格式
type: docs
weight: 20
url: /zh/net/manipulating-adobe-photoshop-formats/
---

## **将PSD图层合并到其他图层中**

## **将图像导出为PSD**
PSD，即PhotoShop文档，是Adobe Photoshop用于处理图像的默认文件格式。Aspose.PSD允许您加载、编辑和保存PSD文件，以便可以在Photoshop中打开和编辑这些文件。本文展示了如何使用Aspose.PSD将文件保存为PSD，并讨论了保存到此格式时可以使用的一些设置。[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)是[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions)命名空间中的专用类，用于将图像导出为PSD。要导出到PSD，创建Image类的实例，可以从现有图像文件（例如缩略图）加载，也可以从头开始创建。本文解释了如何操作。在下面的示例中，图像是从头开始创建的。创建并填充像素数据后，使用Image类的Save方法保存图像，并将PsdOptions对象作为第二个参数。可以为高级转换设置PsdOptions类的一些属性。其中一些属性是ColorMode，[CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod)和Version。Aspose.PSD通过CompressionMethod枚举支持以下压缩方法：

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

通过[ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes)枚举支持以下颜色模式：

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


可以添加其他资源，例如PSD v4.0、v5.0及更高版本的缩略图资源，或PSD v4.0及更高版本的网格和引导资源。以下代码通过从头创建一个Image文件，填充像素，并使用RLE压缩和灰度色彩模式将其保存为PSD。以下代码片段显示如何将图像导出为PSD。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}


## **将图像导入到PSD图层**
本文演示了使用Aspose.PSD将图像添加到或导入到PSD图层。Aspose.PSD API公开了高效且易于使用的方法来实现此目标。Aspose.PSD公开了Layer类的[DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage)方法，以将图像添加/导入到PSD文件中。DrawImage方法需要指定位置和图像值以将图像添加/导入到PSD文件中。将图像导入到PSD图层的步骤如下：

- 使用由Image类提供的工厂方法Load将PSD文件加载为图像。
- 从Png、Jpeg、Tiff、Gif、Bmp、Psd或j2k文件的流创建Layer类的实例
- 使用AddLayer方法将Layer添加到Psd
- 保存结果。


以下代码片段显示了如何将图像导入到PSD图层。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **在PSD图层中替换颜色**
本文演示了如何使用Aspose.PSD将图像添加到或导入到PSD图层。Aspose.PSD API公开了高效且易于使用的方法来实现此目标。Aspose.PSD公开了Layer类的DrawImage方法，以添加/导入图像到PSD文件。DrawImage方法需要指定位置和图像值以将图像添加/导入到PSD文件。将图像导入到PSD图层的步骤如下：

- 使用由Image类提供的工厂方法Load将PSD文件加载为图像。
- 创建Layer类的实例并将PSD图像图层分配给它。
- 加载需要添加的图像或从头开始创建一个图像。
- 调用Layer.DrawImage方法，同时指定位置和图像实例。
- 保存结果。


以下代码片段显示了如何将图像导入到PSD图层。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}

## **从PSD文件创建缩略图**
PSD是Adobe Photoshop应用程序的本机文档格式。Adobe Photoshop（版本5.0及更高版本）会将缩略图信息存储在一个图像资源块中，该块由一个28字节的初始标头组成，后面跟随着RGB（红色、绿色、蓝色）顺序的JFIF缩略图。Aspose.PSD API提供了一种简单易用的机制来访问PSD文件的资源。这些资源还包括可以获取和根据应用程序需要保存到磁盘的缩略图资源。以下代码片段显示了如何从PSD文件创建缩略图。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}

## **创建索引PSD文件**
Aspose.PSD for .NET API可以从头开始创建索引PSD文件。本文演示了使用PsdOptions和[PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage)类来创建带有一些形状的索引PSD。创建索引PSD文件需要执行以下简单步骤：

- 创建PsdOptions的实例并设置其源。
- 将PsdOptions的ColorMode属性设置为ColorModes.Indexed。
- 从RGB空间创建新的颜色调色板，并将其设置为PsdOptions的Palette属性。
- 将CompressionMethod属性设置为所需的压缩算法。
- 通过调用PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create)方法创建一个新的PSD图像。
- 根据需求绘制图形或执行其他操作。
- 调用PsdImage.Save方法以提交所有更改。


以下代码片段显示了如何创建索引PSD文件。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}

## **将PSD图层导出为光栅图像**
Aspose.PSD for .NET允许您将PSD文件中的图层导出为光栅图像。请使用[Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index)方法将图层导出到图像。以下示例代码加载一个PSD文件，并使用Aspose.PSD.FileFormats.Psd.Layers.Layer.Save将其每个图层导出为PNG图像。一旦所有图层都导出为PNG图像，您可以使用您喜欢的图像查看器打开它们。以下代码片段显示了如何将PSD图层导出为光栅图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}

## **更新PSD文件中的文本图层**
Aspose.PSD for .NET允许您操作PSD文件中文本图层中的文本。请使用[Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)类更新PSD图层中的文本。以下代码片段加载一个PSD文件，访问文本图层，更新文本，然后使用[Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index)方法将PSD文件另存为新名称。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **检测合并的PSD**
Aspose.PSD for .NET允许您检测给定的PSD文件是否已合并。Aspose.PSD.FileFormats.Psd.PsdImage类引入了IsFlatten属性以实现此功能。以下代码片段加载了一个PSD文件，并访问[IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten)属性。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}

## **合并PSD图层**
本文展示了如何在转换PSD文件为JPG时将图层合并到PSD文件中。在下面的示例中，通过将文件路径传递给Image类的静态Load方法加载现有的PSD文件。加载后，将图像转换/转换为PsdImage。创建一个JpegOptions类的实例，并设置其各种属性。现在调用PsdImage实例的Save方法。以下代码片段显示了如何合并PSD图层。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}

## **支持带Alpha的PSD灰度**
本文展示了如何在将PSD文件转换为PNG时，支持PSD文件中具有Alpha的灰度。在下面的示例中，通过将文件路径传递给Image类的静态Load方法加载现有的PSD文件。加载后，将图像转换/转换为PsdImage。创建一个PngOptions类的实例，并设置其各种属性。将[ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype)属性设置为TruecolorWithAlpha。现在调用PngOptions实例的Save方法。以下代码片段显示了如何转换为带Alpha的灰度PNG。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}

## **支持PSD图层效果**
本文展示了如何支持PSD图层中的不同效果，如**模糊**、**内部** **发光**、**外部发光**。以下代码片段显示了如何支持图层效果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}

## **支持图层创建日期和时间**
本文展示了如何支持PSD图层的创建日期以及时间。以下代码片段显示了如何创建图层。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.cs" >}}

## **支持表色高亮**
本文展示了如何加载PSD图像，然后更改和突出显示表颜色，将其保存为图像。已提供代码片段。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.cs" >}}

## **支持图层蒙版**
本文展示了如何支持PSD图像的图层蒙版，然后保存这些图像。以下代码片段已提供。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerMask-SupportOfLayerMask.cs" >}}

## **支持图层矢量蒙版**
本文展示了Aspose.PSD对图层矢量蒙版的支持。以下代码片段显示了Aspose.PSD如何支持图层矢量蒙版。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerVectorMask-SupportOfLayerVectorMask.cs" >}}

## **运行时支持文本图层**
本文展示了如何为PSD图像在运行时添加文本图层。以下代码片段已提供。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}

## **调整图层支持**
本文展示了如何调整图层，如果图层为空，则合并图层，并保存为PSD图像。以下代码片段已提供。

{{< gist "aspose-psd" "c68d1f8aa6f2af15b98e4d34e14a504a" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.cs" >}}

## **管理亮度和对比度**
本文展示了如何通过各图层循环遍历并管理亮度和对比度，然后将其保存为PSD图像。以下代码片段已提供。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageBrightnessContrastAdjustmentLayer-ManageBrightnessContrastAdjustmentLayer.cs" >}}

## **管理曝光图层**
本文展示了如何添加和编辑曝光图层，管理曝光图层，然后将其保存为PSD图像。以下代码片段已提供。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageExposureAdjustmentLayer-ManageExposureAdjustmentLayer.cs" >}}

## **管理通道混合器调整图层**
本文展示了如何管理调整图层并设置不同颜色，然