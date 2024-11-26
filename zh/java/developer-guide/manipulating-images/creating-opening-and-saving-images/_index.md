---
title: 创建、打开和保存图像
type: docs
weight: 30
url: /zh/java/creating-opening-and-saving-images/
---

## **创建图像文件**
Aspose.PSD for Java 允许开发人员创建他们自己的图像。使用 Image 类公开的静态 Create 方法来创建新图像。您只需为所需的输出图像格式提供 ImageOptions 命名空间中的一个类的适当对象即可。要创建图像文件，首先创建 ImageOptions 命名空间中一个类的实例。这些类确定输出图像格式。以下是 ImageOptions 命名空间中的一些类（请注意，目前仅支持 PSD 文件格式系列的创建）：

PsdOptions 设置用于创建 PSD 文件的选项。可以通过设置输出路径或设置流来创建图像文件。
### **通过设置路径创建**
从 ImageOptions 命名空间创建 PsdOptions 并设置各种属性。要设置的最重要属性是 Source 属性。此属性指定图像数据存储位置（在文件或流中）。在下面的示例中，源是一个文件。设置属性后，将对象传递给其中一个静态 Create 方法，并传递宽度和高度参数。宽度和高度以像素为单位定义。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **使用流创建**
使用流创建图像的过程与使用路径相同。唯一的区别是，您需要创建 StreamSource 的实例，通过将 Stream 对象传递给其构造函数并将其分配给 Source 属性来实现。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **打开图像文件**
开发人员可以使用 Aspose.PSD for Java API 打开现有的 PSD 图像文件以进行不同的操作，如向图像添加效果或将现有文件转换为另一种格式。无论目的是什么，Aspose.PSD 都提供了两种标准方法来打开现有文件：从文件或从流中。
### **从磁盘打开**
通过将路径和文件名作为参数传递给 Image 类的静态方法 Load 来打开图像文件。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **使用流打开**
有时，需要打开的图像存储为流。在这种情况下，使用 Load 方法的重载版本。该方法接受一个 Stream 对象作为参数来打开图像。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **将图像加载为图层**
本文演示了使用 Aspose.PSD 加载图像作为图层的用法。Aspose.PSD API 提供了高效且易于使用的方法来实现此目的。Aspose.PSD 已经公开了 PsdImage 类的 AddLayer 方法，将图像添加到 PSD 文件作为图层。

将图像加载到 PSD 文件作为图层的步骤简单如下：

- 使用指定的宽度和高度使用 PsdImage 类创建图像的实例。
- 使用 Image 类的工厂方法 Load 加载 PSD 文件作为图像。
- 创建 Layer 类的实例并将 PSD 图层分配给它。
- 使用 PsdImage 类公开的 AddLayer 方法添加创建的图层。
- 保存结果。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **保存图像文件**
Aspose.PSD 允许您从头开始创建图像文件。它还提供了编辑现有图像文件的方法。一旦创建或修改图像，通常将文件保存到磁盘。Aspose.PSD 为您提供了将图像保存到磁盘的方法，可以指定路径或使用 Stream 对象。
### **保存到磁盘**
Image 类表示图像对象，因此该类提供了创建、加载和保存图像文件所需的所有工具。使用 Image 类的 Save 方法保存图像。Save 方法的一个重载版本接受文件位置作为字符串。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **保存到流**
Save 方法的另一个重载版本接受 Stream 对象作为参数，并将图像文件保存到流中。

如果通过指定 Image 构造函数中的 CreateOptions 之一来创建图像，则会自动将图像保存到在 Image 类初始化期间提供的路径或流中，方法是调用不接受任何参数的 Save 方法。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **设置替换缺失字体**
开发人员可以使用 Aspose.PSD for Java API 加载现有的 PSD 图像文件，例如在将 PSD 文档另存为光栅图像（PNG、JPG 和 BMP 格式）时设置默认字体名称。此默认字体应用于所有缺失字体（在当前操作系统中找不到的字体）。一旦修改图像，文件将保存到磁盘。



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}
