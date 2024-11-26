---
title: 应用中值和Wiener滤波器
type: docs
weight: 10
url: /zh/net/applying-median-and-wiener-filters/
---

## **应用中值和Wiener滤波器**
中值滤波是一种非线性数字滤波技术，通常用于去除噪声。这种噪声减少是一种典型的预处理步骤，旨在改善后续处理的结果。Wiener滤波器是用于添加噪声和模糊的图像的均方误差（MSE）最优静态线性滤波器。使用Aspose.PSD for .NET API，开发人员可以将中值滤波器应用于去噪图像，并可以对图像应用高斯Wiener滤波器。本文演示了如何将中值滤波器和高斯Wiener滤波器应用于图像。
### **应用中值滤波器**
Aspose.PSD提供[MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions)类，用于在[光栅图像](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)上应用滤波器。下面提供的代码片段演示了如何将中值滤波器应用于光栅图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **应用高斯Wiener滤波器**
Aspose.PSD提供[GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)类，用于在[光栅图像](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)上应用滤波器。下面提供的代码片段演示了如何将高斯Wiener滤波器应用于光栅图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **应用彩色图像的高斯Wiener滤波器**
Aspose.PSD还为彩色图像提供了[GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)，下面提供的代码片段演示了如何将高斯Wiener滤波器应用于彩色图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **应用运动Wiener滤波器**
Aspose.PSD提供[MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)类，用于在[光栅图像](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)上应用滤波器。下面提供的代码片段演示了如何将运动Wiener滤波器应用于光栅图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **在图像上应用校正滤波器**
本文演示了使用Aspose.PSD for .NET对图像执行校正滤波器的用法。 Aspose.PSD API公开了高效且易于使用的方法，以实现此目标。 Aspose.PSD for .NET已公开了[BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)和[SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)类以用于过滤。 BilateralSmoothingFilterOptions类需要一个整数作为大小。 执行调整的步骤如下：

1. 使用Image类公开的工厂方法Load加载图像。
1. 将图像转换为RasterImage。
1. 创建BilateralSmoothingFilterOptions和SharpenFilterOptions类的实例。
1. 调用[RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter)方法，同时指定矩形作为图像边界和BilateralSmoothingFilterOptions类的实例。
1. 调用[RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter)方法，同时指定矩形作为图像边界和SharpenFilterOptions类的实例。
1. 调整对比度
1. 设置亮度
1. 保存结果。


## **使用Bradley阈值算法**
图像阈值在图形应用中使用。图像阈值的目标是将像素分类为“暗”或“亮”。 Aspose.PSD API允许您在转换图像时使用Bradley阈值。以下代码片段显示了如何定义阈值，并调用Bradley的阈值算法。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
