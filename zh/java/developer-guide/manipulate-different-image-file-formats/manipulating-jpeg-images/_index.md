---
title: 操作JPEG图像
type: docs
weight: 20
url: /zh/java/manipulating-jpeg-images/
---

## **使用ExifData类读取和修改JPEG EXIF标签**

几乎所有数码相机（包括智能手机）、扫描仪和其他处理图像的系统都会保存带有EXIF（可交换图像文件）信息的图像。相机设置和场景信息被相机记录到图像文件中。EXIF数据还包括快门速度、拍摄日期和时间、焦距、曝光补偿、测光模式以及是否使用了闪光灯等信息。Aspose.Imaging APIs使得从给定图像中提取EXIF信息变得非常简单和方便。开发人员也可以根据自己的需求向图像中写入EXIF数据或修改现有信息。Aspose.Imaging已经为读取、写入和修改EXIF数据提供了ExifData类，而Aspose.PSD.Exif.Enums命名空间包含了该过程中使用的相关枚举。

### **读取EXIF数据**

Aspose.PSD APIs提供了一种读取给定图像中EXIF数据的方法。下面提供的步骤演示了使用ExifData类读取图像中的EXIF信息。

- 使用工厂方法Load加载PSD图像。
- 在PSD资源中查找JPEG缩略图。
- 提取ExifData类的一个实例。

获取所需信息并将其写入控制台。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}

开发人员还可以使用以下代码段获取特定信息。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}

### **写入和修改EXIF数据**

使用Aspose.PSD APIs，开发人员可以写入新的EXIF信息并修改图像的现有EXIF数据。这两个过程（写入和修改）都需要加载图像并将EXIF数据获取到ExifData类的实例中。然后，可以访问ExifData类公开的属性并相应设置它们。请注意，用于操作的图像应为通常为PSD缩略图的JPEG或TIFF图像。演示如何使用的示例代码如下：

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}

## **从PSD资源中提取缩略图**

缩略图是图片的缩小版本，用于显示图片的一个重要部分而不是整个画面。一些图像文件（尤其是用数字相机拍摄的图像）中嵌入了一个缩略图像。Aspose.PSD API允许您提取PSD资源缩略图并将其单独存储在磁盘上。缩略资源包含ExifData.Thumbnail属性，可检索缩略图数据。下面提供的代码片段演示了如何使用它。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

使用上述讨论的方法将缩略图存储为其他支持的文件格式。如果您希望将缩略图数据导出为其他图像格式，如BMP和PNG，请使用其他图像导出选项。

### **从JFIF段提取缩略图**

也可以从PSD缩略图资源的ExifData或JFIF段中提取缩略图。以下代码显示了如何从JFIF或ExifData段中提取缩略图数据：

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}

使用上述讨论的方法将缩略图存储为其他支持的文件格式。如果您希望将缩略图数据导出为其他图像格式，如BMP和PNG，请使用其他图像导出选项。

### **向JFIF段添加缩略图**

下面的代码片段演示了如何使用JFIF.Thumbnail属性将缩略图图像添加到已加载的PSD图像的JFIF段中：

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

由于JPEG格式规范限制，带有其他段数据的缩略图图像不能超过65545字节。如果要设置大图像作为缩略图，可能会引发异常。

### **向EXIF段添加缩略图**

下面的代码片段演示了如何使用ExifData.Thumbnail属性将缩略图图像添加到已加载的PSD图像的EXIF段中：

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

在这种情况下，Aspose.PSD API无法估算缩略图图像的大小，但可以检查整个EXIF数据段的大小。这个大小不能超过65535字节。

## **使用JpegExifData类读取和修改JPEG EXIF标签**

Aspose.PSD APIs提供了JpegExifData类，专门用于JPEG图像格式以检索和更新EXIF信息。本文演示了使用JpegExifData类实现相同目的的方法。Aspose.PSD.Exif.JpegExifData类用于JPEG图像的EXIF数据容器，并提供获取标准JPEG EXIF标签的方法，如下所示：

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

### **完整的EXIF标签列表**

上面的代码段使用Aspose.PSD.Exif.JpegExifData类提供的属性读取了一些EXIF标签。这些属性的完整列表在这里。以下代码将使用System.Reflection.PropertyInfo类读取所有EXIF标签。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}

## **自动校正JPEG图像的方向**

拍摄的照片在相机旋转了90°、180°、270°或无（正常方向）时。大多数数码相机将方向信息与JPEG图像的EXIF标签一起存储。可以使用这些信息对图像执行自动旋转以纠正方向。Aspose.PSD APIs为JpegImage类提供了AutoRotate方法，用于自动校正JPEG图像的方向。以下是如何在Java API的Aspose.PSD中使用AutoRotate方法的示例。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}

## **支持JPEG-LS与CMYK和YCCK**

Aspose.PSD for Java API支持JPEG-LS中的CMYK和YCCK颜色模型。下面的代码片段演示了如何在JPEG-LS中使用该支持。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}

## **支持JPEG-LS图像中的2-7位每样本**

Aspose.PSD for Java API支持JPEG-LS图像中的2-7位每样本。下面的代码片段演示了如何在JPEG-LS中使用该支持。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}

## **为JPEG图像设置ColorType和CompressionType**

Aspose.PSD for Java API支持为JPEG图像设置Color Type和Compression Type，并将它们设置为灰度和渐进。下面的代码片段演示了如何使用该支持。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}

