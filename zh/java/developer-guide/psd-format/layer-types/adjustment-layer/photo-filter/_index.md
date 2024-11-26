---
title: 图片滤镜调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/photo-filter/
---

# 在Java中使用Photoshop图片滤镜调整图层

今天我们将看看如何使用 Aspose.PSD for Java 库将图片滤镜调整图层应用于现有的 Photoshop 文档。

**图片滤镜调整图层 API** 使用着色来改变图像的色彩平衡。处理后的图像看起来与使用真实相机滤镜后一样。请注意，库的图片滤镜调整图层 API 与 Photoshop 中的略有不同，因为尚未预定义滤镜。然而，其他方面都是相同的。这意味着您可以设置色彩的着色，并改变其强度（密度），还可以使用保留亮度选项。

## API 概述

图片滤镜调整图层 API 使用起来非常简单。有一个主要的 [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) 类，是该调整图层的入口点，只包含三个公共属性，即颜色、密度和通过这些属性进行调整的亮度保持。

## 调整色彩平衡

既然没有太多可谈的，我们立即来考虑**使用图片滤镜调整色彩平衡的示例**。我们将手动为鹿雕塑的图像添加一个增暖滤镜（a），以得到色调温暖的图像（c），更加愉悦地观看。

![图片滤镜调整图层示例](photo-filter-adjustment-layer-figure-1.png)

首先，请注意，与[其他调整图层](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers)的工厂方法不同，[添加方法](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-)没有默认方法（无需参数）。因此，要将图片滤镜调整图层添加到已加载的 Photoshop 文档中，需要提供一个颜色参数。因此，要重新创建增暖滤镜效果，只需将橙色作为参数传递给添加方法，然后使用相应的 setter 设置密度：

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

值得一提的是，密度属性的默认值为 100，保留亮度属性的默认值为 true（这就是为什么我们不明确启用此选项的原因）。

## 结论

本文介绍了 Aspose.PSD for Java 的图片滤镜调整图层 API 的用法。这个工具易于使用，允许向图像添加具有可变密度的着色。这是调整整个图像的色彩平衡的快速方式。
