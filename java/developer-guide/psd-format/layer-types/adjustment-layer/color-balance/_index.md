---
title: Color Balance Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/color-balance/
---

# Working with Photoshop Color Balance adjustment layer in Java

In this article we are going to **adjust color balance of the image** in PSD file format in Java. We will use a special library called Aspose.PSD for Java that is a toolbox for manipulation of Photoshop documents.

Since the library works with PSD file format it contains almost [all features](https://docs.aspose.com/psd/java/features/) available in Photoshop editorand **Color Balance adjustment layer** , which is absolutely suitable for this task, is not an exception.

The Color Balance adjustment layer makes it possible to change the balance between primary (RGB) and subtractive (CMY) colors for shadows, midtones and highlights in simple and fast way.

## Adjust Color Balance

As mentioned earlier Color Balance adjustment layer in Aspose.PSD for Java is just what it is **a balancer between primary and subtractive colors**. It means that there three scales for each color pair (cyan/red, magenta/green, yellow/blue). The intensity of particular color in the pair will increase if the value moves toward it and vice versa. Furthermore, those three pairs inherent to each area of the tonal range (shadows, midtones and highlights) that increases flexibility of this kind of adjustment.

So, let us apply this knowledge in practice. For an example we choose a reddish photo of a woman&#39;s face (b). The face is so reddish and we are going to fix that by **adding Color Balance adjustment layer** to decrease red and increase cyan basically (a) to get the face that looks more naturally (c). Again, there is a lot of work to do with this image but within this article it is all what we will do.

![Color Balance adjustment layer example](color-balance-adjustment-layer-example-figure-1.png) The API of Color Balance adjustment layer has flat design. Therefore, the [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) class that is all you need. First of all,preserve luminosity because it is disabled by default. After, add a bit of green and a more yellow for shadows using corresponding methods (names of which consists of the particular tonal range area name and color names in the color pair), then add more cyan and a little of blue for midtones, and finally addmore cyan besides a little of magenta and blue:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

Now, we have got the picture we wanted! It is so simple, is not it?

Pay attention that _the value of each color pair must be in range from -100 to 100_ that is negative values for subtractive colors and positive for primary colors respectively, just like in Photoshop editor.

Refer to our API reference to get to know more technical details about [Color Balance adjustment layer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer).

## Conclusion

In this article we have considered how to adjust Color Balance of the image programmatically in Java using the library Aspose.PSD for Java. The library contains fully-featured API to work with Color Balance adjustment layers in Photoshop documents.