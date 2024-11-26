---
title: 带颜色填充的描边效果
type: docs
weight: 60
url: /zh/net/stroke-effect-with-color-fill/
---

## **带颜色填充的描边效果**
本文演示了如何渲染带颜色填充的描边效果。描边效果用于在图层和形状上添加描边和边框。它可以用于创建实色线条、丰富多彩的渐变，以及图案边框。

渲染带颜色填充的描边效果的步骤如下所示：

- 设置 [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource) 属性。
- 使用 Image 类的 Load 工厂方法将 PSD 文件加载为图像，并定义 [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions)。
- 设置 [**ColorFillSetting**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings) 的设置属性。
- 保存结果。

下面的代码片段展示了如何渲染带颜色填充的描边效果。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
