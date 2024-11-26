---
title: Aspose.PSD for Java 中的智能滤镜操作
weight: 100
type: docs
description: 展示如何在 PSD 文件中使用智能滤镜的示例
keywords: [智能滤镜, 添加噪音, 高斯模糊, 锐化, 滤镜, psd 滤镜, psd api, java, 代码示例]
url: zh/java/smart-filters/
---

## **概述**

在 Aspose.PSD for Java 中有三种应用智能滤镜的方法。

## **直接应用滤镜**

此代码示例演示了如何在 Aspose.PSD for Java 中直接应用智能滤镜。

首先，代码定义了源 PSD 文件，原始图像的输出文件和更新后图像的输出文件。

然后，代码使用 Image.load() 方法加载 PSD 图像，并将其转换为 PsdImage 对象。

使用 save() 方法保存原始图像，指定输出文件名。

实例化 SharpenSmartFilter 对象以表示所需的智能滤镜。

接下来，代码使用 psdImage.getLayers()[1] 从 PSD 图像中检索常规图层。

使用循环将 sharpenFilter 应用于常规图层三次。

最后，使用 save() 方法保存更新后的图像，提供输出文件名。

这段代码演示了在 Aspose.PSD for Java 中直接应用智能滤镜。通过使用适当的滤镜对象并将它们应用于所需的图层，可以在图像上实现所需的效果。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## **操作智能对象中的智能滤镜**

此代码片段概述了如何在 Aspose.PSD for Java 中操作智能对象中的智能滤镜。

首先，代码定义了源 PSD 文件，原始图像的输出文件和更新后图像的输出文件。

使用 Image.load() 方法加载 PSD 图像，然后将其转换为 PsdImage 对象。

使用 save() 方法保存原始图像，指定输出文件名。

然后，代码将 PSD 图像的第二个图层转换为 SmartObjectLayer 对象，表示智能对象图层。

随后，代码演示了编辑智能滤镜，展示了两种类型：GaussianBlurSmartFilter 和 AddNoiseSmartFilter。

对于 GaussianBlurSmartFilter，代码更新滤镜值，如半径、混合模式、不透明度和激活状态。

对于 AddNoiseSmartFilter，代码将噪音分布设置为 NoiseDistribution.Uniform。

接下来，代码向智能对象图层添加两个新的滤镜项：另一个 GaussianBlurSmartFilter 和一个 AddNoiseSmartFilter。

添加新滤镜后，使用 updateResourceValues() 方法应用更改。

最后，代码演示了直接将滤镜应用于图层及其蒙版，分别使用 apply() 和 applyToMask() 方法。

然后使用 save() 方法保存更新后的图像，提供输出文件名。

通过查看此代码示例，您可以了解如何在 Aspose.PSD for Java 中操作智能对象中的智能滤镜。该库提供了一系列智能滤镜，每种都具有自己一套可定制的属性和方法，可实现对图像的所需效果。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## **将智能滤镜应用于图层蒙版**

将智能滤镜应用于蒙版：一种有效的图像编辑技术

智能滤镜在图像编辑软件中很常见，用户可以使用它们对图像应用各种滤镜和效果。智能滤镜的一个有趣技术是将其应用于蒙版。本文探讨了将智能滤镜应用于蒙版，并讨论了在图像编辑领域中的实用性。

了解蒙版：在探讨将智能滤镜应用于蒙版之前，了解蒙版的概念至关重要。在图像编辑中，蒙版是一个灰度图像，指定图像特定区域的透明度。蒙版使得可以选择性地将滤镜、调整或效果应用于图像的特定部分，而不影响其他部分。

将智能滤镜应用于蒙版：当智能滤镜应用于蒙版时，它们仅影响蒙版指定的区域，提供对滤镜影响的精确控制。通过操纵蒙版，用户可以调节滤镜效果的强度和范围。

请参考前面的示例和方法：[API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
