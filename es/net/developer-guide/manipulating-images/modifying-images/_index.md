---
title: Modificando Imágenes
type: docs
weight: 50
url: /es/net/modifying-images/
---

## **Difuminado para Imágenes Raster**
El dithering es una técnica de crear la ilusión de nuevos colores y tonos variando el patrón de puntos que realmente crean una imagen. Es el medio más común de reducir el rango de colores de las imágenes a 256 (o menos) colores. Aspose.PSD proporciona soporte de dithering para la clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) al introducir el método Dither que acepta dos parámetros. El primero es de tipo DitheringMethod que se aplica con dos opciones posibles: FloydSteinbergDithering y ThresholdDithering. El segundo parámetro para el método [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) es BitCount en entero. BitCount define el tamaño de muestreo para el resultado del dithering. El valor predeterminado es 1 que representa blanco y negro, mientras que los valores permitidos son 1, 4, 8 generando paletas con 2, 4 y 256 colores respectivamente.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **Ajuste de Brillo, Contraste y Gamma**
Los ajustes de color en imágenes digitales son una de las características básicas que la mayoría de las bibliotecas de procesamiento de imágenes proporcionan. Los ajustes de color se pueden categorizar de la siguiente manera.

1. El brillo se refiere a la claridad u oscuridad de un color. Aumentar el brillo de una imagen ilumina todos los colores mientras que disminuir el brillo oscurece todos los colores.
1. El contraste se refiere a hacer que los objetos o detalles dentro de una imagen sean más evidentes. Aumentar el contraste de una imagen incrementa la diferencia entre las áreas claras y oscuras para que las áreas claras se vuelvan más claras y las áreas oscuras más oscuras. Disminuir el contraste hará que las áreas más claras y oscuras se mantengan aproximadamente iguales pero la imagen en general se vuelve más homogénea.
1. Gamma optimiza el contraste y brillo de la iluminación indirecta que está iluminando un objeto en la imagen.
### **Ajuste de Brillo**
Aspose.PSD para la API de .NET proporciona el método [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) para la clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) que se puede usar para ajustar el brillo de la imagen pasando un valor entero como parámetro. El valor de parámetro más alto denota una imagen más brillante. Aquí se muestra la imagen original y la imagen resultante para comparación.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **Ajuste de Contraste**
El método [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) expuesto por la clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) se puede usar para ajustar el contraste de una imagen pasando un valor flotante como parámetro.

El valor del parámetro más alto denota un mayor contraste en la imagen dada. Aquí se muestra la imagen original y la imagen resultante para comparación.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **Ajuste de Gamma**
El método [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) expuesto por la clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) tiene dos versiones. Una de las sobrecargas acepta un valor flotante y realiza la corrección Gamma para los coeficientes de los canales rojo, azul y verde. Mientras que la otra sobrecarga acepta tres parámetros flotantes que representan cada coeficiente de color por separado. El siguiente ejemplo de código demuestra cómo ajustar el Gamma en una imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **Desenfocar una Imagen**
Este artículo demuestra el uso de Aspose.PSD para .NET para realizar el efecto de desenfoque en una imagen. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD para .NET ha expuesto la clase [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) para crear un efecto de desenfoque sobre la marcha. La clase [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) necesita valores de radio y sigma para crear un efecto de desenfoque en una imagen. Los pasos para realizar el cambio de tamaño son tan simples como se muestra a continuación.

1. Cargar una imagen usando el método de fábrica Load expuesto por la clase Image.
1. Convertir la imagen en [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Crear una instancia de la clase [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) con el constructor predeterminado o proporcionar valores de radio y sigma en el constructor.
1. Llamar al método [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter especificando el rectángulo como límites de la imagen y la instancia de la clase [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Guardar los resultados.

El siguiente ejemplo de código demuestra cómo crear un efecto de desenfoque en una imagen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **Verificar la Transparencia de la Imagen**
Este artículo demuestra el uso de Aspose.PSD para .NET para verificar la transparencia de la imagen. Los pasos para verificar la transparencia de la imagen son tan simples como se muestran a continuación.

1. Cargar una imagen usando el método de fábrica [Load](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) expuesto por la clase [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Verificar la opacidad de la imagen; si la opacidad es cero, la imagen es transparente.
1. El siguiente ejemplo de código demuestra cómo verificar si la imagen es transparente o no.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **Implementar un Compresor GIF con Pérdida**
Utilizando Aspose.PSD para .NET, los desarrolladores pueden establecer una diferencia de píxeles. La compresión de GIF se basa en un "diccionario" de secuencias de píxeles observadas. Un codificador normal busca en el diccionario la secuencia más larga de píxeles que coincidan exactamente con los píxeles de la imagen. El codificador con pérdida selecciona la secuencia más larga de píxeles que es "lo suficientemente similar" a los píxeles de la imagen. A continuación se muestra la demostración de código de dicha funcionalidad.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **Implementar el Remuestreo Bicúbico**
El remuestreo significa que se están cambiando las dimensiones de los píxeles de una imagen. Cuando se reduce la resolución, se están eliminando píxeles y, por lo tanto, se está eliminando información y detalle de la imagen. Cuando se aumenta la resolución, se están agregando píxeles. Photoshop agrega estos píxeles utilizando interpolación. Este artículo demuestra cómo se puede realizar el Remuestreo Bicúbico utilizando Aspose.PSD para .NET.

A continuación se muestra la demostración de código de dicha funcionalidad.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **Capa de Ajuste del Equilibrio de Color**
Este artículo demuestra el uso de Aspose.PSD para .NET para realizar la **capa de ajuste del equilibrio de color** en una imagen. La capa de ajuste del equilibrio de color le brinda la capacidad de realizar ajustes en la coloración de sus imágenes. Presenta los tres canales de color y sus colores complementarios y puede ajustar el equilibrio de estos pares para cambiar la apariencia de una foto.

A continuación se muestra la demostración de código de dicha funcionalidad.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ColorBalanceAdjustment-ColorBalanceAdjustment.cs" >}}
## **Capa de Ajuste de Inversión**
Este artículo demuestra cómo se puede realizar la **capa de ajuste de inversión** utilizando Aspose.PSD para .NET. Una capa de ajuste es un tipo especial de capa utilizado principalmente para la corrección del color. En lugar de tener un contenido propio, ajustan la información en las capas debajo de ellas. La capa de ajuste de inversión produce un efecto de negativo en una foto al invertir los colores de una imagen.

A continuación se muestra la demostración de código de dicha funcionalidad.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.cs" >}}
