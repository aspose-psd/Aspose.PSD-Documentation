---
title: 使用Java更新PSD填充图层
weight: 100
type: docs
description: 使用各种调整图层的示例，包括颜色填充、渐变填充和图案填充
keywords: [填充图层, 颜色填充, 渐变填充, 图案填充, psd api, java, 代码示例]
url: zh/java/psd-fill-layer-editing/
---

## **概述**

创建常规图层涉及使用createRegularLayer函数，该函数需要参数来定义图层的位置和大小。此函数创建一个新图层，设置其边界，并使用指定的颜色填充它。

对于颜色填充图层，您可以使用FillLayer.createInstance方法与FillType.Color参数。一旦创建填充图层，通过fill_settings属性访问其填充设置，并使用ColorFillSettings类的color属性设置所需的颜色。在这种情况下，颜色设置为Color.getCoral()。此外，填充图层的裁剪属性设置为1，使其作为剪裁蒙版。

渐变填充图层类似地使用FillLayer.create_instance方法创建，但使用FillType.Gradient参数。与颜色填充图层一样，您可以通过fill_settings访问填充设置，并设置渐变颜色点和透明度点。在此示例中，使用GradientColorPoint类定义渐变颜色点，使用GradientTransparencyPoint类定义透明度点。填充图层的裁剪属性也设置为1。

图案填充图层使用FillLayer.createInstance与FillType.Pattern参数创建。再次，通过fill_settings访问填充设置，并设置图案数据及其他属性。在此代码中，使用PatternFillSettings类定义图案数据，并将裁剪属性设置为1。

创建填充图层后，使用addLayer方法将它们添加到PSD图像中，为每个填充图层指定显示名称和其他属性。

最后，使用提供的代码保存PSD图像及其相应的PNG图像。PNG选项已配置为使用真彩色以及透明度。

请参阅完整示例以了解更多详细信息。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
