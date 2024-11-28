---
title: Using Graphics API to edit Layers in PSD files
weight: 100
type: docs
description: Example of using Graphics API in the Aspose.PSD for Java
keywords: [update layer, draw circle, draw ellipse, draw fill circle, graphics, psd api, java, code sample]
url: java/graphics-api/
---

## **Overview**
To begin, load the PSD file using the Image.load() method or create a Psd Image from scratch. Use the inputFile variable to represent the path to your PSD file, and specify any loading options with loadOpt, if necessary.

Next, access the first layer of the PSD image using the psdImage.getLayers()[0] syntax to obtain a reference to the layer object for manipulation.

To edit the layer, create a Graphics object by passing the layer as a parameter. This object provides various methods for drawing shapes and applying brushes.

A Pen object is used to define the color and thickness of the outline of shapes. Similarly, brushes like LinearGradientBrush are used to define fill colors.

Draw shapes on the layer using methods like graphics.drawEllipse() to outline shapes and graphics.fillEllipse() to fill them.

After making desired changes to the layer, save the modified PSD image using psdImage.save().

Additionally, you can save the modified image in other formats like PNG by using appropriate options.

That's it! You have successfully used the Graphics API of Aspose.PSD for Java to edit layers in a PSD file. Explore more features and functionalities of the Aspose.PSD library to enhance your image editing capabilities.

Please check full example.

## **Example**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}