---
title: Modifying Images
type: docs
weight: 50
url: /net/modifying-images/
---

## **Dithering for Raster Images**
Dithering is a technique of creating the illusion of new colors and shades by varying the pattern of dots that actually create an image. It is the most common means of reducing the color range of images down to the 256 (or fewer) colors. Aspose.PSD provides the dithering support for RasterImage class by introducing the Dither method that accepts two parameters. First is of type DitheringMethod to be applied with two possible options FloydSteinbergDithering and ThresholdDithering. The second parameter to the Dither method is the BitCount in integer. BitCount defines the sampling size for the dithering result. The default value is 1 that represents black and white, whereas allowed values are 1, 4, 8 generating palettes with 2, 4 and 256 colors respectively.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **Adjusting Brightness, Contrast and Gamma**
Color adjustments in digital images is one of the core features that most of the image processing libraries provide. Color adjustments can be categorized in the following.

1. Brightness refers to the lightness or darkness of a color. Increasing the brightness of an image lights out all colors whereas decreasing the brightness darkens all colors.
1. Contrast refers to making the objects or details within an image more obvious. Increasing the contrast of an image increases the difference between light and dark areas so that the light areas become lighter and dark areas become darker. Decreasing the contrast will make lighter and darker areas stay approximately the same but the overall image becomes more homogeneous.
1. Gamma optimizes the contrast and brightness of the indirect lighting that is illuminating an object in the image.
### **Adjusting Brightness**
Aspose.PSD for .NET API provides the AdjustBrightness method for the RasterImage class that can be used to adjust the image brightness by passing an integer value as a parameter. The highest parameter value denotes to a brighter image. Here is the original image and the resultant image for comparison.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Adjusting Contrast**
The AdjustContrast method exposed by the RasterImage class can be used to adjust the Contrast of an image by passing a float value as a parameter.

The highest parameter value denotes a higher contrast in the given image. Here is the original image and the resultant image for comparison.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Adjusting Gamma**
The AdjustGamma method exposed by the RasterImage class has two versions. One of the overloads accepts one float value and performs the Gamma correction for red, blue & green channel coefficients. Whereas the other overload accepts three float parameters representing each color coefficient separately. The following code example demonstrates how to AdjustGamma on an image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Blur an Image**
This article demonstrates the usage of Aspose.PSD for .NET to perform Blur effect on an image. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD for .NET has exposed the GaussianBlurFilterOptions class to create a blur effect on the fly. GaussianBlurFilterOptions class need radius and sigma values to create a blur effect on an image. The steps to perform Resize are as simple as below:

1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into RasterImage.
1. Create an instance of GaussianBlurFilterOptions class with default constructor or provide radius and sigma values in the constructor.
1. Call the RasterImage.Filter method while specifying rectangle as image bounds and GaussianBlurFilterOptions class instance.
1. Save the results.

The following code example demonstrates how to create a blur effect on an image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Verify Image Transparency**
This article demonstrates the usage of Aspose.PSD for .NET to check image transparency. The steps to check image transparency are as simple as below:

1. Load an image using the factory method Load exposed by Image class.
1. Check image opacity if opacity is zero image is transparent.
1. The following code example demonstrates how to check the image is transparent or not.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implement Lossy GIF Compressor**
Using Aspose.PSD for .NET, developers can set a pixel difference. GIF's compression is based on a "dictionary" of strings of pixels seen. Normal encoder searches the dictionary for the longest string of pixels that exactly match pixels in the image. Lossy encoder picks the longest string of pixels that's "similar enough" to pixels in the image. Below is the code demonstration of the said functionality.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implement Bicubic Resampling**
Resampling means you are changing the pixel dimensions of an image. When you downsample, you are eliminating pixels and therefore deleting information and detail from your image. When you upsample, you are adding pixels. Photoshop adds these pixels by using interpolation. This article demonstrates how you can perform the Bicubic Resampling by using Aspose.PSD for .NET.

Below is the code demonstration of the said functionality.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Color Balance Adjustment Layer**
This article demonstrates the usage of Aspose.PSD for .NET to perform the **Color Balance adjustment layer** on an image. The color balance adjustment layer gives you the ability to make adjustments to the coloring of their images. It presents the three color channels and their complementary colors and you can adjust the balance of these pairs to change the appearance of a photo.

Below is the code demonstration of the said functionality.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustmentLayer.cs" >}}
## **Invert Adjustment Layer**
This article demonstrates how you can perform the **Invert adjustment layer** by using Aspose.PSD for .NET.  An adjustment layer is a special kind of layer used mostly for color correction. Rather than having a content of their own, they adjust the information on the layers below them. The Invert adjustment layer makes a photo negative effect by inverting the colors of an image.

Below is the code demonstration of the said functionality.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}




