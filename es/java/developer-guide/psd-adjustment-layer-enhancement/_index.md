---
title: Uso de capa de ajuste para mejoras de PSD
weight: 100
type: docs
description: Ejemplos de uso de capa de ajuste a través de Aspose.PSD para Java
keywords: [capa de ajuste, mejorar foto, ajuste de curvas, mejora de niveles, invertir, filtro fotográfico, api psd, java, ejemplo de código]
url: es/java/mejora-de-capa-de-ajuste/
---

## **Resumen**

Este artículo explora la edición de capas de ajuste en Aspose.PSD para Java. Las capas de ajuste son una característica potente en la edición de imágenes que te permiten realizar cambios no destructivos en tus imágenes. Aspose.PSD proporciona un conjunto completo de clases de capas de ajuste que puedes utilizar para modificar varios aspectos de tus imágenes.

Para demostrar la edición de capas de ajuste, proporcionaremos un fragmento de código de ejemplo al final de la página que carga una imagen PSD y aplica diferentes ajustes a sus capas.

En el siguiente fragmento de código, empezamos cargando la imagen PSD utilizando el método PsdImage.load(). Luego, configuramos las opciones para guardar los archivos PNG de salida. La clase PngOptions nos permite especificar el tipo de color para la imagen de salida.

A continuación, iteramos a través de cada capa de la imagen PSD y verificamos su tipo utilizando el método isAssignable(). Si la capa es de un tipo específico, la convertimos a ese tipo utilizando el método cast() y aplicamos el ajuste deseado. Por ejemplo, ajustamos el brillo y contraste de una BrightnessContrastLayer, modificamos los niveles de una LevelsLayer, agregamos un punto de curva a una CurvesLayer, etc.

Puedes agregar código adicional para aplicar otros ajustes a sus respectivas capas. Aspose.PSD proporciona una amplia gama de clases de capas de ajuste, como [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) y más.

Finalmente, guardamos la imagen modificada utilizando el método save() de la clase PsdImage.

Esto proporciona una descripción básica de cómo editar capas de ajuste en Aspose.PSD para Java. Puedes personalizar los ajustes según tus necesidades y explorar las diversas opciones disponibles en la documentación de la API.

Por favor, revisa el ejemplo completo a continuación.

## **Ejemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
