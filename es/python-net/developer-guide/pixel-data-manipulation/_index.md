---
title: Manipulación de datos de píxeles usando Aspose.PSD para Python
weight: 100
type: docs
description: Ejemplo de cómo actualizar rápida y directamente los datos de píxeles crudos utilizando la API de Python Aspose.PSD
keywords: [editar píxeles, editar psd, editar capa, manipulación de datos crudos, editar datos psd, api psd, python, muestra de código]
url: /es/python-net/manipulacion-de-datos-de-pixel/
---

## **Introducción**
Aspose.PSD es una biblioteca poderosa que te permite trabajar con archivos de Adobe Photoshop (PSD) en Python. En este artículo, exploraremos cómo manipular datos de píxeles en un archivo PSD utilizando Aspose.PSD.

## **Visión general**
El código proporcionado demuestra cómo crear un archivo PSD, agregar la nueva capa y luego manipular directamente los datos de píxeles, y guardar la imagen modificada.

Importación de módulos necesarios: El primer paso es importar los módulos necesarios. Importamos el módulo BytesIO de la biblioteca io, así como las clases PsdImage y Layer de los módulos aspose.psd.fileformats.psd y aspose.psd.fileformats.psd.layers respectivamente.

Luego, definimos las rutas de archivo de entrada y salida.

Apertura del archivo de entrada como un flujo: Abrimos el archivo de entrada como un flujo utilizando la función open y el modo "rb". El argumento de almacenamiento en búfer se establece en 0 para deshabilitar el almacenamiento en búfer. El contenido del archivo se lee en un flujo BytesIO y el flujo se coloca al principio utilizando stream.seek(0).

Creamos un objeto de capa PSD pasando el flujo al constructor de la clase Layer.

Creamos una nueva imagen PSD utilizando el constructor de la clase PsdImage y proporcionamos el ancho y alto de la capa como argumentos.

Asignamos la capa a la propiedad layers de la imagen PSD utilizando el operador de asignación (=).

Para manipular los datos de píxeles, primero cargamos los píxeles ARGB32 de la capa utilizando el método load_argb_32_pixels. Almacenamos el resultado en la variable de píxeles.

Luego, definimos un rango de índices (pixelsRange) basado en la longitud del array de píxeles. Iteramos sobre los índices y verificamos si un índice es divisible por 5. Si lo es, establecemos el valor del píxel en ese índice en 500000. Así, solo queremos crear un patrón repetitivo. Puedes cambiar los datos de los píxeles como desees.

Luego guardamos los datos de píxeles modificados de nuevo en la capa utilizando el método save_argb_32_pixels.

Finalmente, guardamos la imagen PSD en el archivo de salida utilizando el método save.

En este artículo, hemos explorado cómo manipular datos de píxeles en un archivo PSD utilizando Aspose.PSD para Python. Comprendiendo el código proporcionado, puedes realizar varias operaciones a nivel de píxel, como modificar píxeles en función de ciertas condiciones. Aspose.PSD proporciona un conjunto completo de características para trabajar con archivos PSD de forma programática, convirtiéndolo en una herramienta valiosa para tareas de manipulación de imágenes en Python.

Ten en cuenta que el código proporcionado asume que ya has instalado la biblioteca Aspose.PSD y sus dependencias. Puedes encontrar más información sobre cómo instalar y usar Aspose.PSD para Python en la documentación oficial.

Por favor, consulta el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentacion-Python-Aspose-manipulacion-de-datos-de-pixel.py" >}}
