---
title: Manipulación de imágenes TIFF
type: docs
weight: 50
url: /es/net/manipulacion-imagenes-tiff/
---

## **Agregar marcos con configuraciones diferentes**
TIFF es un formato muy flexible que permite agregar diferentes marcos con dimensiones, compresión y otras configuraciones diferentes. Las APIs de Aspose.PSD te permiten agregar cualquier marco TIFF de cualquier tamaño, lo que ayuda a crear documentos complejos. Si se requiere ajustar los marcos durante el proceso de agregarlos para que todos sean iguales, realiza los siguientes pasos:

- Crea un nuevo marco en blanco con las opciones deseadas o copia el marco fuente con las opciones de salida especificadas mediante el método CreateFrameFrom.
- Cambia el tamaño del marco/imagen fuente a las dimensiones deseadas utilizando el método Resize.
- Agrega los píxeles del marco/imagen fuente al nuevo marco.
- Agrega el nuevo marco a la imagen TIFF de salida.
## **Exportar capas de una imagen PSD a formato de archivo TIFF de varias páginas**
A veces es necesario exportar las capas de una imagen PSD a un archivo TIFF de varias páginas. Este artículo demostrará cómo podemos realizar esta tarea utilizando la API de Aspose.PSD para .NET. Primero, cargaremos la imagen PSD desde el disco. Luego iteraremos sobre las capas de la imagen PSD y crearemos un TiffFrame a partir de las capas correspondientes. Finalmente guardaremos la imagen Tiff resultante en un único archivo en el disco.



## **Configuración de TiffOptions**
Los desarrolladores pueden ajustar diferentes propiedades de la clase [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) para obtener los resultados deseados. En este documento, nos enfocaremos en 4 propiedades principales que controlan los atributos de la imagen resultante.

Estas propiedades se enumeran a continuación.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

Cuando inicializamos una estructura TiffOptions vacía, cada opción se establece en su valor predeterminado, por ejemplo, la compresión se establece en Ninguna, BitsPerSample se establece en 1 y Photometric como MinimumIsWhite. Guardar en este formato hará que la imagen final sea en blanco y negro, y este es el comportamiento esperado para esa combinación de opciones. Para obtener resultados en color, debes establecer todas las propiedades mencionadas anteriormente en valores que correspondan al espacio de color deseado o puedes inicializar la estructura TiffOptions con configuraciones predefinidas como se discute más adelante en este artículo. A continuación se proporciona una tabla que describe los valores de parámetro esperados que puedes establecer para lograr los resultados deseados. Ten en cuenta que debes establecer las 4 columnas a través de TiffOptions para guardar cualquier imagen cargada/creada en formato TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Paleta|LZW/Sin compresión|1/4/8/16 (paleta, modo de color) solo un canal|Ninguno|
|MinimumIsWhite/MinimumIsBlack|LZW/Sin compresión|1/4/8/16 (modo de escala de grises) solo un canal|Ninguno|
|Paleta|LZW/Sin compresión|8 (paleta, modo de color) solo un canal|Horizontal (mayor compresión lograda para LZW mismos patrones)|
|MinimumIsWhite/MinimumIsBlack|LZW/Sin compresión|8 (modo de escala de grises) solo un canal|Horizontal (mayor compresión lograda para LZW mismos patrones)|
|RGB|LZW/Sin compresión|[8,8,8] (3 canales RGB)|Ninguno/Horizontal|
|RGB|LZW/Sin compresión|[8,8,8,8] (3 canales RGB y canal alfa adicional se puede establecer a través de TiffOptions.AlphaStorage) En realidad, se admite cualquier recuento adicional de canales, pero cada canal debe tener un tamaño de 8 bits como [8,8,8,8,8,8]|Ninguno/Horizontal|
Las 4 propiedades deben establecerse a través de TiffOptions para guardar cualquier formato de imagen en formato TIFF. Al emplear diferentes combinaciones, algunos visores (incluido el Visor de fotos de Windows) pueden rechazar renderizar la imagen resultante debido al soporte limitado que ofrecen. En ese caso, elige un visor diferente para tus pruebas.
### **Configuraciones predefinidas para la clase TiffOptions**
Para facilitar a los usuarios y evitar la mala configuración de la instancia de TiffOptions, la API de Aspose.PSD para .NET ha expuesto otro constructor que acepta un parámetro de tipo [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). Según el valor seleccionado de la enumeración TiffExpectedFormat, la API configura automáticamente todas las propiedades obligatorias para la instancia de TiffOptions a fin de producir los resultados deseados. Antes de pasar al código de ejemplo, aquí tienes la lista de los campos de TiffExpectedFormat y sus detalles para una mejor comprensión del uso.


