---
title: Creating, Opening and Saving Images
type: docs
weight: 30
url: /java/creating-opening-and-saving-images/
---

## **Creating Image Files**
Aspose.PSD for Java allows developers to create their own images. Use the static Create method exposed by the Image class to create new images. All you need to do is to supply the appropriate object of one of the classes from the ImageOptions namespace for the desired output image format. To create an image file, first create an instance of one of the classes from the ImageOptions namespace. These classes determine output image format. Below are some classes from the ImageOptions namespace (note that only PSD file formats family are currently supported for creation):

PsdOptions sets the options for creating a PSD file. Image files can be created setting an output path or by setting a stream.
### **Creating by Setting Path**
Create PsdOptions from ImageOptions namespace and set the various properties. The most important property to set is the Source property. This property specifies where the image data resides (in a file or a stream). In the example below, the source is a file. After setting the properties, pass the object to one of the static Create methods along with width and height parameter. The width and height are defined in pixels.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **Creating Using Stream**
The process for creating an image using a stream is same as for using a path. The only difference is that you need to create an instance of StreamSource by passing a Stream object to its constructor and assigning it to the Source property.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **Opening Image Files**
Developers can use Aspose.PSD for Java API to open existing PSD image files for different purposes, like adding effects to the image or to convert an existing file to another format. Whatever the purpose is, Aspose.PSD provides two standard ways to open existing files: from file or from a stream.
### **Opening from Disk**
Open an image file by passing the path and file name as a parameter to the static method Load exposed by the Image class.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Opening using a Stream**
Sometimes the image that we need to open is stored as a stream. In such cases, use the overloaded version of the Load method. This accepts a Stream object as an argument to open the image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **Load Image as Layer**
This article demonstrates the usage of Aspose.PSD to load an image as a layer. Aspose.PSD APIs have exposed efficient & easy to use methods to achieve this goal. Aspose.PSD has exposed the AddLayer method of the PsdImage class to add an image into a PSD file as a layer.

The steps to load an image into PSD as layer are as simple as below:

- Create an instance of image using the PsdImage class with specified width and height.
- Load a PSD file as an image using the factory method Load exposed by Image class.
- Create an instance of Layer class and assign the PSD image layer to it.
- Adds the created layer using AddLayer method expose by PsdImage class
- Save the results.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **Saving Image Files**
Aspose.PSD lets you create image files from scratch. It also provides the means to edit existing image files. Once the image is created or modified, the file is usually saved to disk. Aspose.PSD provides you with methods for saving images to a disk by specifying a path or using a Stream object.
### **Saving to Disk**
The Image class represents an image object, so this class provides all the tools needed to create, load and save an image file. Use the Image class Save method to save images. One overloaded version of the Save method accepts the file location as a string.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **Saving to a Stream**
Another overloaded version of the Save method accepts the Stream object as an argument and saves the image file to the stream.

If the image is created by specifying any of the CreateOptions in the Image constructor, the image is automatically saved to the path or stream supplied during the initialization of the Image class by calling the Save method that doesn't accept any parameter.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **Setting for Replacing Missing Fonts**
Developers can use Aspose.PSD for Java API to load existing PSD image files for different purposes, for example to set default font name when saving PSD documents as raster image (into PNG, JPG and BMP formats). This default font should be used as a replacement for all missing fonts (fonts that are not found in current Operating System). Once the image is modified, the file will be saved to disk.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}




