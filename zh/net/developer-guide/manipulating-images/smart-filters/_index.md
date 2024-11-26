---
title: 在С#中使用Aspose.PSD进行智能滤镜操作
weight: 100
type: docs
description: 展示如何在PSD文件中使用智能滤镜的示例
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, C#, csharp, code sample]
url: zh/net/smart-filters/
---

## 概述

在С#中使用Aspose.PSD有三种应用智能滤镜的方式。

### 直接应用滤镜

该示例演示了如何在С#中直接应用智能滤镜。

首先，指定源PSD文件、原始图像的输出文件和更新后图像的输出文件。

接下来，使用`Image.Load`方法加载PSD图像并将其转换为`PsdImage`对象。

使用指定的输出文件名使用`Save`方法保存原始图像。

创建一个`SharpenSmartFilter`对象，代表要应用的智能滤镜。

使用`psdImage.Layers[1]`从PSD图像中检索常规图层。

在循环中将`sharpenFilter`应用于常规图层三次。

最后，使用指定的输出文件名使用`Save`方法保存更新后的图像。

此代码演示了如何在С#中直接应用智能滤镜。通过使用适当的滤镜对象并将其应用于所需图层，可以在图像上获得所需的效果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### 操作智能滤镜中的智能对象

该示例展示了如何操作智能对象中的智能滤镜。

首先，指定源PSD文件、原始图像的输出文件和更新后图像的输出文件。

使用`Image.Load`方法加载PSD图像并将其转换为`PsdImage`对象。

使用指定的输出文件名使用`Save`方法保存原始图像。

将PSD图像的第二个图层转换为`SmartObjectLayer`对象。

编辑智能滤镜。该示例演示了如何使用`GaussianBlurSmartFilter`和`AddNoiseSmartFilter`。

对于`GaussianBlurSmartFilter`，更新滤镜值，包括半径、混合模式、不透明度和启用状态。

对于`AddNoiseSmartFilter`，将噪音分布设置为`NoiseDistribution.UNIFORM`。

向智能对象图层添加新的滤镜项目：另一个`GaussianBlurSmartFilter`和`AddNoiseSmartFilter`。

使用`UpdateResourceValues`方法应用更改。

使用`Apply`和`ApplyToMask`方法将滤镜直接应用于图层和图层的蒙版。

使用指定的输出文件名使用`Save`方法保存更新后的图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### 将智能滤镜应用于图层蒙版

智能滤镜是一种强大的图像编辑工具，允许用户应用各种滤镜和效果。其中一个有趣的技术是将它们应用于蒙版，可以精确控制滤镜影响的区域。

蒙版是一种确定特定图像区域透明度的灰度图像，可以选择性地应用滤镜、调整或效果。

当将智能滤镜应用于蒙版时，滤镜仅应用于蒙版指定的区域。这种精确控制允许调整滤镜的强度和范围。

有关更详细的信息和示例，请参阅[Aspose.PSD for C#文档](https://docs.aspose.com/psd/net/)。
