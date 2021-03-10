---
title: Rendering of Rotated Text Layers
type: docs
weight: 40
url: /net/rendering-of-rotated-text-layers/
---

## **Rendering of Rotated Text Layers**
Aspose.PSD provides the feature of rendering of rotated Text layers. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Now call the [Save](https://apireference.aspose.com/psd/net/aspose.psd/image/methods/save/index) method of the [PsdImage](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) instance.

The following code snippet shows you how to render rotated [Text layer](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)s.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}
## **Rotate Vector Mask and Text Layers**
Aspose.PSD provides the feature to rotate Vector Mask and Text layers. Aspose.PSD has exposed the RotateFlip method to rotate Vector Mask and Text layers. The steps to rotate the layers are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Set required [RotateFlipType](https://apireference.aspose.com/psd/net/aspose.psd/rotatefliptype).
- Call [RotateFlip](https://apireference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip) method
- Save the results.

The following code snippet shows you how to rotate Vector Mask and Text layers.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
