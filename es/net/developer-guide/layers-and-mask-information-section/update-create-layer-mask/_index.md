---
title: Trabajar con máscaras en Aspose.PSD para C#
weight: 100
type: docs
description: Ejemplos de cómo trabajar con Máscaras de Recorte, Raster y Vector dentro de un Archivo PSD
keywords: [máscaras, máscara de capa, máscara vectorial, máscara de recorte, psd, psd api, C#, csharp, ejemplo de código]
url: es/net/actualizar-crear-mascara-de-capa/
---

## Resumen

Hay tres tipos de máscaras en archivos PSD:
1. Máscaras de Recorte
2. Máscaras Raster
3. Máscaras Vectoriales

Este artículo cubre los tres tipos.

### Máscaras de Recorte

Las máscaras de recorte son una característica poderosa en el diseño gráfico y software de edición de imágenes que te permiten controlar la visibilidad de una capa basándose en la forma y contenido de otra capa. Básicamente, una máscara de recorte restringe la visibilidad de una capa a la forma definida por otra capa debajo de ella.

Para crear una máscara de recorte, necesitas dos capas: la capa base y la capa de recorte. La capa base define la forma o área que será visible, mientras que la capa de recorte contiene el contenido que estará limitado a la forma de la capa base.

Cuando aplicas una máscara de recorte, el contenido de la capa de recorte solo es visible dentro de los límites de la capa base. Cualquier contenido fuera de los límites de la capa base se oculta o se recorta.

Las máscaras de recorte son particularmente útiles para aplicar efectos, como texturas o patrones, a áreas específicas de una imagen o ilustración. Al usar una máscara de recorte, puedes asegurarte de que el efecto esté limitado al área deseada sin afectar al resto de la imagen.

### Máscaras Raster

Las máscaras raster en archivos PSD son esenciales para controlar la visibilidad de áreas específicas dentro de una capa. A diferencia de las máscaras vectoriales, que utilizan formas matemáticas para definir áreas enmascaradas, las máscaras raster utilizan información basada en píxeles para determinar cuáles partes de una capa son visibles u ocultas.

Una máscara raster consiste en una imagen en escala de grises aplicada a una capa. Las áreas blancas de la máscara representan las porciones visibles, mientras que las áreas negras representan las porciones ocultas. Tonos de gris intermedios crean transparencia parcial o áreas semi-visibles.

Usando máscaras raster, puedes lograr efectos de enmascaramiento intrincados, permitiendo un control preciso sobre la visibilidad de las capas basado en detalles a nivel de píxel. Esta función es particularmente útil para tareas que requieren ediciones detalladas y mezcla dentro de una imagen.

### Máscaras Vectoriales

Las máscaras vectoriales en archivos PSD son una herramienta versátil usada para definir la visibilidad de áreas específicas dentro de una capa basadas en formas matemáticas. A diferencia de las máscaras raster, que utilizan información basada en píxeles, las máscaras vectoriales utilizan trayectorias y curvas para crear áreas enmascaradas suaves y escalables.

Una máscara vectorial es esencialmente una trayectoria aplicada a una capa. La forma de la trayectoria determina qué partes de la capa son visibles y cuáles están ocultas. Al manipular los puntos de control y curvas de la trayectoria, puedes crear áreas enmascaradas precisas e intrincadas.

Las máscaras vectoriales son particularmente útiles para crear máscaras limpias y escalables que pueden ajustarse fácilmente sin pérdida de calidad. Esta función es ideal para tareas que requieren alta precisión y flexibilidad al definir áreas visibles dentro de una capa.

Para obtener más información sobre cómo añadir máscaras vectoriales, visita la página de [Máscaras Vectoriales](psd/es/net/capa-mascara-vector/).

## Ejemplo
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "TrabajarConMascaras-TrabajarConMascaras.cs" >}}

Para obtener información más detallada y ejemplos, visita la [documentación de Aspose.PSD para C#](https://docs.aspose.com/psd/net/).
