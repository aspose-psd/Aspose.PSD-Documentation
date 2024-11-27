---
title: Изграждане на PSD или PSB изображение от нулата с използването на Python
weight: 100
type: docs
description: Пример за това как Aspose.PSD за Python може да създаде Psd изображение от нулата
keywords: [създаване на psd, създаване на psb, създаване на нов, създаване на слой, създаване на текстов слой, psd api, python, пример за код]
url: /bg/python-net/create-psd-psb-images-from-scratch/
---

## **Общ преглед**
За да създадете PSD или PSB файл от нулата, използвайки Aspose.PSD за Python, можете да следвате стъпките по-долу:

Импортирайте необходимите модули и класове от библиотеката Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Укажете името и пътя на изходния файл:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Създайте PSD изображение с желаните размери:

```python 
with PsdImage(500, 500) as img:
```

Добавете обикновен слой на PSD и го актуализирайте, използвайки графичния API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Създайте текстов слой:
```python 
textLayer = img.add_text_layer("Примерен текст", Rectangle(200, 200, 100, 100))
```

Добавете ефект на сянка на текстовия слой:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Запазете PSD файла:
```python 
img.save(outputFile)
```

Този код създава PSD изображение с размери 500x500 пиксела. Той добавя обикновен слой и чертае елипса върху него, използвайки молив и четка. След това добавя текстов слой с текста "Примерен текст" и прилага ефект на сянка към него. Накрая, той запазва PSD файла с посоченото име на изходния файл.

Моля, обърнете внимание, че за този код да работи, ще трябва да инсталирате Aspose.PSD библиотеката и да я настроите правилно във вашия Python среда. Можете да се обърнете към официалната документация на Aspose.PSD за повече информация относно начина на инсталиране и използване на библиотеката.

Моля, проверете пълния пример.

## **Пример**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}