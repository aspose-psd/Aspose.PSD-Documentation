---
title: Recortar, Rotar y Redimensionar Imágenes
type: docs
weight: 40
url: /es/java/recortar-rotar-y-redimensionar-imagenes/
---

## **Recorte de Imágenes**
El recorte de imágenes generalmente se refiere a la eliminación de las partes exteriores de una imagen para mejorar el encuadre. El recorte también puede usarse para cortar alguna porción de una imagen para aumentar el enfoque en una área particular. La API de Aspose.PSD admite dos enfoques diferentes para el recorte de imágenes: mediante desplazamientos y mediante un rectángulo.
### **Recorte por Desplazamientos**
La clase RasterImage proporciona una versión sobrecargada del método Crop que acepta 4 valores enteros que denotan Izquierda, Derecha, Arriba y Abajo. Basándose en estos cuatro valores, el método Crop mueve los límites de la imagen hacia el centro de la imagen mientras descarta la porción exterior. El fragmento de código a continuación demuestra cómo recortar una imagen por desplazamientos.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Recorte por Rectángulo**
La clase RasterImage proporciona otra versión sobrecargada del método Crop que acepta una instancia de la clase Rectangle. Puede recortar cualquier porción de una imagen proporcionando los límites deseados al objeto Rectangle. El fragmento de código a continuación demuestra cómo recortar cualquier imagen por Rectángulo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Rotar e Invertir una Imagen**
Aspose.PSD para Java es una biblioteca fácil de usar porque proporciona métodos simples para realizar operaciones complejas. Por ejemplo, Aspose.PSD para Java ha proporcionado el método RotateFlip para su clase base Image si una aplicación requiere rotar una imagen. Independientemente del formato de la imagen, la biblioteca puede realizar un procedimiento específico de Rotación e Inversión en ella.
### **Rotar una Imagen**
El método Image.RotateFlip se puede utilizar para rotar la imagen 90/180/270 grados e invertir la imagen horizontal o verticalmente. El método Image.RotateFlip acepta un parámetro de tipo RotateFlipType que especifica el tipo de rotación e inversión que se aplicará a la imagen. Los pasos para realizar Rotar e Invertir son tan simples como se muestra a continuación,

1. Cargar la imagen utilizando el método de fábrica Load expuesto por la clase Image.
1. Llamar al método Image.RotateFlip especificando el RotateFlipType apropiado.
1. Guardar los resultados.

El siguiente ejemplo de código demuestra cómo configurar la propiedad RotateFlip de una Imagen y el enumerador RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Rotar una Imagen en un Ángulo Específico**
Aspose.PSD para Java API expone el método RasterImage.Rotate para facilitar a sus usuarios que deseen rotar una imagen en un ángulo específico. A diferencia del método RasterImage.RotateFlip, el método RasterImage.Rotate acepta tres parámetros:

1. Ángulo de rotación: Un parámetro de tipo float que especifica el ángulo de rotación al que se debe girar la imagen. Un valor positivo rota la imagen en sentido horario; un valor negativo realiza una rotación en sentido antihorario.
1. Redimensionar proporcionalmente: Un parámetro de tipo booleano que especifica si el tamaño de la imagen debe cambiarse de acuerdo con las proyecciones del rectángulo rotado (puntos de esquina). Si se establece en false, las dimensiones de la imagen no se verán afectadas y solo se rotarán los contenidos internos de la imagen.
1. Color de fondo: Un parámetro de tipo Color que especifica el color que se llenará en el fondo de la imagen rotada.

El fragmento de código a continuación demuestra el uso del método RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Redimensionar Imágenes**
Este artículo demuestra el uso de Aspose.PSD para Java para realizar la operación de Redimensionar en una imagen. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para Java ha expuesto el método Resize para la clase Image que puede utilizarse para redimensionar imágenes existentes sobre la marcha. Hay dos sobrecargas del método Resize para adaptarse a las necesidades de la aplicación.
### **Redimensionamiento Simple**
Los pasos para realizar Redimensionar son tan simples como se muestra a continuación:

1. Cargar la imagen utilizando el método de fábrica Load expuesto por la clase Image.
1. Llamar al método Image.Resize especificando la nueva Altura y Anchura.
1. Guardar los resultados.

El siguiente ejemplo de código demuestra cómo Redimensionar una imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Redimensionamiento con Enumeración ResizeType**
Aspose.PSD API ha expuesto la enumeración ResizeType que se puede utilizar con Image.Resize para lograr resultados deseados. El fragmento de código proporcionado a continuación demuestra el uso de la enumeración ResizeType, mientras que los detalles de los miembros de la enumeración ResizeType se pueden encontrar en la parte inferior de esta página.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Si desea obtener un resultado de calidad después de aplicar el redimensionamiento, se sugiere que siempre utilice ResizeType.LanczosResample porque producirá resultados altamente cualitativos pero puede funcionar más lento que ResizeType.NearestNeighbourResample. Por otro lado, el algoritmo ResizeType.NearestNeighbourResample se utiliza específicamente para el redimensionamiento rápido mientras se compromete con la calidad de la imagen. Este método puede ser útil para la generación de miniaturas en tiempo real u otros procesos similares donde se requiere rendimiento.
## **Redimensionar Imagen Proporcionalmente**
Puede redimensionar imágenes pasando nuevos valores de altura y anchura como parámetros al método Image.Resize pero en ese caso debe calcular la relación de aspecto usted mismo. Esto se debe a que cuando se altera la anchura o la altura de una imagen, la imagen se escala o se encoge para llenar el nuevo tamaño. Si los cambios en la anchura y altura de una imagen no están en proporción, esto puede dar como resultado una imagen estirada y distorsionada. Este artículo demuestra el uso de Aspose.PSD para la API de Java para redimensionar imágenes pasando ya sea una nueva altura o anchura mientras se permite que la API calcule automáticamente el otro valor proporcional.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Enumeración ResizeType**
ResizeType determina el tipo de redimensionamiento que se debe realizar en la imagen según el filtro seleccionado.

Miembros de la enumeración ResizeType

|**Nombre del Miembro**|**Valor**|**Descripción**|
| :- | :- | :- |
|LeftTopToLeftTop|0|El punto superior izquierdo de la nueva imagen coincidirá con el punto superior izquierdo de la imagen original. Se realizará un recorte si es necesario.|
|RightTopToRightTop|1|El punto superior derecho de la nueva imagen coincidirá con el punto superior derecho de la imagen original. Se realizará un recorte si es necesario.|
|RightBottomToRightBottom|2|El punto inferior derecho de la nueva imagen coincidirá con el punto inferior derecho de la imagen original. Se realizará un recorte si es necesario.|
|LeftBottomToLeftBottom|3|El punto inferior izquierdo de la nueva imagen coincidirá con el punto inferior izquierdo de la imagen original. Se realizará un recorte si es necesario.|
|CenterToCenter|4|El centro de la nueva imagen coincidirá con el centro de la imagen original. Se realizará un recorte si es necesario.|
|LanczosResample|5|Remuestrear utilizando el algoritmo Lanczos con una máscara de 7x7.|
|NearestNeighbourResample|6|Remuestrear utilizando el algoritmo del vecino más cercano.|
