---
title: Manipulating TIFF Images
type: docs
weight: 50
url: /net/manipulating-tiff-images/
---

## **Add Frames with Different Settings**
TIFF is a very flexible format and it allows different frames to be added, with different dimensions, compression and other settings. Aspose.PSD APIs allow you to add any TIFF frame of any size which helps in creating complex documents. If there is a requirement to adjust the frames during the add process to make them all equal, perform the following steps:

- Create a new blank frame with the desired options or copy the source frame with the output options specified using the CreateFrameFrom method.
- Resize the source frame/image to the desired dimensions using the Resize method.
- Add the source frame/image pixels to the new frame.
- Add the new frame to the output TIFF image.
## **Export layers of PSD image to Multi Page Tiff file format**
Sometimes you need to export PSD image layers to Multi-page TIFF file format. This article will demonstrate how we can perform this task using Aspose.PSD for .NET API. First, we will load PSD image from disk. Then we will iterate over PSD image layers and create TiffFrame from corresponding layers. Finally we will save the resultant Tiff image into single file on disk.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **TiffOptions Configuration**


Developers can adjust different properties of Tiffoptions class to get desired results. In this document, we will focus on 4 main properties that controls the resultant image attributes.

These properties are listed below.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Whenever we initialize an empty Tiffoptions structure, each option is set to its default value, for instance compression is set to None, BitsPerSample is set as 1 and Photometric as MinIsWhite. Saving into this format will make the final image black n white and this is expected behavior for such options combination. In order to get the colored results you have to set all the above mentioned properties to values that correspond to desired color space or you can initialize the Tiffoptions structure with predefined settings as discussed later in this article. Provided below is a table describing the expected parameter values that you can set in order to achieve desired results. Please note, you should set all 4 columns through Tiffoptions in order to save any loaded/created image to TIFF file format.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16 (palette, color mode) single channel only|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16 (gray-scale mode) single channel only|None|
|Palette|LZW/Uncompressed|8 (palette, color mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8 (gray-scale mode) single channel only|Horizontal (more compression achieved for LZW same patterns)|
|RGB|LZW/Uncompressed|[8,8,8] (3 RGB channels)|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8] (3 RGB channels and additional alpha channel may be set through TiffOptions.AlphaStorage) Actually any additional channels count is supported but each channel must have 8 bit size like [8,8,8,8,8,8]|None/Horizontal|
All 4 properties should be set through TiffOptions in order to save any image format to Tiff format. When employing different combinations, some viewers (including the Windows Photo Viewer) may refuse to render the resultant image due to the limited support they offer. In such case, please pick different viewer for your testing.
### **Predefined Settings for TiffOptions Class**
In order to facilitate the users and to avoid the miss-configuration of the Tiffoptions instance, the Aspose.PSD for .NET API has exposed another constructor that accepts a parameter of type TiffExpectedFormat. Based on the selected value from the TiffExpectedFormat enumeration, the API auto configures all the mandatory properties for the Tiffoptions instance in order to produce the desired results. Before we move towards the sample code, here is the list of the TiffExpectedFormat fields and their details for better understanding of the usage.



- TiffExpectedFormat.Default: Setting the field to Default acts similar to the default constructor of Tiffoptions class with no compression set and BitsPerPixel set to 1 in order to produce a black n white result. It is advised to use this field when other format specific properties are to be set manually according to the desired results.
- TiffExpectedFormat.TiffCcitRle: Specific to RLE encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
- TiffExpectedFormat.TiffCcittFax3: Specific to CCITT Fax3 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
- TiffExpectedFormat.TiffCcittFax4: Specific to CCITT Fax4 encoding while saving the result in 1 BitsPerPixel (black n white) TIFF format.
- TiffExpectedFormat.TiffDeflateBW: Specific to Deflate compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
- TiffExpectedFormat.TiffDeflateRGB: Specific to Deflate compression while saving the result in RGB (color) TIFF format.
- TiffExpectedFormat.TiffJpegRGB: Specific to Jpeg compression while saving the result in RGB (color) TIFF format.
- TiffExpectedFormat.TiffJpegYCBCR: Specific to Deflate compression while saving the result in YCBCR (color) TIFF format.
- TiffExpectedFormat.TiffLzwBW: Specific to LZW compression while saving the result in 1 BitsPerPixel (black n white) TIFF format.
- TiffExpectedFormat.TiffLzwRGB: Specific to LZW compression while saving the result in RGB (color) TIFF format.
- TiffExpectedFormat.TiffLzwRGBA: Specific to LZW compression while saving the result in RGBA (color with transparency) TIFF format.
- TiffExpectedFormat.TiffNoCompressionBW: Specific to uncompressed TIFF format while saving the result in 1 BitsPerPixel (black n white).
- TiffExpectedFormat.TiffNoCompressionRGB: Specific to uncompressed TIFF format while saving the result in RGB (color).
- TiffExpectedFormat.TiffNoCompressionRGBA: Specific to uncompressed TIFF format while saving the result in RGBA (color with transparency).



The following code snippet elaborates the usage of TiffExpectedFormat fields while creating an instance of Tiffoptions class.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Support for Deflate and Adobe Deflate Compression**
The TIFF (Tagged Image File Format) file format supports various types of compression whereas the compression type is stored as a tag (an integer value) in the file. One of such compression methods is Adobe Deflate (previously known as Deflate). The Aspose.PSD for .NET API supports this compression method for exporting & creating of TIFF images.
### **Saving Image into TIFF with Deflate Compression**
Converting the loaded images into TIFF with Deflate/Adobe Deflate compression is easy as follow.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Creating TiffImage with Adobe Deflate Compression**
Below provided sample demonstrates the usage of Aspose.PSD for .NET API to create an image from scratch using the Adobe Deflate compression method.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **Compressing TIFF Images**
Aspose.PSD for .NET API can be used to convert PSD images to TIFF image format and even change the compression of the resulting TIFF image. The API can also be used to store different images as frames in a TIFF image for archiving purposes while compressing the images to lowest data size. The image compression in any case should be performed by reducing the source data size regardless of the compression algorithm used. In order to achieve the best compression ratio we may use indexed color spaces. The below provided code snippet performs the best compression using 16 indexed colors only and LZW compression algorithm however the source colors are slightly dithered.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}

