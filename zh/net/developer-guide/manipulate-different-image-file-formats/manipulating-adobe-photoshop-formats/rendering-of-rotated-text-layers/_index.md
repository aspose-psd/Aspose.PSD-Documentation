---
title: 旋转文本图层的渲染
type: docs
weight: 40
url: /zh/net/rendering-of-rotated-text-layers/
---

## **旋转文本图层的渲染**
Aspose.PSD提供了旋转文本图层的渲染功能。在下面的示例中，通过将文件路径传递给Image类的静态Load方法来加载现有PSD文件。现在调用[PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage)实例的[Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index)方法。

以下代码片段向您展示了如何渲染旋转的[文本图层](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer)。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}

## **旋转矢量蒙版和文本图层**
Aspose.PSD提供了旋转矢量蒙版和文本图层的功能。Aspose.PSD已经公开了RotateFlip方法以旋转矢量蒙版和文本图层。旋转图层的步骤如下简单：

- 使用Image类公开的工厂方法Load将PSD文件加载为图像。
- 设置所需的[RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype)。
- 调用[RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip)方法。
- 保存结果。

以下代码片段向您展示了如何旋转矢量蒙版和文本图层。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
