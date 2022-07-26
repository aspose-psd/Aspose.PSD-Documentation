---
title: Photo Filter Adjustment Layer
type: docs
weight: 30
url: /java/layer-types/adjustment-layer/photo-filter/
---

# Working with Photoshop Photo Filter adjustment layer in Java

Today we will see how to apply Photo Filter adjustment layer to an existing Photoshop document using Aspose.PSD for Java that is the library to manipulate PSD file format.

**The Photo Filter adjustment layer API** changes the color balance of the image using tinting. The result image will look the same as after using a real camera filter. Notice that the Photo Filter adjustment layer API of the library slightly differs from Photoshop one because there are no predefined filters yet. However, it is the same in all other respects. It means that you can set a color of the tint and change its intensity (density) as well as use Preserve Luminosity option.

## API overview

The Photo Filter adjustment layer API is fairly simple to use. There is the main [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) class that serves as entry point to this adjustment layer and contains only three public properties, namely, color, density and preserve luminosity by means of which the adjustment occurs.

## Adjust color balance

Since, there is not much to talk about, let us consider **an example of the color balance adjustment** using Photo Filter right away. We are going to add a warming filter (a) manually for the image of deer sculpture (b) to get the image in warm tones (c) that is more pleasant to look at.

![Photo Filter Adjustment Layer Example](photo-filter-adjustment-layer-figure-1.png)

First of all, notice that [the factory method](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) differs from ones for [other adjustment layers](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) because there is no default method (without arguments). Therefore, to add a Photo Filter adjustment layer into loaded Photoshop document a single argument is required that is [color](https://reference.aspose.com/psd/java/com.aspose.psd/Color). So, to recreate the warming filter effect just pass on orange as an argument to the factory method, then set density using corresponding setters:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

It worth adding that the Density property has default value that is 100 as well as true is default value for the Preserve Luminosity property (it is the reason why we do not explicitly enable this option).

## Conclusion

In this article we considered the usage of Photo Filter adjustment layer API of Aspose.PSD for Java. This tool is simple to use and allows to add a tint to an image with variable density. It is a quick way to adjust color balance of the whole image.