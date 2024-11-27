---
title: Utilizando la API de gráficos para editar capas en archivos PSD
weight: 100
type: docs
description: Ejemplo de uso de la API de gráficos en Aspose.PSD para Java
keywords: [actualizar capa, dibujar círculo, dibujar elipse, dibujar círculo relleno, gráficos, api psd, java, muestra de código]
url: es/java/graphics-api/
---

## **Resumen**
Para comenzar, carga el archivo PSD utilizando el método Image.load() o crea una imagen Psd desde cero. Utiliza la variable inputFile para representar la ruta de tu archivo PSD y especifica cualquier opción de carga con loadOpt, si es necesario.

A continuación, accede a la primera capa de la imagen PSD utilizando la sintaxis psdImage.getLayers()[0] para obtener una referencia al objeto de la capa para su manipulación.

Para editar la capa, crea un objeto Graphics pasando la capa como parámetro. Este objeto proporciona varios métodos para dibujar formas y aplicar pinceles.

Se utiliza un objeto Pen para definir el color y el grosor del contorno de las formas. Del mismo modo, se utilizan pinceles como LinearGradientBrush para definir los colores de relleno.

Dibuja formas en la capa utilizando métodos como graphics.drawEllipse() para contornear formas y graphics.fillEllipse() para rellenarlas.

Después de realizar los cambios deseados en la capa, guarda la imagen PSD modificada utilizando psdImage.save().

Además, puedes guardar la imagen modificada en otros formatos como PNG utilizando las opciones adecuadas.

¡Eso es todo! Has utilizado con éxito la API de gráficos de Aspose.PSD para Java para editar capas en un archivo PSD. Explora más funciones y características de la biblioteca Aspose.PSD para mejorar tus capacidades de edición de imágenes.

Por favor, revisa el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-graphics-api.java" >}}
