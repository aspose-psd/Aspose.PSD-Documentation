---
title: Drawing Images using Graphics
type: docs
weight: 20
url: /java/drawing-images-using-graphics/
---

## **Drawing Images using Graphics**


With the Aspose.PSD library you can draw simple shapes like lines, rectangles and circles, as well as complex shapes like polygons, curves, arcs and Bezier shapes. Aspose.PSD library creates such shapes using Graphics class that resides in the Aspose.PSD namespace. Graphics objects are responsible for performing different drawing operations on an image, thus changing the image's surface. The Graphics class uses a variety of helper objects to enhance the shapes:

- Pens, to draw lines, outline shapes, or render other geometric representations.
- Brushes, to define how areas are filled in.
- Fonts, to define the shape of characters of text.
### **Drawing with the Graphics Class**
Below is a code example demonstrating the use of the Graphics class. The example source code has been split into several parts to keep it simple and easy to follow. Step by step, the examples show how to:

1. Create an image.
1. Create and initialize a Graphics object.
1. Clear the surface.
1. Draw an ellipse.
1. Draw a filled polygon and save the image.
### **Programming Samples**
#### **Creating an Image**
Start by creating an image using any of the methods described in Creating Files.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Create and Initialize a Graphics Object**
Then create and initialize a Graphics object by passing the Image object to its constructor.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Clear the Surface**
Clear the Graphics surface by calling the Graphics class Clear method and pass a color as a parameter. This method fills the Graphics surface with the color passed in as argument.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Draw an Ellipse**
You may notice that the Graphics class has exposed plenty of methods to draw and fill shapes. You'll find get the complete list of methods in the Aspose.PSD for Java API Reference. There are several overloaded versions of the DrawEllipse method exposed by the Graphics class. All these methods accept a Pen object as its first argument. The later parameters are passed to define the bounding rectangle around the ellipse. For the sake of this example, use the version accepting a Rectangle object as the second parameter to draw an ellipse using the Pen object in your desired color.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Draw a Filled Polygon**
Next, draw a polygon using the LinearGradientBrush and an array of points. The Graphics class has exposed several overloaded versions of the FillPolygon method. All of these accept a Brush object as its first argument, defining the characteristics of the fill. The second parameter is an array of points. Please note that every two consecutive points in the array specify a side of the polygon.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Drawing Images using Graphics : Complete Source**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}



All classes that implements IDisposable and access unmanaged resources are instantiated in a Using statement to ensure that they are disposed of correctly.
