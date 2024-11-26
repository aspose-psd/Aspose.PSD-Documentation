---
title: 操作JPEG图像
type: docs
weight: 30
url: /zh/net/manipulating-jpeg-images/
---

## **使用ExifData类读取和修改Jpeg EXIF标签**
几乎所有数字相机（包括智能手机）、扫描仪和其他处理图像的系统都会保存带有EXIF（可交换图像文件）信息的图像。相机设置和场景信息由相机记录到图像文件中。 EXIF数据还包括快门速度、拍摄日期和时间、焦距、曝光补偿、测光模式以及是否使用了闪光灯等信息。Aspose.Imaging APIs已经可以轻松简单地从给定图像中提取EXIF信息。开发人员也可以根据自己的需求向图像中写入EXIF数据或修改现有信息。Aspose.PSD为读取、写入和修改EXIF数据提供了[ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata)类，而[Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums)命名空间包含了在此过程中使用的相关枚举。
### **读取EXIF数据**
Aspose.PSD APIs提供了从给定图像中读取EXIF数据的方法。下面提供的步骤说明了使用ExifData类从图像中读取EXIF信息的用法。

- 使用工厂方法Load加载PSD图像。
- 在PSD资源中查找Jpeg缩略图。
- 提取ExifData类的实例。

提取所需信息并将其写入控制台。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


或者，开发人员还可以使用以下代码片段获取特定信息。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **写入和修改EXIF数据**
使用Aspose.PSD APIs，开发人员可以写入新的EXIF信息并修改图像的现有EXIF数据。写入和修改两个过程都需要加载图像并将EXIF数据获取到ExifData类的实例中。然后可以访问ExifData类公开的属性，根据需要进行设置。请注意，用于操作的图像应为通常为PSD缩略图的Jpeg或Tiff图像。演示如何使用的示例代码如下：



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **从PSD资源中提取缩略图**
缩略图是图片的缩小版，用于显示图片的重要部分而不是整个画面。一些图像文件（特别是用数码相机拍摄的图像）在文件中嵌入了缩略图像。Aspose.PSD API允许您提取PSD资源缩略图并将其单独存储到磁盘上。缩略资源包含ExifData.[缩略图](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail)属性，可检索缩略图数据。下面提供的代码片段演示了如何使用它。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


使用上述讨论的方法将缩略图存储为其他支持的文件格式。如果要将缩略图数据导出到其他图像格式，例如BMP和PNG，请使用其他图像导出选项。
### **从JFIF段中提取缩略图**
还可以从PSD缩略资源的ExifData或JFIF段中提取缩略图。以下代码显示如何从JFIF或ExifData段中执行缩略图数据的提取：


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


使用上述讨论的方法将缩略图存储为其他支持的文件格式。如果要将缩略图数据导出到其他图像格式，例如BMP和PNG，请使用其他图像导出选项。
### **向JFIF段添加缩略图**
下面的代码片段演示了如何使用JFIF。缩略图属性将缩略图添加到加载的PSD图像的JFIF段中。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

缩略图与其他段数据一起，由于JPEG格式的规范，不能超过65545字节。如果要将大图像设置为缩略图，可能会引发异常。
### **向EXIF段添加缩略图**
下面的代码片段演示了如何使用ExifData.Thumbnail属性将缩略图添加到加载的PSD图像的EXIF段中。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


在这种情况下，Aspose.PSD API无法估计缩略图大小，但可以检查整个EXIF数据段的大小。这不能超过65535字节。
## **使用JpegExifData类读取和修改Jpeg EXIF标签**
Aspose.PSD APIs提供了专门用于Jpeg图像格式的[JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata)类来检索和更新EXIF信息。本文演示了如何使用JpegExifData类实现相同的效果。Aspose.PSD.Exif.JpegExifData类充当Jpeg图像的EXIF数据容器，提供了检索标准Jpeg EXIF标签的方法，如下所示：



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

### **完整的EXIF标签列表**
上面的代码片段使用Aspose.PSD.Exif.JpegExifData类提供的属性读取了几个EXIF标签。这些属性的完整列表在此处可用。以下代码将使用[System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0)类读取所有EXIF标签。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **自动校正JPEG图像的方向**


照片可以是使用相机旋转90°、180°、270°或无旋转（正常方向）拍摄的。大多数数字相机以EXIF标签的形式将方向信息存储在JEPG图像的图像数据中。此信息可用于在图像上执行自动旋转以更正方向。Aspose.PSD APIs为JpegImage类提供了AutoRotate方法，用于自动校正JPEG图像的方向。以下是如何使用Aspose.PSD for .NET API的AutoRotate方法的方法。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **支持使用CMYK和YCCK的JPEG-LS**


Aspose.PSD for .NET API支持CMYK和YCCK颜色模型与JPEG-LS。下面的代码片段演示了如何使用JPEG-LS的支持。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **支持JPEG-LS图像中的每个样本2-7位**


Aspose.PSD for .NET API支持每个样本2-7位的JPEG-LS图像。下面的代码片段演示了如何使用JPEG-LS的支持。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **为JPEG图像设置ColorType和CompressionType**




Aspose.PSD for .NET API支持颜色类型和压缩类型，并将其设置为JPEG图像的灰度和渐进。下面的代码片段演示了如何使用该支持。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





下面的代码片段演示了如何使用ExifData.Thumbnail属性向加载的PSD图像的EXIF段添加缩略图。



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

在这种情况下，Aspose.PSD API无法估算缩略图的大小，但可以检查整个EXIF数据段的大小。这不能超过65535字节。

