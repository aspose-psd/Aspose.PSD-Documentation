---
title: Working With Text Layers
type: docs
weight: 170
url: /net/working-with-text-layers/
---

## **Add Text Layer**
Aspose.PSD for .NET allows you to add text layer in a PSD file. The steps to add text layer in a PSD file are as simple as below:

- Load a PSD file as an image using the factory method [**Load**](https://apireference.aspose.com/psd/net/aspose.psd/image/methods/load/index) exposed by [Image class](https://apireference.aspose.com/psd/net/aspose.psd/image)
- Call the [**AddTextLayer**](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/methods/addtextlayer) method that accepts text and an instance of the [**Rectangle**](https://apireference.aspose.com/psd/net/aspose.psd/rectangle) class
- Save the results

The following code snippet shows you how to add text layer in a PSD file

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}

## **Set Text Layer Position**
Aspose.PSD for .NET allows you to set a text layer position in a PSD file. The steps to set text layer position in a PSD file are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class
- Call the AddTextLayer method while specifying left and top positions of the text layer
- Save the results

The following code snippet shows you how to set text layer position in a PSD file

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}
## **Get Text Properties from a Text Layer**
Using Aspose.PSD for .NET, you can get and update the text properties of different portions of text available in PSD text layer. This article demonstrates how you can get Paragraphs, Styles and Text properties of the text layer and update them.

The code snippet below shows how to accomplish this requirement.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


Here is another example that demonstrates how a developer can get the text formatting of different text portions from [TextLayer ](https://apireference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer)using [Aspose.PSD for .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}
## **Update Text Layer In PSD File**
Aspose.PSD for .NET allows you to manipulate the text in the text layer of a PSD file. Please use the Aspose.PSD.FileFormats.Psd.Layers.TextLayer class to update text in the PSD layer. The following code snippet loads a PSD file, access the text layer, update the text and save the PSD file with a new name using [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) method.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Support of Text Layers on Runtime**
This article shows how to add text layers on runtime for PSD images. The code snippet has been provided below.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
