---
title: Usando capa de ajuste para mejoras de PSD
weight: 100
type: docs
description: Ejemplos de uso de capa de ajuste a través de Aspose.PSD para Python
keywords: [capa de ajuste, mejorar foto, ajuste de curvas, mejora de niveles, invertir, filtro de foto, api de psd, python, muestra de código]
url: es/python-net/mejora-de-capa-de-ajuste/
---

## **Visión general**

En este artículo, exploraremos la edición de capas de ajuste en Aspose.PSD para Python. Las capas de ajuste son una característica poderosa en la edición de imágenes que le permiten realizar cambios no destructivos en sus imágenes. Aspose.PSD proporciona un conjunto completo de clases de capas de ajuste que puede utilizar para modificar varios aspectos de sus imágenes.

Para demostrar la edición de capas de ajuste, utilizaremos un fragmento de código de ejemplo al final de la página que carga una imagen PSD y aplica diferentes ajustes a sus capas.

En el siguiente fragmento de código, comenzamos cargando la imagen PSD utilizando el método PsdImage.load(). Luego configuramos las opciones para guardar los archivos PNG de salida. La clase PngOptions nos permite especificar el tipo de color para la imagen de salida.

A continuación, iteramos a través de cada capa en la imagen PSD y verificamos su tipo utilizando el método is_assignable(). Si la capa es de un tipo específico, la convertimos a ese tipo utilizando el método cast() y aplicamos el ajuste deseado. Por ejemplo, ajustamos el brillo y contraste de una BrightnessContrastLayer, modificamos los niveles de una LevelsLayer, agregamos un punto de curva a una CurvesLayer, etc.

Puede añadir código adicional para aplicar otros ajustes a sus capas respectivas. Aspose.PSD proporciona una amplia gama de clases de capas de ajuste, tales como [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), y más.

Finalmente, guardamos la imagen modificada utilizando el método save() de la clase PsdImage.

Este código proporciona una visión general básica de cómo editar capas de ajuste en Aspose.PSD para Python. Puede personalizar los ajustes según sus requerimientos y explorar las diversas opciones disponibles en la documentación de la API.

Por favor, consulte el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-mejora-de-capa-de-ajuste.py" >}}
