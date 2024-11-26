---
title: 亮度对比度调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/brightness-contrast/
---

# 使用Java处理Photoshop亮度/对比度调整图层

在本文中，我们将使用Aspose.PSD for Java®库为Adobe® Photoshop®文档应用亮度/对比度调整。此外，我们将逐步了解与这种调整图层相关的库功能。

但首先让我们简单了解一下理论知识。

亮度/对比度调整图层会改变图像的亮度和对比度。但等一下，这到底意味着什么？增加亮度会使颜色值变亮直至变为白色，而减少亮度则会使颜色值变暗直至变为黑色。增加对比度将增加浅色和深色之间的差异，减少对比度将减小这种差异；这意味着浅色变得更亮，而深色变得更暗。

## 色彩模式支持

该库允许在RGB、CMYK或Lab色彩模式中为图像添加亮度/对比度调整图层。

## 当前和旧版行为

当前库实现（v20.6 在撰写时）使用默认的Photoshop算法，保留从阴影到高光的完整色调范围，但尚不支持旧版行为。这意味着该库支持用最新版本的Photoshop（CS4及更高版本）制作的文档中的亮度/对比度调整图层。然而，如果需要，您可以在我们的论坛上[请求亮度/对比度调整图层的旧版实现](https://forum.aspose.com/c/psd)。

## 调整亮度和对比度

现在让我们描述高级API的亮度/对比度调整图层的工作原理（提前说一下，API很简单）。PsdImage类包含一个工厂方法（addBrightnessContrastAdjustmentLayer），用于实例化BrightnessContrastLayer类，该类是亮度和对比度调整的入口。BrightnessContrastLayer类仅包含用于访问亮度和对比度属性以及更改它们的值的一对getter和setter。

![|PSD中的亮度/对比度调整图层示例](brightness-contrast-psd-adjustment-layer-figure-1.png)

因此，让我们以一只狗的图像（b）为例，使用只有对应参数的工厂方法来调整其亮度1和对比度2（a），最终得到一个看起来更加生动的图像（c）：

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

注：

1. 亮度的值必须在-150到150的范围内。
2. 对比度的值必须在-50到100的范围内。

有关更多详细信息，请参阅[BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer)文档。

## 结论

在本文中，我们简要概述了亮度/对比度调整图层，并学会了如何使用工厂方法调整图像的亮度和对比度。

请查阅我们的系列关于[Aspose.PSD for Java调整图层API的文章](/psd/zh/java/layer-types/adjustment-layer/)，以了解更多信息。
