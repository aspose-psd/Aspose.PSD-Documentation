---
title: Manipulación de imágenes PNG
type: docs
weight: 30
url: /es/java/manipulacion-de-imagenes-png/
---

## **Especificar transparencia para imágenes PNG**
Una de las ventajas de guardar imágenes en formato PNG es que PNG puede tener un fondo transparente. Aspose.PSD para Java proporciona la característica para especificar transparencia para las clases PngImage & RasterImage como se muestra en la siguiente sección. Aspose.PSD para Java API se puede utilizar para establecer cualquier color como transparente al crear nuevas imágenes PNG o al convertir imágenes existentes al formato PNG. Para este propósito, la Aspose.PSD para Java API ha expuesto la propiedad TransparentColor y la enumeración PngColorType que se pueden establecer para especificar un color como transparente en la imagen PNG. El fragmento de código proporcionado a continuación demuestra cómo convertir una imagen PSD existente en una imagen PNG utilizando el constructor sobrecargado PngImage y especificando el color deseado como transparente.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-EspecificarTransparencia-EspecificarTransparencia.java" >}}
## **Establecer resolución para imágenes PNG**
Aspose.PSD para Java expone la clase ResolutionSetting que se puede utilizar para establecer la resolución para todos los formatos de imagen, incluido PNG. Este artículo demuestra el uso de la Aspose.PSD para Java API para establecer los parámetros de resolución horizontal y vertical para el formato de imagen PNG. El siguiente fragmento de código carga una imagen PSD existente y la convierte al formato PNG, cambiando también la resolución.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-EstablecerResolucion-EstablecerResolucion.java" >}}
## **Comprimir archivos PNG**
El Formato de Gráficos de Red Portátiles (PNG) es un formato de compresión sin pérdida para transmitir un mapa de bits a través de redes. Cuando guarda una imagen como archivo PNG en cualquier programa, es posible que se le solicite elegir un nivel de compresión en un rango de 0 a cualquier nivel máximo. Establecer este valor comprime en realidad el tamaño del archivo y no disminuye la calidad de la imagen. Este artículo describe cómo Aspose.PSD APIs le permite controlar el tamaño del archivo PNG. Las APIs de Aspose.PSD se pueden utilizar para establecer los Niveles de Compresión para el formato de archivo PNG utilizando la clase PngOptions que tiene una propiedad CompressionLevel de tipo entero. Esta propiedad acepta un valor de 0 a 9, donde 9 es la compresión máxima. El fragmento de código proporcionado a continuación demuestra cómo establecer los Niveles de Compresión utilizando Aspose.PSD para Java API.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-ComprimirArchivos-ComprimirArchivos.java" >}}
## **Especificar profundidad de bits para imágenes PNG**
La profundidad de bits en imágenes es la cantidad de bits utilizados para indicar el color de un píxel en una imagen de mapa de bits. Al igual que todos los demás formatos de mapa de bits, la profundidad de color PNG también se representa en bits como 1 bit (2 colores), 2 bits (4 colores), 4 bits (16 colores) y 8 bits (256 colores). La API de Aspose.PSD para Java se puede utilizar para establecer la profundidad de bits para imágenes PNG utilizando la propiedad BitDepth expuesta por la clase PngOptions. En este momento, la propiedad BitDepth se puede establecer en 1, 2, 4 u 8 bits para tipos de color en escala de grises e indexados. Para todos los demás tipos de color, solo se admiten 8 bits. El fragmento de código proporcionado a continuación demuestra cómo establecer la profundidad de bits para una imagen PNG.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-EspecificarProfundidadBits-EspecificarProfundidadBits.java" >}}
## **Aplicar métodos de filtro en imágenes PNG**
Aspose.PSD para Java expone la enumeración PngFilterType que se puede utilizar para establecer el tipo de filtro para la imagen PNG. El fragmento de código proporcionado a continuación demuestra cómo aplicar un filtro en un archivo PSD existente para convertirlo en una imagen PNG utilizando PngFilterType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-AplicarMetodoFiltro-AplicarMetodoFiltro.java" >}}
## **Cambiar el color de fondo de una imagen PNG transparente**
Las imágenes en formato PNG pueden tener un fondo transparente. Aspose.PSD para Java proporciona la función de cambiar el color de fondo de una imagen PNG que tiene fondo transparente. Aspose.PSD para Java API se puede utilizar para establecer/cambiar el color de una imagen PNG transparente. El fragmento de código proporcionado a continuación demuestra cómo establecer/cambiar el color de fondo de una imagen PNG transparente.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificarYConvertirImagenes-PNG-CambiarColorFondo-CambiarColorFondo.java" >}}
