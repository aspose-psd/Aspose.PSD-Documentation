---
title: Editing raster layer masks in PSD file via API
type: docs
weight: 20
url: /net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **Overview**
**To automate PSD format editing and change PSD file without Adobe® Photoshop® you can use the Aspose.PSD API provided below. There are C# and .NET code snippets that can help you to modify PSD files.**

Using PSD Layer and Vector Masks we are able to hide and show layer pixels without permanently deleting them. Raster masks are also called a layer mask or user mask. Access to both raster and vector masks in Aspose.PSD is provided through the [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) layer property which can be an instance of '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' and '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' classes that are child classes of abstract 'LayerMaskData' class. If a layer has both raster and vector masks then [LayerMaskDataFull ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)instance is provided. If a layer has only a raster or a vector mask then [LayerMaskDataShort ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)instance is provided. If the LayerMaskData property is null then the layer has no masks or only a disabled vector mask.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>A raster mask and a disabled vector mask LayerMaskDataShort</p><p>A disabled raster mask  LayerMaskDataShort</p><p>A raster mask and a vector mask  LayerMaskDataFull</p><p>A raster mask  LayerMaskDataShort</p><p>A vector mask  LayerMaskDataShort</p><p>A disabled vector mask null (But vector resource is present)</p>|
| :- | :- |
## **How to get a layer raster mask in the PSD file?**
At first, we should find out if a layer has both vector and layer masks:

Below provided sample code demonstrates how to get a layer raster mask

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Otherwise, type of the LayerMaskData layer property is LayerMaskDataShort. In this case, let’s check if the layer has only a raster mask by checking the Flags property. It should not contain [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData** flag, otherwise the mask is a vector mask cache**.**

Getting mask code snippet:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

If you need to **extract a raster mask** as LayerMaskDataShort (for further manipulations) even when both masks present, the LayerMaskDataFull should be extracted and converted to LayerMaskDataShort. The following code can be used for both cases:

Extracting a raster mask from PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **How to check if a layer in the PSD file has a raster mask?**
The following C# code may help you to check if a layer has a raster mask:

How to know if raster mask applied to [PSD Layer](/psd/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **How to remove / add / update a layer raster mask in the PSD file?**
Just removing / adding / updating the LayerMaskData is not enough for correct saving because channels are not updated; though it may provide correct rendering. This does not change the mask channels:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

We should use the layer AddLayerMask method for removing / adding / updating.

This adds/updates both the mask and channels:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

This removes both the mask and channels:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Removing a layer raster mask in the PSD image**
Firstly, we check if the mask is in the short format and if it not vector one we can just call the AddLayerMask method with null to delete the raster mask. But if it is in the full format we have to convert it to a short format thus leaving the vector mask only. For removing a layer mask this following C# .NET code snippet can be used:

Code snippet how to remove Layer Mask from PSD File.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Updating a layer raster mask in the PSD image**
This is straightforward:  if the mask is in the short format we have to change ImageData and MaskRectangle if need, otherwise [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)and [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)should be changed. The following C# .NET code snippet can be used for updating a layer mask:

Update PSD Layer Mask with C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Here is an example of possible actions that change a raster mask. This one inverts a layer user mask:

Update PSD Layer Mask with C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Updating a vector mask in the PSD file when a layer raster mask is present**
It is supposed that a user has already changed a vector path resource. Then it can update the vector mask simply by calling the [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask)layer method:

Update [PSD Layer Vector Mask ](/psd/net/layer-vector-mask/)with C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Adding a layer raster mask in the PSD file**
If a layer has no mask we can add the given raster mask simply by calling the AddLayerMask layer method.

If the mask has no [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags)flag then it already has a raster mask and we have to update it as described above. Otherwise, if this mask is in a short format we convert it to the full format. If not we use it as is. Then update UserMaskData, UserMaskRectangle, and other properties with the given mask properties. The following C# .NET code snippet can be used for adding (updating) a layer mask:

Add new Layer Mask to PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **How to check if a layer mask is enabled?**
To find out layer raster mask enabled state we can check LayerMaskFlags.Disabled flag state in the Flags property for LayerMaskDataShort or in the RealFlags for LayerMaskDataFull. The following C# .NET code snippet can be used for getting a layer mask enabled state:

Check if a mask is enabled:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **How to enable or disable a raster layer mask?**
To enable or disable a layer raster mask we can change the LayerMaskFlags.Disabled flag state in the Flags property for LayerMaskDataShort or in the RealFlags for LayerMaskDataFull. The following C# .NET code snippet can be used for changing a layer mask enabled state:

Enable or disable Raster Layer Mask:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}

