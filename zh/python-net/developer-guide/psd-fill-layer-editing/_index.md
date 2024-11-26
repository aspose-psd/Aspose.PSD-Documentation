---
title: 用Python更新PSD填充图层
weight: 100
type: 文档
description: 使用所有类型的调整图层的示例，包括颜色填充，渐变填充和图案填充
keywords: [填充图层，颜色填充，渐变填充，图案填充，psd api，python，代码示例]
url: zh/python-net/psd-fill-layer-editing/
---

## **概述**

要创建一个常规图层，可以使用提供的 create_regular_layer 函数。此函数使用左侧，顶部，宽度和高度参数来定义图层的位置和大小。它创建一个新图层，设置其边界，并用指定颜色填充。

要创建一个颜色填充图层，可以使用 FillLayer.create_instance 方法并带有 FillType.COLOR 参数。创建填充图层后，可以使用 fill_settings 属性访问其填充设置，并使用 ColorFillSettings 类的 color 属性设置颜色。在提供的代码中，颜色设置为Color.coral。填充图层的裁剪属性设置为1，使图层作为裁剪蒙版。

要创建渐变填充图层，可以使用 FillLayer.create_instance 方法并带有 FillType.GRADIENT 参数。类似于颜色填充图层，可以使用 fill_settings 属性访问填充设置并设置渐变颜色点和透明度点。在提供的代码中，使用 GradientColorPoint 类来定义渐变颜色点，并使用GradientTransparencyPoint 类来定义透明度点。填充图层的裁剪属性也设置为1。

要创建图案填充图层，可以使用 FillLayer.create_instance 方法并带有 FillType.PATTERN 参数。同样，可以使用 fill_settings 属性访问填充设置并设置图案数据和其他属性。在提供的代码中，使用 PatternFillSettings 类来定义图案数据，并将裁剪属性设置为1。

在创建填充图层之后，可以使用 add_layer 方法将它们添加到PSD图像中。还可以为每个填充图层指定显示名称和其他属性。

最后，可以使用提供的代码保存PSD图像和相应的PNG图像。设置 PNG 选项以使用带有透明度的真彩色。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-fill-layer-editing.py" >}}
