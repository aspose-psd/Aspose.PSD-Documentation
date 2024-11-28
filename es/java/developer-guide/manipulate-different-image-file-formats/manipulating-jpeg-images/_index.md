---
title: Manipulación de imágenes JPEG
type: docs
weight: 20
url: /es/java/manipulacion-de-imagenes-jpeg/
---

## **Usar la clase ExifData para leer y modificar etiquetas EXIF JPEG**


Casi todas las cámaras digitales (incluyendo smartphones), escáneres y otros sistemas que manejan imágenes guardan imágenes con información EXIF (Exchangeable Image File). La cámara registra en el archivo de imagen la configuración de la cámara y la información de la escena. Los datos EXIF también incluyen la velocidad de obturación, la fecha y hora en que se tomó una foto, la longitud focal, la compensación de exposición, el patrón de medición y si se usó un flash. Las APIs de Aspose.Imaging han hecho posible extraer la información EXIF de una imagen dada de una manera fácil y sencilla. Los desarrolladores también pueden escribir datos EXIF en las imágenes o modificar la información existente según sea necesario. Aspose.Imaging ha proporcionado la clase ExifData para leer, escribir y modificar los datos EXIF, donde Aspose.PSD.Exif.Enums namespace contiene las enumeraciones relevantes utilizadas en el proceso.
### **Lectura de datos EXIF**
Las APIs de Aspose.PSD proporcionan medios para leer datos EXIF de una imagen dada. Los pasos proporcionados a continuación ilustran el uso de la clase ExifData para leer la información EXIF de una imagen.

- Cargar la imagen PSD usando el método de fábrica Load.
- Encontrar la miniatura JPEG entre los recursos PSD.
- Extraer una instancia de la clase ExifData.

Obtener la información requerida y escribirla en la consola.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



Alternativamente, los desarrolladores también pueden obtener la información específica utilizando el siguiente fragmento de código.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **Escritura y Modificación de Datos EXIF**
Utilizando las APIs de Aspose.PSD, los desarrolladores pueden escribir nueva información EXIF y modificar datos EXIF existentes de una imagen. Ambos procesos (Escritura y Modificación) requieren cargar una imagen y obtener los datos EXIF en una instancia de la clase ExifData. Luego se puede acceder a las propiedades expuestas por la clase ExifData para configurarlas según sea necesario. Tenga en cuenta que las imágenes para manipulación deben ser imágenes JPEG o TIFF que generalmente son miniaturas PSD. Un código de ejemplo para demostrar el uso es el siguiente:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **Extracción de miniaturas de los recursos PSD**
Las miniaturas son versiones de menor tamaño de imágenes, usadas para mostrar una parte significativa de la imagen en lugar del cuadro completo. Algunos archivos de imagen (especialmente los tomados con una cámara digital) tienen una imagen en miniatura incrustada en el archivo. La API de Aspose.PSD le permite extraer miniaturas de los recursos PSD y almacenarlas por separado en disco. Los recursos de miniaturas contienen la propiedad ExifData.Thumbnail que puede recuperar los datos de miniatura. El fragmento de código proporcionado a continuación demuestra cómo usarlo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Utilice el enfoque discutido anteriormente para almacenar la miniatura en otros formatos de archivo admitidos. Si desea exportar datos de miniatura a otros formatos de imagen como BMP y PNG, utilice otras opciones de exportación de imagen.
### **Extracción de miniaturas de segmentos JFIF**
También es posible extraer miniaturas de los segmentos ExifData o JFIF de los recursos de miniaturas PSD. El siguiente código muestra cómo realizar la extracción de datos de miniatura de los segmentos JFIF o ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



Utilice el enfoque discutido anteriormente para almacenar la miniatura en otros formatos de archivo admitidos. Si desea exportar datos de miniatura a otros formatos de imagen como BMP y PNG, utilice otras opciones de exportación de imagen.
### **Agregar miniatura al segmento JFIF**
El fragmento de código a continuación muestra cómo usar la propiedad JFIF.Thumbnail para agregar una imagen en miniatura al segmento JFIF de una imagen PSD cargada.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

Las imágenes en miniatura con otros datos de segmento no pueden ocupar más de 65,545 bytes debido a las especificaciones del formato JPEG. En casos donde se deben establecer imágenes grandes como miniatura, puede surgir una excepción.


### **Agregar miniatura al segmento EXIF**
El fragmento de código a continuación muestra cómo usar la propiedad ExifData.Thumbnail para agregar una imagen en miniatura al segmento EXIF de una imagen PSD cargada.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

En este caso, la API de Aspose.PSD no puede estimar el tamaño de la imagen en miniatura, pero puede verificar el tamaño de todo el segmento de datos EXIF. Esto no puede ser mayor de 65,535 bytes.
## **Usar la clase JpegExifData para leer y modificar etiquetas EXIF JPEG**
Las APIs de Aspose.PSD proporcionan la clase JpegExifData que es exclusiva para los formatos de imagen JPEG para recuperar y actualizar información EXIF. Este artículo demuestra el uso de la clase JpegExifData para lograr lo mismo. La clase Aspose.PSD.Exif.JpegExifData sirve como contenedor de datos EXIF para imágenes JPEG, y ofrece medios para recuperar etiquetas EXIF estándar de JPEG como se muestra a continuación:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **Lista completa de etiquetas EXIF**
El fragmento de código anterior lee algunas etiquetas EXIF utilizando las propiedades ofrecidas por la clase Aspose.PSD.Exif.JpegExifData. La lista completa de estas propiedades está disponible aquí. El siguiente código leerá todas las etiquetas EXIF utilizando la clase System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **Corrección automática de la orientación de las imágenes JPEG**
Las fotos pueden tomarse con una cámara girada a 90°, 180°, 270° o ninguna (orientación normal). La mayoría de las cámaras digitales almacenan la información de orientación junto con los datos de imagen como etiquetas EXIF de las imágenes JPEG. Esta información se puede utilizar para realizar la rotación automática en las imágenes para corregir la orientación. Las APIs de Aspose.PSD proporcionan el método AutoRotate para la clase JpegImage para corregir automáticamente la orientación de las imágenes JPEG. Así es como se puede usar el método AutoRotate con Aspose.PSD para la API de Java.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **Soporte para JPEG-LS con CMYK y YCCK**


Aspose.PSD para la API de Java proporciona soporte para los modelos de color CMYK y YCCK con JPEG-LS. El fragmento de código a continuación demuestra cómo usar ese soporte para JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportForJPEGLSWithCMYK-SupportForJPEGLSWithCMYK.java" >}}
## **Soporte para imágenes JPEG-LS de 2-7 bits por muestra**


Aspose.PSD para la API de Java proporciona soporte para imágenes JPEG-LS de 2 a 7 bits por muestra. El fragmento de código a continuación demuestra cómo usar ese soporte para JPEG-LS.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-SupportFor2And7BitsJPEG-SupportFor2And7BitsJPEG.java" >}}
## **Establecer ColorType y CompressionType para imágenes JPEG**




Aspose.PSD para la API de Java proporciona soporte para Tipo de Color y Tipo de Compresión y establecerlos como escala de grises y progresivo para imágenes JPEG. El fragmento de código a continuación demuestra cómo usar ese soporte.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.java" >}}


