---
title: 使用调整图层进行PSD增强
weight: 100
type: docs
description: 通过Aspose.PSD for C#使用调整图层的示例
keywords: [调整图层, 照片增强, 曲线调整, 级别增强, 反相, 照片滤镜, psd api, C#, csharp, 代码示例]
url: zh/net/adjustment-layer-enhancement/
---

## 概览

在本文中，我们将探讨在Aspose.PSD for C#中编辑调整图层。调整图层是图像编辑中的一个强大功能，允许您对图像进行非破坏性更改。Aspose.PSD提供了一套全面的调整图层类，您可以使用这些类修改图像的各个方面。

为了演示调整图层的编辑，我们将在页面底部使用一个示例代码片段，加载一个PSD图像并对其图层应用不同的调整。

在下面的代码片段中，我们首先使用`PsdImage.Load()`方法加载PSD图像。然后设置保存输出PNG文件的选项。`PngOptions`类允许我们指定输出图像的颜色类型。

接下来，我们遍历PSD图像中的每个图层，并使用`IsAssignable()`方法检查其类型。如果图层是特定类型的，则使用`Cast()`方法将其转换为该类型并应用所需的调整。例如，我们可以调整`BrightnessContrastLayer`的亮度和对比度，修改`LevelsLayer`的级别，向`CurvesLayer`添加曲线点，等等。

您可以添加其他代码以将其他调整应用于各自的图层。Aspose.PSD提供了各种调整图层类，例如 [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) 等。

最后，我们使用`PsdImage`类的`Save()`方法保存修改后的图像。

此代码提供了一个关于如何在Aspose.PSD for C#中编辑调整图层的基本概述。您可以根据需求自定义调整并探索API文档中提供的各种选项。

## 示例

以下是一个演示如何使用Aspose.PSD for C#调整图层的代码示例：

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

更详细的信息和示例，请访问[Aspose.PSD for C#文档](https://docs.aspose.com/psd/net/)。
