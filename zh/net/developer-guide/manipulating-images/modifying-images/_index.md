---
title: 修改图像
type: docs
weight: 50
url: /zh/net/modifying-images/
---

## **位图图像的抖动**
抖动是一种通过改变实际创建图像的点的模式来创造新颜色和阴影 illusio的技术。它是减少图像的色彩范围到 256 种（或更少）色彩的最常见方式。Aspose.PSD 通过引入接受两个参数的 Dither 方法为 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类提供了抖动支持。第一个参数是要应用的 DitheringMethod 类型，有两种可能的选择：FloydSteinbergDithering 和 ThresholdDithering。[Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) 方法的第二个参数是整数类型的 BitCount 。 BitCount 定义了抖动结果的采样大小。默认值为 1，代表黑白色彩，而允许的值为 1, 4, 8，分别生成具有 2、4 和 256 种色彩的调色板。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}

## **调整亮度、对比度和伽玛**
数字图像中的颜色调整是大多数图像处理库提供的核心功能之一。颜色调整可以分为以下几种。

1. 亮度是指颜色的明亮程度或暗淡程度。增加图像的亮度会使所有颜色变亮，而减少亮度会使所有颜色变暗。
1. 对比度是指使图像中的对象或细节更加明显。增加图像的对比度会增加光线和暗区之间的差异，使得光亮区域变得更亮，暗区域变得更暗。降低对比度将使亮和暗区域保持大致相同，但整体图像变得更加均匀。
1. 伽玛优化了照明图像的对比度和亮度。

### **调整亮度**
Aspose.PSD for .NET API 为 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类提供了 [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) 方法，可通过传递整数值来调整图像亮度。参数值越高，图像越亮。以下是用于比较的原始图像和处理后的图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}

### **调整对比度**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类公开的 [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) 方法可通过传递浮点值来调整图像的对比度。

参数值越高，给定图像的对比度越高。以下是用于比较的原始图像和处理后图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}

### **调整伽玛**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类公开的 [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) 方法有两个版本。其中一个重载接受一个浮点值，并对红色、蓝色和绿色通道系数执行伽玛校正。而另一个重载接受三个浮点参数，分别表示每个颜色系数。以下代码示例演示了如何在图像上应用 AdjustGamma。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}

## **模糊图像**
本文演示了如何使用 Aspose.PSD for .NET 在图像上执行模糊效果。Aspose.PSD 的 API 提供了高效且易于使用的方法来实现此目标。Aspose.PSD for .NET 公开了 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 类，用于动态创建模糊效果。[GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 类需要半径（radius）和 sigma 值来在图像上创建模糊效果。执行重塑的步骤如下：

1. 使用 Image 类公开的工厂方法 Load 加载图像。
1. 将图像转换为 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)。
1. 使用默认构造函数创建 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 类的实例，或在构造函数中提供 radius 和 sigma 值。
1. 在指定矩形作为图像边界的情况下，调用 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter 方法，并提供 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 类的实例。
1. 保存结果。

以下代码示例演示了如何在图像上创建模糊效果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}

## **验证图像透明度**
本文演示了如何使用 Aspose.PSD for .NET 检查图像透明度。检查图像透明度的步骤如下：

1. 使用 Image 类公开的工厂方法 [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) 加载图像。
1. 检查图像的不透明度，如果不透明度为零，则图像是透明的。
以下代码示例演示了如何检查图像是否透明。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}

## **实现有损 GIF 压缩器**
使用 Aspose.PSD for .NET，开发人员可以设置像素差异。GIF 的压缩基于所见像素字符串的“字典”。普通编码器在字典中搜索与图像中像素完全匹配的最长像素字符串。有损编码器选择与图像中的像素“足够相似”的最长像素字符串。以下是所述功能的代码演示。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}

## **实现双三次重采样**
重采样意味着您正在更改图像的像素尺寸。当您降采样时，您正在消除像素，因此从图像中删除信息和细节。当您上采样时，您正在添加像素。Photoshop 使用插值来添加这些像素。本文演示了如何使用 Aspose.PSD for .NET 执行双三次重采样。

以下是所述功能的代码演示。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}

## **色彩平衡调整图层**
本文演示了如何使用 Aspose.PSD for .NET 在图像上执行**色彩平衡调整图层**。色彩平衡调整图层使您能够调整图像的着色。它呈现三个颜色通道及其互补颜色，您可以调整这些对来改变照片的外观。

以下是所述功能的代码演示。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}

## **反相调整图层**
本文演示了如何使用 Aspose.PSD for .NET 执行**反相调整图层**。调整图层是一种用于颜色校正的特殊图层。它们不是具有自己内容的图层，而是调整其下图层的信息。反相调整图层通过反转图像的颜色产生照片底片效果。

以下是所述功能的代码演示。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
