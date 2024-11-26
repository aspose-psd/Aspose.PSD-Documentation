---
title: 使用Graphics绘制图像
type: docs
weight: 20
url: /zh/net/drawing-images-using-graphics/
---

## **使用Graphics绘制图像**
使用Aspose.PSD库，您可以绘制简单的形状，如直线、矩形和圆，以及复杂的形状，如多边形、曲线、弧形和贝塞尔形状。Aspose.PSD库使用位于Aspose.PSD命名空间中的[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类创建这些形状。Graphics对象负责在图像上执行不同的绘图操作，从而改变图像的表面。[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类使用各种辅助对象来增强形状：

·         画笔，用于绘制线条、轮廓形状或呈现其他几何表示。

·         笔刷，定义填充区域的方式。

·         字体，定义文本的字符形状。
### **使用Graphics类绘图**
以下是演示使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类的代码示例。示例源代码已分成几个部分，以保持简单易懂。逐步介绍了如何：

1. 创建图像。
1. 创建并初始化Graphics对象。
1. 清除表面。
1. 绘制椭圆。
1. 绘制填充多边形并保存图像。
### **编程示例**
#### **创建图像**
首先使用Creating Files中描述的任何方法创建图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **创建并初始化Graphics对象**
然后通过将Image对象传递给其构造函数来创建和初始化Graphics对象。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **清除表面**
通过调用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类的Clear方法并将颜色作为参数传递来清除Graphics表面。该方法将Graphics表面用传递的颜色填充。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **绘制椭圆**
您可能注意到[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类公开了许多绘制和填充形状的方法。您可以在Aspose.PSD for .NET API参考中找到这些方法的完整列表。Graphics类公开了几个重载版本的DrawEllipse方法。所有这些方法都接受Pen对象作为第一个参数。将后续参数传递以定义围绕椭圆的矩形。为了本示例，使用接受Rectangle对象作为第二参数的版本，使用所需颜色的Pen对象绘制椭圆。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **绘制填充多边形**
接下来，使用LinearGradientBrush和一系列点绘制多边形。Graphics类公开了多个重载版本的FillPolygon()方法。所有这些方法都接受Brush对象作为第一个参数，定义填充的特性。第二个参数是一系列点。请注意，数组中每两个连续的点指定多边形的一条边。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **使用Graphics绘制图像：完整源码**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

所有实现IDisposable并访问非托管资源的类都通过Using语句进行实例化，以确保其正确释放。
