---
title: 将签名添加到图像
type: docs
weight: 70
url: /zh/net/adding-a-signature-to-an-image/
---

## **添加签名**

将签名添加到图像有时需要对图像进行数字签名，以避免伪造。另一个想法可能是使图像更像是在画廊展示。无论原因是什么，Aspose.PSD API提供了在图像上添加签名的功能，使用最简单的机制如下所述。请注意，此示例使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类来在原始图像表面上绘制另一幅带有签名的图像。为了演示该操作，我们将从磁盘加载PSD图像，并使用Graphics类的[DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage)方法在原始图像表面上绘制另一幅图像作为签名。我们将使用[PngOptions](https://reference.aspose.com/psd/net/aspose.psd/imageoptions/pngoptions)类将得到的图像以PNG格式保存。以下是一个示例代码，演示如何向图像添加签名。示例源代码已经分为几个部分，以便于理解。逐步，示例展示了如何：

- 加载主图像和次图像（签名图像）。
- 创建和初始化Graphics对象。
- 使用Graphics类的DrawImage方法绘制图像。
- 以PNG格式保存结果。
### **程序示例**
#### **加载图像**
首先，创建Image类的实例，从磁盘加载示例图像。
#### **创建和初始化图形对象**
加载图像后，创建并初始化Graphics类对象，同时使用主要图像的对象。
#### **在主图像上绘制次图像**
然后使用Graphics类的DrawImage方法，在主图像上添加次图像。DrawImage方法有多种重载，第一个参数接受Image对象，而其他参数对应图像绘制位置。为了演示，以下代码使用DrawImage的重载版本，第二个参数接受Point对象，并尝试将签名绘制在主图像的右下角。
#### **保存图像**
最后，使用PngOptions类将图像保存回本地磁盘为PNG文件。
#### **完整代码**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddSignatureToImage-AddSignatureToImage.cs" >}}
