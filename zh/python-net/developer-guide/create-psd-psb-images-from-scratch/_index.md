---
title: 用Python从头开始创建PSD或PSB图像
weight: 100
type: docs
description: 演示Aspose.PSD for Python如何从头创建Psd图像
keywords: [创建psd, 创建psb, 创建新, 创建图层, 创建文本图层, psd api, python, 代码示例]
url: zh/python-net/create-psd-psb-images-from-scratch/
---

## **概述**
要使用Aspose.PSD for Python从头创建PSD或PSB文件，可以按照以下步骤进行操作：

从Aspose.PSD库中导入必要的模块和类：
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

指定输出文件名和路径：

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

使用所需尺寸创建PSD图像：

```python 
with PsdImage(500, 500) as img:
```

添加普通PSD图层并使用图形API进行更新：

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

创建文本图层：
```python 
textLayer = img.add_text_layer("示例文本", Rectangle(200, 200, 100, 100))
```

为文本图层添加阴影效果：
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

保存PSD文件：
```python 
img.save(outputFile)
```

此代码将创建一个尺寸为500x500像素的PSD图像。它添加一个普通图层，并使用笔和画笔在其中绘制椭圆。然后，它添加一个文本图层，显示文本“示例文本”，并对其应用阴影效果。最后，它使用指定的输出文件名保存PSD文件。

请注意，为使此代码正常工作，您需要在Python环境中安装并正确设置Aspose.PSD库。您可以参考官方Aspose.PSD文档以获取有关如何安装和使用该库的更多信息。

请查看完整示例。

## **示例**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
