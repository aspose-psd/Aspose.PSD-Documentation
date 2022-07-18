---
title: PSD Layer
type: docs
weight: 70
url: /net/psd-layer/
---

## **Overview**
Adobe® Photoshop® PSD Layer is one of the best concepts in graphics processing. Layers contain information about pixels, can have a different count of channels.

One of the most important parts of Layer in Photoshop Document is Layer Resources. You get the full list of supported [Layer Resources](/psd/net/list-of-psd-layer-resources/) in PSD from our documentation.

You can find UI to manipulate the layer on the following screenshot:

![todo:image_alt_text](psd-layer_1.png)

But Aspose.PSD specializes on programmatic manipulation of PSD Layer via [C# ](/psd/net/home/)and [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Additional documentation can be found in this Article: [Manipulating Images](/psd/net/manipulating-images-html/). All manipulation can be processed to PSD Preview and Layer, you find more info in[Aspose.PSD Raster Image API Reference](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
## **Available PSD Layer API**
- Layer Effects
- Layers common properties
- Layer Metadata
## **Examples of Layer Editing via C#**
### **Adding of new Layer**
If you want to add an empty Layer to opened [PSD File](/psd/net/psd-file/) you can use the following code.

Add new Layer to PSD File using API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}
### **Adding of new Layer from Jpeg, Png, Gif, Ai, Tiff, Bmp files**
Files of any [supported formats ](/psd/net/supported-file-formats/)can be added as a new layer to your image. But you can't load it directly.

You can the code below to add new PSD Layer from the file of any supported format from the stream

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
### **Flatten all layers or layer groups**
It can be useful if you don't want to give an editable PSD file to your users. Also, you can identify through API if the file was flattened.

Layer Flattening of PSD File:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
