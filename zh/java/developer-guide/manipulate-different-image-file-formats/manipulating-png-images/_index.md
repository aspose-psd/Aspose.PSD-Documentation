---
title: 操作 PNG 图像
type: docs
weight: 30
url: /zh/java/manipulating-png-images/
---

## **为 PNG 图像指定透明度**
保存图像为 PNG 格式的一个优点是 PNG 可以具有透明背景。Aspose.PSD for Java 提供了为 PngImage & RasterImage 类指定透明度的功能，如下部分所示。Aspose.PSD for Java API 可用于在创建新的 PNG 图像或将现有图像转换为 PNG 格式时设置任何颜色为透明。为此，Aspose.PSD for Java API 公开了 TransparentColor 属性和 PngColorType 枚举，可设置以指定 PNG 图像中要呈现为透明的任何颜色。下面提供的代码片段演示了如何通过使用 PngImage 的重载构造函数并指定期望的颜色作为透明来将现有 PSD 图像转换为 PNG 图像。



{{< gist代码 "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **为 PNG 图像设置分辨率**
Aspose.PSD for Java 公开了 ResolutionSetting 类，该类可用于为包括 PNG 在内的所有图像格式设置分辨率。本文演示了如何使用 Aspose.PSD for Java API 设置 PNG 图像格式的水平和垂直分辨率参数。下面的代码片段加载一个现有的 PSD 图像，并将其转换为 PNG 格式，同时更改分辨率。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **压缩 PNG 文件**
可移植网络图形（PNG）是一种用于在网络上传输位图的无损压缩格式。在任何程序中将图像保存为 PNG 文件时，可能会要求您选择从 0 到任意最大级别的压缩级别。设置此值实际上会压缩文件大小，而不会降低图像质量。本文描述了 Aspose.PSD API 如何允许您控制 PNG 文件大小。Aspose.PSD API 可用于设置 PNG 文件格式的压缩级别，使用具有 int 类型 CompressionLevel 属性的 PngOptions 类。该属性接受从 0 到 9 的值，其中 9 是最大压缩。下面提供的代码片段演示了如何使用 Aspose.PSD for Java API 设置压缩级别。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **为 PNG 图像指定位深度**
图像的位深度是用于指示位图图像中单个像素颜色的位数。与所有其他位图格式一样，PNG 颜色深度也用比特表示，如 1 比特（2 种颜色）、2 比特（4 种颜色）、4 比特（16 种颜色）和 8 比特（256 种颜色）。Aspose.PSD for Java API 可用于使用 PngOptions 类公开的 BitDepth 属性为 PNG 图像设置位深度。目前，BitDepth 属性可设置为 1、2、4 或 8 比特用于灰度和索引颜色类型。对于所有其他颜色类型，仅支持 8 比特。下面提供的代码片段演示了如何为 PNG 图像设置位深度。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **在 PNG 图像上应用滤镜方法**
Aspose.PSD for Java 公开了 PngFilterType 枚举，可用于为 PNG 图像设置滤镜类型。下面提供的代码片段演示了如何通过使用 PngFilterType 在现有 PSD 文件上应用滤镜以生成 PNG 图像。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **更改透明 PNG 图像的背景色**
PNG 格式图像可以具有透明背景。Aspose.PSD for Java 提供了更改具有透明背景的 PNG 图像的背景色的功能。Aspose.PSD for Java API 可用于设置/更改透明 PNG 图像的背景色。下面提供的代码片段演示了如何设置/更改透明 PNG 图像的背景色。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
