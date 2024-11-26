---
title: 操纵TIFF图片
type: docs
weight: 40
url: /zh/java/manipulating-tiff-images/
---

## **使用不同设置添加帧**
TIFF是一种非常灵活的格式，允许添加不同的帧，具有不同的尺寸、压缩和其他设置。Aspose.PSD API允许您添加任何尺寸的TIFF帧，有助于创建复杂的文档。如果需要在添加过程中调整帧以使它们全部相等，请执行以下步骤：

- 使用所需选项创建新的空白帧，或使用CreateFrameFrom方法复制指定输出选项的源帧。
- 使用Resize方法将源帧/图像调整到所需尺寸。
- 将源帧/图像像素添加到新帧上。
- 将新帧添加到输出的TIFF图像中。

## **将PSD图像的图层导出为多页TIFF文件格式**
有时需要将PSD图像图层导出为多页TIFF文件格式。本文将演示如何使用Aspose.PSD for Java API执行此任务。首先，我们将从磁盘加载PSD图像。然后，我们将迭代PSD图像的图层，并从相应的图层创建TiffFrame。最后，我们将将生成的TIFF图像保存到磁盘上的单个文件中。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}

## **TiffOptions配置**

开发人员可以调整TiffOptions类的不同属性以获得期望的结果。在本文档中，我们将重点放在控制生成图像属性的4个主要属性上。

以下列出了这些属性。

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

当我们初始化一个空的TiffOptions结构时，每个选项都设置为其默认值，例如压缩设置为无，BitsPerSample设置为1，Photometric设置为MinIsWhite。将图像保存为此格式将使最终图像为黑白，并且这是此类选项组合的预期行为。为了获得彩色结果，您必须将上述所有属性设置为与期望颜色空间对应的值，或者您可以根据本文后面讨论的预定义设置初始化TiffOptions结构。下表描述了您可以设置的预期参数值。请注意，为了将任何加载/创建的图像保存为TIFF文件格式，应该通过TiffOptions设置所有4列。

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/无压缩|1/4/8/16（调色板，彩色模式）仅单通道|无|
|MinIsWhite/MinIsBlack|LZW/无压缩|1/4/8/16（灰度模式）仅单通道|无|
|Palette|LZW/无压缩|8（调色板，彩色模式）仅单通道|水平（对于LZW来说，相同图案可以获得更好的压缩）|
|MinIsWhite/MinIsBlack|LZW/无压缩|8（灰度模式）仅单通道|水平（对于LZW来说，相同图案可以获得更好的压缩）|
|RGB|LZW/无压缩|[8,8,8]（3个RGB通道）|无/水平|
|RGB|LZW/无压缩|[8,8,8,8]（3个RGB通道和额外的alpha通道可以通过TiffOptions.AlphaStorage设置）事实上，支持任何额外通道计数，但是每个通道必须具有8位大小，如[8,8,8,8,8,8]|无/水平|
所有4个属性应该通过TiffOptions设置，以便将任何图像格式保存为Tiff格式。使用不同组合时，某些查看器（包括Windows照片查看器）可能会拒绝呈现结果图像，因为它们提供的支持有限。在这种情况下，请选择其他查看器进行测试。
### **TiffOptions类的预定义设置**
为了方便用户并避免TiffOptions实例的错误配置，Aspose.PSD for Java API公开了另一个构造函数，它接受TiffExpectedFormat类型的参数。根据TiffExpectedFormat枚举中选择的值，API会自动配置TiffOptions实例的所有强制属性，以产生期望的结果。在我们开始查看示例代码之前，以下是TiffExpectedFormat字段及其详细信息的列表，以便更好地理解用法。

- TiffExpectedFormat.Default：将字段设置为Default与Tiffoptions类的默认构造函数类似，未设置任何压缩，BitsPerPixel设置为1，以产生黑白结果。建议在根据所需结果手动设置其他格式特定属性时使用此字段。
- TiffExpectedFormat.TiffCcitRle：特定于RLE编码，将结果保存为1 BitsPerPixel（黑白）TIFF格式。
- TiffExpectedFormat.TiffCcittFax3：特定于CCITT Fax3编码，将结果保存为1 BitsPerPixel（黑白）TIFF格式。
- TiffExpectedFormat.TiffCcittFax4：特定于CCITT Fax4编码，将结果保存为1 BitsPerPixel（黑白）TIFF格式。
- TiffExpectedFormat.TiffDeflateBW：特定于Deflate压缩，将结果保存为1 BitsPerPixel（黑白）TIFF格式。
- TiffExpectedFormat.TiffDeflateRGB：特定于Deflate压缩，将结果保存为RGB（彩色）TIFF格式。
- TiffExpectedFormat.TiffJpegRGB：特定于Jpeg压缩，将结果保存为RGB（彩色）TIFF格式。
- TiffExpectedFormat.TiffJpegYCBCR：特定于Deflate压缩，将结果保存为YCBCR（彩色）TIFF格式。
- TiffExpectedFormat.TiffLzwBW：特定于LZW压缩，将结果保存为1 BitsPerPixel（黑白）TIFF格式。
- TiffExpectedFormat.TiffLzwRGB：特定于LZW压缩，将结果保存为RGB（彩色）TIFF格式。
- TiffExpectedFormat.TiffLzwRGBA：特定于LZW压缩，将结果保存为RGBA（带透明度的彩色）TIFF格式。
- TiffExpectedFormat.TiffNoCompressionBW：特定于无压缩TIFF格式，将结果保存为1 BitsPerPixel（黑白）。
- TiffExpectedFormat.TiffNoCompressionRGB：特定于无压缩TIFF格式，将结果保存为RGB（彩色）。
- TiffExpectedFormat.TiffNoCompressionRGBA：特定于无压缩TIFF格式，将结果保存为RGBA（带透明度的彩色）。

以下代码片段详细说明了在创建Tiffoptions类实例时使用TiffExpectedFormat字段。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}

## **支持Deflate和Adobe Deflate压缩**
TIFF（标记图像文件格式）文件格式支持各种类型的压缩，其中压缩类型作为一个标记（整数值）存储在文件中。其中一种压缩方法是Adobe Deflate（以前称为Deflate）。Aspose.PSD for Java API支持此压缩方法以导出和创建TIFF图像。
### **使用Deflate压缩将图像保存为TIFF**
将加载的图像转换为采用Deflate/Adobe Deflate压缩的TIFF很容易，如下所示。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **使用Adobe Deflate压缩创建TiffImage**
下面提供的示例演示了使用Aspose.PSD for Java API从头开始使用Adobe Deflate压缩方法创建图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **压缩TIFF图片**
Aspose.PSD for Java API可用于将PSD图像转换为TIFF图像格式，甚至更改生成的TIFF图像的压缩。API还可用于将不同图像存储为TIFF图像中的帧，以供存档目的，同时将图像压缩到最小数据大小。无论使用哪种压缩算法，图像压缩都应通过减少源数据大小来进行。为了实现最佳压缩比，我们可以使用索引的颜色空间。以下代码片段通过仅使用16种索引颜色和LZW压缩算法执行最佳压缩，但源颜色略有抖动。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
