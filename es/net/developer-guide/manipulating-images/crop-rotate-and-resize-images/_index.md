---
title: Recortar, Rotar y Redimensionar Imágenes
type: docs
weight: 40
url: /es/net/recortar-rotar-y-redimensionar-imagenes/
---

## **Recortar Imágenes**
El recorte de imágenes generalmente se refiere a la eliminación de las partes externas de una imagen para ayudar a mejorar el encuadre. El recorte también se puede utilizar para cortar alguna parte de una imagen y aumentar el enfoque en una área particular. La API de Aspose.PSD admite dos enfoques diferentes para el recorte de imágenes: por desplazamientos y por rectángulo.
### **Recortar por Desplazamientos**
La clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) proporciona una versión sobrecargada del método Crop que acepta 4 valores enteros que denotan Izquierda, Derecha, Arriba y Abajo. En base a estos cuatro valores, el método Crop mueve los límites de la imagen hacia el centro de la imagen mientras descarta la porción exterior. El fragmento de código a continuación muestra cómo recortar una imagen por desplazamientos.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Recortar por Rectángulo**
La clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) también proporciona otra versión sobrecargada del método Crop que acepta una instancia de la clase Rectangle. Se puede recortar cualquier parte de una imagen proporcionando los límites deseados al objeto Rectangle. El fragmento de código a continuación muestra cómo recortar cualquier imagen por Rectángulo.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Rotar y Voltear una Imagen**
Aspose.PSD para .NET es una biblioteca fácil de usar porque proporciona métodos simples para realizar operaciones complejas. Por ejemplo, Aspose.PSD para .NET ha proporcionado el método RotateFlip para su clase base Image si una aplicación requiere rotar una imagen. Independientemente del formato de la imagen, la biblioteca puede realizar un procedimiento específico de Rotar y Voltear.
### **Rotar una Imagen**
El método Image.RotateFlip se puede utilizar para rotar la imagen 90/180/270 grados y voltear la imagen horizontal o verticalmente. El método Image.RotateFlip acepta un parámetro de RotateFlipType que especifica el tipo de rotación y volteo que se aplicará a la imagen. Los pasos para realizar Rotar y Voltear son tan simples como los siguientes,

1. Cargar la imagen utilizando el método de fabricación Load expuesto por la clase Image.
1. Llamar al método Image.RotateFlip especificando el RotateFlipType apropiado.
1. Guardar los resultados.

El siguiente ejemplo de código muestra cómo establecer la propiedad RotateFlip de una imagen y la enumeración RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Rotar una Imagen en un Ángulo Específico**
Aspose.PSD para .NET API expone el método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate para facilitar a sus usuarios que deseen rotar una imagen en un ángulo específico. A diferencia del método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, el método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate acepta tres parámetros:

1. Ángulo de rotación: un parámetro de tipo flotante que especifica el ángulo de rotación al que se debe girar la imagen. Un valor positivo gira la imagen en el sentido de las agujas del reloj; un valor negativo realiza una rotación en sentido antihorario.
1. Redimensionar proporcionalmente: un parámetro de tipo booleano que especifica si el tamaño de la imagen debe cambiarse según las proyecciones del rectángulo rotado (puntos de la esquina). Si se establece en falso, las dimensiones de la imagenserán intocadas y solo se rotarán los contenidos internos de la imagen.
1. Color de fondo: un parámetro de tipo Color que especifica el color a llenar en el fondo de la imagen rotada.

El fragmento de código a continuación muestra el uso del método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Redimensionar Imágenes**
Este artículo demuestra el uso de Aspose.PSD para .NET para realizar la operación de Redimensionar en una imagen. Las APIs de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para .NET ha expuesto el método Resize para la clase Image que se puede utilizar para redimensionar imágenes existentes sobre la marcha. Hay dos sobrecargas del método Resize para adaptarse a las necesidades de la aplicación.
### **Redimensionar Simple**
Los pasos para realizar la Redimensión son tan simples como los siguientes:

1. Cargar la imagen utilizando el método de fabricación Load expuesto por la clase Image.
1. Llamar al método Image.Resize especificando la nueva Altura y Ancho.
1. Guardar los resultados.

El siguiente ejemplo de código muestra cómo Redimensionar una imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Redimensionar con la Enumeración ResizeType**
Aspose.PSD API ha expuesto la enumeración ResizeType que se puede utilizar con Image.Resize para lograr los resultados deseados. El fragmento de código proporcionado a continuación demuestra el uso de la enumeración ResizeType, mientras que los detalles de los miembros de la enumeración ResizeType se pueden encontrar en la parte inferior de esta página.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



Si desea obtener un resultado de calidad después de aplicar el redimensionamiento, se sugiere que siempre use ResizeType.LanczosResample porque producirá resultados de alta calidad pero puede trabajar más lentamente que ResizeType.NearestNeighbourResample. Por otro lado, el algoritmo ResizeType.NearestNeighbourResample se utiliza específicamente para el redimensionamiento rápido a expensas de la calidad de la imagen. Este método puede ser útil para la generación de miniaturas en tiempo real u otros procesos similares donde se requiera rendimiento.
## **Redimensionar Imagen Proporcionalmente**
Puede redimensionar imágenes pasando nuevos valores de altura y ancho como parámetros al método Image.Resize pero en ese caso debe calcular la relación de aspecto usted mismo. Esto se debe a que cuando la anchura o altura de una imagen se modifica, la imagen se escala o reduce para ocupar el nuevo tamaño. Si los cambios en la anchura y altura de una imagen no están en proporción, esto puede dar como resultado una imagen estirada y distorsionada. Este artículo demuestra el uso de Aspose.PSD para .NET API para redimensionar imágenes pasando ya sea la nueva altura o ancho al permitir que la API calcule automáticamente el otro valor proporcional.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Enumeración ResizeType**
ResizeType determina el tipo de redimensionamiento que se realizará en la imagen según el filtro seleccionado.

Miembros de la Enumeración [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**Nombre del Miembro**|**Valor**|**Descripción**|
| :- | :- | :- |
|LeftTopToLeftTop|0|El punto superior izquierdo de la nueva imagen coincidirá con el punto superior izquierdo de la imagen original. Se producirá un recorte si es necesario.|
|RightTopToRightTop|1|El punto superior derecho de la nueva imagen coincidirá con el punto superior derecho de la imagen original. Se producirá un recorte si es necesario.|
|RightBottomToRightBottom|2|El punto inferior derecho de la nueva imagen coincidirá con el punto inferior derecho de la imagen original. Se producirá un recorte si es necesario.|
|LeftBottomToLeftBottom|3|El punto inferior izquierdo de la nueva imagen coincidirá con el punto inferior izquierdo de la imagen original. Se producirá un recorte si es necesario.|
|CenterToCenter|4|El centro de la nueva imagen coincidirá con el centro de la imagen original. Se producirá un recorte si es necesario.|
|LanczosResample|5|Redimensionar usando el algoritmo Lanczos usando una máscara 7x7.|
|NearestNeighbourResample|6|Redimensionar usando el algoritmo del vecino más cercano.|
