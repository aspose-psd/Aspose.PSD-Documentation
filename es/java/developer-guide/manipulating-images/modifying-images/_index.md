---
title: Modificando Imágenes
type: docs
weight: 50
url: /es/java/modificando-imagenes/
---

## **Dithering para Imágenes de Mapa de Bits**
El dithering es una técnica para crear la ilusión de nuevos colores y tonos variando el patrón de puntos que en realidad crean una imagen. Es el medio más común para reducir el rango de colores de las imágenes a 256 (o menos) colores. Aspose.PSD proporciona soporte para dithering en la clase RasterImage mediante la introducción del método Dither que acepta dos parámetros. El primero es de tipo DitheringMethod a aplicar con dos opciones posibles: FloydSteinbergDithering y ThresholdDithering. El segundo parámetro para el método Dither es BitCount en entero. BitCount define el tamaño de muestreo para el resultado de dithering. El valor predeterminado es 1 que representa blanco y negro, mientras que los valores permitidos son 1, 4, 8, generando paletas con 2, 4 y 256 colores respectivamente.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}

## **Ajuste de Brillo, Contraste y Gama**
Los ajustes de color en imágenes digitales son una de las características principales que la mayoría de las librerías de procesamiento de imágenes proporcionan. Los ajustes de color se pueden categorizar de la siguiente manera.

1. El brillo se refiere a la claridad u oscuridad del color. Aumentar el brillo de una imagen aclara todos los colores, mientras que disminuir el brillo oscurece todos los colores.
1. El contraste se refiere a hacer que los objetos o detalles dentro de una imagen sean más evidentes. Aumentar el contraste de una imagen aumenta la diferencia entre las áreas claras y oscuras para que las áreas claras se vuelvan más claras y las áreas oscuras se vuelvan más oscuras. Disminuir el contraste hará que las áreas más claras y más oscuras permanezcan aproximadamente iguales, pero la imagen general se vuelve más homogénea.
1. Gamma optimiza el contraste y el brillo de la iluminación indirecta que está iluminando un objeto en la imagen.

### **Ajustar Brillo**
Aspose.PSD para Java API proporciona el método AdjustBrightness para la clase RasterImage que se puede utilizar para ajustar el brillo de la imagen pasando un valor entero como parámetro. El valor más alto del parámetro denota una imagen más brillante. Aquí está la imagen original y la imagen resultante para comparación.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}

### **Ajustar Contraste**
El método AdjustContrast expuesto por la clase RasterImage se puede usar para ajustar el contraste de una imagen pasando un valor flotante como parámetro.

El valor más alto del parámetro denota un mayor contraste en la imagen dada. Aquí está la imagen original y la imagen resultante para comparación.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}

### **Ajustar Gama**
El método AdjustGamma expuesto por la clase RasterImage tiene dos versiones. Una de las sobrecargas acepta un valor flotante y realiza la corrección Gamma para los coeficientes de canal rojo, azul y verde. Mientras que la otra sobrecarga acepta tres parámetros flotantes que representan cada coeficiente de color por separado. El siguiente ejemplo de código demuestra cómo Ajustar Gama en una imagen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}

## **Desenfocar una Imagen**
Este artículo demuestra el uso de Aspose.PSD para Java para realizar un efecto de desenfoque en una imagen. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para Java ha expuesto la clase GaussianBlurFilterOptions para crear un efecto de desenfoque sobre la marcha. La clase GaussianBlurFilterOptions necesita valores de radio y sigma para crear un efecto de desenfoque en una imagen. Los pasos para realizar el Redimensionado son tan simples como se describe a continuación:

1. Cargar una imagen usando el método de fábrica Load expuesto por la clase Image.
1. Convertir la imagen en RasterImage.
1. Crear una instancia de la clase GaussianBlurFilterOptions con el constructor predeterminado o proporcionar valores de radio y sigma en el constructor.
1. Llamar al método RasterImage.Filter especificando el rectángulo como límites de la imagen y la instancia de la clase GaussianBlurFilterOptions.
1. Guardar los resultados.

El siguiente ejemplo de código muestra cómo crear un efecto de desenfoque en una imagen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}

## **Verificar la Transparencia de la Imagen**
Este artículo demuestra el uso de Aspose.PSD para Java para verificar la transparencia de la imagen. Los pasos para verificar la transparencia de la imagen son tan simples como se describen a continuación:

1. Cargar una imagen usando el método de fábrica Load expuesto por la clase Image.
1. Verificar la opacidad de la imagen; si la opacidad es cero, la imagen es transparente.
1. El siguiente ejemplo de código muestra cómo verificar si la imagen es transparente o no.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}

## **Implementar Compresor GIF con Pérdida**
Usando Aspose.PSD para Java, los desarrolladores pueden establecer la diferencia de píxeles. La compresión de GIF se basa en un "diccionario" de cadenas de píxeles vistos. El codificador normal busca en el diccionario la cadena más larga de píxeles que coincida exactamente con los píxeles en la imagen. El codificador con pérdida elige la cadena más larga de píxeles que es "suficientemente similar" a los píxeles en la imagen. A continuación se muestra la demostración de código de la funcionalidad mencionada.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}

## **Implementar Reescalado Bicúbico**
El reescalado significa que se están cambiando las dimensiones de píxeles de una imagen. Cuando se reduce el tamaño, se eliminan píxeles y, por lo tanto, se elimina información y detalles de su imagen. Cuando se aumenta el tamaño, se están agregando píxeles. Photoshop agrega estos píxeles utilizando interpolación. Este artículo demuestra cómo puede realizar la Reescala Bicúbica utilizando Aspose.PSD para Java.

A continuación se muestra la demostración de código de la funcionalidad mencionada.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}

## **Capa de Ajuste Invertido**
Este artículo demuestra cómo puedes realizar la **capa de ajuste invertido** utilizando Aspose.PSD para Java. Una capa de ajuste es un tipo especial de capa utilizado mayormente para la corrección del color. En lugar de tener un contenido propio, ajustan la información en las capas que están debajo de ellas. La capa de ajuste invertido crea un efecto de negativo fotográfico al invertir los colores de una imagen.

A continuación se muestra la demostración de código de la funcionalidad mencionada.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}
