---
title: Psd混合选项操作
weight: 100
type: docs
description: Aspose.PSD for Python可以帮助您使用简单的代码更新混合选项。
keywords: [混合选项, 混合, 添加效果, 改变不透明度, 改变阴影颜色, 添加阴影, psd api, python, 代码示例]
url: zh/python-net/blending-options/
---

## **概述**
在Aspose.PSD for Python中，您可以操作混合选项来修改PSD图像中图层的外观。您提供的代码演示了如何使用混合选项的一些示例。

首先，该代码加载一个PSD图像，并将其保存为原始PNG文件。然后，它修改特定图层的不透明度和混合模式。例如，它将第二图层的不透明度设置为100，并将第五图层的混合模式更改为“色相”。

此外，代码向某些图层添加混合效果。它使用add_drop_shadow()方法向第七图层添加阴影效果。阴影角度设置为30度，阴影颜色设置为RGB(255, 0, 0)。

此外，代码将第九图层的混合模式更改为“变亮”。它还使用add_color_overlay()方法向第五图层添加颜色叠加效果。颜色叠加颜色设置为RGB(30, 50, 0)，不透明度设置为150。

最后，代码将修改后的图像保存为更新后的PNG文件。

总的来说，Aspose.PSD for Python提供了广泛的混合选项，可用于操作PSD图像中图层的外观。这些选项包括修改不透明度，更改混合模式以及添加各种混合效果，如投影阴影和颜色叠加。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-blending-options.py" >}}
