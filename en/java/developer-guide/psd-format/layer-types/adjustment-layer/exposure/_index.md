---
title: Exposure Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/exposure/
---

# Working with Photoshop Exposure adjustment layer in Java

In this article we are going to add Exposure adjustment layer into Adobe® Photoshop® document using Aspose.PSD for Java – PSD file format manipulation library. The library works without installed Photoshop editor because it uses own image processing algorithms. We have also learnt some details related to the library exposure adjustment API.

## API overview

The Exposure adjustment layer configures through the [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) class that contains the following properties to work with exposure adjustment:

- It defines how much light the photo has by squeezing or stretching the whole histogram relative to the blacks. So, it affects mainly highlights.
- Unlike exposure offset affects mainly shadows.
- Gamma correction. It corrects image luminance.

## Correct exposure

Correcting exposure and related properties are as simple as changing a few properties of the class. Let us apply some exposure adjustment (a) to an underexposured photo of a library (b) to make it perceivable to the human eye (c).

![Exposure Adjustment Layer Example](exposure-adjustment-layer-figure-1.png)

The whole adjustment is made mainly using gamma correction. However, exposure and offset are also adjusted a little. All you need to do is to set appropriate values to already mentioned properties:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Pay attention that exposure must be in range from -20.0 to 20.0, offset value must be in range from -0.5 to 0.5 and the range of value of gamma correction must be between 9.99 and 0.01.

Refer to [API reference of Exposure adjustment layer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) for more details.

## Conclusion

In this article we have learnt how to add Exposure adjustment layer into a PSD file to lighten the image as well as considered some API details.