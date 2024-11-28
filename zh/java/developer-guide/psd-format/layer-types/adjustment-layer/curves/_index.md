---
title: 曲线调整图层
type: 文档
weight: 30
url: /zh/java/layer-types/adjustment-layer/curves/
---

# 在Java中使用Photoshop曲线调整图层

本文旨在展示Aspose.PSD for Java库在**处理Adobe® Photoshop®文档中的曲线调整图层**时的功能。该库完全自主，因此无需安装Photoshop照片编辑器。您可以在我们的知识库中找到[功能的完整列表](https://docs.aspose.com/psd/java/features/)。现在，让我们回到曲线。

## API概述

曲线工具可以表示为具有高光的对角线曲线（曲线）在图表上的右上角，以及具有阴影的曲线在右下角。

该库提供了用于处理曲线的API，即[CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer)类。但是，该类有**两种完全不同的方法**来处理曲线。因此，它一次可以在两种模式中的其中一种进行编辑：

- 连续（曲线表示为具有弯曲处的点的路径）
- 离散（曲线表示为虚线）

因此，该库通过连续](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager)和[离散管理器](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager)分别提供了修改曲线的两种方法。接下来，我们将解释如何在具体示例中使用它们。

## 使用连续管理器调整颜色和色调

[Curves Continuous Manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **配置连续曲线的弯曲点**用于复合通道（RGB）以及每个单独的颜色通道。为了演示目的，将对交响乐队的暗图像应用一些曲线调整(a)，以获得具有更多温暖色调的明亮图像(b)：

![曲线调整图层图1](curves-psd-adjustment-layer-figure-1.png)

由于有两种管理器，必须在获取之前显式选择一个（在此情况下为连续管理器）。之后，我们可以直接在指定坐标处为所需的颜色通道（复合RGB、红色和蓝色）添加曲线点以重新创建曲线形状：
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

坐标原点在左下角。点的最大坐标值限于数据类型（字节）且等于255（对于有符号类型为127）。

还有一些其他[方法](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager)可供使用。

## 使用离散管理器调整色调

曲线离散管理器还可以定位曲线点（实际上可以更改颜色和色调），但不同之处在于它们是以不同的方式进行的。首先，**曲线由点**或点（而不是实线）组成。第二，此管理器**不会将点放在图表上的任何位置**。相反，它**将点向上或向下移动**，其值范围分别为255到0之间。默认情况下，曲线点的值是递增的，以使曲线形成45度的角度。

因此，有了这些理解，很容易重新创建“负（RBG）”Photoshop预设(a)，并将其应用于山谷的灰度图像(b)，最终得到山谷的负表示(c)。

![曲线调整图层图2](curves-psd-adjustment-layer-figure-2.png) 首先，请不要忘记选择相应的管理器以便使用它，然后从255向下到0为每个曲线点设置曲线点值：

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

该管理器还提供了一些[其他方法](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager)来管理曲线。

## 结论

在本文中，我们学习了如何使用Aspose.PSD for Java在Photoshop文档中以两种完全不同的方式（连续和离散管理器）处理曲线调整图层。
