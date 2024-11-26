---
title: 通道混合器调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/channel-mixer/
---

# 在Java中使用Photoshop通道混合器调整图层

今天我们将看看如何在Java中以编程方式混合Photoshop文档中的通道颜色。由于Photoshop编辑器不支持Java脚本，我们将使用一个名为Aspose.PSD for Java的特殊PSD文件格式操作库。

这个库包含了**用于处理颜色通道的API**。有几种混合颜色的方法，但在本文中，我们将重点介绍通道混合器调整图层。

通道混合器调整图层API **允许操作颜色通道**，以制作锡合成图像或创建不同的创意色彩效果，甚至将图像转换为黑白图像。接下来，我们将讨论如何使用Aspose.PSD for Java将通道混合器调整应用于现有的Photoshop文档，但首先我们需要讨论整体API功能。

## API概述

创建通道混合器调整图层没有什么特别的。它可以通过[默认工厂方法](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--)来添加，该方法返回ChannelMixerLayer类的一个实例。该类包含了像单色选项和获取输出通道的方法的通用功能。特定输出通道可以是两种类型之一：[CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) 或 [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel)。[MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel)的类型取决于图像的[颜色模式](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--)。

## 使图像单色

现在，让我们考虑一个示例，将通道混合器调整图层应用于现有的Photoshop文档。由于这种类型的调整图层尚不支持预设，我们将**重新创建黑白红外线（RGB）Photoshop预设**（a）。该预设将应用于一颗盛开的树的图像（b）。我们希望实现红外摄影效果（c）。

![通道混合器调整图层示例](channel-mixer-adjustment-psd-layer-figure-1.png) 首先，要重新创建黑白红外线（RGB）Photoshop预设，需要启用单色标志，并设置每种颜色（红色、绿色和蓝色）的适当原始值用于灰色输出通道：

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

图像必须处于RGB颜色模式才能使代码工作（因为要转换为RgbMixerChannel类）。CMYK颜色模式也受支持，但仅适用于相应颜色模式的图像。

请记住，每种颜色的值以及Constant属性必须在 -200 到 200 的范围内。

## 结论

在本文中，我们讨论了如何使用Aspose.PSD for Java的通道混合器API来调整颜色通道和将图像转换为黑白图像。
