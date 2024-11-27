---
title: Manipulación de imágenes JPEG
type: docs
weight: 30
url: /es/net/manipulando-imagenes-jpeg/
---

## **Utilizando la Clase ExifData para Leer y Modificar Etiquetas EXIF de Jpeg**
Casi todas las cámaras digitales (incluidos los teléfonos inteligentes), escáneres y otros sistemas que manejan imágenes guardan las imágenes con información EXIF (Exchangeable Image File). La configuración de la cámara y la información de la escena son registradas por la cámara en el archivo de imagen. Los datos EXIF también incluyen la velocidad de obturación, la fecha y la hora en que se tomó una foto, la longitud focal, la compensación de exposición, el patrón de medición y si se utilizó un flash. Las API de Aspose.Imaging han hecho posible extraer la información EXIF de una imagen dada de una manera fácil y sencilla. Los desarrolladores también pueden escribir datos EXIF en las imágenes o modificar la información existente según sus necesidades. Aspose.PSD ha proporcionado la [clase ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) para leer, escribir y modificar los datos EXIF, mientras que el espacio de nombres [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) contiene las enumeraciones relevantes utilizadas en el proceso.

### **Lectura de Datos EXIF**
Las API de Aspose.PSD proporcionan medios para leer datos EXIF de una imagen dada. Los pasos proporcionados a continuación ilustran el uso de la clase ExifData para leer la información EXIF de una imagen.

- Cargar la imagen PSD utilizando el método de fábrica Cargar.
- Encontrar una miniatura Jpeg entre los recursos de PSD.
- Extraer una instancia de la clase ExifData.

Obtener la información requerida y escribirla en la consola.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


Alternativamente, los desarrolladores también pueden obtener la información específica utilizando el siguiente fragmento de código.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}

### **Escritura y Modificación de Datos EXIF**
Utilizando las API de Aspose.PSD, los desarrolladores pueden escribir nueva información EXIF y modificar los datos EXIF existentes de una imagen. Ambos procesos (Escritura y Modificación) requieren cargar una imagen y obtener los datos EXIF en una instancia de la clase ExifData. Entonces uno puede acceder a las propiedades expuestas por la clase ExifData para establecerlas en consecuencia. Tenga en cuenta que las imágenes para la manipulación deben ser imágenes Jpeg o Tiff que generalmente son miniaturas PSD. El código de muestra para demostrar el uso es el siguiente:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **Extracción de miniaturas de los recursos PSD**
Las miniaturas son versiones de tamaño reducido de imágenes, utilizadas para mostrar una parte significativa de la imagen en lugar del marco completo. Algunos archivos de imagen (especialmente los tomados con una cámara digital) tienen una imagen miniatura incrustada en el archivo. La API de Aspose.PSD le permite extraer miniaturas de recursos PSD y almacenarlas por separado en el disco. Los recursos de miniatura contienen la propiedad [Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) de ExifData, que puede recuperar los datos de la miniatura. El fragmento de código proporcionado a continuación demuestra cómo usarlo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

Utilice el enfoque discutido anteriormente para almacenar la miniatura en otros formatos de archivo admitidos. Si desea exportar datos de miniatura a otros formatos de imagen como BMP y PNG, por favor utilice otras opciones de exportación de imagen.

### **Extracción de miniaturas de segmentos JFIF**
También es posible extraer miniaturas de los segmentos ExifData o JFIF de los recursos de miniatura PSD. El siguiente código muestra cómo realizar la extracción de datos de miniaturas del segmento JFIF o ExifData:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

Utilice el enfoque discutido anteriormente para almacenar la miniatura en otros formatos de archivo admitidos. Si desea exportar datos de miniatura a otros formatos de imagen como BMP y PNG, por favor utilice otras opciones de exportación de imagen.

### **Agregar Miniatura al Segmento JFIF**
El fragmento de código a continuación demuestra cómo usar la propiedad JFIF. Thumbnail para agregar una imagen miniatura al segmento JFIF de una imagen PSD cargada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

Las imágenes miniatura con otros datos de segmento no pueden ocupar más de 65,545 bytes debido a las especificaciones del formato JPEG. En casos en los que se deben establecer imágenes grandes como miniatura, puede surgir una excepción.

### **Agregar Miniatura al Segmento EXIF**
El fragmento de código a continuación demuestra cómo usar la propiedad ExifData.Thumbnail para agregar una imagen miniatura al segmento EXIF de una imagen PSD cargada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

En este caso, la API de Aspose.PSD no puede estimar el tamaño de la imagen miniatura, pero puede verificar el tamaño del segmento de datos EXIF completo. Este no puede ser mayor de 65,535 bytes.

## **Utilizando la Clase JpegExifData para Leer y Modificar Etiquetas EXIF de Jpeg**
Las API de Aspose.PSD proporcionan la clase [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) que es exclusiva para formatos de imagen Jpeg para recuperar y actualizar la información EXIF. Este artículo demuestra el uso de la clase JpegExifData para lograr lo mismo. La clase Aspose.PSD.Exif.JpegExifData sirve como contenedor de datos EXIF para imágenes Jpeg y proporciona medios para recuperar etiquetas EXIF Jpeg estándar como se muestra a continuación:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

### **Lista Completa de Etiquetas EXIF**
El fragmento de código anterior lee algunas Etiquetas EXIF utilizando las propiedades ofrecidas por la clase Aspose.PSD.Exif.JpegExifData. La lista completa de estas propiedades está disponible aquí. El siguiente código leerá todas las etiquetas EXIF utilizando la [clase PropertyInfo del sistema de reflexión](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}

## **Corrección Automática de la Orientación de Imágenes JPEG**
Las fotos pueden ser tomadas con una cámara girada a 90°, 180°, 270° o ninguna (orientación normal). La mayoría de las cámaras digitales guardan la información de orientación junto con los datos de la imagen como etiquetas EXIF de las imágenes JEPG. Esta información se puede utilizar para realizar la rotación automática en las imágenes para corregir la orientación. Las API de Aspose.PSD proporcionan el método AutoRotate para la clase JpegImage para corregir automáticamente la orientación de las imágenes JPEG. Así es como se puede usar el método AutoRotate con la API de Aspose.PSD para .NET.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}

## **Soporte para JPEG-LS con CMYK y YCCK**
Aspose.PSD para .NET API proporciona soporte para modelos de color CMYK y YCCK con JPEG-LS. El fragmento de código a continuación demuestra cómo utilizar ese soporte para JPEG-LS.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}

## **Soporte para imágenes JPEG-LS de 2-7 bits por muestra**
Aspose.PSD para .NET API proporciona soporte para imágenes JPEG-LS de 2-7 bits por muestra. El fragmento de código a continuación demuestra cómo utilizar ese soporte para JPEG-LS.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}

## **Configurar ColorType y CompressionType para imágenes JPEG**
Aspose.PSD para .NET API proporciona soporte para Color Type y Compression Type y los establece como escala de grises y progresivo para imágenes JPEG. El fragmento de código a continuación demuestra cómo utilizar ese soporte.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}

El fragmento de código a continuación demuestra cómo usar la propiedad ExifData.Thumbnail para agregar una imagen miniatura al segmento EXIF de una imagen PSD cargada.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

En este caso, la API de Aspose.PSD no puede estimar el tamaño de la imagen miniatura, pero puede verificar el tamaño de todo el segmento de datos EXIF. Esto no puede ser mayor de 65,535 bytes.
