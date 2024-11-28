---
title: 支持填充图层
type: docs
weight: 50
url: /zh/java/support-of-fill-layers/
---

## **使用颜色填充的填充图层支持**
本文演示了如何使用颜色填充PSD图层。请使用Aspose.PSD.FileFormats.Psd.Layers.FillLayer来向PSD图层添加颜色。以下代码片段加载了一个PSD文件，访问了FillLayer类，并使用FillLayer.FillSettings属性设置了颜色。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **使用渐变填充的填充图层支持**
本文演示了使用渐变填充来填充PSD图层的用法。Aspose.PSD APIs提供了高效且易于使用的方法来实现此目标。Aspose.PSD公开了GradientColorPoint和GradientTransparencyPoint类，以将渐变效果添加到图层中。

填充PSD图层以渐变填充的步骤如下：

- 使用Image类公开的工厂方法Load加载PSD文件作为图像。
- 设置FillLayer对象的各种属性。
- 创建包含所需颜色和颜色位置的ColorPoints列表。
- 创建包含所需透明度和透明点位置的transparencyPoints列表。
- 调用FillLayer.Update方法。
- 保存结果。


以下代码片段展示了如何将渐变填充添加到PSD图层。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **使用颜色填充的描边效果**
本文演示了如何使用颜色填充渲染描边效果。描边效果用于向图层和形状添加描边和边框。它可用于创建纯色线条、多彩的渐变色以及图案边框。

使用颜色填充渲染描边效果的步骤如下：

- 设置**LoadEffectsResource**属性。
- 使用Image类公开的工厂方法Load加载PSD文件作为图像，并定义**PsdLoadOptions**。
- 设置**ColorFillSetting**的各种属性。
- 保存结果。

以下代码片段展示了如何使用颜色填充渲染描边效果。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}
