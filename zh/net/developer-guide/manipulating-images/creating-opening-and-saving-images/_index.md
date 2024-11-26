---
title: 创建、打开和保存图像
type: docs
weight: 30
url: /zh/net/creating-opening-and-saving-images/
---

## **创建图像文件**
Aspose.PSD for .NET 允许开发人员创建自己的图像。使用 Image 类公开的静态 Create 方法创建新图像。您只需要为所需的输出图像格式提供 ImageOptions 命名空间中一个类的适当对象即可。要创建图像文件，首先创建 ImageOptions 命名空间中一个类的实例。这些类确定了输出图像格式。以下是 ImageOptions 命名空间中的一些类（请注意，当前仅支持 PSD 文件格式系列用于创建）：

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) 设置创建 PSD 文件的选项。通过设置输出路径或流来创建图像文件。
### **通过设置路径创建**
从 [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 命名空间创建 PsdOptions 并设置各种属性。设置的最重要属性是 Source。此属性指定图像数据的位置（在文件或流中）。在下面的示例中，源是一个文件。设置属性后，将对象传递给其中一个静态 [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) 方法，以及宽度和高度参数。宽度和高度以像素为单位定义。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **使用流创建**
使用流创建图像的过程与使用路径相同。唯一的区别是需要通过将 Stream 对象传递给构造函数，然后将其分配给 Source 属性创建 [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) 的实例。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **打开图像文件**
开发人员可以使用 Aspose.PSD for .NET API 打开现有的 PSD 图像文件以进行不同的操作，例如向图像添加效果或将现有文件转换为其他格式。无论目的是什么，Aspose.PSD 提供了两种打开现有文件的标准方式：从文件或从流中。
### **从磁盘打开**
通过将路径和文件名作为参数传递给 Image 类公开的静态 Load 方法来打开图像文件。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **使用流打开**
有时需要打开的图像存储为流。在这种情况下，使用 Load 方法的重载版本。它接受一个流对象作为参数来打开图像。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **将图像作为图层加载**
本文演示了使用 Aspose.PSD 将图像作为图层加载的用法。Aspose.PSD API 提供了高效且易于使用的方法来实现这一目标。Aspose.PSD 公开了 PsdImage 类的 AddLayer 方法，以将图像添加到 PSD 文件作为一个图层。

将图像加载到 PSD 作为图层的步骤如下简单：

- 使用指定宽度和高度创建 PsdImage 类的图像实例。
- 使用 Image 类公开的工厂方法 Load 加载 PSD 文件作为图像。
- 创建 Layer 类的实例并将 PSD 图像图层分配给它。
- 使用 PsdImage 类公开的 AddLayer 方法添加创建的图层。
- 保存结果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **从流加载图像作为图层**
本文演示了使用 Aspose.PSD 从流加载图像作为图层的用法。要从流加载图像，只需将包含图像的流对象传递给 Layer 类的构造函数。使用 PsdImage 类公开的 AddLayer 方法添加创建的图层并保存结果。

这是示例代码。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **保存图像文件**
Aspose.PSD 允许您从头开始创建图像文件。它还提供编辑现有图像文件的手段。一旦创建或修改图像，通常将文件保存到磁盘。Aspose.PSD 为将图像保存到磁盘提供了方法，可以通过指定路径或使用 Stream 对象进行保存。
### **保存到磁盘**
Image 类代表一个图像对象，因此这个类提供了创建、加载和保存图像文件所需的所有工具。使用 Image 类的 Save 方法保存图像。Save 方法的重载版本之一接受文件位置作为字符串。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **保存到流**
Save 方法的另一个重载版本接受 Stream 对象作为参数，并将图像文件保存到流中。

如果指定了 Image 构造函数中的任何 CreateOptions 来创建图像，则通过调用不接受任何参数的 Save 方法，该图像将自动保存到在初始化 Image 类时提供的路径或流中。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **设置替换丢失字体**
开发人员可以使用 Aspose.PSD for .NET API 加载现有的 PSD 图像文件以进行不同的操作，例如将 PSD 文档另存为光栅图像（PNG、JPG 和 BMP 格式）时设置默认字体名称。此默认字体应用于所有缺失的字体（即当前操作系统中未找到的字体）。一旦修改图像，文件将保存到磁盘。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
