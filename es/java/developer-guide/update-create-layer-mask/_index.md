---
title: Trabajar con máscaras en Aspose.PSD para Java
weight: 100
type: docs
description: Ejemplos de cómo trabajar con Máscaras de Recorte, Raster y Vector dentro de un Archivo PSD
keywords: [máscaras, máscara de capa, máscara vectorial, máscara de recorte, psd, api de psd, java, ejemplo de código]
url: es/java/update-create-layer-mask/
---

## **Resumen**

**Resumen**
	
	Existen 3 tipos de máscaras en archivos PSD:
	1. Máscaras de Recorte
	2. Máscaras Raster
	3. Máscaras Vectoriales
	
	Este artículo cubre los 3 tipos.

** Máscaras de Recorte **

Las máscaras de recorte son una característica sólida en software de diseño gráfico y edición de imágenes, especialmente en Java. Permiten un control preciso sobre la visibilidad de una capa en función de la forma y contenido de otra capa. Básicamente, una máscara de recorte restringe la visibilidad de una capa a la forma de otra capa debajo de ella.

Para implementar una máscara de recorte en Java, primero necesitarás dos capas: la capa base y la capa que deseas recortar. La capa base define la forma o área que permanecerá visible, mientras que la capa a recortar contiene el contenido que se conformará a la forma de la capa base.

Cuando se aplica una máscara de recorte en Java, el contenido de la capa recortada solo es visible dentro de los límites de la capa base. Cualquier contenido fuera de estos límites estará oculto o recortado.

Las máscaras de recorte son especialmente valiosas al aplicar efectos, como texturas o patrones, a áreas específicas de una imagen o trabajo artístico. Al emplear una máscara de recorte, puedes limitar el efecto al área deseada sin afectar al resto de la imagen.

Consulta el ejemplo al final de la página para mayor claridad.

** Máscaras Raster **

Las máscaras raster en archivos Java se emplean para gestionar la visibilidad de áreas específicas dentro de una capa. A diferencia de las máscaras vectoriales, que utilizan formas matemáticas para definir áreas enmascaradas, las máscaras raster dependen de información basada en píxeles para determinar regiones visibles u ocultas.

Una máscara raster consta de una imagen en escala de grises aplicada a una capa. Las áreas blancas de la máscara denotan visibilidad, mientras que las áreas negras representan porciones ocultas. Tonos de gris intermedios pueden crear transparencia parcial o regiones semivisibles.

Consulta el ejemplo al final de la página para una mejor comprensión.

** Máscaras Vectoriales **

Las máscaras vectoriales en archivos Java son herramientas versátiles utilizadas para delimitar la visibilidad de áreas específicas dentro de una capa basada en formas matemáticas. A diferencia de las máscaras raster, que dependen de datos basados en píxeles, las máscaras vectoriales emplean trazados y curvas para crear áreas enmascaradas suaves y escalables.

Una máscara vectorial consiste esencialmente en un trazado aplicado a una capa. La forma de este trazado determina qué partes de la capa son visibles y cuáles están ocultas. Al manipular los puntos de control y curvas del trazado, se pueden crear áreas enmascaradas precisas e intrincadas.

Consulta la [página de Máscaras Vectoriales](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) para obtener información sobre cómo agregar máscaras vectoriales utilizando recursos.

## **Ejemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentación-Java-Aspose-psd-update-create-layer-mask.java" >}}
