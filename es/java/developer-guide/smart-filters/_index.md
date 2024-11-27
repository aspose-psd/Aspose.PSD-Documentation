---
title: Manipulación inteligente de filtros en Aspose.PSD para Java
weight: 100
type: docs
description: Ejemplos de cómo usar Filtros Inteligentes en Archivos PSD
keywords: [filtro inteligente, añadir ruido, desenfoque gaussiano, acentuar, filtro, filtro psd, api psd, java, muestra de código]
url: es/java/filtros-inteligentes/
---

## **Visión general**

Hay 3 métodos para aplicar filtros inteligentes en Aspose.PSD para Java.

## ** Aplicación Directa de Filtro **
Este ejemplo de código demuestra cómo aplicar filtros inteligentes directamente en Aspose.PSD para Java.

Inicialmente, el código define el archivo PSD de origen, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

Luego, el código carga la imagen PSD usando el método Image.load() y la convierte en un objeto PsdImage.

La imagen original se guarda usando el método save(), especificando el nombre del archivo de salida.

Se instancia un objeto SharpenSmartFilter para representar el filtro inteligente deseado.

A continuación, el código recupera la capa regular de la imagen PSD usando psdImage.getLayers()[1].

Se utiliza un bucle para aplicar el filtro de acentuado a la capa regular tres veces.

Finalmente, la imagen actualizada se guarda usando el método save() con el nombre del archivo de salida proporcionado.

Este código ejemplifica la aplicación directa de filtros inteligentes en Aspose.PSD para Java. Al utilizar objetos de filtro apropiados y aplicarlos a las capas deseadas, se pueden lograr efectos deseados en imágenes.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-filtro-inteligente-aplicación-directa.java" >}}

## ** Manipulación de Filtros Inteligentes en Objetos Inteligentes **

Este fragmento de código describe cómo manipular filtros inteligentes dentro de objetos inteligentes en Aspose.PSD para Java.

Inicialmente, el código define el archivo PSD de origen, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

La imagen PSD se carga usando el método Image.load() y luego se convierte en un objeto PsdImage.

La imagen original se guarda usando el método save(), especificando el nombre del archivo de salida.

Luego, el código convierte la segunda capa de la imagen PSD en un objeto SmartObjectLayer, que representa la capa de objeto inteligente.

Posteriormente, el código demuestra la edición de filtros inteligentes, mostrando dos tipos: GaussianBlurSmartFilter y AddNoiseSmartFilter.

Para GaussianBlurSmartFilter, el código actualiza los valores del filtro como radio, modo de fusión, opacidad y estado de activación.

Para AddNoiseSmartFilter, el código establece la distribución de ruido en NoiseDistribution.Uniform.

A continuación, el código agrega dos nuevos elementos de filtro a la capa de objeto inteligente: otro GaussianBlurSmartFilter y un AddNoiseSmartFilter.

Después de la adición de nuevos filtros, el código aplica cambios usando el método updateResourceValues().

Por último, el código demuestra la aplicación directa de filtros a la capa y su máscara usando los métodos apply() y applyToMask(), respectivamente.

Luego, la imagen actualizada se guarda usando el método save() con el nombre del archivo de salida proporcionado.

Siguiendo este ejemplo de código, puede comprender cómo manipular filtros inteligentes dentro de objetos inteligentes en Aspose.PSD para Java. La biblioteca ofrece una amplia variedad de filtros inteligentes, cada uno con su propio conjunto de propiedades y métodos que se pueden personalizar para lograr efectos deseados en imágenes.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-filtro-inteligente-características.java" >}}

## ** Aplicación de Filtros Inteligentes a la Máscara de Capa **

Aplicar Filtros Inteligentes a las Máscaras: Una Potente Técnica de Edición de Imágenes

Los filtros inteligentes, comunes en software de edición de imágenes, permiten a los usuarios aplicar diversos filtros y efectos a sus imágenes. Una técnica intrigante habilitada por los filtros inteligentes es su aplicación a máscaras. Este artículo explora la aplicación de filtros inteligentes a máscaras y discute su utilidad en el ámbito de la edición de imágenes.

Entendiendo las Máscaras: Antes de adentrarse en la aplicación de filtros inteligentes a máscaras, es crucial comprender el concepto de una máscara. En la edición de imágenes, una máscara es una imagen en escala de grises que dicta la transparencia de áreas específicas dentro de una imagen. Las máscaras permiten la aplicación selectiva de filtros, ajustes o efectos a partes particulares de una imagen mientras se dejan otras sin afectar.

Aplicar Filtros Inteligentes a Máscaras: Cuando se aplican filtros inteligentes a máscaras, afectan solo a las áreas especificadas por la máscara, ofreciendo un control preciso sobre el impacto del filtro. Al manipular la máscara, los usuarios pueden modular la intensidad y extensión del efecto del filtro.

Consulte el ejemplo anterior y el método: [Referencia de API Aplicar Filtro Inteligente a Máscara](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
