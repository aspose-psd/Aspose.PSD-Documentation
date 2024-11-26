---
title: Color Space Conversion for JPEG through ICC Profiles
type: docs
weight: 60
url: /net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **Color Management for JPEG Format**


This article discusses the usage of ICC profiles to perform the color space management while handling JPEG format with Aspose.PSD APIs. JPEG’s inner color space is YCbCr however this [format](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) can also accommodate Grayscale, RGB, CMYK and YCCK color spaces to store the image’s metadata. Aspose.PSD APIs mainly operate in RGB space therefore the API has to perform to and from color space conversion in order to properly handle JPEG files. Grayscale to RGB & YCbCr to RGB conversions can be done with mathematical transformations but CMYK & YCCK spaces cannot be easily converted to RGB space.

The Aspose.PSD APIs has to perform direct RGB to CMYK color transformation for JPEG images having CMYK color space. On the other hand, the images having YCCK color space requires RGB to CMYK to YCCK color transformation, where CMYK to YCCK transformation uses the [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) conversion applied for the first three channels, leaving the k-channel untouched. In short, Aspose.PSD APIs have to perform interconversion of RGB and CMYK color spaces for both CMYK & YCCK images, and such transformations are performed with the help of ICC profiles that are basically look-up tables describing the properties of a color and helping in the color transformations.


## **ICC Profiles**
ICC conversion mechanism uses "Profiles" which maps the source color space to device-independent CIELAB or CIEXYZ color spaces. Aspose.PSD can convert data into color space as required while using these two color spaces with additional profiles. Therefore, for ICC conversion the user needs to supply two profiles – one RGB profile to get to the inner CIE color space and one CMYK profile to get the CMYK color characteristics. In order to achieve the CMYK to RGB conversion, one need to swap profiles, that is; use CMYK profile as source profile and RGB profile as destination profile.
## **Color Conversion for JPEG through ICC Profiles**
Aspose.PSD APIs conceal the details, providing an easy to use mechanism to specify ICC profiles via [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions) class. Moreover, Aspose.PSD uses the sample profiles of SWOP, CMYK and sRGB embedded into it's core therefore in most common usage cases, the user does not need to seek for any specific profiles. There is a drawback of such corrections, that is; such color space conversions are irreversible because we cannot expect to get same color after RGB to CMYK to RGB conversion because of incompatible color spaces and different color profiles. The following code snippet demonstrates the usage of Aspose.PSD for .NET API to specify RGB and CMYK color profiles for YCCK JPEG image. In the example below RGB and CMYK color profiles are changed and image is saved into YCCK color space. Please note that those [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) and [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) properties will work for changing pixel data for YCCK color space. All other color spaces do not fetch the color profiles for updating the color data.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}


If no profiles are set then Aspose.PSD for .NET API will use the default profiles instead. The example below uses destination profiles properties that change the destination color space for the most JPEG Images.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}
