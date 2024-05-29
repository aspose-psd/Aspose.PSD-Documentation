---
title: Smart Filter Manipulation in Aspose.PSD for Python
weight: 100
type: docs
description: Examples of how to use Smart Filters in PSD File
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, python, code sample]
url: python-net/smart-filters/
---

## **Overview**

There are 3 ways to apply smart filters in Aspose.PSD for Python.

## **Direct Filter Applying**
In this code sample, we can see an example of how to directly apply smart filters in Aspose.PSD for Python.

First, the code specifies the source PSD file, the output file for the original image, and the output file for the updated image.

Next, the code loads the PSD image using the Image.load() method and casts it to a PsdImage object.

The original image is then saved using the save() method, with the output file name specified.

A SharpenSmartFilter object is created, which represents the smart filter to be applied.

The code then retrieves the regular layer from the PSD image using im.layers[1].

A loop is then used to apply the sharpenFilter to the regular layer three times.

Finally, the updated image is saved using the save() method and the output file name specified.

This code demonstrates how to directly apply smart filters in Aspose.PSD for Python. By using the appropriate filter objects and applying them to the desired layers, you can achieve the desired effects on your images.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipulation Smart Filters in The Smart Objects**

First, the code specifies the source PSD file, the output file for the original image, and the output file for the updated image.

The PSD image is loaded using the Image.load() method, and then cast to a PsdImage object.

The original image is saved using the save() method, with the output file name specified.

The code then casts the second layer of the PSD image to a SmartObjectLayer object, representing the smart object layer.

The code then proceeds to edit the smart filters. In this example, it demonstrates how to work with two types of smart filters: GaussianBlurSmartFilter and AddNoiseSmartFilter.

For the GaussianBlurSmartFilter, the code updates the filter values, including the radius, blend mode, opacity, and whether it is enabled or not.

For the AddNoiseSmartFilter, the code sets the noise distribution to NoiseDistribution.UNIFORM.

Next, the code adds two new filter items to the smart object layer: another GaussianBlurSmartFilter and an AddNoiseSmartFilter.

After adding the new filters, the code applies the changes using the update_resource_values() method.

Finally, the code demonstrates how to directly apply the filters to the layer and to the mask of the layer using the apply() and apply_to_mask() methods, respectively.

The updated image is then saved using the save() method and the output file name specified.

By following this code sample, you can learn how to work with smart filters in Aspose.PSD for Python. The library provides a wide range of smart filters, each with its own set of properties and methods that can be customized to achieve the desired effects on your images.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Applying Smart Filters to Layer Mask**

Applying Smart Filters to Masks: A Powerful Image Editing Technique

Smart filters are a popular feature in image editing software that allow users to apply various filters and effects to their images. One interesting technique that can be achieved using smart filters is applying them to masks. In this article, we will explore how to apply smart filters to masks and discuss their usage in the world of image editing.

What is a Mask? Before we delve into applying smart filters to masks, let's first understand what a mask is. In image editing, a mask is a grayscale image that determines the transparency of certain areas of an image. A mask can be used to selectively apply filters, adjustments, or effects to specific parts of an image, while leaving other areas unchanged.

Applying Smart Filters to Masks: When applying smart filters to masks, the filters are only applied to the areas specified by the mask. This allows for precise control over which parts of the image are affected by the filter. By manipulating the mask, you can determine the intensity and extent of the filter's effect.

Please check previous example and the method: [API Reference Applying Smart Filter To Mask](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)