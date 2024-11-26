---
title: Aspose.PSD .NET适配器全手册
type: docs
weight: 10
url: /zh/net/adapters/full-manual
keywords: 适配器全手册 PSD PSB AI WebP SVG PNG JPEG TIFF GIF BMP 快速入门指南
description: Aspose.PSD适配器全手册。
---

## 概览

这是关于如何使用Aspose.PSD适配器扩展Aspose.PSD功能的完整手册。
适配器是专用的Nuget软件包，可实现Aspose.PSD与其他Aspose产品的无缝集成，使您能够轻松地将文件导出到各种不受支持的格式，而无需编写额外的集成代码。

## 许可证应用

请查看有关应用许可证的完整[文章](/zh/psd/net/adapters/license)来了解更多关于适配器的信息。

{{% alert color="primary" %}}
请注意，要使用适配器，您需要同时拥有Aspose.PSD和被适配软件的许可证。
{{% /alert %}}

可以使用以下示例来应用许可证：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-License.cs" >}}

最好在项目的初始化模块中只应用一次许可证

## 引用Aspose.PSD适配器

首先，您需要从[Nuget](https://www.nuget.org/aspose.psd.adapters.imaging)引用Aspose.PSD.Adapters.Imaging，或者从[Aspose发布页面](https://releases.aspose.com/psd/net/)下载它们（适配器当前包含在主发行包的二进制文件中）到您的项目中。

![必需引用](references.png)

可能您还需要引用其他附加包

## 启用适配软件的加载器和导出器

### 启用适配器
当您需要使用适配器时，请使用以下代码：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Enable-Adapters.cs" >}}
 
### 禁用适配器
在开发过程中，您可能会遇到在某些情况下需要禁用适配器的情况。这种常见情况是，您需要在一个代码部分中使用Aspose.PSD的加载器，而在另一个代码部分中使用被适配软件的加载器。在这种情况下，只需使用以下代码：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Disable-Adapters.cs " >}}

## 使用适配器加载图像

使用适配器，您可以加载如SVG或WebP等[Aspose.PSD不支持的流行格式]((/zh/net/adapters/load-unsupported-formats))。

### 简单使用
只需使用以下代码进行加载：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Loading-Unsupported-Formats.cs" >}}

### 用于复杂图像处理的中级用法
如果您需要指定被适配软件提供的其他附加选项，请查看以下示例：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Aspose-PSD-Adapters-CSharp-Full-Manual-Complex-Loading.cs" >}}

您可以使用所有成像功能处理SVG图像，然后通过一个方法调用导出它。

## 使用适配器导出图像

在许多情况下，您不需要[打开不支持的格式](/zh/net/adapters/load-unsupported-formats)，而需要将文件[导出为此类格式](/zh/net/adapters/export-to-unsupported-formats)。在这种情况下，您应该启用导出器，并使用以下代码：
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Adapters-CSharp-Add-Imaging-Adapters-Exporting-to-Unsupported-Formats.cs" >}}

## 结论

使用Aspose.PSD适配器加载和导出文件对开发人员而言是一个改变游戏规则的举措。这些强大的Nuget软件包允许您将Aspose.PSD与其他Aspose产品无缝集成，从而更轻松地打开并处理不支持的文件格式，而无需编写额外的集成代码。使用Aspose.PSD适配器，您可以通过消除额外的代码和手动转换过程来节省时间和精力。无论您是在加载还是导出文件，Aspose.PSD适配器都提供了一种便捷而高效的解决方案，为您的项目带来新的可能性。体验Aspose.PSD适配器的力量，将您的开发流程提升至新的高度。
