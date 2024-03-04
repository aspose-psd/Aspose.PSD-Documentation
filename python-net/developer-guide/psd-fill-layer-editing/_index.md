---
title: PSD Fill Layer updating using Python
weight: 100
type: docs
description: Examples of using all types of adjustment layers including Color Fill, Gradient Fill and Pattern Fill
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, python, code sample]
url: python-net/psd-fill-layer-editing/
---

## **Overview**

To create a regular layer, you can use the create_regular_layer function provided in the code. This function takes the left, top, width, and height parameters to define the position and size of the layer. It creates a new layer, sets its bounds, and fills it with a specified color.

To create a color fill layer, you can use the FillLayer.create_instance method with the FillType.COLOR parameter. After creating the fill layer, you can access its fill settings using the fill_settings property and set the color using the color property of the ColorFillSettings class. In the provided code, the color is set to Color.coral. The clipping property of the fill layer is set to 1, which makes the layer act as a clipping mask.

To create a gradient fill layer, you can use the FillLayer.create_instance method with the FillType.GRADIENT parameter. Similar to the color fill layer, you can access the fill settings using the fill_settings property and set the gradient color points and transparency points. In the provided code, the gradient color points are defined using the GradientColorPoint class, and the transparency points are defined using the GradientTransparencyPoint class. The clipping property of the fill layer is also set to 1.

To create a pattern fill layer, you can use the FillLayer.create_instance method with the FillType.PATTERN parameter. Again, you can access the fill settings using the fill_settings property and set the pattern data and other properties. In the provided code, the pattern data is defined using the PatternFillSettings class, and the clipping property is set to 1.

After creating the fill layers, you can add them to the PSD image using the add_layer method. You can also specify the display name and other properties for each fill layer.

Finally, you can save the PSD image and the corresponding PNG image using the provided code. The PNG options are set to use truecolor with alpha for transparency.

Please check full example.

## **Example**
{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}