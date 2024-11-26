---
title: การแปลงรูปภาพ
type: docs
weight: 20
url: /th/java/converting-images/
---

## **การแปลงรูปภาพเป็นขาวดำและระดับสีเทา**
บางครั้งคุณอาจต้องการที่จะแปลงรูปภาพสีเข้าสู่ขาวดำหรือระดับสีเทาสำหรับวัตถุประสงค์ในการพิมพ์หรือเก็บถาวร บทความนี้จะสาธิตการใช้ Aspose.PSD สำหรับ API Java เพื่อบทเรียนนี้อธิบายวิธีการใช้สองวิธีดังต่อไปนี้.

- การทำภาพดำขาว
- การทำระดับสีเทา
### **การทำภาพดำขาว**
เพื่อให้อธิบายแนวคิดของการทำภาพดำขาวเราจำเป็นต้องกำหนดภาพไบนารี่ที่เป็นภาพดิจิตัลที่สามารถมีค่าเพียงสองค่าสำหรับแต่ละพิกเซล โดยปกติแล้วสองสีที่ใช้สำหรับภาพไบนารี่คือสีดำและสีขาวแม้ว่าสามารถใช้สองสีใดๆก็ได้. การทำภาพดำขาวคือกระบวนการที่แปลงภาพเป็นระดับสองหมายความว่าแต่ละพิกเซลถูกเก็บเป็นเซ็ตเดียว (0 หรือ 1) ที่ 0 หมายถึงไม่มีสีและ 1 หมายถึงมีสี Aspose.PSD สำหรับ API Java รองรับวิธีการทำภาพดำขาวสองวิธี ณ ตอนนี้
#### **การทำภาพดำขาวด้วยค่าเกณฑ์คงที่**
โค้ดตัวอย่างต่อไปนี้จะแสดงให้คุณเห็นวิธีการใช้การทำภาพดำขาวด้วยค่าเกณฑ์คงที่โดยสามารถนำไปใช้กับภาพได้

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **การทำภาพดำขาวด้วยค่าเกณฑ์ Otsu**
โค้ดตัวอย่างต่อไปนี้จะแสดงให้คุณเห็นวิธีการใช้การทำภาพดำขาวด้วยค่าเกณฑ์ Otsu โดยสามารถนำไปใช้กับภาพได้

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **การทำระดับสีเทา**
การทำระดับสีเทาคือกระบวนการที่แปลงภาพทูลต่อไปเป็นภาพที่ปรากฎระดับสีเทาแบ่งภาพที่ต่อเนื่องไปเป็นภาพที่มีเฉดเทาอย่างไม่ต่อเนื่อง โค้ดตัวอย่างต่อไปนี้จะแสดงให้คุณเห็นวิธีการใช้การทำระดับสีเทา

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **แปลงชั้นต่างๆของรูปภาพ GIF เป็นภาพ TIFF**
บางครั้งจำเป็นต้องสกัดและแปลงชั้นของ PSD Image เป็นรูปแบบภาพแรสเตอร์อื่น เพื่อตอบสนองความต้องการของแอพพลิเคชัน Aspose.PSD API รองรับคุณสมบัติในการสกัดและแปลงชั้นของ PSD Image เป็นรูปแบบภาพแรสเตอร์อื่นโดยเริ่มแรกเราจะสร้างอินสสแตนซ์ของภาพและโหลด PSD Image จากดิสก์ท้องถิน จากนั้นเราจะวนซ้ำแต่ละชั้นในคุณสมบัติชั้น จากนั้นเราจะแปลงบล๊อกเป็นภาพ TIFF โค้ดตัวอย่างต่อไปนี้จะแสดงให้คุณเห็นวิธีการแปลงชั้นรูปภาพ PSD เป็นภาพ TIFF

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **การแปลงไฟล์ PSD CMYK เป็น TIFF CMYK**
โดยใช้ Aspose.PSD สำหรับ Java, นักพัฒนาสามารถแปลงไฟล์ PSD CMYK เป็นรูปแบบ tiff CMYK บทความนี้จะแสดงวิธีการส่งออก/แปลงไฟล์ PSD CMYK เป็นรูปแบบ tiff CMYK ด้วย Aspose.PSD โดยใช้ Aspose.PSD สำหรับ Java คุณสามารถโหลดรูปภาพ PSD แล้วคุณสามารถตั้งค่าคุณสมบัติต่างๆ โดยใช้คลาส TiffOptions และบันทึกรูปภาพหรือส่งออก โค้ดตัวอย่างต่อไปนี้จะแสดงให้คุณเห็นวิธีที่คุณสามารถทำได้

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Exporting Images**
Along with a rich set of image processing routines, Aspose.PSD provides specialized classes to convert PSD file formats to other formats. Using this library, PSD images conversion is very simple and intuitive. Below are some specialized classes for this purpose in ImageOptions namespace.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

It is easy to export PSD images with Aspose.PSD for Java API. All you need is an object of the appropriate class from ImageOptions namespace. By using these classes, you can easily export any image created, edited or simply loaded with Aspose.PSD for Java to any supported format.
## **Combining Images**
This example uses Graphics class and shows how to combine two or more images into a single complete image. To demonstrate the operation, the example creates a new PsdImage and draws images on the canvas surface using Draw Image method exposed by Graphics class. Using Graphics class two or more images can be combined in such way that the resultant image will look as a complete image with no space between the image parts and no pages. The canvas size must be equal to the size of resultant image. Following is the code demonstration that shows how to use Draw Image method of the Graphics class to combine images in a single image.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Expand and Crop Images**
Aspose.PSD API allows you to expand or crop an image during image conversion process. Developer needs to create a rectangle with X and Y coordinates and specify the width and height of the rectangle box. The X,Y and Width, Height of rectangle will depict the expansion or cropping of the loaded image. If it is required to expand or crop the image during image conversion, perform the following steps:

1. Create an instance of RasterImage class and load the existing image.
1. Create an Instance of ImageOption class.
1. Create an instance of Rectangle class and initialize the X,Y and Width, Height of the rectangle
1. Call Save method of the RasterImage class while passing output file name, image options and the rectangle object as parameters.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Read and Write XMP Data To Images**
XMP (Extensible Metadata Platform) is an ISO standard. XMP standardizes a data model, a serialization format and core properties for the definition and processing of extensible metadata. It also provides guidelines for embedding XMP information into popular image such as JPEG, without breaking their readability by applications that do not support XMP. Using Aspose.PSD for Java API developers can read or write XMP metadata to images. This article demonstrates how XMP metadata can be read from image and write XMP metadata to images.
### **Create XMP Metadata, Write It And Read From File**
With the help of XMP namespace developer can create XMP metadata object and write it to an image. The following code snippet shows you how to use the XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage and DublinCorePackage packages contained in XMP namespace.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Export Images in Multi Threaded Environment**
Aspose.PSD for Java now supports converting images in multi threaded environment. Aspose.PSD for Java ensures the optimized performance of operations during execution of code in multi-threaded environment. All image option classes (e.g. BmpOptions, TiffOptions, JpegOptions, etc.) in the Aspose.PSD for Java implement IDisposable interface. Therefore it is a must that developer properly dispose off the image options class object in case Source property is set. Following code snippet demonstrates the said functionality.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD now supports SyncRoot property while working in multi-threaded environment. Developer can use this property to synchronize access to the source stream. Following code snippet demonstrates how the SyncRoot property can be used.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
