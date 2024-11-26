---
title: PSD Fill Layer updating using Java
weight: 100
type: docs
description: Examples of using all types of adjustment layers including Color Fill, Gradient Fill and Pattern Fill
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, java, code sample]
url: java/psd-fill-layer-editing/
---

## **Overview**

Creating a regular layer involves using the createRegularLayer function, which requires parameters for defining the layer's position and size. This function creates a new layer, sets its bounds, and fills it with a specified color.

For a color fill layer, you utilize the FillLayer.createInstance method with the FillType.Color parameter. Once the fill layer is created, access its fill settings through the fill_settings property and set the desired color using the color property of the ColorFillSettings class. In this context, the color is set to Color.getCoral(). Additionally, the clipping property of the fill layer is set to 1, causing it to function as a clipping mask.

Gradient fill layers are created similarly using the FillLayer.create_instance method, but with the FillType.Gradient parameter. Like color fill layers, you access the fill settings through fill_settings and set the gradient color points and transparency points. In this example, the gradient color points are defined with the GradientColorPoint class, and the transparency points with the GradientTransparencyPoint class. The clipping property of the fill layer is also set to 1.

Pattern fill layers are created using FillLayer.createInstance with the FillType.Pattern parameter. Once again, access the fill settings via fill_settings and set the pattern data and other properties. In this code, the pattern data is defined using the PatternFillSettings class, and the clipping property is set to 1.

Once the fill layers are created, add them to the PSD image using the addLayer method, specifying the display name and other properties for each fill layer.

Lastly, save the PSD image and its corresponding PNG image with the provided code. The PNG options are configured to use true color with alpha for transparency.

Please refer to the full example for more details.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}