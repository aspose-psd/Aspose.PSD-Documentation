---
title: Manipulating Adobe Photoshop Formats
type: docs
weight: 20
url: /net/manipulating-adobe-photoshop-formats/
---

## **Merge PSD layers into Other layers**

## **Exporting Image to PSD**
PSD, PhotoShop document, is the default file format used by Adobe Photoshop for working with images. Aspose.PSD allows you to load, edit and save files to PSD so that they can be opened and edited in PhotoShop. This article shows how to save a file to PSD with Aspose.PSD, and it also discusses some of the settings that can be used when saving to this format. PsdOptions is a specialized class in the ImageOptions namespace used to export images to PSD. To export to PSD, create an instance of the Image class, either loaded from an existing image file (thumbnails for example) or created from scratch. This article explains how. In the examples below, an image is created from scratch. Once it is created and pixel data is populated, save the image using the Image class Save method, and supply a PsdOptions object as the second argument. Several of the PsdOptions class properties can be set for advanced conversion. Some of the properties are ColorMode, CompressionMethod and Version. Aspose.PSD supports the following compression methods through the CompressionMethod enumeration:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

The following color modes are supported through the ColorModes enumeration:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Additional resources can be added, such as thumbnail resources for PSD v4.0, v5.0 and higher, or grid and guide resources for PSD v4.0 and higher. The code below creates an Image file from scratch, populates the pixels and saves it to PSD with RLE compression and grayscale color mode. The following code snippet shows you how to export Image to PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Importing image to PSD layer**
This article demonstrates the usage of Aspose.PSD to add or import an image to a PSD layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the DrawImage method of the Layer class to add/import an image into a PSD file. DrawImage method needs location and image values to add/import an image into a PSD file. The steps to import an image into PSD layer are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Create an instance of Layer class from the stream with Png, Jpeg, Tiff, Gif, Bmp, Psd or j2k file
- Add Layer to Psd using AddLayer method
- Save the results.



The following code snippet shows you how to import the image to PSD layer.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Color replacement in PSD layers**
This article demonstrates the usage of Aspose.PSD to add or import an image to a PSD layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the DrawImage method of the Layer class to add/import an image into a PSD file. DrawImage method needs location and image values to add/import an image into a PSD file. The steps to import an image into PSD layer are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Create an instance of Layer class and assign the PSD image layer to it.
- Load the image that needs to be added or create a one from scratch.
- Call the Layer.DrawImage method while specifying location and image instance.
- Save the results.



The following code snippet shows you how to import image to PSD layer.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Creating Thumbnails from PSD Files**
PSD is the native document format of Adobe's Photoshop application. Adobe Photoshop (version 5.0 and later) stores thumbnail information for preview display in an image resource block that consists of an initial 28-byte header, followed by a JFIF thumbnail in RGB (red, green, blue) order. Aspose.PSD API provides an easy to use mechanism to access the resources of the PSD file. These resources also include the thumbnail resource that in turn can be fetched and saved to disc as per application needs. The following code snippet shows you how to create thumbnails from PSD Files.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Creating Indexed PSD Files**
Aspose.PSD for .NET API can create Indexed PSD files from scratch. This article demonstrates the use of PsdOptions and PsdImage classes to create an Indexed PSD while drawing some shapes over the newly created canvas. The following simple steps are required to create an Indexed PSD file.

- Create an instance of PsdOptions and set its source.
- Set ColorMode property of the PsdOptions to ColorModes.Indexed.
- Create a new palette of colors from RGB space and set it as Palette property of PsdOptions.
- Set CompressionMethod property to the required compression algorithm.
- Create a new PSD image by calling the PsdImage.Create method.
- Draw graphics or perform other operations as per requirement.
- Call PsdImage.Save method to commit all changes.



