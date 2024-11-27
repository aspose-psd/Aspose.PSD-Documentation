---
title: Manipulación de imágenes TIFF
type: docs
weight: 40
url: /es/java/manipulando-imagenes-tiff/
---

## **Agregar marcos con diferentes ajustes**
TIFF es un formato muy flexible y permite agregar diferentes marcos, con diferentes dimensiones, compresión y otros ajustes. Las APIs de Aspose.PSD le permiten agregar cualquier marco TIFF de cualquier tamaño, lo cual ayuda en la creación de documentos complejos. Si hay un requisito para ajustar los marcos durante el proceso de adición para hacerlos todos iguales, realice los siguientes pasos:

- Cree un nuevo marco en blanco con las opciones deseadas o copie el marco fuente con las opciones de salida especificadas utilizando el método CreateFrameFrom.
- Redimensione el marco/imagen fuente a las dimensiones deseadas utilizando el método Resize.
- Agregue los píxeles del marco/imagen fuente al nuevo marco.
- Agregue el nuevo marco a la imagen TIFF de salida.
## **Exportar capas de una imagen PSD a un archivo TIFF de varias páginas**
A veces se necesita exportar las capas de una imagen PSD a un archivo TIFF de varias páginas. Este artículo demostrará cómo podemos realizar esta tarea utilizando la API Aspose.PSD para Java. Primero, cargaremos la imagen PSD desde el disco. Luego recorreremos las capas de la imagen PSD y crearemos un TiffFrame a partir de las capas correspondientes. Finalmente, guardaremos la imagen TIFF resultante en un solo archivo en el disco.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **Configuración de TiffOptions**
Los desarrolladores pueden ajustar diferentes propiedades de la clase Tiffoptions para obtener los resultados deseados. En este documento, nos enfocaremos en 4 propiedades principales que controlan los atributos de la imagen resultante.

Estas propiedades se enumeran a continuación.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

Cuando inicializamos una estructura vacía de Tiffoptions, cada opción se establece en su valor predeterminado, por ejemplo, la compresión se establece en Ninguna, BitsPerSample se establece en 1 y Photometric como MinIsWhite. Guardar en este formato hará que la imagen final sea en blanco y negro, y este es el comportamiento esperado para esa combinación de opciones. Para obtener resultados en color, debe establecer todas las propiedades mencionadas anteriormente en valores que correspondan al espacio de color deseado o puede inicializar la estructura de Tiffoptions con configuraciones predefinidas, como se discute más adelante en este artículo. A continuación se proporciona una tabla que describe los valores de parámetros esperados que puede establecer para lograr los resultados deseados. Tenga en cuenta que debe establecer las 4 columnas a través de Tiffoptions para guardar cualquier imagen cargada/creada en formato TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Paleta|LZW/No comprimido|1/4/8/16 (paleta, modo de color) un solo canal solamente|Ninguno|
|MinIsWhite/MinIsBlack|LZW/No comprimido|1/4/8/16 (modo de escala de grises) un solo canal solamente|Ninguno|
|Paleta|LZW/No comprimido|8 (paleta, modo de color) un solo canal solamente|Horizontal (más compresión lograda para LZW en los mismos patrones)|
|MinIsWhite/MinIsBlack|LZW/No comprimido|8 (modo de escala de grises) un solo canal solamente|Horizontal (más compresión lograda para LZW en los mismos patrones)|
|RGB|LZW/No comprimido|[8,8,8] (3 canales RGB)|Ninguno/Horizontal|
|RGB|LZW/No comprimido|[8,8,8,8] (3 canales RGB y canal alfa adicional que se puede establecer a través de TiffOptions.AlphaStorage) Realmente se admite cualquier cantidad adicional de canales pero cada canal debe tener un tamaño de 8 bits como [8,8,8,8,8,8]|Ninguno/Horizontal|
Las 4 propiedades deben establecerse a través de TiffOptions para guardar cualquier formato de imagen en formato TIFF. Al emplear diferentes combinaciones, algunos visualizadores (incluido el Visor de fotos de Windows) pueden negarse a renderizar la imagen resultante debido al soporte limitado que ofrecen. En tal caso, elija un visualizador diferente para sus pruebas.
### **Configuraciones predefinidas para la clase TiffOptions**
Para facilitar a los usuarios y evitar la mala configuración de la instancia de Tiffoptions, la API Aspose.PSD para Java ha expuesto otro constructor que acepta un parámetro de tipo TiffExpectedFormat. Según el valor seleccionado de la enumeración TiffExpectedFormat, la API configura automáticamente todas las propiedades obligatorias para la instancia de Tiffoptions para producir los resultados deseados. Antes de pasar al código de ejemplo, aquí está la lista de los campos TiffExpectedFormat y sus detalles para una mejor comprensión del uso.



