---
title: Support of Fill Layers
type: docs
weight: 90
url: /net/support-of-fill-layers/
---


## **Fill Layers With Pattern Fill**
This article demonstrates how to fill the [PSD ](https://wiki.fileformat.com/image/psd/)layer with the Pattern fill. A Pattern* *is an image, color, shadow or line that is used to fill an area of an image. Please use the Aspose.PSD.FileFormats.Psd.Layers.FillLayer to add Pattern in the PSD layer. The following code snippets load a PSD file, access the [Filllayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)class and sets the Pattern using the [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) properties.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



Here is another example which demonstrates how [Aspose.PSD](https://products.aspose.com/psd/net) renders the pattern by using [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)and [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings)[ ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Fill Layers With Gradient Fill**
This article demonstrates the usage of Gradient fill to fill the PSD layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) and [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) classes to add a Gradient effect into a layer.

` `The steps to fill [the PSD ](https://wiki.fileformat.com/image/psd/)layer with a Gradient fill are as simple as below:

- Load a PSD file as an image using the factory method [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) exposed by [Image](https://reference.aspose.com/net/psd/aspose.psd/image) class.
- Set settings properties of [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) object.
- Create a list of [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) with required colors and positions of color.
- Create a list of transparency points with required opacity and position of transparency point.
- Call the [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) method
- Save the results.



The following code snippet shows you how to add Gradient fill to fill PSD layer.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



Here is another example which uses a [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** **property to fill PSD layer with Gradient fill. Aspose.PSD supports the following gradient types through the GradientType enumeration:

- **GradientType.Linear:**       In a linear gradient, the color transitions from the starting hue to end in a straight line.** 
- **GradientType.Radial:**       In a radial gradient, the colors fan out from the starting point in a circular pattern.
- **GradientType.Angle:**        An angle gradient sweeps counterclockwise around the starting point.
- **GradientType.Reflected:** In a reflected gradient, the color is mirrored on both sides of the starting point.
- **GradientType.Diamond:**   Diamond gradient creates a diamond shape from the starting point.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Support of Scale Property for Gradient Fill Layer**
This article demonstrates how to scale FillLayer with gradient fill using Aspose.PSD for .NET. For this purpose, a new property [**Scale**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) has been added in [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)**.** 

Following is the code demonstration that shows how to use **Scale** property.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Fill Layers With Color Fill**
This article demonstrates how to fill [PSD](https://wiki.fileformat.com/image/psd/) layer with Color. Please use the [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) class to add Color in PSD layer. The following code snippet loads a PSD file, access the Fill layer class and sets the color using the [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) property.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}