The following code snippet shows you how to create indexed PSD files.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Exporting PSD Layer to Raster Image**
Aspose.PSD for .NET allows you to export layers in a PSD file into raster images. Please use the Aspose.PSD.FileFormats.Psd.Layers.Layer.Save method to export the layer to the image. The following sample code loads a PSD file and exports each of its layers into a PNG image using Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Once all layers are exported into PNG images, you can open them using your favorite image viewer. The following code snippet shows you how to export PSD layer to a raster image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **Update Text Layer In PSD File**
Aspose.PSD for .NET allows you to manipulate the text in the text layer of a PSD file. Please use the Aspose.PSD.FileFormats.Psd.Layers.TextLayer class to update text in the PSD layer. The following code snippet loads a PSD file, access the text layer, update the text and save the PSD file with a new name using Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText method.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Detecting Flattened PSD**
Aspose.PSD for .NET allows you to detect whether a given PSD file is flattened or not. IsFlatten property has been introduced in the Aspose.PSD.FileFormats.Psd.PsdImage class to achieve this functionality. The following code snippet loads a PSD file and access the property IsFlatten.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **Merge PSD layers**
This article shows how to merge layers in a PSD file while converting a PSD file to JPG with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Once it is loaded, convert/cast the image to PsdImage. Create an instance of the JpegOptions class and set it various properties. Now call the Save method of the PsdImage instance. The following code snippet shows you how to merge PSD layers.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}
## **Grayscale Support With Alpha for PSD**
This article shows how to support Grayscale with alpha for PSD file while converting a PSD file to PNG with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Once it is loaded, convert/cast the image to PsdImage. Create an instance of the PngOptions class and set its various properties. Set the ColorType property to TruecolorWithAlpha. Now call the Save method of the PngOptions instance. The following code snippet shows you how to convert to Grayscale PNG with Alpha.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}
## **Support Layer Effects For PSD**
This article shows how support different effects like **Blur**, **Inner** **Glow**, **Outer Glow** for PSD layer. The following code snippet shows you how to support layer effects.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}
## **Support Layer Creation Date and Time**
This article shows how to support date and time layer creation for PSD layer. The following code snippet shows you how to create layers.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.cs" >}}
## **Support for Sheet Color High Lighting**
This article shows how to load PSD images than change and highlight sheet colors and save that as an image. The code snippet has been provided.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.cs" >}}
## **Support of Layer Mask**
This article shows how to support layer of mask for PSD images than save those images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerMask-SupportOfLayerMask.cs" >}}
## **Support of Layer Vector Mask**
This article shows Support of layer vector masks for Aspose.PSD. The following code snippet shows you how Aspose.PSD supports layer vector masks.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLayerVectorMask-SupportOfLayerVectorMask.cs" >}}
## **Support of Text Layers on Runtime**
This article shows how to add text layers on runtime for PSD images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
## **Support of Adjustment Layers**
This article shows how to adjust layers and then if layer is null than merge layer and save as PSD images. The code snippet has been provided below.

