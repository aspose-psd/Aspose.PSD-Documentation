---
title: 使用 GraphicsPath 绘制图像
type: docs
weight: 30
url: /zh/java/drawing-images-using-graphicspath/
---

## **使用 GraphicsPath 绘制图像**
GraphicsPath 类负责创建和维护图形路径。GraphicsPath 不会引用图像，也不会改变图像本身，相反，它可以被视为一个包含描述 Graphics 类可以绘制的路径的元数据的对象。GraphicsPath 类使用图形；每个图形都由一系列连接的线条和曲线或几何形状原语组成。每个形状可以分为形状段。您可以向 GraphicsPath 对象添加、移除和更改不同的图形或形状。当 GraphicsPath 完全描述完毕后，使用相应的 Graphics 类方法（DrawPath 和 Fill Paths）来绘制或填充路径。Graphics 类将每个形状段绘制出来以生成最终图像。

### **使用 GraphicsPath 类进行绘图**
以下是演示使用 GraphicsPath 类的示例。示例源代码分为几部分，以使其简单易懂。逐步示例向您展示如何：

- 创建一个图像。
- 初始化一个 Graphics 对象。
- 清除表面。
- 创建 GraphicsPath 的实例。
- 创建一个图形。
- 向图形添加形状。
- 创建一个 Figures 数组。
- 绘制路径。
- 填充路径。


### **使用 GraphicsPath 绘制图像: 编程示例**
#### **GraphicsPath：创建一个图像**
首先使用在创建文件中描述的任何方法创建一个图像。
#### **GraphicsPath：初始化 Graphics 对象**
通过将 Image 对象传递给其构造函数来创建和初始化 Graphics 对象。
#### **GraphicsPath：清除表面**
通过调用 Graphics 类 Clear 方法并传递一个颜色作为参数来清除 Graphics 表面。这个方法使用参数传入的颜色填充 Graphics 表面。
#### **GraphicsPath：创建 GraphicsPath 的实例**
使用 GraphicsPath 创建一个 GraphicsPath 的实例，默认设置为 Alternate。此模式确定如何填充封闭图形的内部。GraphicsPath 的另一个可能值是 Winding。
#### **GraphicsPath：创建一个图形**
创建 Figure 类的实例。正如前面讨论的，Figure 可以包含 Shapes，而这些形状位于 Aspose.PSD.Shapes 命名空间中。
#### **GraphicsPath：向图形添加形状**
Figure 类公开的 Add Shapes 方法允许您向图形添加形状。在下面的代码示例中，向 Figure 对象添加了几个形状。
#### **GraphicsPath：将图形添加到数组中**
可以使用 GraphicsPath 类公开的 AddFigures 方法向 GraphicsPath 对象添加多个图形。此方法接受一个图形数组作为参数。
#### **GraphicsPath：绘制路径**
使用 Graphics 类公开的 DrawPath 方法绘制 GraphicsPath。该方法接受两个参数。第一个参数是 Pen 类的对象，确定路径的颜色、宽度和样式。第二个参数是表示路径本身的 GraphicsPath 类的对象。
#### **GraphicsPath：填充路径**

您可以通过将 GraphicsPath 对象传递给 Graphics 类公开的 Fill Paths 方法来填充路径。Fill Paths 方法根据当前设置为路径的填充模式（Alternate 或 Winding）来填充路径。如果路径有任何开放式图形，则会按照这些图形已关闭的方式填充路径。

Fill Paths 方法接受两个参数。第一个参数是 Aspose.PSD.Brushes 命名空间中任何刷类的对象。第二个参数是路径本身。为了本示例，使用 HatchBrush，这是带有阴影样式、前景色和背景色的矩形刷。在将 HatchBrush 对象传递给 Fill Paths 方法之前，设置其属性。
### **GraphicsPath：完整源代码**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}



所有实现 IDisposable 接口的类都会在 Using 语句中实例化，以确保它们被正确地处理。