- TiffExpectedFormat.Default: Configurar el campo a Default actúa de manera similar al constructor predeterminado de la clase TiffOptions con ninguna compresión y BitsPerPixel configurado en 1 para producir un resultado en blanco y negro. Se recomienda usar este campo cuando otras propiedades específicas del formato deben configurarse manualmente según los resultados deseados.
- TiffExpectedFormat.TiffCcitRle: Específico para la codificación RLE al guardar el resultado en formato TIFF a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffCcittFax3: Específico para la codificación CCITT Fax3 al guardar el resultado en formato TIFF a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffCcittFax4: Específico para la codificación CCITT Fax4 al guardar el resultado en formato TIFF a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffDeflateBW: Específico para la compresión Deflate al guardar el resultado en formato TIFF a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffDeflateRGB: Específico para la compresión Deflate al guardar el resultado en formato TIFF en RGB (color).
- TiffExpectedFormat.TiffJpegRGB: Específico para la compresión Jpeg al guardar el resultado en formato TIFF en RGB (color).
- TiffExpectedFormat.TiffJpegYCBCR: Específico para la compresión Jpeg al guardar el resultado en formato TIFF en YCBCR (color).
- TiffExpectedFormat.TiffLzwBW: Específico para la compresión LZW al guardar el resultado en formato TIFF a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffLzwRGB: Específico para la compresión LZW al guardar el resultado en formato TIFF en RGB (color).
- TiffExpectedFormat.TiffLzwRGBA: Específico para la compresión LZW al guardar el resultado en formato TIFF en RGBA (color con transparencia).
- TiffExpectedFormat.TiffNoCompressionBW: Específico para el formato TIFF sin compresión al guardar el resultado a 1 BitsPerPixel (blanco y negro).
- TiffExpectedFormat.TiffNoCompressionRGB: Específico para el formato TIFF sin compresión al guardar el resultado en RGB (color).
- TiffExpectedFormat.TiffNoCompressionRGBA: Específico para el formato TIFF sin compresión al guardar el resultado en RGBA (color con transparencia).



El siguiente fragmento de código detalla el uso de los campos de TiffExpectedFormat al crear una instancia de la clase TiffOptions.



## **Soporte para compresión Deflate y Adobe Deflate**
El formato de archivo TIFF (Tagged Image File Format) soporta varios tipos de compresión, siendo el tipo de compresión almacenado como una etiqueta (un valor entero) en el archivo. Uno de estos métodos de compresión es Adobe Deflate (anteriormente conocido como Deflate). La API de Aspose.PSD para .NET admite este método de compresión para la exportación y creación de imágenes TIFF.
### **Guardar imagen en TIFF con compresión Deflate**
Convertir las imágenes cargadas en TIFF con compresión Deflate/Adobe Deflate es fácil de seguir.


### **Crear TiffImage con compresión Adobe Deflate**
El siguiente ejemplo muestra el uso de la API de Aspose.PSD para .NET para crear una imagen desde cero utilizando el método de compresión Adobe Deflate.


### **Comprimir imágenes TIFF**
La API de Aspose.PSD para .NET se puede utilizar para convertir imágenes PSD a formato de imagen TIFF e incluso cambiar la compresión de la imagen TIFF resultante. La API también se puede usar para almacenar diferentes imágenes como marcos en una imagen TIFF con fines de archivo, comprimiendo las imágenes al tamaño de datos más bajo. La compresión de la imagen en cualquier caso debe realizarse reduciendo el tamaño de los datos fuente independientemente del algoritmo de compresión utilizado. Para lograr la mejor relación de compresión, podemos utilizar espacios de color indexados. El siguiente fragmento de código proporciona la mejor compresión utilizando solo 16 colores indexados y el algoritmo de compresión LZW, sin embargo, los colores fuente están ligeramente entrelazados.

