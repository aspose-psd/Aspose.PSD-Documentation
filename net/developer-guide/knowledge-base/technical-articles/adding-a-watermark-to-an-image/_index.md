---
title: Adding a Watermark to an Image
type: docs
weight: 30
url: /net/adding-a-watermark-to-an-image/
---

## **Adding a Watermark to an Image**
This document explains how to add a watermark to an image using Aspose.PSD. Adding a watermark to an image is a common requirement for image processing applications. This example uses the Graphics class to draw a string on the image surface.
### **Adding a Watermark**
To demonstrate the operation, we will load a BMP image from disk and draw a string as the watermark on the image surface using the Graphics class DrawString method. We'll save the image to PNG format using the PngOptions class. Below is a code example that demonstrates how to add a watermark to an image. The example source code has been split into parts to make it easy to follow. Step by step, the examples show how to:

1. [Load](https://apireference.aspose.com/psd/net/aspose.psd.image/load/methods/2) an image.
1. Create and initialize a [Graphics](https://apireference.aspose.com/psd/net/aspose.psd/graphics) object.
1. Create and initialize Font and [SolidBrush](https://apireference.aspose.com/psd/net/aspose.psd.brushes/solidbrush) objects.
1. Draw a string as watermark using the Graphics class [DrawString](https://apireference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) method.
1. Save image to PNG.

The following code snippet shows you how to add watermark on the image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **Adding a Diagonal Watermark**
Adding a diagonal watermark to an image is similar to adding a horizontal watermark as discussed above, with a few differences. To demonstrate the operation, we will load a JPG image from disk, add transformations using an object of [Matrix](https://apireference.aspose.com/psd/net/aspose.psd/matrix) class and draw a string as the watermark on the image surface using the Graphics class DrawString method. Below is a code example that demonstrates how to add a diagonal watermark to an image. The example source code has been split into parts to make it easy to follow. Step by step, the examples show how to:

1. Load an image.
1. Create and initialize a Graphics object.
1. Create and initialize [Font](https://apireference.aspose.com/psd/net/aspose.psd/font) and SolidBrush objects.
1. Get size of image in [SizeF](https://apireference.aspose.com/psd/net/aspose.psd/sizef) object.
1. Create an instance of Matrix class and perform composite transformation.
1. Assign transformation to Graphics object.
1. Create and initialize a [StringFormat](https://apireference.aspose.com/psd/net/aspose.psd/stringformat) object.
1. Draw a string as watermark using the Graphics class DrawString method.
1. Save resultant image.

The following code snippet shows you how to add a diagonal watermark.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