{{< gist "aspose-psd" "c68d1f8aa6f2af15b98e4d34e14a504a" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfAdjusmentLayers-SupportOfAdjusmentLayers.cs" >}}
## **Manage Brightness and Contrast in Adjustment Layers**
This article shows how to iterate through layers and manage brightness and contrast in layers and then save as PSD images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageBrightnessContrastAdjustmentLayer-ManageBrightnessContrastAdjustmentLayer.cs" >}}
## **Manage Exposure Layers**
This article shows how to add and edit exposure layers and manage exposure layers and then save as PSD images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageExposureAdjustmentLayer-ManageExposureAdjustmentLayer.cs" >}}
## **Manage Channel Mixer Adjust Layers**
This article shows how to manage adjustment layers and set different colors and then save as PSD images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManageChannelMixerAdjusmentLayer-ManageChannelMixerAdjusmentLayer.cs" >}}
## **Merge PSD layers into Other layers**
This article shows how to merge layers into other layers in a PSD file with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. Now call the Save method of the PsdImage instance. The following code snippet shows you how to merge PSD layers.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergeOnePSDlayerToOther-MergeOnePSDlayerToOther.cs" >}}
## **Support For TextBoundBox**
This article shows how to Support text bound box in a PSD file with Aspose.PSD. In the example below, an existing PSD file is loaded by passing the file path to the Image class static Load method. TextBoundBox is the maximum layer size for the Text layer. Now call the Save method of the PsdImage instance. The following code snippet shows you how to merge PSD layers.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-TextLayerBoundBox-TextLayerBoundBox.cs" >}}
## **Support For IOPA Resources**
This article shows how to Support Iopa resource in a PSD file with Aspose.PSD. The following code snippet shows you how to support Iopa in PSD layers.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddIopaResource-AddIopaResource.cs" >}}
## **Manage Opacity of Layers**
This article shows how to manage opacity of layers in a PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-FillOpacityOfLayers-FillOpacityOfLayers.cs" >}}
## **Rendering of Curves Adjustment Layers**
This article shows how to rendered curves adjust of layers in a PSD file and render them into PNG as well with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfCurvesAdjustmentLayer-RenderingOfCurvesAdjustmentLayer.cs" >}}
## **Add Curves Adjustment Layers**
This article shows how to add curves adjustment layers in a PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddCurvesAdjustmentLayer-AddCurvesAdjustmentLayer.cs" >}}
## **Support of Clipping Mask**
This article shows how to support clipping mask in a PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfClippingMask-SupportOfClippingMask.cs" >}}
## **Manager Photo Filter Adjustment Layer**
This article shows how to iterate through each photo filter layers and add and edit them and save them as PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManagePhotoFilterAdjustmentLayer-ManagePhotoFilterAdjustmentLayer.cs" >}}
## **Support Flatten Layers**
This article shows how to flatten whole PSD file and merge one layer into another and save them as PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ManagePhotoFilterAdjustmentLayer-ManagePhotoFilterAdjustmentLayer.cs" >}}
## **Adding and Rendering of Level Layers**
This article shows how to iterate through each level layers and set different levels than save that as PSD and PNG file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfLevelAdjustmentLayer-RenderingOfLevelAdjustmentLayer.cs" >}}
## **Add Hue Saturation of Adjustment Layers**
This article shows how to iterate through each Hue layers and set different ranges and colors than save that as PSD file with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddHueSaturationAdjustmentLayer-AddHueSaturationAdjustmentLayer.cs" >}}
## **Add Level Adjustment Layers**
This article shows how to iterate through each level layers and set different levels than save that as PSD with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddLevelAdjustmentLayer-AddLevelAdjustmentLayer.cs" >}}
## **Support for Interrupt Monitor**
This article shows how to create and monitor interrupts in Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-InterruptMonitorTest-InterruptMonitorTest.cs" >}}
## **Support Layer Effects at runtime**
This article shows how to add layer effects at runtime in Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-InterruptMonitorTest-InterruptMonitorTest.cs" >}}
## **Add Curve Adjustment layer**
This article shows how to add curve adjustment layers in PSD using Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddCurvesAdjustmentLayer-AddCurvesAdjustmentLayer.cs" >}}
## **Add Channel Mixer Adjustment layer**
This article shows how to add channel mixer adjustment layers and set different colors and then save as PSD images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddChannelMixerAdjustmentLayer-AddChannelMixerAdjustmentLayer.cs" >}}
## **Rendering of Channel Mixer Adjustment layer**
This article shows how to render channel mixer adjustment layers and set different colors channel and then save as PSD and PNG images. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddChannelMixerAdjustmentLayer-AddChannelMixerAdjustmentLayer.cs" >}}
## **Rendering Exposure Adjustment layer**
This article shows how to iterate through each exposure level layers and set different exposure values than save that as PSD as well as PNG with Aspose.PSD. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingExposureAdjustmentLayer-RenderingExposureAdjustmentLayer.cs" >}}
## **Support Blend Modes**
Using Aspose.PSD for .NET, developers can use different blend modes. Below is the code demonstration of the said functionality.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SupportBlendModes-SupportBlendModes.cs" >}}
## **Support Color Overlay Effect**
Using Aspose.PSD for .NET, developers can set a new layer with a **color** on top of that image and set it to the blending mode "**Color**." To add a more **effect**, you put the **color** image on top of these 2 layers and use the "**Overlay**" blending mode. Below is the code demonstration of the said functionality.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorOverLayEffect-ColorOverLayEffect.cs" >}}
## **Support Drop Shadow Effect**
Using Aspose.PSD for .NET, developers can set drop shadow effects to different elements. Below is the code demonstration of the said functionality.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SupportShadowEffect-SupportShadowEffect.cs" >}}
## **Rendering for export of Color Overlay effect**
Using Aspose.PSD for .NET, developers can render documents of color overlay effect. Below is the code demonstration of the said functionality.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RenderingColorEffect-RenderingColorEffect.cs" >}}
## **Rendering for export of Drop Shadow effect**
Using Aspose.PSD for .NET, developers can render documents of the drop shadow effect. Below is the code demonstration of the said functionality.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RenderingDropShadow-RenderingDropShadow.cs" >}}

## **Support of GdFlResource**
This article shows Support of GdFlResource in a PSD file with Aspose.PSD. The following code snippet shows you how Aspose.PSD supports GdFlResource.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfGdFlResource-SupportOfGdFlResource.cs" >}}
## **Support of VmskResource**
This article shows Support of VmskResource in a PSD file with Aspose.PSD. The following code snippet shows you how Aspose.PSD supports VmskResource.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfVmskResource-SupportOfVmskResource.cs" >}}
## **Support of RGB Color**


This article shows how Aspose.PSD support RGB color mode with 16bit per channels. The code snippet has been provided below.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRGBColor-SupportOfRGBColor.cs" >}}






