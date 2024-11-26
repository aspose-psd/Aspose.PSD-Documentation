---
title: Создание изображения PSD или PSB с нуля с использованием Python
weight: 100
type: docs
description: Пример того, как Aspose.PSD для Python может создавать изображение Psd с нуля
keywords: [создание psd, создание psb, создание нового, создание слоя, создание текстового слоя, psd api, python, образец кода]
url: ru/python-net/create-psd-psb-images-from-scratch/
---

## **Обзор**
Чтобы создать файл PSD или PSB с нуля с использованием Aspose.PSD для Python, вы можете следовать следующим шагам:

Импортировать необходимые модули и классы из библиотеки Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Указать имя и путь выходного файла:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Создать изображение PSD с желаемыми размерами:

```python 
with PsdImage(500, 500) as img:
```

Добавить обычный слой PSD и обновить его с помощью графического API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Создать текстовый слой:
```python 
textLayer = img.add_text_layer("Пример текста", Rectangle(200, 200, 100, 100))
```

Добавить эффект тени к текстовому слою:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Сохранить файл PSD:
```python 
img.save(outputFile)
```

Этот код создает изображение PSD с размерами 500x500 пикселей. Он добавляет обычный слой и рисует на нем эллипс с помощью ручки и кисти. Затем добавляет текстовый слой с текстом "Пример текста" и применяет к нему эффект тени. Наконец, он сохраняет файл PSD с указанным именем выходного файла.

Обратите внимание, что для работы этого кода вам понадобится установить библиотеку Aspose.PSD и правильно настроить ее в вашей среде Python. Вы можете обратиться к официальной документации Aspose.PSD для получения более подробной информации о том, как установить и использовать библиотеку.

Пожалуйста, проверьте полный пример.

## **Пример**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
