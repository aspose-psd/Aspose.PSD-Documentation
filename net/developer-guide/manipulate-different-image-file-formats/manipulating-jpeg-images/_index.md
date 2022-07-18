---
title: Manipulating JPEG Images
type: docs
weight: 30
url: /net/manipulating-jpeg-images/
---

## **Using ExifData Class to Read and Modify Jpeg EXIF Tags**
Almost all digital cameras (including smartphones), scanners and other systems handling image save images with EXIF (Exchangeable Image File) information. Camera settings and scene information are recorded by the camera into the image file. EXIF data also include shutter speed, date and time a photo was taken, focal length, exposure compensation, metering pattern and if a flash was used. Aspose.Imaging APIs has made possible to extract the EXIF information from a given image in a very easy and simple manner. Developers may also write EXIF data to the images or modify the existing information as per their requirement. Aspose.PSD has provided [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) class for reading, writing and modifying the EXIF data, where as [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) namespace contains the relevant enumerations used in the process.
### **Reading EXIF Data**
Aspose.PSD APIs provide means to read EXIF data from a given image. Below provided steps illustrate the usage of ExifData class to read the EXIF information from an image.

- Load PSD Image using the factory method Load.
- Find Jpeg thumbnail among PSD resources.
- Extract an instance of ExifData class.

Fetch the required information and write it to console.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternatively, developers may also get the specific information using the following code snippet.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **Writing & Modifying EXIF Data**
Using Aspose.PSD APIs, developers can write new EXIF information and modify existing EXIF data of an image. Both processes (Writing & Modifying) requires loading of an image and getting the EXIF data into an instance of ExifData class. Then one can access properties exposed by ExifData class to set them accordingly. Please note that images for manipulation should be Jpeg or Tiff images that are usually PSD thumbnails. Sample code to demonstrate the usage is as follow:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Extracting thumbnails from PSD resources**
Thumbnails are reduced-size versions of pictures, used to display a significant part of the picture instead of the full frame. Some image files (especially the ones shot with a digital camera) have a thumbnail image embedded in the file. Aspose.PSD API allows you to extract PSD resource thumbnails and store it separately on disk. Thumbnail resources contain ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) property that can retrieve the thumbnail data. The code snippet provided below demonstrates how to use it.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Use the approach discussed above to store the thumbnail to other supported file formats. If you wish to export thumbnail data to other image formats such as BMP & PNG, please use other image export options.


### **Extracting thumbnails from JFIF segments**
It is also possible to extract thumbnails from the ExifData or JFIF segment of PSD thumbnail resources. The following code shows how to perform the extraction of thumbnail data from JFIF or ExifData segment:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


Use the approach discussed above to store the thumbnail to other supported file formats. If you wish to export thumbnail data to other image formats such as BMP & PNG, please use other image export options.
### **Add Thumbnail to JFIF Segment**
The code snippet below demonstrates how to use the JFIF. Thumbnail property to add a thumbnail image to the JFIF segment of a loaded PSD image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Thumbnail images with other segment data cannot occupy more than 65,545 bytes because of the JPEG format specifications. In cases where large images are to be set as a thumbnail, exception may arise.


### **Add Thumbnail to EXIF Segment**
The code snippet below demonstrate how to use the ExifData.Thumbnail property to add a thumbnail image to the EXIF segment of a loaded PSD image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


In this case, the Aspose.PSD API cannot estimate the thumbnail image size, but it can check the size of the entire EXIF data segment. This cannot be bigger than 65,535 bytes.
## **Using JpegExifData Class to Read and Modify Jpeg EXIF Tags**
Aspose.PSD APIs provide [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) class that is exclusive to Jpeg image formats to retrieve & update EXIF information. This article demonstrates the usage of JpegExifData class to achieve the same. Aspose.PSD.Exif.JpegExifData class serves as EXIF data container for Jpeg images, and provide means to retrieve standard Jpeg EXIF tags as demonstrated below:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **Complete List of EXIF Tags**
The above code snippet reads a few EXIF Tags using the properties offered by Aspose.PSD.Exif.JpegExifData class. Complete list of these properties is available here. Following code will read all the EXIF tags using the [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) class.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **Auto Correct Orientation of JPEG Images**


Photos can be shot with a camera rotated at 90°, 180°, 270°, or none (normal orientation). Most digital cameras stores the orientation information along with the image data as EXIF tags of the JEPG images. This information can be used to perform the auto rotation on the images to correct the orientation. Aspose.PSD APIs provides the AutoRotate method for JpegImage class to auto correct the orientation of JPEG images. Here is how you can use the AutoRotate method with Aspose.PSD for .NET API.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **Support for JPEG-LS with CMYK and YCCK**


Aspose.PSD for .NET API provides support for CMYK and YCCK color models with JPEG-LS. The code snippet below demonstrates how to use that support for JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **Support for 2-7 bits per sample in JPEG-LS images**


Aspose.PSD for .NET API provides support for 2-7 bits per sample JPEG-LS images. The code snippet below demonstrates how to use that support for JPEG-LS.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **Setting ColorType and CompressionType for JPEG images**




Aspose.PSD for .NET API provides support for Color Type and compression Type and set them as gray scale and progressive for JPEG images. The code snippet below demonstrates how to use that support.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





The code snippet below demonstrate how to use the ExifData.Thumbnail property to add a thumbnail image to the EXIF segment of a loaded PSD image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

In this case, the Aspose.PSD API cannot estimate the thumbnail image size, but it can check the size of the entire EXIF data segment. This cannot be bigger than 65,535 bytes.
