---
title: Smart Filter Manipulation in Aspose.PSD for Java
weight: 100
type: docs
description: Examples of how to use Smart Filters in PSD File
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, java, code sample]
url: java/smart-filters/
---

## **Overview**

There are 3 methods for applying smart filters in Aspose.PSD for Java.

## ** Direct Filter Applying **
This code sample demonstrates how to directly apply smart filters in Aspose.PSD for Java.

Initially, the code defines the source PSD file, the output file for the original image, and the output file for the updated image.

Then, the code loads the PSD image using the Image.load() method and casts it to a PsdImage object.

The original image is saved using the save() method, specifying the output file name.

A SharpenSmartFilter object is instantiated to represent the desired smart filter.

Next, the code retrieves the regular layer from the PSD image using psdImage.getLayers()[1].

A loop is utilized to apply the sharpenFilter to the regular layer three times.

Finally, the updated image is saved using the save() method with the output file name provided.

This code exemplifies the direct application of smart filters in Aspose.PSD for Java. By utilizing appropriate filter objects and applying them to desired layers, desired effects can be achieved on images.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## ** Manipulation Smart Filters in The Smart Objects **

This code snippet outlines how to manipulate smart filters within smart objects in Aspose.PSD for Java.

Initially, the code defines the source PSD file, the output file for the original image, and the output file for the updated image.

The PSD image is loaded using the Image.load() method and then cast to a PsdImage object.

The original image is saved using the save() method, specifying the output file name.

The code then casts the second layer of the PSD image to a SmartObjectLayer object, representing the smart object layer.

Subsequently, the code demonstrates editing smart filters, showcasing two types: GaussianBlurSmartFilter and AddNoiseSmartFilter.

For the GaussianBlurSmartFilter, the code updates filter values such as radius, blend mode, opacity, and activation status.

For the AddNoiseSmartFilter, the code sets the noise distribution to NoiseDistribution.Uniform.

Next, the code adds two new filter items to the smart object layer: another GaussianBlurSmartFilter and an AddNoiseSmartFilter.

Following the addition of new filters, the code applies changes using the updateResourceValues() method.

Lastly, the code demonstrates directly applying filters to the layer and its mask using the apply() and applyToMask() methods, respectively.

The updated image is then saved using the save() method with the output file name provided.

By following this code sample, you can understand how to manipulate smart filters within smart objects in Aspose.PSD for Java. The library offers a wide array of smart filters, each with its own set of properties and methods that can be customized to achieve desired effects on images.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** Applying Smart Filters to Layer Mask **

Applying Smart Filters to Masks: A Potent Image Editing Technique

Smart filters, prevalent in image editing software, enable users to apply diverse filters and effects to their images. One intriguing technique enabled by smart filters is their application to masks. This article explores applying smart filters to masks and discusses their utility in the realm of image editing.

Understanding Masks: Before delving into applying smart filters to masks, it's crucial to grasp the concept of a mask. In image editing, a mask is a grayscale image dictating the transparency of specific areas within an image. Masks enable selective application of filters, adjustments, or effects to particular parts of an image while leaving others unaffected.

Applying Smart Filters to Masks: When smart filters are applied to masks, they affect only the areas specified by the mask, offering precise control over the filter's impact. By manipulating the mask, users can modulate the intensity and extent of the filter's effect.

Please refer to the previous example and the method: [API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)