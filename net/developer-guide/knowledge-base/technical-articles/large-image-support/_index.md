---
title: Large Image Support
type: docs
weight: 40
url: /net/large-image-support/
---

## **Large Image Support**
Since the standard .NET library has some limitations as to the image size it can process, we introduced a new mechanism for large images support. The new approach overcomes the limitations but due to data size limitations the max supported dimensions for creation and loading are 2,147,483,647 x 2,147,483,647 pixels.
### **Working with Large Images**
Aspose.PSD has improved performance and support for large images. Images that are hundreds of megabytes in size is no longer a problem so you can create, load and draw over those images. However, due to the partial processing and handling of OutOfMemoryException exceptions, performance may be very low on very large images. This is due to the fact that Aspose.PSD tries to re-allocate a smaller amount of data for processing and each reallocation step is very costly. The benefits of the new architecture are obvious:

- There's no limitation to the image size.
- You are not limited to the memory available on your PC.

If you experience slow processing, it is advised to increase the total amount of RAM to fit all your pixels into memory. If you don't, processing is still possible but is slower. The approach is as follows:

- Call the [LoadPartialPixels](https://apireference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadpartialpixels) method with the desired rectangle and delegate to receive the loaded pixels specified.

Aspose.PSD tries to load the whole rectangle.

- If there is enough memory to fit all the pixels, then all the pixels are simply returned to the caller.
- If there is not enough memory, the caller receives a subset of pixels from inside the specified rectangle. When those pixels have been processed, the caller receives the next rectangle. Processing ends when the whole rectangle is processed.

Aspose.PSD tries to extract as many lines as possible. If there's not enough memory to fit a single line of pixels, then a single line is split into parts conforming to the rectangles having 1 height. You may also draw on large images. The drawing process tries to affect the whole desired rectangle. If there is not enough memory, drawing is performed on partial rectangles until the whole area is drawn. Additionally, Aspose.PSD supports saving and exporting large images. Save the source image to disk or export it to another file format. The save or export process is performed by using partial rectangles if required. 
### **Supported Image Formats**
The following formats are supported for large images processing:

- [BMP](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GIF](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [TIFF](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PSD](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)
- [JPG](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [PNG](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

The above formats may be safely processed through creation, modifying, applying drawing operations, saving to disk or exporting into regardless of image size.
