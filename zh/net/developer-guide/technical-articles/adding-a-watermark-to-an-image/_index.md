---
title: 向图像添加水印
type: docs
weight: 30
url: /zh/net/adding-a-watermark-to-an-image/
---

## **向图像添加水印**
本文介绍如何使用Aspose.PSD向图像添加水印。向图像添加水印是图像处理应用程序的常见需求。该示例使用Graphics类在图像表面绘制字符串。

### **添加水印**
为了演示该操作，我们将从磁盘加载一个BMP图像，并使用Graphics类的DrawString方法在图像表面上绘制一个字符串作为水印。我们将使用PngOptions类将图像保存为PNG格式。以下是演示如何向图像添加水印的代码示例。示例源代码已分为几个部分，以便于跟踪。逐步介绍示例展示了如何：

1. [加载](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) 一个图像。
1. 创建并初始化一个[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)对象。
1. 创建并初始化Font和[SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush)对象。
1. 使用Graphics类的[DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring)方法绘制字符串作为水印。
1. 将图像保存为PNG。

以下代码片段展示了如何向图像添加水印。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **添加对角线水印**
向图像添加对角线水印与以上讨论的添加水平水印类似，但有一些不同之处。为了演示该操作，我们将从磁盘加载一个JPG图像，使用Matrix类的对象添加变换，并使用Graphics类的DrawString方法在图像表面上绘制一个字符串作为水印。以下是演示如何向图像添加对角线水印的代码示例。示例源代码已分为几个部分，以便于跟踪。逐步介绍示例展示了如何：

1. 加载图像。
1. 创建并初始化Graphics对象。
1. 创建并初始化[Font](https://reference.aspose.com/psd/net/aspose.psd/font)和SolidBrush对象。
1. 使用[SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef)对象获取图像大小。
1. 创建Matrix类的实例并执行复合变换。
1. 将变换分配给Graphics对象。
1. 创建并初始化[StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat)对象。
1. 使用Graphics类的DrawString方法绘制字符串作为水印。
1. 保存结果图像。

以下代码片段展示了如何添加对角线水印。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
