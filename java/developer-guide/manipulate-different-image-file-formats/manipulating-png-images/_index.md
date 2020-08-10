---
title: Manipulating PNG Images
type: docs
weight: 30
url: /java/manipulating-png-images/
---

## **Specifying Transparency for PNG Images**
One of the advantages of saving images in PNG format is that PNG can have transparent background. Aspose.PSD for Java provides the feature for specifying transparency for the PngImage & RasterImage classes as demonstrated in the below section. Aspose.PSD for Java API can be used to set any color as transparent while creating new PNG images or converting existing images to PNG format. For this purposes, the Aspose.PSD for Java API has exposed TransparentColor property and PngColorType enumeration that can be set to specify any color to be rendered as transparent in the PNG image. The below provided code snippet demonstrates how to convert an existing PSD image to PNG image by using PngImage overloaded constructor and specifying the desired color as transparent.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Setting Resolution for PNG Images**
Aspose.PSD for Java exposes the ResolutionSetting class which can be used to set the resolution for all image formats including PNG. This article demonstrates the usage of the Aspose.PSD for Java API to set the horizontal & vertical resolution parameters for the PNG image format. The code snippet below loads an existing PSD image and converts it to PNG format also changing the resolution.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Compressing PNG Files**
The Portable Network Graphic (PNG) is a lossless compression format for transmitting a bitmap over networks. When you save an image as a PNG file in any program, you may be asked to choose a compression level in a range from 0 to any max level. Setting this value actually compresses the file size and does not decrease the image quality. This article describes how Aspose.PSD APIs allows you to control the PNG file size. Aspose.PSD APIs can be used to set the Compression Levels for the PNG file format using the PngOptions class that has an int type CompressionLevel property. This property accepts a value from 0 to 9 where 9 is the maximum compression. The below provided code snippet demonstrates how to set the Compression Levels using Aspose.PSD for Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Specifying Bit Depth for PNG Images**
Bit depth in imaging is the number of bits used to indicate the color of a single pixel in a bitmap image. Like all other bitmap formats, PNG color depth is also represented in bit such as 1-bit (2 colors), 2-bit (4 colors), 4-bit (16 colors) and 8-bit (256 colors). Aspose.PSD for Java API can be used to set bit depth for PNG images using BitDepth property exposed by the PngOptions class. At the moment, the BitDepth property can be set to 1, 2, 4 or 8 bits for grayscale and indexed color types. For all other color types only 8 bits are supported. The below provided code snippet demonstrates how to set the Bit Depth for a PNG image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Applying Filter Methods on PNG Images**
Aspose.PSD for Java exposes the PngFilterType enumeration  which can be used to set the filter type for PNG image. The below provided code snippet demonstrates how to apply  filter on existing PSD file to PNG image by using PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Changing Background Color of a Transparent PNG Image**
PNG format images can have transparent background. Aspose.PSD for Java provides the feature to change the background color of a PNG image that has transparent background. Aspose.PSD for Java API can be used to set/change color of a transparent PNG image. The below provided code snippet demonstrates how to set/change the background color of a transparent PNG image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
