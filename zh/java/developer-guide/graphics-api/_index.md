---
title: 使用图形API编辑PSD文件中的图层
weight: 100
type: docs
description: 在Java中使用Aspose.PSD的图形API的示例
keywords: [更新图层, 画圆, 画椭圆, 填充圆, 图形, psd api, java, 代码示例]
url: zh/java/graphics-api/
---

## **概述**
首先，使用Image.load()方法加载PSD文件或从头开始创建Psd Image。使用inputFile变量来代表你的PSD文件路径，并在需要时使用loadOpt指定任何加载选项。

接下来，使用psdImage.getLayers()[0]语法访问PSD图像的第一个图层，以获取对图层对象进行操作的引用。

要编辑图层，通过将图层作为参数传递来创建一个Graphics对象。此对象提供用于绘制形状和应用画笔的各种方法。

Pen对象用于定义形状轮廓的颜色和粗细。类似地，像LinearGradientBrush这样的画笔用于定义填充颜色。

使用例如graphics.drawEllipse()来绘制形状的轮廓和graphics.fillEllipse()来填充形状等方法将形状绘制在图层上。

在对图层进行所需更改后，使用psdImage.save()保存修改后的PSD图像。

此外，您可以使用适当的选项将修改后的图像保存为PNG等其他格式。

就是这样！您已成功使用Aspose.PSD的Java图形API编辑PSD文件中的图层。探索更多Aspose.PSD库的功能和功能，以增强您的图像编辑能力。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
