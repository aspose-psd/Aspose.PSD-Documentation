---
title: 转换图像
type: docs
weight: 20
url: /zh/java/转换图像/
---

## **将图像转换为黑白和灰度**
有时您可能需要将彩色图像转换为黑白或灰度以进行打印或归档。本文演示了如何使用Aspose.PSD for Java API通过以下两种方法实现此目的。

- 二值化
- 灰度化
### **二值化**
为了理解二值化的概念，定义二值图像很重要；即每个像素只能有两种可能值的数字图像。通常，二值图像使用黑色和白色两种颜色，虽然任何两种颜色都可以使用。二值化是将图像转换为双级的过程，意味着每个像素都被存储为单个位（0或1），其中0表示无色彩，1表示有色彩。Aspose.PSD for Java API当前支持两种二值化方法。
#### **使用固定阈值进行二值化**
以下代码片段展示了如何将固定阈值二值化应用于图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **使用Otsu阈值进行二值化**
以下代码片段展示了如何将Otsu阈值二值化应用于图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **灰度化**
灰度化是将连续色调图像转换为具有不连续灰色阴影的图像的过程。以下代码片段展示了如何使用灰度化。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **将GIF图像图层转换为TIFF图像**
有时需要将PSD图像的图层提取并转换为另一种栅格图像格式以满足应用程序需求。Aspose.PSD API支持将PSD图像的图层提取并转换为另一种栅格图像格式的功能。首先，我们将创建图像实例并从本地磁盘加载PSD图像，然后我们将在Layer属性中对每个图层进行迭代。然后我们将将块转换为TIFF图像。以下代码片段展示了如何将PSD图像图层转换为TIFF图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **将CMYK PSD转换为CMYK TIFF**
使用Aspose.PSD for Java，开发人员可以将CMYK PSD文件转换为CMYK tiff格式。本文展示了如何使用Aspose.PSD将CMYK PSD文件导出/转换为CMYK tiff格式。使用Aspose.PSD for Java，您可以加载PSD图像，然后可以使用TiffOptions类设置各种属性并保存或导出图像。以下代码片段展示了如何实现此功能。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **导出图像**
除了丰富的图像处理例程外，Aspose.PSD还提供专门的类来将PSD文件格式转换为其他格式。使用此库，PSD图像的转换非常简单直观。以下是ImageOptions命名空间中用于此目的的一些专门的类。

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

使用Aspose.PSD for Java API导出PSD图像非常简单。您只需要来自ImageOptions命名空间的适当类的对象。通过使用这些类，您可以轻松地将使用Aspose.PSD for Java创建、编辑或仅加载的任何图像导出到任何支持的格式。
## **合并图像**
此示例使用Graphics类，展示了如何将两个或多个图像合并为单个完整图像。为了演示该操作，示例创建了一个新的PsdImage，并使用Graphics类公开的Draw Image方法在画布表面上绘制图像。使用Graphics类，可以以这样的方式组合两个或多个图像，使得生成的图像看起来像一个完整的图像，其中图像部分之间没有空间，也没有页面。画布大小必须等于生成图像的大小。以下是代码示例，展示了如何使用Graphics类的Draw Image方法将图像组合成单个图像。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **扩展和裁剪图像**
Aspose.PSD API允许您在图像转换过程中扩展或裁剪图像。开发人员需要创建具有X和Y坐标的矩形，并指定矩形框的宽度和高度。矩形的X、Y、宽度和高度将描述加载图像的扩展或裁剪。如果需要在图像转换过程中扩展或裁剪图像，请执行以下步骤：

1. 创建RasterImage类的实例并加载现有图像。
1. 创建ImageOption类的实例。
1. 创建Rectangle类的实例并初始化矩形的X、Y、宽度和高度。
1. 调用RasterImage类的Save方法，同时传递输出文件名、图像选项和矩形对象作为参数。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **读取和写入XMP数据到图像**
XMP（可扩展元数据平台）是一种ISO标准。XMP标准化了数据模型、序列化格式和用于定义和处理可扩展元数据的核心属性。它还提供了将XMP信息嵌入到常见图像中（如JPEG）而不破坏不支持XMP的应用程序的可读性的指南。使用Aspose.PSD for Java API，开发人员可以读取或写入图像的XMP元数据。本文演示了如何从图像中读取XMP元数据并向图像写入XMP元数据。
### **创建XMP元数据、写入并从文件读取**
开发人员可以使用XMP命名空间创建XMP元数据对象并将其写入图像。以下代码片段展示了如何使用XMP命名空间中包含的XmpHeaderPi、XmpTrailerPi、XmpMeta、XmpPacketWrapper、PhotoshopPackage和DublinCorePackage包。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **在多线程环境中导出图像**
Aspose.PSD for Java现在支持在多线程环境中转换图像。Aspose.PSD for Java确保在多线程环境中执行代码时操作的优化性能。Aspose.PSD for Java中的所有图像选项类（例如BmpOptions、TiffOptions、JpegOptions等）都实现了IDisposable接口。因此，开发人员在设置了Source属性的情况下必须正确释放图像选项类对象。以下代码片段演示了所述功能。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}

Aspose.PSD现在支持在多线程环境中使用SyncRoot属性。开发人员可以使用此属性来同步访问源流。以下代码片段演示了如何使用SyncRoot属性。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
