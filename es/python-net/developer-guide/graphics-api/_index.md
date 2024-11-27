---
title: Usar la API de gráficos para editar capas en archivos PSD
weight: 100
type: docs
description: Ejemplo de cómo utilizar la API de gráficos en Aspose.PSD para Python
keywords: [actualizar capa, dibujar círculo, dibujar elipse, dibujar círculo relleno, gráficos, api psd, python, muestra de código]
url: es/python-net/graphics-api/
---

## **Descripción general**
Primero, necesitas cargar el archivo PSD utilizando el método Image.load() o crear una imagen Psd desde cero. En el ejemplo, la variable inputFile representa la ruta de tu archivo PSD, y loadOpt representa las opciones de carga (si las hay).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```

A continuación, puedes acceder a la primera capa de la imagen PSD utilizando la sintaxis psdImage.layers[0]. Esto te proporciona una referencia al objeto de capa que puedes manipular.

```python 
layer = psdImage.layers[0]
```

Para editar la capa, necesitas crear un objeto Graphics pasando la capa como parámetro. Este objeto proporciona varios métodos para dibujar formas y aplicar pinceles.

```python 
graphics = Graphics(layer)
```

En el ejemplo de código, se crea un objeto Pen para definir el color y el grosor del contorno de la forma de elipse. La constante Color.alice_blue representa el color, y puedes ajustar el grosor según sea necesario.

```python 
pen = Pen(Color.alice_blue)
```

De manera similar, se crea un objeto LinearGradientBrush para definir el color de relleno de la forma de elipse. El Rectangle(250, 250, 150, 100) representa la posición y el tamaño de la forma de elipse, y Color.red y Color.aquamarine representan los colores de inicio y fin del degradado.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```

Para dibujar la forma de elipse en la capa, puedes utilizar el método graphics.draw_ellipse(). El Rectangle(100, 100, 200, 200) representa la posición y tamaño de la forma de elipse.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```

Para rellenar la forma de elipse con el pincel de degradado, puedes utilizar el método graphics.fill_ellipse(). El Rectangle(250, 250, 150, 100) representa la posición y tamaño de la forma de elipse.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

Después de realizar los cambios deseados en la capa, puedes guardar la imagen PSD modificada utilizando el método psdImage.save(). En el ejemplo, la variable psdName representa la ruta para guardar el archivo PSD modificado.

```python 
psdImage.save(psdName)
```

Además, también puedes guardar la imagen modificada en otros formatos, como PNG, utilizando la clase PngOptions. La variable pngName representa la ruta para guardar el archivo PNG.

```python 
psdImage.save(pngName, PngOptions())
```

¡Eso es todo! Has utilizado con éxito la API de gráficos de Aspose.PSD para Python para editar capas en un archivo PSD. Siéntete libre de explorar más características y funcionalidades de la biblioteca Aspose.PSD para mejorar tus capacidades de edición de imágenes.

Por favor, verifica el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py" >}}
