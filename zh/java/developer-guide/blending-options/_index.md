---
title: PSD混合选项操作
weight: 100
type: docs
description: Aspose.PSD for Java可以帮助您使用简单的代码片段调整混合选项。
keywords: [混合选项，混合，添加效果，改变不透明度，改变阴影颜色，添加阴影，psd api，java，代码示例]
url: zh/java/blending-options/
---

## **概述**
使用Aspose.PSD for Java，您可以修改混合选项以增强PSD图像中图层的外观。下面是一个展示如何利用混合选项的Java代码示例。

首先，代码加载一个PSD图像并将其保存为原始的PNG文件。随后，它改变特定图层的不透明度和混合模式。例如，它将第二图层的不透明度设置为100，并将第五图层的混合模式更改为色调。

此外，代码将混合效果应用到指定的图层。通过使用`addDropShadow()`方法，它为第七个图层引入了一个投影阴影效果，指定阴影角度为30度，阴影颜色为RGB(255, 0, 0)。

此外，代码将第九图层的混合模式调整为Lighten。另外，它通过`addColorOverlay()`方法向第五图层应用颜色覆盖效果，将颜色覆盖设置为RGB(30, 50, 0)，不透明度为150。

最后，代码将修改后的图像保存为更新后的PNG文件。

总的来说，Aspose.PSD for Java提供了多种混合选项来操作PSD图像中图层的外观。这些选项包括修改不透明度、改变混合模式以及实现各种混合效果，如投影阴影和颜色覆盖。

## **示例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose.Psd-blending-options.java" >}}
