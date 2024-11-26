---
title: Smart Filter Manipulation in Aspose.PSD for С#
weight: 100
type: docs
description: Examples of how to use Smart Filters in PSD File
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, C#, csharp, code sample]
url: net/smart-filters/
---

## Overview

There are three ways to apply smart filters in Aspose.PSD for C#.

### Direct Filter Applying

This example demonstrates how to directly apply smart filters in Aspose.PSD for C#.

First, specify the source PSD file, the output file for the original image, and the output file for the updated image.

Next, load the PSD image using the `Image.Load` method and cast it to a `PsdImage` object.

Save the original image using the `Save` method with the specified output file name.

Create a `SharpenSmartFilter` object, representing the smart filter to be applied.

Retrieve the regular layer from the PSD image using `psdImage.Layers[1]`.

Apply the `sharpenFilter` to the regular layer three times in a loop.

Finally, save the updated image using the `Save` method with the specified output file name.

This code demonstrates how to directly apply smart filters in Aspose.PSD for C#. By using the appropriate filter objects and applying them to the desired layers, you can achieve the desired effects on your images.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulating Smart Filters in Smart Objects

This example shows how to manipulate smart filters within smart objects.

First, specify the source PSD file, the output file for the original image, and the output file for the updated image.

Load the PSD image using the `Image.Load` method and cast it to a `PsdImage` object.

Save the original image using the `Save` method with the specified output file name.

Cast the second layer of the PSD image to a `SmartObjectLayer` object.

Edit the smart filters. This example demonstrates working with `GaussianBlurSmartFilter` and `AddNoiseSmartFilter`.

For `GaussianBlurSmartFilter`, update the filter values including radius, blend mode, opacity, and enabled state.

For `AddNoiseSmartFilter`, set the noise distribution to `NoiseDistribution.UNIFORM`.

Add new filter items to the smart object layer: another `GaussianBlurSmartFilter` and `AddNoiseSmartFilter`.

Apply the changes using the `UpdateResourceValues` method.

Apply the filters directly to the layer and to the mask of the layer using the `Apply` and `ApplyToMask` methods respectively.

Save the updated image using the `Save` method with the specified output file name.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Applying Smart Filters to Layer Mask

Smart filters are a powerful image editing tool that allows users to apply various filters and effects. One interesting technique is applying them to masks, which can precisely control the areas affected by the filter.

A mask is a grayscale image determining the transparency of certain image areas, selectively applying filters, adjustments, or effects.

When applying smart filters to masks, filters are applied only to the areas specified by the mask. This precise control allows for manipulation of the filter's intensity and extent.

For more detailed information and examples, refer to the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).
