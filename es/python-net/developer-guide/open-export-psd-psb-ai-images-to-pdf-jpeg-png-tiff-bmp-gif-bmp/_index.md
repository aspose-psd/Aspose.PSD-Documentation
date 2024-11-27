---
title: Abrir archivos PSD, PSB y AI y exportarlos a PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Ejemplo de exportación de archivos PSD, PSB y AI a otros formatos
keywords: [abrir psd, abrir ai, abrir psb, exportar a png, exportar a pdf, exportar a jpeg, exportar a tiff, psd api, python, muestra de código]
url: /es/python-net/abrir-exportar-imagenes-psd-psb-ai-a-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Visión general**
Para convertir archivos PSD, PSB y AI a diferentes formatos, puede utilizar la biblioteca Aspose.PSD en Python. Esta biblioteca ofrece varias opciones y ajustes para personalizar el proceso de conversión.

Primero, es necesario importar las clases y módulos necesarios de la biblioteca Aspose.PSD. Asegúrese de haber instalado la biblioteca antes de ejecutar el código.

En este código, definimos varias opciones para diferentes formatos, como PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB y PSD. Estas opciones le permiten personalizar el archivo de salida según sus requerimientos.

Luego, definimos un diccionario de formatos que asigna las extensiones de archivo a sus respectivas opciones de guardado.

Para convertir un archivo PSD a otros formatos, es necesario cargar el archivo PSD utilizando PsdImage.load() y luego iterar a través del diccionario de formatos. Para cada formato, especifique el nombre del archivo de salida y guarde la imagen utilizando el método image.save().

De manera similar, para convertir un archivo AI a otros formatos, cargue el archivo AI utilizando AiImage.load() e itere a través del diccionario de formatos. Especifique el nombre del archivo de salida y guarde la imagen utilizando el método image.save().

Asegúrese de proporcionar las rutas de archivo correctas para los archivos PSD y AI de origen.

¡Eso es todo! Ahora puede utilizar este código para convertir archivos PSD, PSB y AI a varios formatos utilizando Aspose.PSD para Python.

Por favor, revise el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
