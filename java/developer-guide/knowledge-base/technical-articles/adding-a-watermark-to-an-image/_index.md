---
title: Adding a Watermark to an Image
type: docs
weight: 20
url: /java/adding-a-watermark-to-an-image/
---

## **Adding a Watermark to an Image**
This document explains how to add a watermark to an image using Aspose.PSD. Adding a watermark to an image is a common requirement for image processing applications. This example uses the Graphics class to draw a string on the image surface.
### **Adding a Watermark**
To demonstrate the operation, we will load a BMP image from disk and draw a string as the watermark on the image surface using the Graphics class DrawString method. We will save the image to PNG format using the PngOptions class. Below is a code example that demonstrates how to add a watermark to an image. The example source code has been split into parts to make it easy to follow. Step by step, the examples show how to:

1. Load an image.
1. Create and initialize a Graphics object.
1. Create and initialize Font and SolidBrush objects.
1. Draw a string as watermark using the Graphics class DrawString method.
1. Save image to PNG.

The following code snippet shows you how to add watermark on the image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **Adding a Diagonal Watermark**
Adding a diagonal watermark to an image is similar to adding a horizontal watermark as discussed above, with a few differences. To demonstrate the operation, we will load a JPG image from disk, add transformations using an object of Matrix class and draw a string as the watermark on the image surface using the Graphics class DrawString method. Below is a code example that demonstrates how to add a diagonal watermark to an image. The example source code has been split into parts to make it easy to follow. Step by step, the examples show how to:

1. Load an image.
1. Create and initialize a Graphics object.
1. Create and initialize Font and SolidBrush objects.
1. Get size of image in SizeF object.
1. Create an instance of Matrix class and perform composite transformation.
1. Assign transformation to Graphics object.
1. Create and initialize a StringFormat object.
1. Draw a string as watermark using the Graphics class DrawString method.
1. Save resultant image.

The following code snippet shows you how to add a diagonal watermark.





{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
