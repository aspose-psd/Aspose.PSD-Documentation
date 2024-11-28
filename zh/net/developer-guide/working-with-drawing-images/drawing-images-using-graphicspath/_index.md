---
title: 使用GraphicsPath绘制图像
type: docs
weight: 30
url: /zh/net/drawing-images-using-graphicspath/
---

## **使用GraphicsPath绘制图像**
[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)类负责创建和维护图形路径。GraphicsPath不引用特定图像并且不改变图像本身，反而可以被看作一个包含描述Graphics类可绘制路径的元数据的对象。GraphicsPath类使用图形，每个图形都由一系列连接的线条和曲线或几何形状基元组成。每个形状都可以分割为形状段。您可以在GraphicsPath对象中添加、删除和更改不同的图形或形状。当GraphicsPath完全描述完成后，使用相应的Graphics类方法（DrawPath和Fill Paths）来绘制或填充路径。Graphics类获取每个形状段并将其绘制以生成最终图像。

### **使用GraphicsPath类进行绘制**
以下是一个演示如何使用[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)类的示例。为了简单易懂，示例源代码分为几个部分。逐步地，示例向您展示如何：

- 创建一个图像。
- 初始化一个Graphics对象。
- 清除表面。
- 创建[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)的实例。
- 创建一个图形。
- 向图形添加形状。
- 创建一个图形数组。
- 绘制路径。
- 填充路径。


### **使用GraphicsPath绘制图像的编程示例**
#### **GraphicsPath：创建图像**
首先，使用在创建文件中描述的任何方法创建一个图像。
#### **GraphicsPath：初始化Graphics对象**
通过将Image对象传递给其构造函数来创建和初始化Graphics对象。
#### **GraphicsPath：清除表面**
通过调用Graphics类的Clear方法并传递Color作为参数来清除Graphics表面。此方法使用传入的颜色填充Graphics表面。
#### **GraphicsPath：创建GraphicsPath的实例**
创建一个将GraphicsPath设置为默认交错的GraphicsPath实例。此模式确定如何填充闭合图形的内部。另一个可能的GraphicsPath值是Winding。
#### **GraphicsPath：创建一个图形**
创建Figure类的一个实例。正如前面讨论的，Figure可以包含Shapes，Shapes位于Aspose.PSD.Shapes命名空间中。
#### **GraphicsPath：向图形添加形状**
Figure类公开的Add Shapes方法允许您向图形添加形状。在下面的代码示例中，向一个Figure对象添加了多个形状。
#### **GraphicsPath：将图形添加到数组**
可以使用GraphicsPath类公开的AddFigures方法向GraphicsPath对象添加多个图形。该方法接受一个图形数组作为参数。
#### **GraphicsPath：绘制路径**
使用Graphics类公开的DrawPath方法绘制GraphicsPath。该方法接受两个参数。第一个参数是Pen类的对象，确定路径的颜色、宽度和样式。第二个参数是GraphicsPath类的对象，代表路径本身。
#### **GraphicsPath：填充路径**


您可以通过将GraphicsPath对象传递给Graphics类的Fill Paths方法来填充路径。Fill Paths方法根据当前设置为路径的填充模式（交错或交织）填充路径。如果路径中有任何开放的图形，则路径将被填充，就好像这些图形是闭合的一样。

Fill Paths方法接受两个参数。第一个参数是来自Aspose.PSD.Brushes命名空间的任何刷子类的对象。第二个参数是路径本身。为了此示例，请使用HatchBrush，它是一种具有阴影样式、前景颜色和背景颜色的矩形刷子。在将HatchBrush对象传递给Fill Paths方法之前，设置其属性。
### **GraphicsPath：完整的源代码**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



所有实现IDisposable接口的类都在Using语句中实例化，以确保它们被正确处理。

