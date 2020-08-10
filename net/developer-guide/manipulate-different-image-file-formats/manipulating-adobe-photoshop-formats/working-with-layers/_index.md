---
title: Working with Layers
type: docs
weight: 150
url: /net/working-with-layers/
---

## **Create a Layer Group**
A layer group consists of one or more layers and it helps to organize similar or related layers. Using Aspose.PSD for .NET you can create a layer group. For this purpose, a new method [**AddLayerGroup**](https://apireference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup)** **has been added in a **[PsdImage ](https://apireference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)**class to adds the layer group**.** 

** 

The steps to create layer groups are as simple as below:

- Create an instance of an image using the PsdImage class with specified width, height and image options.
- Create a [**LayerGroup** ](https://apireference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup)with the specified group name and index.
- Create an instance of the Layer class and assign the PSD image to it.
- Add the created layer to the layer group using the AddLayer method exposed by LayerGroup class
- Save the results.

The following code snippet shows you how to create a layer group.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Rename a Layer**
You can use any name that you would like, but the typical practice is to use a general description of the object or element that is on that layer. This article demonstrates how you can change the name of a layer using Aspose.PSD for .NET. For this purpose, a new property **DisplayName** has been added in Layer class to display a layer name properly. It has been observed that when Photoshop saves a layer name using the **Name** property, then Korean characters are stored as byte 63'?' in ASCII. So, if you want to display a layer name properly then use the **DisplayName** property because the **Name** property does not support Korean characters.

The following code sample shows how you can rename a layer.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **Support of Linked Layers**
Linking layers is like grouping the layers. If you are linking two or more layers then It will allow you to make certain changes to both of the linked layers. For example, if you apply transformations to one layer then it will be applied to all other linked layers. This article demonstrates how you can get and unlink linked layers using [Aspose.PSD](https://products.aspose.com/psd).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}



