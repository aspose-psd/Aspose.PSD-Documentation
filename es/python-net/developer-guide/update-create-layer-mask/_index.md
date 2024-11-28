---
title: Trabajar con máscaras en Aspose.PSD para Python
weight: 100
type: docs
description: Ejemplos de cómo trabajar con Máscaras de Recorte, Raster y Vector dentro de un Archivo PSD
keywords: [máscaras, máscara de capa, máscara vectorial, máscara de recorte, psd, api psd, python, muestra de código]
url: es/python-net/update-create-layer-mask/
---

## **Visión general**

**Visión general**

Hay 3 tipos de máscaras en archivos PSD:
1. Máscaras de Recorte
2. Máscaras Raster
3. Máscaras Vectoriales

Este artículo cubre los 3 tipos.

**Máscaras de Recorte**

Las máscaras de recorte son una característica poderosa en software de diseño gráfico y edición de imágenes. Te permiten controlar la visibilidad de una capa basada en la forma y contenido de otra capa. En otras palabras, una máscara de recorte restringe la visibilidad de una capa a la forma de otra capa debajo de ella.

Para crear una máscara de recorte, primero necesitas dos capas: la capa base y la capa que deseas recortar. La capa base define la forma o área que será visible, mientras que la capa que deseas recortar contiene el contenido que se recortará a la forma de la capa base.

Cuando aplicas una máscara de recorte, el contenido de la capa recortada solo es visible dentro de los límites de la capa base. Cualquier contenido fuera de los límites de la capa base estará oculto o recortado.

Las máscaras de recorte son particularmente útiles cuando deseas aplicar un efecto, como una textura o patrón, a una área específica de una imagen o obra de arte. Al usar una máscara de recorte, puedes confinar el efecto al área deseada sin afectar al resto de la imagen.

Por favor, comprueba el ejemplo al final de la página.

**Máscaras Raster**

Las máscaras raster en archivos PSD se utilizan para controlar la visibilidad de áreas específicas dentro de una capa. A diferencia de las máscaras vectoriales, que utilizan formas matemáticas para definir las áreas enmascaradas, las máscaras raster utilizan información basada en píxeles para determinar qué partes de una capa son visibles u ocultas.

Una máscara raster consiste en una imagen en escala de grises que se aplica a una capa. Las áreas blancas de la máscara representan las porciones visibles, mientras que las áreas negras representan las porciones ocultas. Tonos de gris en medio se pueden utilizar para crear transparencia parcial o áreas semivisibles.

Por favor, comprueba el ejemplo al final de la página.

**Máscaras Vectoriales**

Las máscaras vectoriales en archivos PSD son una herramienta versátil utilizada para definir la visibilidad de áreas específicas dentro de una capa basada en formas matemáticas. A diferencia de las máscaras raster, que utilizan información basada en píxeles, las máscaras vectoriales utilizan caminos y curvas para crear áreas enmascaradas suaves y escalables.

Una máscara vectorial es esencialmente un camino que se aplica a una capa. La forma del camino determina qué partes de la capa son visibles y cuáles están ocultas. Manipulando los puntos de control y curvas del camino, puedes crear áreas enmascaradas precisas e intrincadas.

Por favor, consulta la [página de Máscaras Vectoriales](psd/es/net/layer-vector-mask/) para obtener información sobre cómo se pueden agregar máscaras vectoriales utilizando recursos.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentación-Python-Aspose-psd-update-create-layer-mask.py" >}}
