---
title: Black and White Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/levels/
---

## Working with Photoshop Levels adjustment layer in Java

In this article we will learn how to adjust tonal range and color balance of a photo in [PSD file format](/psd/java/psd-format/) programmatically in Java. We do not use Adobe® Photoshop® photo editor itself. Instead, we use the library Aspose.PSD for Java that works on its own to manipulate the Photoshop document.

Although, Aspose.PSD for Java supports more than enough [tools to edit the photo](/psd/java/manipulating-images/) as we want, let us **go with Levels adjustment layer API** that is one of the simplest and quickest ways to do the work.

## API overview

The current implementation (20.6 on the moment of writing) of Levels adjustment layer API **supports all base features of Photoshop Levels** , namely, adjusting input and output Levels for the composite channel (RGB) as well as for each primary color channel (red, green and blue).

The API of Levels adjustment layer is straightforward. The class [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) is an entry point to Levels adjustment. It contains a couple of methods to access color channels: getMasterChannel and getChannel(int). Both methods return [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) that has corresponding properties for manipulation of input and output Levels. The difference is that getMasterChannel serves to adjust composite color channel (RGB) whereas getChannel access particular color channel (red, green or blue) by its index.

## Compatibility with color modes

It is worth adding that Levels adjustment layer **is compatible with the vast majority of color modes** according to Photoshop Levels. Therefore, it is possible to adjust Levels for images in Grayscale (gray channel), RGB (RGB, red, green and blue channels), CMYK (CMYK, cyan, magenta, yellow and black channels), Duotone (monotone channel) and LAB (lightness, a and b channels) color modes.

## Adjust tonal range

Put simply, the tonal correction applies to an image to remap the shadows and the highlights for better distribution of midtones. Generally, **it makes the image look more contrast** , if done correctly. For example, let us take a photo of a dog (b) and adjust its tonal range (a – the screenshot is captured from Photoshop Levels window for clarity) to make the photo look more contrast (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levels Layer Figure 1](levels-adjustment-figure-1.png)|

To **adjust the overall tonal range** of an image, input Levels of the master channel should be set:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

It&#39;s needed to keep in mind that input Levels should be in range from 0 to 253 for shadows, from 9.99 to 0.01 for midtones and from 2 to 255 for highlights. The range of output Levels must be between 0 and 255.

Need even more examples? You can find them on [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) and in [knowledge base](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusion

To summarize, Aspose.PSD for Java has handy and simple API for changing tonal range and color balance of an image that is compatible with almost all color modes. The Levels adjustment layer API of the library looks similar to Photoshop Levels, therefore, it&#39;s easy to get started even if you have never worked with the library before.