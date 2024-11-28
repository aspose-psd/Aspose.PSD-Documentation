---
title: 黑白调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/levels/
---

## 在Java中使用Photoshop Levels调整图层

在这篇文章中，我们将学习如何在Java中以编程方式调整照片的色调范围和颜色平衡，而不使用Adobe® Photoshop®照片编辑器本身。相反，我们使用Aspose.PSD for Java库，该库可以独立操作Photoshop文档。

虽然Aspose.PSD for Java支持超过足够的[工具来编辑照片](/psd/zh/java/manipulating-images/)，我们将选择使用Levels调整图层API，因为这是最简单和最快速的方式之一。

## API 概述

Levels调整图层API的当前实现（截至撰写时的20.6版本）**支持所有Photoshop Levels的基本功能**，即为复合通道（RGB）以及每个主要颜色通道（红色、绿色和蓝色）调整输入和输出Levels。

Levels调整图层的API很简单。类[LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer)是Levels调整的入口点。它包含一些方法来访问颜色通道：getMasterChannel和getChannel(int)。这两个方法返回[LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel)，它具有相应的属性来操纵输入和输出Levels。不同之处在于getMasterChannel用于调整复合颜色通道（RGB），而getChannel通过其索引访问特定颜色通道（红色、绿色或蓝色）。

## 与颜色模式的兼容性

值得一提的是，Levels调整图层**与绝大多数Photoshop Levels支持的颜色模式兼容**。因此，可以调整灰度（灰色通道）、RGB（RGB、红色、绿色和蓝色通道）、CMYK（CMYK、青色、洋红、黄色和黑色通道）、双色调（单色通道）和LAB（亮度、a和b通道）颜色模式的图像的Levels。

## 调整色调范围

简单来说，色调校正适用于图像，以重新映射阴影和高光，以更好地分布中间色调。一般来说，**如果做得正确，它会使图像看起来更具对比度**。例如，让我们拍一张狗的照片（b）并调整其色调范围（a - 该屏幕截图是从Photoshop Levels窗口中捕获的，方便理解），使照片看起来更加具有对比度（c）。

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levels Layer Figure 1](levels-adjustment-figure-1.png)|

要 **调整图像的整体色调范围**，应设置主通道的输入Levels：

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

需要记住，阴影的输入Levels应在0到253的范围内，中调的输入范围为9.99到0.01，高光的输入范围为2到255。输出Levels的范围必须在0到255之间。

需要更多示例？可以在[Github](https://github.com/aspose-psd/Aspose.PSD-for-Java)和[知识库](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers)中找到。

## 结论

总之，Aspose.PSD for Java具有便捷简单的API，用于改变图像的色调范围和颜色平衡，兼容几乎所有的颜色模式。该库的Levels调整图层API看起来类似于Photoshop Levels，因此，即使您以前没有使用过该库，也很容易上手。
