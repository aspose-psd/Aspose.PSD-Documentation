---
title: Створення зображення PSD або PSB з нуля за допомогою Python
weight: 100
type: docs
description: Приклад того, як Aspose.PSD для Python може створити зображення Psd з нуля
keywords: [створення psd, створення psb, створення нового, створення шару, створення текстового шару, psd api, python, зразок коду]
url: uk/python-net/create-psd-psb-images-from-scratch/
---

## **Огляд**
Щоб створити файл PSD або PSB з нуля за допомогою Aspose.PSD для Python, ви можете дотримуватися наведених нижче кроків:

Імпортуйте необхідні модулі та класи з бібліотеки Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Вкажіть ім'я та шлях вихідного файлу:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

Створіть зображення PSD з вказаними розмірами:

```python 
with PsdImage(500, 500) as img:
```

Додайте звичайний шар PSD та оновіть його за допомогою графічного API:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Створіть текстовий шар:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

Додайте ефект тіні до текстового шару:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Збережіть файл PSD:
```python 
img.save(outputFile)
```

Цей код створює зображення PSD з розмірами 500x500 пікселів. Він додає звичайний шар та малює на ньому еліпс за допомогою ручки та пензля. Потім додає текстовий шар з текстом "Sample Text" та застосовує до нього ефект тіні. На останок він зберігає файл PSD з вказаним ім'ям вихідного файлу.

Зверніть увагу, що для роботи цього коду вам потрібно мати встановлену та налагоджену бібліотеку Aspose.PSD у вашому середовищі Python. Ви можете звернутися до офіційної документації Aspose.PSD для отримання додаткової інформації щодо встановлення та використання бібліотеки.

Будь ласка, перевірте повний приклад.

## **Приклад**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
