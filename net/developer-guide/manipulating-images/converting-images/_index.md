---
title: Converting Images
type: docs
weight: 20
url: /net/converting-images/
---

## **Converting Images to Black n White and Grayscale**
Sometimes you may require to convert colored images to Black n White or Grayscale for printing or archiving purposes. This article demonstrates the use of Aspose.PSD for .NET API to achieve this using two methods as stated below.

- Binarization
- Grayscaling
### **Binarization**
In order to understand the concept of Binarization, it is important to define a Binary Image; that is a digital image that can have only two possible values for each pixel. Normally, the two colors used for a binary image are black and white though any two colors can be used. Binarization is the process of converting an image to bi-level meaning that each pixel is stored as a single bit (0 or 1) where 0 denotes the absence of color and 1 means presence of color. Aspose.PSD for .NET API currently supports two Binarization methods.
#### **Binarization with Fixed Threshold**
The following code snippet shows you how to use fixed threshold binarization can be applied to an image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarization with Otsu Threshold**
The following code snippet shows you how Otsu threshold binarization can be applied to an image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Grayscaling**
Gray-scaling is the process of converting a continuous-tone image to an image with discontinues gray shades. The following code snippet shows you how to use Grayscaling.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Convert GIF Image Layers To TIFF Image**
Sometimes it is needed to extract and convert layers of a PSD Image into another raster image format to meet an application need. Aspose.PSD API supports the feature of extracting and converting layers of a PSD Image into another raster image format. Firstly, we will create an instance of image and load PSD image from the local disk, then we will iterate each layer in the Layer property. Then we will convert the block to TIFF image. The following code snippet shows you how to convert PSD image layers to TIFF images.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Converting CMYK PSD to CMYK TIFF**
Using Aspose.PSD for .NET, developers can convert CMYK PSD file to CMYK tiff format. This article shows how to export/convert CMYK PSD file to CMYK tiff format with Aspose.PSD. Using Aspose.PSD for .NET you can load PSD images and then you can set various properties using [TiffOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class and save or export the image. The following code snippet shows you how to achieve this feature.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Exporting Images**
Along with a rich set of image processing routines, Aspose.PSD provides specialized classes to convert PSD file formats to other formats. Using this library, PSD images conversion is very simple and intuitive. Below are some specialized classes for this purpose in [ImageOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

It is easy to export PSD images with Aspose.PSD for .NET API. All you need is an object of the appropriate class from [ImageOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. By using these classes, you can easily export any image created, edited or simply loaded with Aspose.PSD for .NET to any supported format.
## **Combining Images**
This example uses Graphics class and shows how to combine two or more images into a single complete image. To demonstrate the operation, the example creates a new PsdImage and draws images on the canvas surface using Draw Image method exposed by Graphics class. Using Graphics class two or more images can be combined in such a way that the resultant image will look as a complete image with no space between the image parts and no pages. The canvas size must be equal to the size of the resultant image. Following is the code demonstration that shows how to use [DrawImage](https://apireference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) method of the [Graphics](https://apireference.aspose.com/psd/net/aspose.psd/graphics) class to combine images in a single image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Expand and Crop Images**
Aspose.PSD API allows you to expand or crop an image during image conversion process. Developer needs to create a rectangle with X and Y coordinates and specify the width and height of the rectangle box. The X, Y and Width, Height of rectangle will depict the expansion or cropping of the loaded image. If it is required to expand or crop the image during image conversion, perform the following steps:

1. Create an instance of [RasterImage](https://apireference.aspose.com/psd/net/aspose.psd/rasterimage) class and load the existing image.
1. Create an Instance of ImageOption class.
1. Create an instance of [Rectangle](https://apireference.aspose.com/psd/net/aspose.psd/rectangle) class and initialize the X,Y and Width, Height of the rectangle
1. Call [Save](https://apireference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) method of the RasterImage class while passing output file name, image options and the rectangle object as parameters.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Read and Write XMP Data To Images**
XMP (Extensible Metadata Platform) is an ISO standard. XMP standardizes a data model, a serialization format and core properties for the definition and processing of extensible metadata. It also provides guidelines for embedding XMP information into a popular image such as JPEG, without breaking their readability by applications that do not support XMP. Using Aspose.PSD for .NET API developers can read or write XMP metadata to images. This article demonstrates how XMP metadata can be read from an image and write XMP metadata to images.
### **Create XMP Metadata, Write It And Read From File**
With the help of Xmp namespace developer can create XMP metadata object and write it to an image. The following code snippet shows you how to use the XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage and DublinCorePackage packages contained in [Xmp](https://apireference.aspose.com/psd/net/aspose.psd.xmp) namespace.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Export Images in Multi Threaded Environment**
Aspose.PSD for .NET now supports converting images in multi-threaded environment. Aspose.PSD for .NET ensures the optimized performance of operations during execution of code in a multi-threaded environment. All [image option](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions) classes (e.g. BmpOptions, TiffOptions, JpegOptions, etc.) in the Aspose.PSD for .NET implement IDisposable interface. Therefore it is a must that developer properly dispose off the image options class object in case Source property is set. Following code snippet demonstrates the said functionality.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD now supports SyncRoot property while working in a multi-threaded environment. Developer can use this property to synchronize access to the source stream. Following code snippet demonstrates how the SyncRoot property can be used.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
