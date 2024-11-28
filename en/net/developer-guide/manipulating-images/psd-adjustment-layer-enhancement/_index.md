---
title: Using Adjustment Layer for PSD Enhancements
weight: 100
type: docs
description: Examples of using adjustment layers via Aspose.PSD for C#
keywords: [adjustment layer, photo enhance, curves adjustment, levels enhancement, invert, photo filter, psd api, C#, csharp, code sample]
url: net/adjustment-layer-enhancement/
---

## Overview

In this article, we will explore the editing of adjustment layers in Aspose.PSD for C#. Adjustment layers are a powerful feature in image editing that allow you to make non-destructive changes to your images. Aspose.PSD provides a comprehensive set of adjustment layer classes that you can use to modify various aspects of your images.

To demonstrate the editing of adjustment layers, we will use a sample code snippet at the end of the page that loads a PSD image and applies different adjustments to its layers.

In the code snippet below, we start by loading the PSD image using the `PsdImage.Load()` method. We then set up the options for saving the output PNG files. The `PngOptions` class allows us to specify the color type for the output image.

Next, we iterate through each layer in the PSD image and check its type using the `IsAssignable()` method. If the layer is of a specific type, we cast it to that type using the `Cast()` method and apply the desired adjustment. For example, we adjust the brightness and contrast of a `BrightnessContrastLayer`, modify the levels of a `LevelsLayer`, add a curve point to a `CurvesLayer`, and so on.

You can add additional code to apply other adjustments to their respective layers. Aspose.PSD provides a wide range of adjustment layer classes, such as [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), and more.

Finally, we save the modified image using the `Save()` method of the `PsdImage` class.

This code provides a basic overview of how to edit adjustment layers in Aspose.PSD for C#. You can customize the adjustments according to your requirements and explore the various options available in the API documentation.

## Example

Here’s a code sample demonstrating how to use adjustment layers using Aspose.PSD for C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

For more detailed information and examples, please visit the [Aspose.PSD for C# documentation](https://docs.aspose.com/psd/net/).
