---
title: 操纵TIFF图像
type: docs
weight: 50
url: /zh/net/manipulating-tiff-images/
---

## **使用不同设置添加框架**
TIFF是一种非常灵活的格式，它允许添加具有不同维度、压缩和其他设置的不同框架。Aspose.PSD API允许您添加任何大小的任何TIFF框架，从而有助于创建复杂的文档。如果在添加过程中需要调整框架以使它们全部相等，执行以下步骤：

- 使用所需选项创建一个新的空框架或使用CreateFrameFrom方法指定输出选项复制源框架。
- 使用Resize方法将源框架/图像调整为所需的尺寸。
- 将源框架/图像像素添加到新框架。
- 将新框架添加到输出的TIFF图像中。
## **将PSD图像的图层导出为多页Tiff文件格式**
有时需要将PSD图像图层导出为多页Tiff文件格式。本文将演示如何使用Aspose.PSD for .NET API执行此任务。首先，我们将从磁盘加载PSD图像。然后，我们将遍历PSD图像图层并从相应图层创建TiffFrame。最后，我们将把生成的Tiff图像保存到磁盘上的单个文件中。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **TiffOptions配置**
开发人员可以调整[TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)类的不同属性，以获得所需的结果。在本文档中，我们将重点介绍控制结果图像属性的4个主要属性。

这些属性如下。

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

当初始化空的TiffOptions结构时，每个选项都设置为其默认值，例如压缩设置为None，BitsPerSample设置为1，Photometric设置为MinIsWhite。保存为此格式将使最终图像变为黑白，这对于此类选项组合是预期行为。要获得彩色结果，必须将上述所有属性设置为对应所需颜色空间的值，或者您可以像本文后面讨论的那样使用预定义设置初始化TiffOptions结构。以下是描述所需参数值的表格，您可以根据此表格设置TiffOptions中的所有4列，以实现所需结果。请注意，为了将任何加载/创建的图像保存为TIFF文件格式，应通过TiffOptions设置所有4个属性。  

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/Uncompressed|1/4/8/16（调色板，颜色模式）只有单通道|None|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|1/4/8/16（灰度模式）只有单通道|None|
|Palette|LZW/Uncompressed|8（调色板，颜色模式）只有单通道|Horizontal（对于LZW，相同模式实现更多压缩）|
|MinIsWhite/MinIsBlack|LZW/Uncompressed|8（灰度模式）只有单通道|Horizontal（对于LZW，相同模式实现更多压缩）|
|RGB|LZW/Uncompressed|[8,8,8]（3个RGB通道）|None/Horizontal|
|RGB|LZW/Uncompressed|[8,8,8,8]（3个RGB通道和额外的Alpha通道可能通过TiffOptions.AlphaStorage设置）。实际上，支持任何附加通道数，但每个通道必须具有8位大小，如[8,8,8,8,8,8]|None/Horizontal|
为了将任何图像格式保存为Tiff格式，应通过TiffOptions设置所有4个属性。当使用不同组合时，一些查看器（包括Windows照片查看器）可能由于其提供的有限支持而拒绝呈现生成的图像。在这种情况下，请选择其他查看器进行测试。
### **TiffOptions类的预定义设置**
为了方便用户并避免TiffOptions实例的错误配置，Aspose.PSD for .NET API暴露了另一个构造函数，接受[TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat)类型的参数。根据TiffExpectedFormat枚举中选择的值，API会自动配置TiffOptions实例的所有必需属性，以生成所需的结果。在继续查看示例代码之前，请看下面列出的TiffExpectedFormat字段及其详细信息，以更好理解用法。


- TiffExpectedFormat.Default：将字段设置为Default操作类似于TiffOptions类的默认构造函数，未设置任何压缩，并将BitsPerPixel设置为1，以生成黑白结果。建议在需要手动设置其他格式特定属性以产生所需结果时使用此字段。
- TiffExpectedFormat.TiffCcitRle：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于RLE编码。
- TiffExpectedFormat.TiffCcittFax3：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于CCITT Fax3编码。
- TiffExpectedFormat.TiffCcittFax4：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于CCITT Fax4编码。
- TiffExpectedFormat.TiffDeflateBW：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于Deflate压缩。
- TiffExpectedFormat.TiffDeflateRGB：在RGB（彩色）TIFF格式中保存结果时，特定于Deflate压缩。
- TiffExpectedFormat.TiffJpegRGB：在RGB（彩色）TIFF格式中保存结果时，特定于Jpeg压缩。
- TiffExpectedFormat.TiffJpegYCBCR：在YCBCR（彩色）TIFF格式中保存结果时，特定于Deflate压缩。
- TiffExpectedFormat.TiffLzwBW：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于LZW压缩。
- TiffExpectedFormat.TiffLzwRGB：在RGB（彩色）TIFF格式中保存结果时，特定于LZW压缩。
- TiffExpectedFormat.TiffLzwRGBA：在RGBA（带有透明度的彩色）TIFF格式中保存结果时，特定于LZW压缩。
- TiffExpectedFormat.TiffNoCompressionBW：在1 BitsPerPixel（黑白）TIFF格式中保存结果时，特定于未压缩的TIFF格式。
- TiffExpectedFormat.TiffNoCompressionRGB：在RGB（彩色）TIFF格式中保存结果时，特定于未压缩的TIFF格式。
- TiffExpectedFormat.TiffNoCompressionRGBA：在RGBA（带有透明度的彩色）TIFF格式中保存结果时，特定于未压缩的TIFF格式。


以下代码片段详细说明了在创建TiffOptions类实例时如何使用TiffExpectedFormat字段。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **支持Deflate和Adobe Deflate压缩**
TIFF（标记图像文件格式）文件格式支持各种类型的压缩，而压缩类型存储为文件中的标签（整数值）。其中一种这样的压缩方法是Adobe Deflate（以前称为Deflate）。Aspose.PSD for .NET API支持此压缩方法用于导出和创建TIFF图像。
### **使用Deflate压缩保存图像到TIFF**
将加载的图像转换为具有Deflate/Adobe Deflate压缩的TIFF非常简单，如下所示。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **使用Adobe Deflate压缩创建TiffImage**
下面提供的示例演示了使用Aspose.PSD for .NET API从头开始创建图像，使用Adobe Deflate压缩方法。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **压缩TIFF图像**
Aspose.PSD for .NET API可用于将PSD图像转换为TIFF图像格式，甚至更改结果TIFF图像的压缩。API还可用于将不同的图像作为帧存储在TIFF图像中以进行归档，同时将图像压缩至最低数据大小。无论使用何种压缩算法，任何情况下的图像压缩都应通过减少源数据大小来实现。为了实现最佳压缩比，我们可以使用索引颜色空间。下面提供的代码段通过仅使用16种索引颜色以及LZW压缩算法执行最佳压缩，但源颜色稍微抖动。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
