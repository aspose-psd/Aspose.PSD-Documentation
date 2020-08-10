---
title: Using PSD files as templates for automation - Business Cards Case
type: docs
weight: 10
url: /net/using-psd-files-as-templates-for-automation-business-cards-case/
---

### **Overview**
This article describes often used cases when you need to update some layers In [PSD File](https://wiki.fileformat.com/image/psd/) programmatically, where the PSD/PSB file has some known template-like structure. This can be used to create a big amount of Business Cards for different people (Business Cards Case). Or you need to make a translation of the PSD file to different languages with the replacement of some graphic material in it.

After reading this article you will know how you can make this:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_1.png)
### **Simple case**
For example, you have some PSD Template with the known Layer Names. So you need to change, update or replace PSD Layer via C#. Firstly you need to open the template file with Aspose.PSD.

How to open PSD File via C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-1.cs" >}}

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_2.png)



Then we new need to find a layer that we want to replace by its name. Here is a simple implementation for this.

How to find the layer in PSD file by its name

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-2.cs" >}}



When the layer is found, we can update it in a common way, using [Graphics](https://apireference.aspose.com/psd/net/aspose.psd/graphics):

How to Draw on the PSD layer Graphics

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-3.cs" >}}

In this case, we draw a newly loaded [PNG image](https://wiki.fileformat.com/image/png/) on the existing PSD layer, so the old data will be lost in the new file.

But what if we also need to update text? The process will be similar. Find [Text Layer](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) by its name then we programmatically [update the Text Layer of Photoshop File](/psd/net/render-text-with-different-colors-in-text-layer/).

How to update Text Layer in Photoshop using C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-4.cs" >}}



At the end we need to save our changes:

How to save changed PSD file using [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-5.cs" >}}



The resulting image:

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_3.png)


### **A complex case with additional features**
Above we showed the most simple way to replace image in a layer of PSD File.

But Aspose.PSD can offer more complex additional features like adding a new layer, removing old layers, and update of text layer using different styles in multi-line text.

We can find [Layer ](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer)that we want to replace, then we find its index in Layers List, remove him and insert a new Layer after the creation of it from [Jpeg File](https://wiki.fileformat.com/image/jpeg/) to the same place.

Create a new layer from file and insert it to PSD Image using [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-6.cs" >}}



At the end of this file code snippet, we correct the layer position and save new Layers’ array to Psd Image.

How to copy [PsdImage ](https://apireference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)Layer properties

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-7.cs" >}}



And after all, we need to update text layers in the existing PSD image by C#. Aspose.PSD supports[updating of TextLayer by Portions](/psd/net/working-with-text-layers/). Each [text portion](https://apireference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) has a unique combination of Style and Paragraph properties.

How to copy [PsdImage ](https://apireference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage)Layer properties

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-PsdFileAsATemplate-Snippet-8.cs" >}}



As a result, we have changed the PSD template via code with a new Layer from Jpeg, Png, J2k, Bmp, Gif, or Tiff file and multi-line [text with different styles](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-modifyingandconvertingimages-psd-renderingofdifferentstylesinonetextlayer-renderingofdifferentstylesinonetextlayer-cs) in each row.

![todo:image_alt_text](using-psd-files-as-templates-for-automation-business-cards-case_4.png)
