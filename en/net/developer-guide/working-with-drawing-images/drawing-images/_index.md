---
title: Drawing Images
type: docs
weight: 10
url: /net/drawing-images/
---

## **Drawing Lines**
This example uses [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class to draw the line shapes on the Image surface. To demonstrate the operation, the example creates a new Image and draws lines on the Image surface using [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) method exposed by Graphics class. First, we will create a PsdImage specifying its height and width.

Once the image has been created, we will use the Clear method exposed by the Graphics class to set its background color. The[DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class is used to draw a line on an image connecting two point structures. This method has several overloads accepting the instance of Pen class and coordinates pairs of points or Point/PointF structures as arguments. The Pen Class defines an object used to draw lines, curves and figures. The Pen class has several overloaded constructors to draw lines with specified color, width & brush. The SolidBrush class is used for drawing continuously with specific color. Finally image is exported to bmp file format. The following code snippet shows you how to draw the line shapes on the Image surface.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **Drawing Ellipse**
Drawing ellipse example is the second article in the drawing shapes series. We will use [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class to draw the ellipse shape on the Image surface. To demonstrate the operation, the example creates a new Image and draws ellipse shape on the Image surface using DrawEllipse method exposed by [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class. First, we will create a PsdImage specifying its height and width.

After creating image, we will create and initialize Graphics class object and set image background color using the Clear method of the Graphics class. The DrawEllipse method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class is used to draw ellipse shape on an image surface specified by the bounding rectangle structure. This method has several overloads accepting the instances of the Pen and Rectangle/RectangleF classes or a pair of coordinates, a height, and a width as arguments. The Pen class defines an object used to draw lines, curves and figures. The Pen class has several overloaded constructors to draw lines with specified color, width & brush. The Rectangle class stores a set of four integers that represent the location and size of a rectangle. The Rectangle class has several overloaded constructors to draw the rectangle structure with specified size and location. The SolidBrush class is used for drawing continuously with specific color. Finally image is exported to bmp file format. The following code snippet shows you how to draw ellipse shape on the Image surface.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **Drawing Rectangle**
In this example we will draw the rectangle shape on the Image surface. To demonstrate the operation, the example creates a new Image and draw rectangle shape on the Image surface using DrawRectangle method exposed by [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class. First, we will create a PsdImage specifying its height and width. Then, we will set the background color of the Image by using the Clear method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class.

The DrawRectangle method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class is used to draw rectangle shape on an image surface specified by the rectangle structure. This method has several overloads accepting the instances of the Pen and Rectangle/RectangleF classes or coordinate pair, a width, and a height as arguments. The Rectangle class stores a set of four integers that represent the location and size of a rectangle. The Rectangle class has several overloaded constructors to draw the rectangle structure with specified size and location. Finally image is exported to bmp file format. The following code snippet shows you how to rectangle shape on the Image surface.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **Drawing Arc**
In this session of drawing shape series, we will draw the Arc shape on the Image surface. We will use DrawArc method of [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) to demonstrate the operation on a BMP image. First, we will create a PsdImage specifying its height and width. Once the image has been created, we will use the Clear method exposed by the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class to set its background color.

The DrawArc method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class is used to draw the Arc shape on an image surface. DrawArc represent a portion of an ellipse specified by the rectangle structure or pair of the coordinates. This method has several overloads accepting the instances of the Pen classes and Rectangle /RectangleF structure or a pair of the coordinates, a width, and a height as arguments. Finally image is exported to bmp file format. The following code snippet shows you how to draw Arc shape on the Image surface.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **Drawing Bezier**
This example uses [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class to draw the Bezier shape on the Image surface. To demonstrate the operation, the example creates a new Image and draw Bezier shape on the Image surface using DrawBezier method exposed by [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class. First, we will create a PsdImage specifying its height and width. Once the image has been created, we will use the Clear method exposed by the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class to set its background color.

The DrawBezier method of the [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) class is used to draw Bezier spline shape on an image surface defined by four Point structures. This method has several overloads accepting the instances of the Pen class and four ordered pair of coordinates or four Point/PointF structures or array of Point/PointF structures. The Pen class defines an object used to draw lines, curves and figures. The Pen class has several overloaded contractors to draw lines with specified color, width & brush. Finally image is exported to bmp file format. The following code snippet shows you how to draw the bezier shape on the Image surface.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}
## **Drawing Images using Core Functionality**
Aspose.PSD is a library that offers many valuable features including creating images from scratch. Draw using the core functionality like manipulating an image's bitmap information, or use the advanced features like [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) and [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) to draw shapes on image surface with the help of different brushes and pens. Using Aspose.PSD's RasterImage class, you can retrieve an image area's pixel information manipulate it. The RasterImage class contains the entire core drawing functionality, like getting and setting pixels and other methods for image manipulation. Create a new image using any of the methods described in Creating Files and assign it to an instance of the RasterImage class. Use the RasterImage class LoadPixels method to retrieve the pixel information of a portion of an image. Once you have an array of pixels, you can manipulate it by, for example, changing the color of each pixel. After manipulating the pixel information, set it back to the desired area in the image using the RasterImage class SavePixels method. The following code snippet shows you how to draw images using core functionality.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
