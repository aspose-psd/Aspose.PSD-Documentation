---
title: 应用中值滤波器和维纳滤波器
type: docs
weight: 10
url: /zh/java/applying-median-and-wiener-filters/
---

## **应用中值滤波器和维纳滤波器**
中值滤波器是一种非线性数字滤波技术，通常用于去除噪声。这种噪声减少是用于改善后续处理结果的典型预处理步骤。维纳滤波器是针对受到附加噪声和模糊影响的图像而言的均方误差（MSE）最佳稳态线性滤波器。使用Aspose.PSD for Java API，开发人员可以对图像应用中值滤波器进行去噪，并可以对图像应用高斯维纳滤波器。本文演示了如何将中值滤波器和高斯维纳滤波器应用于图像。
### **应用中值滤波器**
Aspose.PSD提供了MedianFilterOptions类，用于在RasterImage上应用滤波器。下面提供的代码片段演示了如何将中值滤波器应用于光栅图像。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **应用高斯维纳滤波器**
Aspose.PSD提供了GaussWienerFilterOptions类，用于在RasterImage上应用滤波器。下面提供的代码片段演示了如何将高斯维纳滤波器应用于光栅图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **应用有色图像的高斯维纳滤波器**
Aspose.PSD还为彩色图像提供了GaussWienerFilterOptions。下面提供的代码片段演示了如何将高斯维纳滤波器应用于彩色图像。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **应用运动维纳滤波器**
Aspose.PSD提供了MotionWienerFilterOptions类，用于在RasterImage上应用滤波器。下面提供的代码片段演示了如何将运动维纳滤波器应用于光栅图像。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **对图像应用校正滤波器**
本文演示了使用Aspose.PSD for Java对图像执行校正滤波器的用法。Aspose.PSD API提供了高效且易于使用的方法来实现这一目标。Aspose.PSD for Java为滤波提供了BilateralSmoothingFilterOptions和SharpenFilterOptions类。BilateralSmoothingFilterOptions类需要一个整数作为大小。执行调整尺寸的步骤如下：


1. 使用Image类公开的Load工厂方法加载图像。
1. 将图像转换为RasterImage。
1. 创建BilateralSmoothingFilterOptions和SharpenFilterOptions类的实例。
1. 调用RasterImage.Filter方法，同时指定矩形作为图像边界和BilateralSmoothingFilterOptions类实例。
1. 调用RasterImage.Filter方法，同时指定矩形作为图像边界和SharpenFilterOptions类实例。
1. 调整对比度
1. 设置亮度
1. 保存结果。

以下代码片段显示了如何应用校正滤波器。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **使用Bradley阈值算法**
图像阈值化在图形应用程序中有所应用。图像阈值化的目标是将像素分类为“暗”或“亮”。Aspose.PSD API允许您在转换图像时使用Bradley阈值化。以下代码片段演示了如何定义阈值并调用Bradley的阈值算法。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
