---
title: Creating, Opening and Saving PSD Files
type: docs
weight: 10
url: /java/creating-opening-and-saving-psd-files/
---

## **Exporting Image to PSD**
PSD, PhotoShop document, is the default file format used by Adobe PhotoShop for working with images. Aspose.PSD allows you to load, edit and save files to PSD so that they can be opened and edited in PhotoShop. This article shows how to save a file to PSD with Aspose.PSD, and it also discusses some of the settings that can be used when saving to this format. PsdOptions is a specialized class in the ImageOptions namespace used to export images to PSD. To export to PSD, create an instance of the Image class, either loaded from an existing image file (thumbnails for example) or created from scratch. This article explains how. In the examples below, an image is created from scratch. Once it is created and pixel data is populated, save the image using the Image class Save method, and supply a PsdOptions object as the second argument. Several of the PsdOptions class properties can be set for advanced conversion. Some of the properties are ColorMode, CompressionMethod and Version. Aspose.PSD supports the following compression methods through the CompressionMethod enumeration:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

The following color modes are supported through the ColorModes enumeration:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Additional resources can be added, such as thumbnail resources for PSD v4.0, v5.0 and higher, or grid and guide resources for PSD v4.0 and higher. The code below creates a BMP file from scratch, populates the pixels and saves it to PSD with RLE compression and grayscale color mode. The following code snippet shows you how to export Image to PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importing image to PSD layer**
This article demonstrates the usage of Aspose.PSD to add or import an image to a PSD layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the DrawImage method of the Layer class to add/import an image into a PSD file. DrawImage method needs location and image values to add/import an image into a PSD file. The steps to import image into PSD layer are as simple as below:

- Load a PSD file as an image using the factory method Load exposed by Image class.
- Create an instance of Layer class and assign the PSD image layer to it.
- Load the image that needs to be added or create a one from scratch.
- Call the Layer.DrawImage method while specifying location and image instance.
- Save the results.



The following code snippet shows you how to import image to PSD layer.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Creating Thumbnails from PSD Files**
PSD is the native document format of Adobe's Photoshop application. Adobe Photoshop (version 5.0 and later) stores thumbnail information for preview display in an image resource block that consists of an initial 28-byte header, followed by a JFIF thumbnail in RGB (red, green, blue) order. Aspose.PSD API provides an easy to use mechanism to access the resources of PSD file. These resources also include the thumbnail resource that in turn can be fetched and saved to disc as per application needs. The following code snippet shows you how to create thumbnails from PSD Files.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Creating Indexed PSD Files**
Aspose.PSD for Java API can create Indexed PSD files from scratch. This article demonstrates the use of PsdOptions and PsdImage classes to create an Indexed PSD while drawing some shapes over the newly created canvas. The following simple steps are required to create an Indexed PSD file.

- Create an instance of PsdOptions and set it's source.
- Set ColorMode property of the PsdOptions to ColorModes.Indexed.
- Create a new palette of colors from RGB space and set it as Palette property of PsdOptions.
- Set CompressionMethod property to required compression algorithm.
- Create a new PSD image by calling the PsdImage.Create method.
- Draw graphics or perform other operations as per requirement.
- Call PsdImage.Save method to commit all changes.



The following code snippet shows you how to create indexed PSD files.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Exporting PSD Layer to Raster Image**
Aspose.PSD for Java allows you to export layers in a PSD file into raster images. Please use the Aspose.PSD.FileFormats.Psd.Layers.Layer.Save method to export the layer to image. The following sample code loads a PSD file and exports each of its layer into a PNG image using Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Once all layers are exported into PNG images, you can open them using your favorite image viewer. The following code snippet shows you how to export PSD layer to raster image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
