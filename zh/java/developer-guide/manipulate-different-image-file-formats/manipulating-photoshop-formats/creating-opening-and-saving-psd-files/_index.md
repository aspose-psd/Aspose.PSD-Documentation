---
title: 创建、打开和保存PSD文件
type: 文档
weight: 10
url: /zh/java/creating-opening-and-saving-psd-files/
---

## **将图像导出为PSD**
PSD（Photoshop文档）是Adobe Photoshop用于处理图像的默认文件格式。Aspose.PSD允许您加载、编辑和保存PSD文件，以便在Photoshop中打开和编辑。本文展示了如何使用Aspose.PSD将文件保存为PSD，并讨论了保存到该格式时可以使用的一些设置。PsdOptions是ImageOptions命名空间中的一个专门的类，用于将图像导出为PSD。要导出为PSD，需要创建一个Image类的实例，可以是从现有图像文件（例如缩略图）加载的，也可以是从头开始创建的。本文对此进行了解释。在下面的示例中，从头开始创建了一个图像。创建后填充像素数据，使用Image类的Save方法保存图像，并将PsdOptions对象作为第二个参数传递。PsdOptions类的几个属性可以设置为高级转换。其中一些属性是ColorMode、CompressionMethod和Version。Aspose.PSD通过CompressionMethod枚举支持以下压缩方法：

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

通过ColorModes枚举支持以下颜色模式：

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



可以添加其他资源，如PSD v4.0、v5.0及更高版本的缩略图资源，或PSD v4.0及更高版本的网格和参考线资源。以下代码创建了一个BMP文件，填充像素并以RLE压缩和灰度色彩模式保存为PSD。以下代码片段向您展示如何将图像导出为PSD。



## **将图像导入PSD图层**
本文演示了使用Aspose.PSD将图像添加或导入到PSD图层的用法。Aspose.PSD API提供了高效且易于使用的方法来实现此目标。Aspose.PSD公开了Layer类的DrawImage方法，用于将图像添加/导入到PSD文件中。DrawImage方法需要位置和图像值，以向PSD文件添加/导入图像。将图像导入到PSD图层的步骤如下所示：

- 使用Image类公开的工厂方法Load将PSD文件作为图像加载。
- 创建一个Layer类的实例，并将PSD图像图层分配给它。
- 加载需要添加的图像或从头开始创建一个。
- 调用Layer.DrawImage方法，同时指定位置和图像实例。
- 保存结果。



以下代码片段向您展示如何将图像导入到PSD图层。

## **从PSD文件创建缩略图**
PSD是Adobe Photoshop应用程序的原生文档格式。Adobe Photoshop（5.0版本及更高版本）在图像资源块中存储用于预览显示的缩略图信息，该资源块由一个初始28字节的标头组成，后跟按RGB（红色，绿色，蓝色）顺序排列的JFIF缩略图。Aspose.PSD API提供了一个易于使用的机制来访问PSD文件的资源。这些资源还包括缩略图资源，可以根据应用程序的需求获取并保存到磁盘。以下代码片段向您展示如何从PSD文件创建缩略图。

## **创建索引PSD文件**
Aspose.PSD for Java API可以从头开始创建索引PSD文件。本文演示了使用PsdOptions和PsdImage类创建Indexed PSD时，在新创建的画布上绘制一些形状的用法。创建Indexed PSD文件需要以下简单的步骤：

- 创建一个PsdOptions实例并设置其源。
- 将PsdOptions的ColorMode属性设置为ColorModes.Indexed。
- 从RGB空间创建一个新的颜色调色板，并将其设置为PsdOptions的Palette属性。
- 将CompressionMethod属性设置为所需的压缩算法。
- 通过调用PsdImage.Create方法创建一个新的PSD图像。
- 根据需要绘制图形或执行其他操作。
- 调用PsdImage.Save方法提交所有更改。



以下代码片段向您展示如何创建索引PSD文件。

## **将PSD图层导出为光栅图像**
Aspose.PSD for Java允许您将PSD文件中的图层导出为光栅图像。请使用Aspose.PSD.FileFormats.Psd.Layers.Layer.Save方法将图层导出为图像。以下示例代码加载一个PSD文件，并使用Aspose.PSD.FileFormats.Psd.Layers.Layer.Save将其每个图层导出为PNG图像。将所有图层导出为PNG图像后，您可以使用您喜爱的图像查看器打开它们。以下代码片段向您展示如何将PSD图层导出为光栅图像。
