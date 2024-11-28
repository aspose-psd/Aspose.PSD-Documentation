---
title: 使用调整图层增强PSD
weight: 100
type: docs
description: 使用Aspose.PSD for Python通过调整图层的示例
keywords: [调整图层，照片增强，曲线调整，级别增强，反转，照片滤镜，psd api，python，代码示例]
url: zh/python-net/adjustment-layer-enhancement/
---

## **概览**

在本文中，我们将探讨在Aspose.PSD for Python中编辑调整图层。调整图层是图像编辑中的一个强大功能，允许您对图像进行非破坏性更改。Aspose.PSD提供了一套全面的调整图层类，您可以使用这些类修改图像的各个方面。

为了演示调整图层的编辑，我们将使用一个代码示例，在页面的末尾加载一个PSD图像并对其图层应用不同的调整。

在下面的代码示例中，我们首先使用PsdImage.load()方法加载PSD图像。然后设置保存输出PNG文件的选项。PngOptions类允许我们指定输出图像的颜色类型。

接下来，我们遍历PSD图像中的每个图层，并使用is_assignable()方法检查其类型。如果图层属于特定类型，我们使用cast()方法将其转换为该类型，并应用所需的调整。例如，我们调整BrightnessContrastLayer的亮度和对比度，修改LevelsLayer的级别，为CurvesLayer添加曲线点，等等。

您可以添加其他代码以对其各自的图层应用其他调整。Aspose.PSD提供了一系列调整图层类，例如[ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)，[HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer)，[ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer)，[BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer)，[PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer)，[ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer)，[InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer)，[PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer)，[ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer)，[SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer)等等。

最后，我们使用PsdImage类的save()方法保存修改后的图像。

本代码提供了如何在Aspose.PSD for Python中编辑调整图层的基本概述。您可以根据自己的需求定制调整，并探索API文档中提供的各种选项。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
