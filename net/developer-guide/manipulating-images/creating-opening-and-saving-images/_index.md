---
title: Creating, Opening and Saving Images
type: docs
weight: 30
url: /net/creating-opening-and-saving-images/
---

## **Creating Image Files**
Aspose.PSD for .NET allows developers to create their own images. Use the static Create method exposed by the Image class to create new images. All you need to do is to supply the appropriate object of one of the classes from the ImageOptions namespace for the desired output image format. To create an image file, first create an instance of one of the classes from the ImageOptions namespace. These classes determine the output image format. Below are some classes from the ImageOptions namespace (note that only PSD file formats family are currently supported for creation):

[PsdOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) sets the options for creating a PSD file. Image files can be created by setting an output path or by setting a stream.
### **Creating by Setting Path**
Create PsdOptions from [ImageOptions](https://apireference.aspose.com/psd/net/aspose.psd.imageoptions) namespace and set the various properties. The most important property to set is the Source property. This property specifies where the image data resides (in a file or a stream). In the example below, the source is a file. After setting the properties, pass the object to one of the static [Create](https://apireference.aspose.com/psd/net/aspose.psd/image/methods/create) methods along with width and height parameter. The width and height are defined in pixels.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **Creating Using Stream**
The process for creating an image using a stream is the same as for using a path. The only difference is that you need to create an instance of [StreamSource]() by passing a Stream object to its constructor and assigning it to the Source property.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **Opening Image Files**
Developers can use Aspose.PSD for .NET API to open existing PSD image files for different purposes, like adding effects to the image or to convert an existing file to another format. Whatever the purpose is, Aspose.PSD provides two standard ways to open existing files: from file or from a stream.
### **Opening from Disk**
Open an image file by passing the path and file name as a parameter to the static method Load exposed by the Image class.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Opening using a Stream**
Sometimes the image that we need to open is stored as a stream. In such cases, use the overloaded version of the Load method. This accepts a Stream object as an argument to open the image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **Load Image as Layer**
This article demonstrates the usage of Aspose.PSD to load an image as a layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the AddLayer method of the PsdImage class to add an image into a PSD file as a layer.

The steps to load an image into PSD as a layer are as simple as below:

- Create an instance of an image using the PsdImage class with a specified width and height.
- Load a PSD file as an image using the factory method Load exposed by Image class.
- Create an instance of the Layer class and assign the PSD image layer to it.
- Add the created layer using the AddLayer method expose by PsdImage class
- Save the results.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **Load Image as Layer from a Stream**
This article demonstrates the usage of Aspose.PSD to load an image as a layer from a stream. To load an image from a stream, simply pass a stream object that contains an image to the Layer class constructor. Add the created layer using the AddLayer method exposed by the PsdImage class and save the results.



Here is the sample code.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Saving Image Files**
Aspose.PSD lets you create image files from scratch. It also provides the means to edit existing image files. Once the image is created or modified, the file is usually saved to disk. Aspose.PSD provides you with methods for saving images to a disk by specifying a path or using a Stream object.
### **Saving to Disk**
The Image class represents an image object, so this class provides all the tools needed to create, load and save an image file. Use the Image class Save method to save images. One overloaded version of the Save method accepts the file location as a string.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **Saving to a Stream**
Another overloaded version of the Save method accepts the Stream object as an argument and saves the image file to the stream.

If the image is created by specifying any of the CreateOptions in the Image constructor, the image is automatically saved to the path or stream supplied during the initialization of the Image class by calling the Save method that doesn't accept any parameter.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **Setting for Replacing Missing Fonts**
Developers can use Aspose.PSD for .NET API to load existing PSD image files for different purposes, for example, to set default font name when saving PSD documents as a raster image (into PNG, JPG and BMP formats). This default font should be used as a replacement for all missing fonts (fonts that are not found in the current Operating System). Once the image is modified, the file will be saved to disk.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}




