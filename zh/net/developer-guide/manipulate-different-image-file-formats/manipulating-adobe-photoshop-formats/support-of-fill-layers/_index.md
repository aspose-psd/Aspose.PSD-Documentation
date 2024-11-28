---
title: 支持填充图层
type: docs
weight: 90
url: /zh/net/support-of-fill-layers/
---

## **使用图案填充图层**
本文演示了如何使用图案填充来填充[PSD](https://wiki.fileformat.com/image/psd/)图层。图案是用于填充图像区域的图像、颜色、阴影或线条。请使用 Aspose.PSD.FileFormats.Psd.Layers.FillLayer 来在 PSD 图层中添加图案。以下代码片段加载一个 PSD 文件，访问 [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 类，并使用 [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) 属性设置图案。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



以下是另一个示例，演示了如何使用 [Aspose.PSD](https://products.aspose.com/psd/net)通过使用 [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)和 [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings) * *来渲染图案。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **使用渐变填充图层**
本文演示了如何使用渐变填充来填充 PSD 图层。Aspose.PSD API 提供了高效且易于使用的方法来实现此目标。Aspose.PSD 已经暴露了 [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) 和 [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) 类，以在图层中添加渐变效果。

`以下是将 PSD 图层填充渐变的简单步骤：

- 使用 [Image.Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) 工厂方法从 PSD 文件加载图像。
- 设置 [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 对象的设置属性。
- 创建一个颜色点列表，包含所需颜色和颜色位置。
- 创建一个透明度点列表，包含所需的不透明度和透明度点位置。
- 调用 [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) 方法。
- 保存结果。


以下代码片段演示了如何向 PSD 图层添加渐变填充。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}


**这里是另一个示例，使用 [GradientFillSettings.GradientType](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** 属性来向 PSD 图层填充渐变。Aspose.PSD 通过 GradientType 枚举支持以下渐变类型：

- **GradientType.Linear:** 线性渐变中，颜色从起始色向终止色以直线过渡。
- **GradientType.Radial:** 辐射渐变中，颜色从起始点向外呈圆形扫射。
- **GradientType.Angle:** 角度渐变绕起始点逆时针扫过。
- **GradientType.Reflected:** 反射渐变中，颜色在起始点两边镜像。
- **GradientType.Diamond:** 菱形渐变在起始点创建菱形形状。


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **支持渐变填充图层的缩放属性**
本文演示了如何使用 Aspose.PSD for .NET 缩放具有渐变填充的 FillLayer。为此，在 IGradientFillSettings 中添加了一个名为 Scale 的新属性。

以下是演示如何使用 Scale 属性的代码示例。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **使用颜色填充图层**
本文演示了如何使用颜色填充 PSD 图层。请使用 Psd.Layers.FillLayer 类在 PSD 图层中添加颜色。以下代码片段加载一个 PSD 文件，访问 Fill layer 类并使用 [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) 属性设置颜色。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


