---
title: 向图像添加签名
type: docs
weight: 10
url: /zh/java/adding-a-signature-to-an-image/
---

## **添加签名**

向图像添加签名有时是必要的，以便对图像进行数字签名，以避免伪造。另一个想法可能是将图像看待得更像是在画廊中展示。无论原因是什么，Aspose.PSD API 提供了在图像上添加签名的功能，使用最简单的机制。请注意，此示例利用 Graphics 类来绘制另一张带有签名的图像到原始图像表面上。为了演示操作，我们将从磁盘加载一个 PSD 图像，并使用 Graphics 类的 DrawImage 方法在原始图像表面上绘制另一张图像作为签名。我们将使用 PngOptions 类将生成的图像以 PNG 格式保存。以下是演示如何向图像添加签名的代码示例。示例源代码已分成多部分以便于跟踪。逐步，示例展示了如何：

- 加载主图像和次级（签名）图像。
- 创建并初始化 Graphics 对象。
- 使用 Graphics 类的 DrawImage 方法绘制图像。
- 以 PNG 格式保存结果。
### **程序样本**
#### **加载图像**
首先，创建 Image 类的实例以从磁盘加载示例图像。
#### **创建和初始化图形对象**
加载图像后，创建并初始化 Graphics 类对象，同时使用主图像的对象。
#### **将次级图像绘制到主图像上**
然后使用 Graphics 类的 DrawImage 方法，将次级图像添加到主图像上。DrawImage 方法有几个重载版本，第一个参数接受一个 Image 对象，而所有其他参数对应于图像要绘制的位置。为了演示，以下代码使用了接受 Point 对象作为第二个参数的 DrawImage 的重载版本，并尝试在主图像的右下角绘制签名。
#### **保存图像**
最后，使用 PngOptions 类将图像保存回本地磁盘为 PNG 文件。
#### **完整源代码**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-AddSignatureToImage-AddSignatureToImage.java" >}}

