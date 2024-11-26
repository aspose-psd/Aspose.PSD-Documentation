---
title: 将水印添加到图像
type: docs
weight: 20
url: /zh/java/adding-a-watermark-to-an-image/
---

## **将水印添加到图像**
本文介绍如何使用Aspose.PSD将水印添加到图像。在图像处理应用程序中，将水印添加到图像是一个常见需求。此示例使用Graphics类在图像表面绘制字符串。
### **添加水印**
为了演示操作，我们将从磁盘加载BMP图像，并使用Graphics类的DrawString方法在图像表面绘制字符串作为水印。我们将使用PngOptions类将图像保存为PNG格式。下面的代码示例演示了如何向图像添加水印。示例源代码已分成多部分，以便于跟踪。通过逐步示例，说明如何：

1. 加载图像。
2. 创建并初始化Graphics对象。
3. 创建并初始化Font和SolidBrush对象。
4. 使用Graphics类的DrawString方法绘制字符串作为水印。
5. 将图像保存为PNG。

下面的代码片段展示了如何在图像上添加水印。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **添加对角水印**
将对角水印添加到图像类似于在上文中讨论的添加水平水印，但有一些不同之处。为了演示操作，我们将从磁盘加载JPG图像，使用Matrix类的对象添加变换，并使用Graphics类的DrawString方法在图像表面绘制字符串作为水印。下面的代码示例演示了如何向图像添加对角水印。示例源代码已分成多部分，以便于跟踪。通过逐步示例，说明如何：

1. 加载图像。
2. 创建并初始化Graphics对象。
3. 创建并初始化Font和SolidBrush对象。
4. 在SizeF对象中获取图像的大小。
5. 创建Matrix类的实例并执行复合变换。
6. 将变换分配给Graphics对象。
7. 创建并初始化StringFormat对象。
8. 使用Graphics类的DrawString方法绘制字符串作为水印。
9. 保存结果图像。

下面的代码片段展示了如何在图像上添加对角水印。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
