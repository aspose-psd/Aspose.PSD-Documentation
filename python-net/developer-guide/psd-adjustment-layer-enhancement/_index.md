---
title: Using Adjustment Layer for PSD Enhancements
weight: 100
type: docs
description: Examples of using adjustment layer via Aspose.PSD for Python
keywords: [adjustment layer, photo enhance, curves adjustment, levels enhancement, invert, photo filter,  psd api, python, code sample]
url: python-net/pixel-data-manipulation/
---

## **Overview**

In this article, we will explore the editing of adjustment layers in Aspose.PSD for Python. Adjustment layers are a powerful feature in image editing that allow you to make non-destructive changes to your images. Aspose.PSD provides a comprehensive set of adjustment layer classes that you can use to modify various aspects of your images.

To demonstrate the editing of adjustment layers, we will use a sample code snippet at the end of page that loads a PSD image and applies different adjustments to its layers. 

In the below code snippet, we start by loading the PSD image using the PsdImage.load() method. We then set up the options for saving the output PNG files. The PngOptions class allows us to specify the color type for the output image.

Next, we iterate through each layer in the PSD image and check its type using the is_assignable() method. If the layer is of a specific type, we cast it to that type using the cast() method and apply the desired adjustment. For example, we adjust the brightness and contrast of a BrightnessContrastLayer, modify the levels of a LevelsLayer, add a curve point to a CurvesLayer, and so on.

You can add additional code to apply other adjustments to their respective layers. Aspose.PSD provides a wide range of adjustment layer classes, such as [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), and more.

Finally, we save the modified image using the save() method of the PsdImage class.

This code provides a basic overview of how to edit adjustment layers in Aspose.PSD for Python. You can customize the adjustments according to your requirements and explore the various options available in the API documentation.

Please check full example.

## **Example**
	{{< gist "dimsa" "27582839af6d67e3ae92f72877437250" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}