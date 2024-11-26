---
title: Drawing Images using GraphicsPath
type: docs
weight: 30
url: /net/drawing-images-using-graphicspath/
---

## **Drawing Images using GraphicsPath**
The [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) class is responsible for creating and maintaining a graphics path. The GraphicsPath has no reference to an image and does not change the image itself, instead, it can be considered as an object that contains metadata that describes the paths that Graphics class can draw. The GraphicsPath class uses figures; each figure is either composed of a sequence of connected lines and curves or a geometric shape primitive. Each shape may be split into shape segments. You can add, remove and change different figures or shapes in a GraphicsPath object. When the GraphicsPath has been fully described, use the corresponding Graphics class methods (DrawPath and Fill Paths) to draw over or fill the paths. The Graphics class takes each shape segment and draws it to produce the final image.
### **Drawing using GraphicsPath Class**
Below is an example demonstrating the use of the [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) class. The example source code has been split in several parts to keep it simple and easy to follow. Step by step, the examples show you how to:

- Create an image.
- Initialize a Graphics object.
- Clear the surface.
- Create an instance of [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath).
- Create a figure.
- Add shapes to the figure.
- Create a Figures array.
- Draw paths.
- Fill paths.


### **Drawing Images using GraphicsPath: Programming Samples**
#### **GraphicsPath : Create an Image**
Start by creating an image using any of the methods described in Creating Files.
#### **GraphicsPath : Initialize a Graphics Objects**
Create and initialize a Graphics object by passing the Image object to its constructor.
#### **GraphicsPath : Clear the Surface**
Clear the Graphics surface by calling the Graphics class Clear method and pass a Color as a parameter. This method fills the Graphics surface with the color passed in as argument.
#### **GraphicsPath : Create an Instance of the GraphicsPath**
Create an instance of GraphicsPath with GraphicsPath set to Alternate by default. This mode determines how to fill the interior of a closed figure. The other possible GraphicsPath value is Winding.
#### **GraphicsPath : Create a Figure**
Create an instance of the Figure class. As discussed earlier, Figure can contain Shapes and shapes reside in the Aspose.PSD.Shapes namespace.
#### **GraphicsPath : Add Shapes to the Figure**
The Add Shapes method exposed by the Figure class lets you add shapes to the figure. In the code examples below, several shapes are added to a Figure object.
#### **GraphicsPath : Add Figures to an Array**
Multiple figures can be added to a GraphicsPath object using the AddFigures method exposed by the GraphicsPath class. This method accepts an array of figures as a parameter.
#### **GraphicsPath : Draw the Paths**
Draw the GraphicsPath using the DrawPath method exposed by Graphics class. The method accepts two parameters. The first parameter is an object of the Pen class, which determines the color, width and style of the path. The second parameter is the object of the GraphicsPath class, representing the path itself.
#### **GraphicsPath : Fill Paths**


You can fill a path by passing a GraphicsPath object to the Fill Paths method exposed by the Graphics class. The Fill Paths method fills the path according to the fill mode (alternate or winding) currently set for the path. If the path has any open figures, the path is filled as if those figures were closed.

The Fill Paths method accepts two parameters. The first parameter is an object of any brush class from the Aspose.PSD.Brushes namespace. The second parameter is the path itself. For the sake of this example, use the HatchBrush which is a rectangular brush with a hatch style, a foreground color, and a background color. Before passing the HatchBrush object to the Fill Paths method, set its properties.
### **GraphicsPath : Complete Source**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



All classes that implements IDisposable are instantiated in a Using statement to ensure that they are disposed of correctly.
