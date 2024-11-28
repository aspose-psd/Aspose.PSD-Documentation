---
title: Support of Fill Layers
type: docs
weight: 50
url: /java/support-of-fill-layers/
---


## **Support of Fill Layers With Color Fill**
This article demonstrates how to fill PSD layer with Color. Please use the Aspose.PSD.FileFormats.Psd.Layers.FillLayer to add Color in PSD layer. The following code snippets loads a PSD file, access the Filllayer class and sets the color using the FillLayer.FillSettings property.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Support of Fill Layers With Gradient Fill**
This article demonstrates the usage of Gradient fill to fill PSD layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the GradientColorPoint and GradientTransparencyPoint classes to add Gradient effect into a layer.

` `The steps to fill PSD layer with Gradient fill are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Set settings properties of FillLayer object.
- Create list of ColorPoints with required colors and position of color.
- Create list of transparencyPoints with required opacity and position of transparency point.
- Call the FillLayer.Update method
- Save the results.



The following code snippet shows you how to add Gradient fill to fill PSD layer.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Stroke Effect With Color Fill**
This article demonstrates how to render stroke effect with color fill. The Stroke effect is used to add strokes and borders to layers and shapes. It can be used to create solid-color lines, colorful gradients, as well as patterned borders.

The steps to render Stroke effect with Color fill are as simple as below:

- Set **LoadEffectsResource** property.
- Load a PSD file as an image using the factory method Load exposed by Image class and define **PsdLoadOptions**.
- Set settings properties of **ColorFillSetting.**
- Save the results.

The following code snippet shows you how to render Stroke effect with Color fill.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}






