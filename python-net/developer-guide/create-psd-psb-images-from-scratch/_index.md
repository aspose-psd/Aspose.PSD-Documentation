---
title: Create PSD or PSB Image From Scratch using Python
weight: 100
type: docs
description: Example of how the Aspose.PSD for Python can create Psd Image from scratch
keywords: [create psd, create psb, create new, create layer, create text layer, psd api, python, code sample]
url: python-net/create-psd-psb-images-from-scratch/
---

## **Overview**
To create a PSD or PSB file from scratch using Aspose.PSD for Python, you can follow the steps below:

Import the necessary modules and classes from the Aspose.PSD library:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Specify the output file name and path:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```
Create a PSD image with the desired dimensions:

```python 
with PsdImage(500, 500) as img:
```
Add a regular PSD layer and update it using the graphic API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Create a text layer:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

Add a drop shadow effect to the text layer:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Save the PSD file:
```python 
img.save(outputFile)
```

This code creates a PSD image with dimensions of 500x500 pixels. It adds a regular layer and draws an ellipse on it using a pen and a brush. It then adds a text layer with the text "Sample Text" and applies a drop shadow effect to it. Finally, it saves the PSD file with the specified output file name.

Please note that you will need to have the Aspose.PSD library installed and properly set up in your Python environment for this code to work. You can refer to the official Aspose.PSD documentation for more information on how to install and use the library.

Please check full example.

## **Example**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}