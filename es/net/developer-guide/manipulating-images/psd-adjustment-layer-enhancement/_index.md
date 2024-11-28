---
title: Utilizando capa de ajuste para mejoras en PSD
weight: 100
type: docs
description: Ejemplos de uso de capas de ajuste a través de Aspose.PSD para C#
keywords: [capa de ajuste, mejoras de fotos, ajuste de curvas, mejora de niveles, invertir, filtro de fotos, API psd, C#, csharp, ejemplo de código]
url: es/net/mejora-de-capa-de-ajuste/
---

## Resumen

En este artículo, exploraremos la edición de capas de ajuste en Aspose.PSD para C#. Las capas de ajuste son una característica poderosa en la edición de imágenes que le permiten realizar cambios no destructivos en sus imágenes. Aspose.PSD proporciona un conjunto completo de clases de capas de ajuste que puede utilizar para modificar varios aspectos de sus imágenes.

Para demostrar la edición de capas de ajuste, usaremos un fragmento de código de ejemplo al final de la página que carga una imagen PSD y aplica diferentes ajustes a sus capas.

En el fragmento de código a continuación, comenzamos cargando la imagen PSD utilizando el método `PsdImage.Load()`. Luego configuramos las opciones para guardar los archivos PNG de salida. La clase `PngOptions` nos permite especificar el tipo de color para la imagen de salida.

A continuación, recorremos cada capa en la imagen PSD y verificamos su tipo utilizando el método `IsAssignable()`. Si la capa es de un tipo específico, la convertimos a ese tipo utilizando el método `Cast()` y aplicamos el ajuste deseado. Por ejemplo, ajustamos el brillo y el contraste de una `BrightnessContrastLayer`, modificamos los niveles de una `LevelsLayer`, agregamos un punto de curva a una `CurvesLayer`, y más.

Puede agregar código adicional para aplicar otros ajustes a sus respectivas capas. Aspose.PSD proporciona una amplia gama de clases de capas de ajuste, como [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), y más.

Finalmente, guardamos la imagen modificada utilizando el método `Guardar()` de la clase `PsdImage`.

Este código proporciona una visión general básica de cómo editar capas de ajuste en Aspose.PSD para C#. Puede personalizar los ajustes según sus requisitos y explorar las diversas opciones disponibles en la documentación de la API.

## Ejemplo

Aquí tienes un ejemplo de código que muestra cómo utilizar capas de ajuste usando Aspose.PSD para C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Para obtener información más detallada y ejemplos, visita la [documentación de Aspose.PSD para C#](https://docs.aspose.com/psd/net/).

