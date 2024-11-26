---
title: 绘制图像
type: docs
weight: 10
url: /zh/java/drawing-images/
---

## **绘制线条**
此示例使用Graphics类在图像表面绘制线条形状。为了演示操作，示例创建了一个新的图像，并使用Graphics类公开的DrawLine方法在图像表面绘制线条。首先，我们将创建一个指定高度和宽度的PsdImage。

创建图像后，我们将使用Graphics类公开的Clear方法设置其背景颜色。Graphics类的DrawLine方法用于在连接两个点结构的图像上绘制一条线。该方法有多个重载，接受Pen类的实例和点或Point/PointF结构的坐标对作为参数。Pen类定义用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，可绘制具有指定颜色、宽度和画笔的线条。SolidBrush类用于以特定颜色连续绘制。最后，将图像导出为BMP文件格式。以下代码片段显示了如何在图像表面上绘制线条形状。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingLines-DrawingLines.java" >}}
## **绘制椭圆**
绘制椭圆示例是绘制形状系列的第二篇文章。我们将使用Graphics类在图像表面上绘制椭圆形状。为了演示操作，示例创建了一个新的图像，并使用Graphics类公开的DrawEllipse方法在图像表面上绘制椭圆形状。首先，我们将创建一个指定高度和宽度的PsdImage。

创建图像后，我们将创建和初始化Graphics类对象，并使用Graphics类的Clear方法设置图像的背景颜色。Graphics类的DrawEllipse方法用于在由边界矩形结构指定的图像表面上绘制椭圆形状。该方法有多个重载，接受Pen和Rectangle/RectangleF类的实例或一对坐标、高度和宽度作为参数。Pen类定义用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，可绘制具有指定颜色、宽度和画笔的线条。Rectangle类存储表示矩形的位置和大小的四个整数。Rectangle类有几个重载的构造函数，可绘制具有指定大小和位置的矩形结构。SolidBrush类用于以特定颜色连续绘制。最后，将图像导出为BMP文件格式。以下代码片段显示了如何在图像表面上绘制椭圆形状。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
## **绘制矩形**
在这个示例中，我们将在图像表面上绘制矩形形状。为了演示操作，示例创建了一个新的图像，并使用Graphics类公开的DrawRectangle方法在图像表面上绘制矩形形状。首先，我们将创建一个指定高度和宽度的PsdImage。然后，我们将使用Graphics类的Clear方法设置图像的背景颜色。

Graphics类的DrawRectangle方法用于在由矩形结构指定的图像表面上绘制矩形形状。该方法有多个重载，接受Pen和Rectangle/RectangleF类的实例或坐标对、宽度和高度作为参数。Rectangle类存储表示矩形的位置和大小的四个整数。Rectangle类有几个重载的构造函数，可绘制具有指定大小和位置的矩形结构。最后，将图像导出为BMP文件格式。以下代码片段显示了如何在图像表面上绘制矩形形状。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingRectangle-DrawingRectangle.java" >}}
## **绘制弧**
在这个绘制形状系列的会话中，我们将在图像表面上绘制弧形状。我们将使用Graphics的DrawArc方法在BMP图像上展示操作。首先，我们将创建一个指定高度和宽度的PsdImage。创建图像后，我们将使用Graphics类公开的Clear方法设置其背景颜色。

Graphics类的DrawArc方法用于在图像表面上绘制弧形状。DrawArc表示由矩形结构或坐标对指定的椭圆的一部分。该方法有多个重载，接受Pen类和Rectangle/RectangleF结构的实例或坐标对、宽度和高度作为参数。最后，将图像导出为BMP文件格式。以下代码片段显示了如何在图像表面上绘制弧形状。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
## **绘制Bezier曲线**
此示例使用Graphics类在图像表面上绘制Bezier曲线形状。为了演示操作，示例创建了一个新的图像，并使用Graphics类公开的DrawBezier方法在图像表面上绘制Bezier曲线形状。首先，我们将创建一个指定高度和宽度的PsdImage。创建图像后，我们将使用Graphics类公开的Clear方法设置其背景颜色。

Graphics类的DrawBezier方法用于在由四个Point结构定义的图像表面上绘制Bezier样条形状。该方法有多个重载，接受Pen类的实例和四个有序的坐标对、四个Point/PointF结构或Point/PointF结构数组作为参数。Pen类定义用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，可绘制具有指定颜色、宽度和画笔的线条。最后，将图像导出为BMP文件格式。以下代码片段显示了如何在图像表面上绘制Bezier曲线形状。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
## **使用核心功能绘制图像**
Aspose.PSD是一个库，提供许多有价值的功能，包括从头开始创建图像。使用核心功能进行绘图，例如操纵图像的位图信息，或者使用高级功能，如Graphics和GraphicsPath，在图像表面上绘制形状，借助不同的画刷和笔。使用Aspose.PSD的RasterImage类，您可以检索图像区域的像素信息并进行操作。RasterImage类包含整个核心绘图功能，例如获取和设置像素以及其他用于图像操作的方法。使用描述中创建文件的任一方法创建新图像，并将其分配给RasterImage类的实例。使用RasterImage类的LoadPixels方法检索图像部分的像素信息。一旦有像素数组，您可以通过例如更改每个像素的颜色来操纵它。在操纵像素信息后，使用RasterImage类的SavePixels方法将其设置回图像中的所需区域。以下代码片段显示了如何使用核心功能绘制图像。


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.java" >}}
