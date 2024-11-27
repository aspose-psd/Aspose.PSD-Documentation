---
title: Manipulación de Filtros Inteligentes en Aspose.PSD para Python
weight: 100
type: docs
description: Ejemplos de cómo usar filtros inteligentes en archivos PSD
keywords: [filtro inteligente, agregar ruido, desenfoque gaussiano, enfocar, filtro, filtro PSD, API de PSD, python, ejemplo de código]
url: es/python-net/filtros-inteligentes/
---

## **Resumen**

Hay 3 formas de aplicar filtros inteligentes en Aspose.PSD para Python.

## **Aplicación directa de Filtros**
En este ejemplo de código, se puede ver un ejemplo de cómo aplicar directamente filtros inteligentes en Aspose.PSD para Python.

Primero, el código especifica el archivo PSD de origen, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

A continuación, el código carga la imagen PSD usando el método Image.load() y la convierte en un objeto PsdImage.

La imagen original se guarda usando el método save(), con el nombre de archivo de salida especificado.

Se crea un objeto SharpenSmartFilter, que representa el filtro inteligente que se va a aplicar.

El código luego recupera la capa regular de la imagen PSD usando img.layers[1].

Luego, se utiliza un bucle para aplicar el filtro de agudizar a la capa regular tres veces.

Finalmente, la imagen actualizada se guarda usando el método save() y se especifica el nombre de archivo de salida.

Este código demuestra cómo aplicar directamente filtros inteligentes en Aspose.PSD para Python. Al usar los objetos de filtro apropiados y aplicarlos a las capas deseadas, se pueden lograr los efectos deseados en sus imágenes.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-psd-filtro-inteligente-aplicación-directa.py" >}}

## **Manipulación de Filtros Inteligentes en Objetos Inteligentes**

Primero, el código especifica el archivo PSD de origen, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

La imagen PSD se carga usando el método Image.load(), y luego se convierte en un objeto PsdImage.

La imagen original se guarda usando el método save(), con el nombre de archivo de salida especificado.

Luego, el código convierte la segunda capa de la imagen PSD en un objeto SmartObjectLayer, que representa la capa de objeto inteligente.

Luego, el código procede a editar los filtros inteligentes. En este ejemplo, se demuestra cómo trabajar con dos tipos de filtros inteligentes: GaussianBlurSmartFilter y AddNoiseSmartFilter.

Para GaussianBlurSmartFilter, el código actualiza los valores del filtro, incluido el radio, el modo de mezcla, la opacidad y si está habilitado o no.

Para AddNoiseSmartFilter, el código establece la distribución del ruido en NoiseDistribution.UNIFORM.

A continuación, el código agrega dos nuevos elementos de filtro a la capa de objeto inteligente: otro GaussianBlurSmartFilter y un AddNoiseSmartFilter.

Después de agregar los nuevos filtros, el código aplica los cambios con el método update_resource_values().

Finalmente, el código demuestra cómo aplicar directamente los filtros a la capa y a la máscara de la capa usando los métodos apply() y apply_to_mask() respectivamente.

La imagen actualizada se guarda luego usando el método save() y se especifica el nombre de archivo de salida.

Siguiendo este ejemplo de código, puede aprender cómo trabajar con filtros inteligentes en Aspose.PSD para Python. La librería proporciona una amplia gama de filtros inteligentes, cada uno con su propio conjunto de propiedades y métodos que se pueden personalizar para lograr los efectos deseados en sus imágenes.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-psd-filtros-inteligentes-funciones.py" >}}

## **Aplicación de Filtros Inteligentes a la Máscara de Capa**

Aplicar Filtros Inteligentes a Máscaras: Una Técnica Poderosa de Edición de Imágenes

Los filtros inteligentes son una característica popular en software de edición de imágenes que permiten a los usuarios aplicar varios filtros y efectos a sus imágenes. Una técnica interesante que se puede lograr utilizando filtros inteligentes es aplicarlos a máscaras. En este artículo, exploraremos cómo aplicar filtros inteligentes a máscaras y discutiremos su uso en el mundo de la edición de imágenes.

¿Qué es una Máscara? Antes de adentrarnos en la aplicación de filtros inteligentes a máscaras, primero entendamos qué es una máscara. En la edición de imágenes, una máscara es una imagen en escala de grises que determina la transparencia de ciertas áreas de una imagen. Una máscara se puede utilizar para aplicar selectivamente filtros, ajustes o efectos a partes específicas de una imagen, mientras se dejan otras áreas sin cambios.

Aplicar Filtros Inteligentes a Máscaras: Cuando se aplican filtros inteligentes a máscaras, los filtros solo se aplican a las áreas especificadas por la máscara. Esto permite un control preciso sobre qué partes de la imagen son afectadas por el filtro. Al manipular la máscara, puedes determinar la intensidad y extensión del efecto del filtro.

Por favor, revisa el ejemplo anterior y el método: [Referencia de API Aplicar Filtro Inteligente a Máscara](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
