---
title: Channel Mixer Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/channel-mixer/
---

# Working with Photoshop Channel Mixer adjustment layer in Java

Today we are going to look how to mix channel colors in Photoshop documents programmatically in Java. Since Photoshop editor does not support Java scripting, we will use special PSD file format manipulation library called Aspose.PSD for Java.

The library contains **API to work with color channels**. There are several ways how to mix colors but, in this article, we will focus on Channel Mixer adjustment layer.

The Channel Mixer adjustment layer API **allows playing with color channels** to make tinned images or create different creative color effects or even convert the image to black and white one. Next, we consider how to apply Channel Mixer adjustment to an existing Photoshop document using Aspose.PSD for Java but first we need to talk about overall API features.

## API overview

There is nothing special in creation of Channel Mixer adjustment layer. It can be added through [the default factory method](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) which return an instance of the ChannelMixerLayer class. This class contains general functionality like Monochrome option and a method for getting an output channel. A particular output channel can be one of two types: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) or [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). The type of [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) depends on [the color mode](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) of the image.

## Make the image monochrome

Now, let us consider and example of applying Channel Mixer adjustment layer to an existing Photoshop document. Since this kind of adjustment layer does not support presets yet, we will **recreate the Black &amp; White Infrared (RGB) Photoshop preset** (a). The preset will be applied to the image of a blooming tree (b). As a result, we want to achieve the effect of infrared photography (c).

![Channel Mixel Adjustment Layer Example](channel-mixer-adjustment-psd-layer-figure-1.png) First, to recreate the Black &amp; White Infrared (RGB) Photoshop preset it is necessary to enable the monochrome flag and set appropriate raw values for each color (red, green and blue) for the Gray output channel:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

The image must be in RGB color mode to make the code work (because of cast to the RgbMixerChannel class). CMYK color mode is also supported but only for images with the corresponding color mode.

Keep in mind that value of each color as well as Constant property must be in range from -200 to 200.

## Conclusion

In this article we considered how to work with Channel Mixer API of Aspose.PSD for Java to adjust colors in color channels as well as convert the image to black and white.