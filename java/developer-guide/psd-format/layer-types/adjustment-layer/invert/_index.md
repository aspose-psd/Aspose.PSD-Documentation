---
title: Invert Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/invert/
---

# Working with Photoshop Invert adjustment layer in Java

In this article we are going to show how to turn image in Photoshop document to negative one programmatically in Java. For this purpose, we will use the library for PSD file format manipulation called Aspose.PSD for Java.

The color inversion API allows to **add a negative effect to an image**. You may already saw how to [invert image colors using Curves adjustment layer](/psd/java/layer-types/adjustment-layer/curves/). However, today we will consider a faster and easier way to do the job the Invert adjustment layer.

## API overview

**The Invert adjustment layer API** consists of the layer class itself that is [InvertAdjustmentLayer](https://apireference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). This class does not have own public members, since it inherits all public members from the parent class ([AdjustmentLayer](https://apireference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). This fact simplifies its usage because all you need to do is to add it to a PSD file and the image becomes negative.

## Invert image colors

So, even if it seems obvious but let us demonstrate for clarity how to **apply Invert adjustment layer to the image** of an astronaut (a) to make the negative effect for that image (b).

![Invert Adjustment Layer Example Before and After](invert-adjustment-layer-figure-1.png)

To **invert colors of the image** just add an Invert adjustment layer into PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

That&#39;s it! There are no specific properties to configure for this type of adjustment layer.

## Conclusion

In this article we learned about Invert adjustment layer API of Aspose.PSD for Java. It is an effortless tool for getting negative images because API of this adjustment layer does not declare any public members.