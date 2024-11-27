---
title: Ejemplo de uso de capas de grupo en Aspose.PSD para Python
weight: 100
type: docs
description: Uso de Capa de Grupo de Archivo PSD a través de Python
keywords: [capa de grupo, capa de grupo, agregar capa a grupo, api psd, python, ejemplo de código]
url: es/python-net/psd-group-layer/
---

## **Descripción General**

Trabajar con capas de grupo en Aspose.PSD para Python es una característica poderosa que te permite organizar y manipular capas dentro de una imagen PSD. Las capas de grupo, también conocidas como capas de carpeta, proporcionan una manera de agrupar múltiples capas juntas y aplicar transformaciones o efectos a todo el grupo.

En este ejemplo, primero creamos una nueva imagen PSD utilizando el método PsdImage.create. Luego, creamos un nuevo objeto LayerGroup utilizando el método add_layer_group del objeto PsdImage. Proporcionamos el nombre de la capa del grupo ("Carpeta"), el índice en el que debería insertarse (0) y un indicador booleano que indica si la capa de grupo debería ser visible (True).

A continuación, creamos dos objetos Layer y configuramos sus nombres de visualización utilizando la propiedad display_name. Agregamos estas capas al grupo utilizando el método add_layer.

Finalmente, podemos acceder a las capas dentro del grupo utilizando la propiedad layers del objeto LayerGroup. En el ejemplo, afirmamos que los nombres de visualización de las primeras y segundas capas en el grupo son "Capa 1" y "Capa 2" respectivamente.

Después de manipular las capas de grupo, podemos guardar la imagen PSD modificada utilizando el método save del objeto PsdImage.

Este es solo un ejemplo básico para ayudarte a comenzar a trabajar con capas de grupo usando Aspose.PSD para Python. La biblioteca proporciona muchas más funciones avanzadas para manipular y transformar capas dentro de imágenes PSD. Puedes consultar la documentación de Aspose.PSD para Python para obtener más detalles y ejemplos sobre cómo trabajar con capas de grupo y otras características de la biblioteca.

Para trabajar con capas de grupo en Aspose.PSD para Python, puedes usar la clase LayerGroup. Aquí tienes un fragmento de código de ejemplo que demuestra cómo crear una capa de grupo, agregar capas a ella y guardar la imagen PSD modificada.

Por favor, consulta el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-psd-group-layer.py" >}}
