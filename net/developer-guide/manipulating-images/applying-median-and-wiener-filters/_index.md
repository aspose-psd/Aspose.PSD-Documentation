---
title: Applying Median and Wiener Filters
type: docs
weight: 10
url: /net/applying-median-and-wiener-filters/
---

## **Applying Median and Wiener Filters**
The median filter is a nonlinear digital filtering technique, often used to remove noise. Such noise reduction is a typical pre-processing step to improve the results of later processing. The Wiener filter is the MSE(mean squared error) optimal stationary linear filter for images degraded by additive noise and blurring. Using Aspose.PSD for .NET API developers can apply a median filter to denoise the image and can apply gauss wiener filter on images. This article demonstrates how the median filter and gauss wiener filter can be applied to images.
### **Applying Median Filter**
Aspose.PSD provides [MedianFilterOptions](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) class to apply a filter on a [RasterImage](https://apireference.aspose.com/net/psd/aspose.psd/rasterimage). The code snippet provided below demonstrates how to apply the median filter to a raster image.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **Applying Gauss Wiener Filter**
Aspose.PSD provides [GaussWienerFilterOptions](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) class to apply a filter on a [RasterImage](https://apireference.aspose.com/net/psd/aspose.psd/rasterimage). The code snippet provided below demonstrates how to apply the gauss wiener filter to a raster image.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **Applying Gauss Wiener Filter For Colored image**
Aspose.PSD provides [GaussWienerFilterOptions ](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)for colored images as well. The code snippet provided below demonstrates how to apply the gauss wiener filter to a color image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **Applying Motion Wiener Filter**
Aspose.PSD provides [MotionWienerFilterOptions ](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)class to apply a filter on a [RasterImage](https://apireference.aspose.com/net/psd/aspose.psd/rasterimage). The code snippet provided below demonstrates how to apply a motion wiener filter to a raster image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **Apply Correction Filter On An Image**
This article demonstrates the usage of Aspose.PSD for .NET to perform correction filters on an image. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD for .NET has exposed the [BilateralSmoothingFilterOptions ](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)and [SharpenFilterOptions ](https://apireference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)classes for filtration. BilateralSmoothingFilterOptions class needs an integer as size. The steps to perform Resize are as simple as below:



1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into RasterImage.
1. Create an instance of BilateralSmoothingFilterOptions and SharpenFilterOptions classes.
1. Call the [RasterImage.Filter](https://apireference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) method while specifying rectangle as image bounds and BilateralSmoothingFilterOptions class instance.
1. Call the [RasterImage.Filter](https://apireference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) method while specifying rectangle as image bounds and SharpenFilterOptions class instance.
1. Adjust the contrast
1. Set brightness
1. Save the results.

The following code snippet shows you how to apply a correction filter.


## **Use Bradley threshold algorithm**
Image thresholding is used in graphics applications. The goal of thresholding an image is to classify pixels as either “dark” or “light”. Aspose.PSD API allows you to use Bradley thresholding while converting images. The following code snippet shows you how to define the threshold value and then invoke the Bradley’s threshold algorithm.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
