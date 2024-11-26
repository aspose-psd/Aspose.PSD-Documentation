---
title: 曝光调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/exposure/
---

# 在Java中使用Photoshop曝光调整图层

在本文中，我们将使用Aspose.PSD for Java - PSD文件格式操作库向Adobe® Photoshop®文档中添加曝光调整图层。该库可以正常工作，无需安装Photoshop编辑器，因为它使用自己的图像处理算法。我们还学习了与库曝光调整API相关的一些细节。

## API概述

曝光调整图层通过[ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)类进行配置，该类包含以下属性可用于处理曝光调整：

- 通过对整个直方图相对于黑色进行压缩或拉伸，定义照片的光线强度。因此，主要影响高光。
- 与曝光偏移不同，主要影响阴影。
- 伽玛校正，用于校正图像的亮度。

## 正确曝光

更正曝光及相关属性就像更改类的一些属性那样简单。让我们对一个图书馆的曝光不足照片应用一些曝光调整（a）以使其对人眼可察觉（c）。

![曝光调整图层示例](exposure-adjustment-layer-figure-1.png)

整个调整主要是使用伽玛校正完成的。但是，曝光和偏移也进行了一些调整。您需要做的就是为已经提到的属性设置适当的值：

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

请注意，曝光值必须在-20.0到20.0范围内，偏移值必须在-0.5到0.5范围内，伽玛校正值的范围必须在9.99到0.01之间。

有关更多详细信息，请参阅[曝光调整图层的API参考](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer)。

## 结论

在本文中，我们学习了如何将曝光调整图层添加到PSD文件中以提亮图像，并考虑了一些API细节。
