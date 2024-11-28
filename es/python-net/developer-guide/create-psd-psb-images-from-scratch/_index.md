---
title: Crear imagen PSD o PSB desde cero usando Python
weight: 100
type: docs
description: Ejemplo de cómo Aspose.PSD para Python puede crear una imagen Psd desde cero
keywords: [crear psd, crear psb, crear nuevo, crear capa, crear capa de texto, psd api, python, muestra de código]
url: es/python-net/crear-imagenes-psd-psb-desde-cero/
---

## **Visión general**
Para crear un archivo PSD o PSB desde cero usando Aspose.PSD para Python, puedes seguir los siguientes pasos:

Importa los módulos y clases necesarios de la biblioteca Aspose.PSD:

```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

Especifica el nombre del archivo de salida y la ruta:

```python 
outputFile = "EjemploCrearArchivoDesdeCero.psd"
```

Crea una imagen PSD con las dimensiones deseadas:

```python 
with PsdImage(500, 500) as img:
```

Agrega una capa PSD regular y actúalizala usando la API gráfica:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Crea una capa de texto:
```python 
textLayer = img.add_text_layer("Texto de Ejemplo", Rectangle(200, 200, 100, 100))
```

Agrega un efecto de sombra a la capa de texto:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

Guarda el archivo PSD:
```python 
img.save(outputFile)
```

Este código crea una imagen PSD con dimensiones de 500x500 píxeles. Agrega una capa regular y dibuja una elipse en ella usando un bolígrafo y un pincel. Luego agrega una capa de texto con el texto "Texto de Ejemplo" y aplica un efecto de sombra a ella. Finalmente, guarda el archivo PSD con el nombre de archivo de salida especificado.

Ten en cuenta que necesitarás tener instalada la biblioteca Aspose.PSD y configurada correctamente en tu entorno de Python para que este código funcione. Puedes consultar la documentación oficial de Aspose.PSD para obtener más información sobre cómo instalar y usar la biblioteca.

Por favor, revisa el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-Psd-crear-imagenes-psd-psb-desde-cero.py" >}}
