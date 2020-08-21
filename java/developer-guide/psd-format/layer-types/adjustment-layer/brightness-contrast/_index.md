---
title: Brightness Contrast Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/brightness-contrast/
---

# Working with Photoshop Brightness/Contrast adjustment layer in Java

In this article we will apply Brightness/Contrast adjustment to an Adobe® Photoshop® document using Aspose.PSD for Java® library. Also, we will learn more about the library features related to this kind of adjustment layer down the road.

But first a bit of theory.

The Brightness/Contrast adjustment layer changes brightness and contrast of the image. But wait a minute, what it actually means? Increasing brightness lightens color value up to white and decreasing brightness darkens the color value down to black. Increasing contrast in turn will increase the difference between light and dark colors and decreasing contrast will decrease that difference respectively; it means that light colors are getting lighter and dark colors are getting darker.

## The color mode support

The library allows to add Brightness/Contrast adjustment layer to images in RGB, CMYK or Lab color mode.

## The current and legacy behavior

The current library implementation (v20.6 on the moment of writing) uses default Photoshop algorithm that preserves the full tonal range from the shadows to highlights, but it doesn&#39;t yet support legacy behavior. It means that the library supports Brightness/Contrast adjustment layer in documents made in latest versions of Photoshop (CS4 and higher). However, you can [request legacy implementation of the Brightness/Contrast adjustment layer](https://forum.aspose.com/c/psd) on our forum if you need it.

## Adjust brightness and contrast

Now let us describe how the high-level API of Brightness/Contrast adjustment layer work (looking ahead, the API is straightforward). The PsdImage class contains a factory method (addBrightnessContrastAdjustmentLayer) for instantiating the BrightnessContrastLayer class that is the gateway for brightness and contrast adjustment. The BrightnessContrastLayer class just contains a pair of getters and setters for accessing brightness and contrast properties as well as changing their values.

![|Brightness/Contrast Adjustment Layer Example in PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

So, let us take an image of a dog (b), for example, to adjust its brightness1 and contrast2 (a), using only the factory method with corresponding arguments, to eventually get an image (c) that looks more vivid:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Notes:

1. The value of brightness must be in range from -150 to 150.
2. The value of contrast must be in range from -50 to 100.

Refer to the documentation of [BrightnessContrastLayer](https://apireference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) for more details.

## Conclusion

In this article we have got a quick overview of Brightness/Contrast adjustment layer and learnt how to adjust brightness and contrast of the image using the factory method.

Refer to our series of [articles on adjustment layer APIs](/psd/java/layer-types/adjustment-layer/) of Aspose.PSD for Javato learn more.