- TiffExpectedFormat.Default: Establecer el campo en Default actúa de manera similar al constructor predeterminado de la clase Tiffoptions sin compresión configurada y BitsPerPixel establecido en 1 para obtener un resultado en blanco y negro. Se recomienda usar este campo cuando otras propiedades específicas del formato deben establecerse manualmente según los resultados deseados.
- TiffExpectedFormat.TiffCcitRle: Específico para la codificación RLE al guardar el resultado en formato TIFF de 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffCcittFax3: Específico para la codificación CCITT Fax3 al guardar el resultado en formato TIFF de 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffCcittFax4: Específico para la codificación CCITT Fax4 al guardar el resultado en formato TIFF de 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffDeflateBW: Específico para la compresión Deflate al guardar el resultado en formato TIFF de 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffDeflateRGB: Específico para la compresión Deflate al guardar el resultado en formato TIFF RGB (color).
- TiffExpectedFormat.TiffJpegRGB: Específico para la compresión Jpeg al guardar el resultado en formato TIFF RGB (color).
- TiffExpectedFormat.TiffJpegYCBCR: Específico para la compresión Deflate al guardar el resultado en formato TIFF YCBCR (color).
- TiffExpectedFormat.TiffLzwBW: Específico para la compresión LZW al guardar el resultado en formato TIFF de 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffLzwRGB: Específico para la compresión LZW al guardar el resultado en formato TIFF RGB (color).
- TiffExpectedFormat.TiffLzwRGBA: Específico para la compresión LZW al guardar el resultado en formato TIFF RGBA (color con transparencia).
- TiffExpectedFormat.TiffNoCompressionBW: Específico para el formato TIFF sin compresión al guardar el resultado en 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffNoCompressionRGB: Específico para el formato TIFF sin compresión al guardar el resultado en formato RGB (color).
- TiffExpectedFormat.TiffNoCompressionRGBA: Específico para el formato TIFF sin compresión al guardar el resultado en formato RGBA (color con transparencia).



El siguiente fragmento de código elabora el uso de los campos de TiffExpectedFormat al crear una instancia de la clase Tiffoptions.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}
## **Soporte para compresión Deflate y Adobe Deflate**
El formato de archivo TIFF (Tagged Image File Format) admite varios tipos de compresión, siendo el tipo de compresión almacenado como una etiqueta (un valor entero) en el archivo. Uno de esos métodos de compresión es Adobe Deflate (anteriormente conocido como Deflate). La API de Aspose.PSD para Java admite este método de compresión para la exportación y creación de imágenes TIFF.
### **Guardar imagen en TIFF con compresión Deflate**
Convertir las imágenes cargadas en TIFF con compresión Deflate/Adobe Deflate es fácil de seguir.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Creación de TiffImage con compresión Adobe Deflate**
El ejemplo proporcionado a continuación demuestra el uso de la API de Aspose.PSD para Java para crear una imagen desde cero utilizando el método de compresión Adobe Deflate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **Compresión de imágenes TIFF**
La API de Aspose.PSD para Java se puede usar para convertir imágenes PSD al formato de imagen TIFF e incluso cambiar la compresión de la imagen TIFF resultante. La API también se puede usar para almacenar diferentes imágenes como marcos en una imagen TIFF con fines de archivo al comprimir las imágenes al tamaño de datos más bajo. La compresión de imágenes en cualquier caso debe realizarse reduciendo el tamaño de los datos fuente independientemente del algoritmo de compresión utilizado. Para lograr la mejor relación de compresión, podemos usar espacios de color indexados. El fragmento de código proporcionado a continuación realiza la mejor compresión usando solo 16 colores indexados y el algoritmo de compresión LZW, sin embargo, los colores fuente están ligeramente entrelazados.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
