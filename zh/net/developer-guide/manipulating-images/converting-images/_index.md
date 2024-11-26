---
title: 图像转换
type: docs
weight: 20
url: /zh/net/converting-images/
---

## **将图像转换为黑白和灰度**
有时您可能需要将彩色图像转换为黑白或灰度，以便进行打印或存档。本文演示了如何使用 Aspose.PSD for .NET API 使用以下两种方法实现此目的。

- 二值化
- 灰度化
### **二值化**
为了理解二值化的概念，重要的是定义二进制图像；即每个像素只能有两个可能值的数字图像。通常，用于二进制图像的两种颜色是黑色和白色，尽管可以使用任意两种颜色。二值化是将图像转换为双级别的过程，意味着每个像素都存储为一个比特（0或1），其中0表示无颜色，1表示有颜色。Aspose.PSD for .NET API 目前支持两种二值化方法。
#### **使用固定阈值进行二值化**
以下代码片段显示了如何将固定阈值二值化应用于图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}

#### **使用 Otsu 阈值进行二值化**
以下代码片段显示了如何将 Otsu 阈值二值化应用于图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}

### **灰度化**
灰度化是将连续色调图像转换为具有不连续灰色阴影的图像的过程。以下代码片段显示了如何使用灰度化。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}

## **将 GIF 图像图层转换为 TIFF 图像**
有时需要将 PSD 图像的图层提取并转换为另一种光栅图像格式以满足应用程序需求。Aspose.PSD API 支持将 PSD 图像的图层提取并转换为另一种光栅图像格式的功能。首先，我们将创建一个图像实例并从本地磁盘加载 PSD 图像，然后我们将迭代图层中的每个图层。然后我们将将块转换为 TIFF 图像。以下代码片段显示了如何将 PSD 图像图层转换为 TIFF 图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}

## **将 CMYK PSD 转换为 CMYK TIFF**
使用 Aspose.PSD for .NET，开发人员可以将 CMYK PSD 文件转换为 CMYK tiff 格式。本文展示了如何使用 Aspose.PSD 将 CMYK PSD 文件导出/转换为 CMYK tiff 格式。使用 Aspose.PSD for .NET 您可以加载 PSD 图像，然后可以使用 [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) 类设置各种属性，然后保存或导出该图像。以下代码片段显示了如何实现此功能。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}

## **导出图像**
除了丰富的图像处理例程之外，Aspose.PSD 还提供了专门的类来将 PSD 文件格式转换为其他格式。使用此库，PSD 图像转换非常简单和直观。以下是 [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 命名空间中用于此目的的一些专用类。

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

使用 Aspose.PSD for .NET API 可以轻松导出 PSD 图像。您只需要从 [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 命名空间中选择适当类的对象即可。通过使用这些类，您可以轻松地将在 Aspose.PSD for .NET 中创建、编辑或加载的任何图像导出到任何支持的格式。

## **合并图像**
此示例使用 Graphics 类，演示了如何将两个或更多图像合并为单个完整图像。为了演示该操作，示例创建了一个新的 PsdImage，并使用 Graphics 类公开的 Draw Image 方法在画布表面上绘制图像。使用 Graphics 类，可以组合两个或更多图像，以便生成的图像看起来是完整图像，图像部分之间没有空白和页面。画布大小必须等于生成图像的大小。以下是演示如何使用 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 类的 [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) 方法将图像组合成单个图像的代码演示。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **扩展和裁剪图像**
Aspose.PSD API 允许您在图像转换过程中扩展或裁剪图像。开发人员需要创建一个具有 X 和 Y 坐标的矩形，并指定矩形框的宽度和高度。矩形的 X、Y 和宽度、高度将描述已加载图像的扩展或裁剪。如果在图像转换期间需要扩展或裁剪图像，请执行以下步骤：

1. 创建 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 类的实例并加载现有图像。
2. 创建 ImageOption 类的实例。
3. 创建 [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) 类的实例，并初始化矩形的 X、Y 和宽度、高度。
4. 在调用 RasterImage 类的 [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) 方法时，传递输出文件名、图像选项和矩形对象作为参数。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **读取和写入 XMP 数据到图像**
XMP（可扩展元数据平台）是 ISO 标准。XMP 标准化了用于定义和处理可扩展元数据的数据模型、序列化格式和核心属性。它还提供了将 XMP 信息嵌入到诸如 JPEG 等流行图像中的指南，而不会破坏那些不支持 XMP 的应用程序的可读性。使用 Aspose.PSD for .NET API，开发人员可以读取或写入 XMP 元数据到图像。本文演示了如何从图像中读取 XMP 元数据并将 XMP 元数据写入图像。
### **创建 XMP 元数据，写入并从文件读取**
通过 Xmp 命名空间，开发人员可以创建 XMP 元数据对象并将其写入图像。以下代码片段显示了如何使用 [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp) 命名空间中包含的 XmpHeaderPi、XmpTrailerPi、XmpMeta、XmpPacketWrapper、PhotoshopPackage 和 DublinCorePackage 包。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}

## **在多线程环境中导出图像**
Aspose.PSD for .NET 现在支持在多线程环境中转换图像。Aspose.PSD for .NET 确保在多线程环境中执行代码期间操作的优化性能。Aspose.PSD for .NET 中的所有 [image option](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 类（例如 BmpOptions、TiffOptions、JpegOptions 等）都实现了 IDisposable 接口。因此，开发人员必须适当地处理设置 Source 属性的图像选项类对象。以下代码片段演示了所述功能。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}

Aspose.PSD 现在在多线程环境中支持 SyncRoot 属性。开发人员可以使用此属性来同步对源流的访问。以下代码片段演示了如何使用 SyncRoot 属性。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
