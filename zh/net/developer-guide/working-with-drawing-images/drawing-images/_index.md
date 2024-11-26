---
title: 绘制图像
type: docs
weight: 10
url: /zh/net/drawing-images/
---

## **绘制线条**
此示例使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类在图像表面上绘制线条形状。为了演示此操作，示例将创建一个新的图像，并使用Graphics类的DrawLine方法在图像表面上绘制线条。首先，我们将创建一个指定高度和宽度的PsdImage。

在图像创建后，我们将使用Graphics类的Clear方法设置其背景颜色。Graphics类的DrawLine方法用于在图像上绘制一条连接两个点结构的线条。该方法有几个重载版本，可接受Pen类的实例以及点或Point / PointF结构的坐标对作为参数。Pen类定义了用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，用于以指定的颜色、宽度和笔刷绘制线条。SolidBrush类用于连续绘制特定颜色。最后将图像导出为bmp文件格式。以下代码片段展示了如何在图像表面上绘制线条。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **绘制椭圆**
绘制椭圆示例是绘制形状系列中的第二篇文章。我们将使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类在图像表面上绘制椭圆形状。为了演示此操作，示例将创建一个新的图像，并使用Graphics类的DrawEllipse方法在图像表面上绘制椭圆形状。首先，我们将创建一个指定高度和宽度的PsdImage。

创建图像后，我们将创建和初始化Graphics类对象，并使用Graphics类的Clear方法设置图像背景颜色。Graphics类的DrawEllipse方法用于在由边界矩形结构指定的图像表面上绘制椭圆形状。该方法有几个重载版本，可接受Pen和Rectangle / RectangleF类的实例或一对坐标，高度和宽度作为参数。Pen类定义了用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，用于以指定的颜色、宽度和笔刷绘制线条。Rectangle类存储表示矩形的位置和大小的四个整数。Rectangle类有几个重载的构造函数，用于以指定的大小和位置绘制矩形结构。SolidBrush类用于连续绘制特定颜色。最后将图像导出为bmp文件格式。以下代码片段展示了如何在图像表面上绘制椭圆形状。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **绘制矩形**
在这个例子中，我们将在图像表面上绘制矩形形状。为了演示此操作，示例将创建一个新的图像，并使用Graphics类的DrawRectangle方法在图像表面上绘制矩形形状。首先，我们将创建一个指定高度和宽度的PsdImage。然后，我们将使用Graphics类的Clear方法设置图像的背景颜色。

Graphics类的DrawRectangle方法用于在由矩形结构指定的图像表面上绘制矩形形状。该方法有几个重载版本，可接受Pen和Rectangle / RectangleF类的实例或坐标对、宽度和高度作为参数。Rectangle类存储表示矩形的位置和大小的四个整数。Rectangle类有几个重载的构造函数，用于以指定的大小和位置绘制矩形结构。最后将图像导出为bmp文件格式。以下代码片段展示了如何在图像表面上绘制矩形形状。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **绘制弧线**
在这个绘制形状系列的会话中，我们将在图像表面上绘制弧线形状。我们将使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)的DrawArc方法演示在BMP图像上的操作。首先，我们将创建一个指定高度和宽度的PsdImage。创建图像后，我们将使用Graphics类的Clear方法设置其背景颜色。

Graphics类的DrawArc方法用于在图像表面上绘制弧线形状。DrawArc表示由矩形结构或坐标对指定的椭圆的一部分。该方法有几个重载版本，可接受Pen类和Rectangle / RectangleF结构的实例或一对坐标，宽度和高度作为参数。最后将图像导出为bmp文件格式。以下代码片段展示了如何在图像表面上绘制弧线形状。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **绘制贝塞尔曲线**
此示例使用[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)类在图像表面上绘制贝塞尔曲线形状。为了演示此操作，示例将创建一个新的图像，并使用Graphics类的DrawBezier方法在图像表面上绘制贝塞尔曲线形状。首先，我们将创建一个指定高度和宽度的PsdImage。创建图像后，我们将使用Graphics类的Clear方法设置其背景颜色。

Graphics类的DrawBezier方法用于在由四个点结构定义的图像表面上绘制贝塞尔曲线形状。该方法有几个重载版本，可接受Pen类的实例和四个有序坐标对或四个Point / PointF结构或一组Point / PointF结构作为参数。Pen类定义了用于绘制线条、曲线和图形的对象。Pen类有几个重载的构造函数，用于以指定的颜色、宽度和笔刷绘制线条。最后将图像导出为bmp文件格式。以下代码片段展示了如何在图像表面上绘制贝塞尔曲线形状。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **使用核心功能绘制图像**
Aspose.PSD是一个库，提供许多有价值的功能，包括从头开始创建图像。可以使用核心功能绘制，如操作图像的位图信息，或使用高级功能绘制[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)和[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath)形状在图像表面上，并借助不同的画笔和笔刷。使用Aspose.PSD的RasterImage类，可以检索图像区域的像素信息并对其进行操作。RasterImage类包含整个核心绘图功能，如获取和设置像素以及其他图像操作方法。使用任何在创建文件中描述的方法创建一个新图像，并将其分配给RasterImage类的实例。使用RasterImage类的LoadPixels方法检索图像的部分像素信息。一旦获得像素数组，可以通过更改每个像素的颜色等方式进行操作。在操作像素信息后，使用RasterImage类的SavePixels方法将其设置回图像中的所需区域。以下代码片段展示了如何使用核心功能绘制图像。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

