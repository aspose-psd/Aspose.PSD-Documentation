---
title: Manipulación inteligente de filtros en Aspose.PSD para С#
weight: 100
type: docs
description: Ejemplos de cómo utilizar Filtros Inteligentes en archivos PSD
keywords: [filtro inteligente, agregar ruido, desenfoque gaussiano, enfocar, filtro, filtro psd, api psd, C#, csharp, ejemplo de código]
url: es/net/filtros-inteligentes/
---

## Resumen

Hay tres formas de aplicar filtros inteligentes en Aspose.PSD para C#.

### Aplicación Directa de Filtro

Este ejemplo demuestra cómo aplicar filtros inteligentes directamente en Aspose.PSD para C#.

Primero, especifique el archivo PSD fuente, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

A continuación, cargue la imagen PSD usando el método `Image.Load` y cárguela en un objeto `PsdImage`.

Guarde la imagen original usando el método `Guardar` con el nombre de archivo de salida especificado.

Cree un objeto `SharpenSmartFilter`, que representa el filtro inteligente que se aplicará.

Recupere la capa regular de la imagen PSD usando `psdImage.Layers[1]`.

Aplique el `filtro de enfoque` a la capa regular tres veces en un bucle.

Finalmente, guarde la imagen actualizada utilizando el método `Guardar` con el nombre de archivo de salida especificado.

Este código demuestra cómo aplicar filtros inteligentes directamente en Aspose.PSD para C#. Al utilizar los objetos de filtro apropiados y aplicarlos a las capas deseadas, puedes lograr los efectos deseados en tus imágenes.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "AplicarFiltroInteligenteDirectamente-AplicarFiltroInteligenteDirectamente.cs" >}}

### Manipulación de Filtros Inteligentes en Objetos Inteligentes

Este ejemplo muestra cómo manipular filtros inteligentes dentro de objetos inteligentes.

Primero, especifique el archivo PSD fuente, el archivo de salida para la imagen original y el archivo de salida para la imagen actualizada.

Cargue la imagen PSD usando el método `Image.Load` y cárguela en un objeto `PsdImage`.

Guarde la imagen original usando el método `Guardar` con el nombre de archivo de salida especificado.

Convierta la segunda capa de la imagen PSD en un objeto `SmartObjectLayer`.

Edite los filtros inteligentes. Este ejemplo demuestra cómo trabajar con `GaussianBlurSmartFilter` y `AddNoiseSmartFilter`.

Para `GaussianBlurSmartFilter`, actualice los valores del filtro, incluido el radio, el modo de mezcla, la opacidad y el estado habilitado.

Para `AddNoiseSmartFilter`, configure la distribución de ruido en `NoiseDistribution.UNIFORM`.

Agregue nuevos elementos de filtro a la capa de objeto inteligente: otro `GaussianBlurSmartFilter` y `AddNoiseSmartFilter`.

Aplique los cambios utilizando el método `UpdateResourceValues`.

Aplique los filtros directamente a la capa y a la máscara de la capa utilizando los métodos `Aplicar` y `AplicarAMáscara` respectivamente.

Guarde la imagen actualizada utilizando el método `Guardar` con el nombre de archivo de salida especificado.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipularFiltrosInteligentesEnObjetosInteligentes-ManipularFiltrosInteligentesEnObjetosInteligentes.cs" >}}

### Aplicación de Filtros Inteligentes a la Máscara de Capa

Los filtros inteligentes son una potente herramienta de edición de imágenes que permite a los usuarios aplicar diversos filtros y efectos. Una técnica interesante es aplicarlos a máscaras, lo que permite controlar con precisión las áreas afectadas por el filtro.

Una máscara es una imagen en escala de grises que determina la transparencia de ciertas áreas de la imagen, aplicando selectivamente filtros, ajustes o efectos.

Al aplicar filtros inteligentes a máscaras, los filtros se aplican solo a las áreas especificadas por la máscara. Este control preciso permite la manipulación de la intensidad y extensión del filtro.

Para obtener más información detallada y ejemplos, consulta la [documentación de Aspose.PSD para C#](https://docs.aspose.com/psd/net/).

