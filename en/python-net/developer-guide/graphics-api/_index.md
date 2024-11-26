---
title: Using Graphics API to edit Layers in PSD files
weight: 100
type: docs
description: Example of using Graphics API in the Aspose.PSD for Python
keywords: [update layer, draw circle, draw ellipse, draw fill circle, graphics, psd api, python, code sample]
url: python-net/graphics-api/
---

## **Overview**
First, you need to load the PSD file using the Image.load() method or create a Psd Image from Scratch. In the example, the inputFile variable represents the path to your PSD file, and loadOpt represents the loading options (if any).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
Next, you can access the first layer of the PSD image using the psdImage.layers[0] syntax. This gives you a reference to the layer object that you can manipulate.

```python 
layer = psdImage.layers[0]
```
To edit the layer, you need to create a Graphics object by passing the layer as a parameter. This object provides various methods for drawing shapes and applying brushes.

```python 
graphics = Graphics(layer)
```
In the code example, a Pen object is created to define the color and thickness of the outline of the ellipse shape. The Color.alice_blue constant represents the color, and you can adjust the thickness as needed.

```python 
pen = Pen(Color.alice_blue)
```
Similarly, a LinearGradientBrush object is created to define the fill color of the ellipse shape. The Rectangle(250, 250, 150, 100) represents the position and size of the ellipse shape, and Color.red and Color.aquamarine represent the start and end colors of the gradient.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
To draw the ellipse shape on the layer, you can use the graphics.draw_ellipse() method. The Rectangle(100, 100, 200, 200) represents the position and size of the ellipse shape.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
To fill the ellipse shape with the gradient brush, you can use the graphics.fill_ellipse() method. The Rectangle(250, 250, 150, 100) represents the position and size of the ellipse shape.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
After making the desired changes to the layer, you can save the modified PSD image using the psdImage.save() method. In the example, the psdName variable represents the path to save the modified PSD file.

```python 
psdImage.save(psdName)
```
Additionally, you can also save the modified image in other formats, such as PNG, by using the PngOptions class. The pngName variable represents the path to save the PNG file.

```python 
psdImage.save(pngName, PngOptions())
```
That's it! You have successfully used the Graphics API of Aspose.PSD for Python to edit layers in a PSD file. Feel free to explore more features and functionalities of the Aspose.PSD library to enhance your image editing capabilities.

Please check full example.

## **Example**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}