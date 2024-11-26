---
title: 使用调整图层增强PSD
weight: 100
type: docs
description: 通过Aspose.PSD for Java使用调整图层的示例
keywords: [调整图层, 照片增强, 曲线调整, 色阶增强, 反转, 照片滤镜, PSD API, Java, 代码示例]
url: zh/java/adjustment-layer-enhancement/
---

## **概览**

本文探讨了在Aspose.PSD for Java中编辑调整图层。调整图层是图像编辑中的一个强大功能，可以让您对图像进行非破坏性更改。Aspose.PSD提供了一套全面的调整图层类，您可以使用这些类来修改图像的各个方面。

为了演示对调整图层的编辑，我们将在页面末尾提供一个样本代码片段，该代码加载PSD图像并对其图层应用不同的调整。

在下面的代码片段中，我们首先使用PsdImage.load()方法加载PSD图像。然后，我们设置保存输出PNG文件的选项。PngOptions类允许我们指定输出图像的颜色类型。

接下来，我们遍历PSD图像中的每个图层，并使用isAssignable()方法检查其类型。如果图层属于特定类型，我们使用cast()方法将其转换为该类型并应用所需的调整。例如，我们可以调整BrightnessContrastLayer的亮度和对比度，修改LevelsLayer的级别，向CurvesLayer添加曲线点，等等。

您可以添加附加代码以应用其他调整到相应的图层。Aspose.PSD提供了许多调整图层类，比如[ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer)，等等。

最后，我们使用PsdImage类的save()方法保存修改后的图像。

这为您提供了如何在Aspose.PSD for Java中编辑调整图层的基本概述。您可以根据需求自定义调整，并在API文档中探索各种可用选项。

请查看下面的完整示例。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
