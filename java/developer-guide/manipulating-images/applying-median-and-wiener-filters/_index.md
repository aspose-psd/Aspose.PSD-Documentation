---
title: Applying Median and Wiener Filters
type: docs
weight: 10
url: /java/applying-median-and-wiener-filters/
---

## **Applying Median and Wiener Filters**
The median filter is a nonlinear digital filtering technique, often used to remove noise. Such noise reduction is a typical pre-processing step to improve the results of later processing. The Wiener filter is the MSE(mean squared error) optimal stationary linearfilter for images degraded by additive noise and blurring. Using Aspose.PSD for Java API developers can apply median filter to denoise the image and can apply Gauss wiener filter on images. This article demonstrates how median filter and Gauss wiener filter can be applied to images.
### **Applying Median Filter**
Aspose.PSD provides MedianFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply median filter to a raster image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Applying Gauss Wiener Filter**
Aspose.PSD provides GaussWienerFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply Gauss wiener filter to a raster image.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Applying Gauss Wiener Filter For Colored image**
Aspose.PSD provides GaussWienerFilterOptions for colored images as well.. The code snippet provided below demonstrates how to apply Gauss wiener filter to a color image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Applying Motion Wiener Filter**
Aspose.PSD provides MotionWienerFilterOptions class to apply filter on a RasterImage. The code snippet provided below demonstrates how to apply motion wiener filter to a raster image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Apply Correction Filter On An Image**
This article demonstrates the usage of Aspose.PSD for Java to perform correction filters on an image. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD for Java has exposed the BilateralSmoothingFilterOptions and SharpenFilterOptions classes for filtration. BilateralSmoothingFilterOptions class needs an integer as size. The steps to perform Resize are as simple as below:



1. Load an image using the factory method Load exposed by Image class.
1. Convert the image into RasterImage.
1. Create an instances of BilateralSmoothingFilterOptions and SharpenFilterOptions classes.
1. Call the RasterImage.Filter method while specifying rectangle as image bounds and BilateralSmoothingFilterOptions class instance.
1. Call the RasterImage.Filter method while specifying rectangle as image bounds and SharpenFilterOptions class instance.
1. Adjust the contrast
1. Set brightness
1. Save the results.

The following code snippet shows you how to apply correction filter.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Use Bradley threshold algorithm**
Image thresholding is used in graphics applications. The goal of thresholding an image is to classify pixels as either “dark” or “light”. Aspose.PSD API allows you to use Bradley thresholding while converting images. The following code snippet shows you how to define the threshold value and then invoke the Bradley’s threshold algorithm.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
