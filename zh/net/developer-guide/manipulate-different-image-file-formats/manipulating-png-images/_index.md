---
title: 操纵 PNG 图像
type: docs
weight: 40
url: /zh/net/manipulating-png-images/
---

## **为 PNG 图像指定透明度**
将图像以 PNG 格式保存的优势之一是 PNG 可以具有透明背景。Aspose.PSD for .NET 提供了为 PNG 图像和位图图像指定透明度的功能，如下一节所示。Aspose.PSD for .NET API 可用于在创建新的 PNG 图像或将现有图像转换为 PNG 格式时将任何颜色设置为透明。为此，Aspose.PSD for .NET API 公开了 [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) 属性和 [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) 枚举，可以设置以指定在 PNG 图像中以透明方式呈现的任何颜色。下面提供的代码片段演示了如何通过指定所需的颜色作为透明颜色，将现有 PSD 图像转换为 PNG 图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}

## **为 PNG 图像设置分辨率**
Aspose.PSD for .NET 公开了 ResolutionSetting 类，可用于为所有图像格式（包括 PNG）设置分辨率。本文演示了如何使用 Aspose.PSD for .NET API 设置 PNG 图像格式的水平和垂直分辨率参数。下面的代码片段加载现有的 PSD 图像，并将其转换为 PNG 格式，同时更改分辨率。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}

## **压缩 PNG 文件**
便携式网络图形（PNG）是用于在网络上传输位图的无损压缩格式。当您在任何程序中将图像保存为 PNG 文件时，可能会要求您在从 0 到任意最大级别的范围内选择压缩级别。设置此值实际上会压缩文件大小，而不会降低图像质量。本文描述了 Aspose.PSD API 如何允许您控制 PNG 文件大小。Aspose.PSD API 可用于为 PNG 文件格式设置压缩级别，使用具有 int 类型 [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) 属性的 PngOptions 类。该属性接受从 0 到 9 的值，其中 9 是最大压缩级别。下面提供的代码片段演示了如何使用 Aspose.PSD for .NET API 设置压缩级别。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}

## **为 PNG 图像指定位深度**
图像处理中的位深度是用于指示位图图像中单个像素颜色的位数。与所有其他位图格式一样，PNG 色深度也用位表示，如 1 位（2 种颜色）、2 位（4 种颜色）、4 位（16 种颜色）和 8 位（256 种颜色）。Aspose.PSD for .NET API 可用于使用 PngOptions 类公开的 [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) 属性为 PNG 图像设置位深度。目前，BitDepth 属性可设置为 1、2、4 或 8 位以用于灰度和索引颜色类型。对于所有其他颜色类型，仅支持 8 位。下面提供的代码片段演示了如何为 PNG 图像设置位深度。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}

## **在 PNG 图像上应用滤镜方法**
图像处理中的位深度是用于指示位图图像中单个像素颜色的位数。与所有其他位图格式一样，PNG 色深度也用位表示，如 1 位（2 种颜色）、2 位（4 种颜色）、4 位（16 种颜色）和 8 位（256 种颜色）。Aspose.PSD for .NET API 可用于使用 PngOptions 类公开的 BitDepth 属性为 PNG 图像设置位深度。目前，BitDepth 属性可设置为 1、2、4 或 8 位以用于灰度和索引颜色类型。对于所有其他颜色类型，仅支持 8 位。下面提供的代码片段演示了如何为 PNG 图像设置位深度。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}

## **更改透明 PNG 图像的背景颜色**
PNG 格式图像可以具有透明背景。Aspose.PSD for .NET 提供了更改具有透明背景的 PNG 图像背景颜色的功能。Aspose.PSD for .NET API 可用于设置/更改透明 PNG 图像的背景颜色。下面提供的代码片段演示了如何设置/更改透明 PNG 图像的背景颜色。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
