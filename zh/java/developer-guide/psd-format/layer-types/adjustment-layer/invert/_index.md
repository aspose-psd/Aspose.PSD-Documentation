---
title: 反转调整图层
type: docs
weight: 30
url: /zh/java/layer-types/adjustment-layer/invert/
---

# 在 Java 中使用 Photoshop 反转调整图层

在本文中，我们将展示如何通过 Java 程序将 Photoshop 文档中的图像转换为负片。为此，我们将使用用于 PSD 文件格式操作的称为 Aspose.PSD for Java 的库。

颜色反转 API 允许**向图像添加负片效果**。您可能已经了解了如何使用曲线调整图层[反转图像颜色](/psd/zh/java/layer-types/adjustment-layer/curves/)。然而，今天我们将考虑一种更快速、更简便的方法来完成工作：使用反转调整图层。

## API 概述

**反转调整图层 API** 包括图层类本身，即[InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer)。由于该类继承自父类（[AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)）的所有公共成员，因此它本身没有公共成员，这简化了其用法，因为您只需将其添加到 PSD 文件中即可，图像即变为负片。

## 反转图像颜色

因此，即使这看似显而易见，我们也要演示一下，如何**向宇航员图像（a）应用反转调整图层**以为该图像产生负片效果（b）。

![反转调整图层示例之前和之后](invert-adjustment-layer-figure-1.png)

要**反转图像的颜色**，只需将反转调整图层添加到 PSD 中：

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

就是这样！对于这种类型的调整图层，无需配置任何特定属性。

## 结论

在本文中，我们了解了 Aspose.PSD for Java 的反转调整图层 API。这是一个轻松获取负片图像的工具，因为此调整图层的 API 不声明任何公共成员。
