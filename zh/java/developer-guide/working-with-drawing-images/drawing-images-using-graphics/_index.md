---
title: 使用Graphics绘制图像
type: docs
weight: 20
url: /zh/java/drawing-images-using-graphics/
---

## **使用Graphics绘制图像**

使用Aspose.PSD库，您可以绘制简单的形状，如直线、矩形和圆，还可以绘制复杂的形状，如多边形、曲线、弧形和贝塞尔曲线。Aspose.PSD库使用位于Aspose.PSD命名空间中的Graphics类创建这些形状。Graphics对象负责在图像上执行不同的绘图操作，从而改变图像的表面。Graphics类使用各种辅助对象来增强这些形状：

- 画笔(Pens)，用于绘制线条、轮廓形状或渲染其他几何表示。
- 画刷(Brushes)，定义填充区域的方式。
- 字体(Fonts)，定义文本字符的形状。

### **使用Graphics类绘图**
以下是演示使用Graphics类的代码示例。示例源代码已分成几个部分，以保持简单易懂。逐步，示例展示如何：

1. 创建一个图像。
1. 创建并初始化一个Graphics对象。
1. 清空表面。
1. 绘制一个椭圆。
1. 绘制一个填充的多边形并保存图像。

### **编程示例**
#### **创建一个图像**
首先，使用创建文件中描述的任何方法创建一个图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **创建并初始化一个Graphics对象**
然后，通过将Image对象传递给其构造函数来创建和初始化一个Graphics对象。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **清空表面**
通过调用Graphics类的Clear方法并传递一个颜色参数来清空Graphics表面。该方法使用传递的颜色填充Graphics表面。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **绘制一个椭圆**
您可能会注意到Graphics类公开了许多方法来绘制和填充形状。您会在Aspose.PSD for Java API参考中找到这些方法的完整列表。Graphics类公开了几个重载版本的DrawEllipse方法。所有这些方法的第一个参数都接受一个Pen对象。后续参数被传递以定义椭圆周围的边界矩形。为了本例，请使用将Rectangle对象作为第二个参数接受的版本，使用所需颜色的Pen对象绘制椭圆。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **绘制一个填充的多边形**
接下来，使用LinearGradientBrush和一个点数组绘制一个多边形。Graphics类公开了几个重载版本的FillPolygon方法。所有这些方法的第一个参数都接受一个Brush对象，定义填充的特性。第二个参数是一个点数组。请注意，数组中每两个连续的点指定多边形的一条边。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **使用Graphics绘制图像：完整源代码**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

所有实现IDisposable接口和访问非托管资源的类都在Using语句中实例化，以确保它们被正确处理。
