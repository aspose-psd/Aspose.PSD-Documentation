---
title: Convertir Imágenes
type: docs
weight: 20
url: /es/net/converting-images/
---

## **Convertir Imágenes a Blanco y Negro y en Escala de Grises**
A veces puede ser necesario convertir imágenes a color a blanco y negro o en escala de grises para fines de impresión o archivado. Este artículo demuestra el uso de Aspose.PSD para la API de .NET para lograr esto mediante dos métodos como se indica a continuación.

- Binariación
- Escala de grises
### **Binariación**
Para entender el concepto de Binariación, es importante definir una Imagen Binaria; es decir, una imagen digital que solo puede tener dos valores posibles para cada píxel. Normalmente, los dos colores utilizados para una imagen binaria son negro y blanco, aunque se pueden utilizar cualquier par de colores. La binariación es el proceso de convertir una imagen a bi-nivel, lo que significa que cada píxel se almacena como un solo bit (0 o 1), donde 0 denota la ausencia de color y 1 significa presencia de color. Aspose.PSD para la API de .NET actualmente admite dos métodos de binariación.
#### **Binariación con Umbral Fijo**
El siguiente fragmento de código le muestra cómo se puede aplicar la binariación con umbral fijo a una imagen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binariación con Umbral de Otsu**
El siguiente fragmento de código le muestra cómo se puede aplicar la binariación con umbral de Otsu a una imagen.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Escala de Grises**
La escala de grises es el proceso de convertir una imagen de tono continuo a una imagen con tonos de gris discontinuos. El siguiente fragmento de código le muestra cómo usar la Escala de Grises.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **Convertir Capas de Imagen GIF a Imagen TIFF**
A veces es necesario extraer y convertir capas de una imagen PSD a otro formato de imagen de trama para satisfacer una necesidad de la aplicación. Aspose.PSD API admite la función de extraer y convertir capas de una imagen PSD a otro formato de imagen de trama. En primer lugar, crearemos una instancia de imagen y cargaremos la imagen PSD desde el disco local, luego iteraremos cada capa en la propiedad de Capa. Luego convertiremos el bloque a la imagen TIFF. El siguiente fragmento de código le muestra cómo convertir las capas de imagen PSD a imágenes TIFF.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **Convertir PSD CMYK a TIFF CMYK**
Con Aspose.PSD para .NET, los desarrolladores pueden convertir un archivo PSD CMYK a formato tiff CMYK. Este artículo muestra cómo exportar/convertir un archivo PSD CMYK a formato tiff CMYK con Aspose.PSD. Usando Aspose.PSD para .NET, puede cargar imágenes PSD y luego puede configurar varias propiedades utilizando la clase [Opciones de Tiff](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) y guardar o exportar la imagen. El siguiente fragmento de código le muestra cómo lograr esta función.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **Exportar Imágenes**
Junto con un amplio conjunto de rutinas de procesamiento de imágenes, Aspose.PSD proporciona clases especializadas para convertir formatos de archivo PSD a otros formatos. Usando esta biblioteca, la conversión de imágenes PSD es muy simple e intuitiva. A continuación se muestran algunas clases especializadas para este propósito en el espacio de nombres [Opciones de Imagen](https://reference.aspose.com/psd/net/aspose.psd.imageoptions).

- [Opciones Bmp](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [Opciones Gif](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [Opciones Jpeg](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Opciones Jpeg2000](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [Opciones Tiff](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [Opciones Png](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Es fácil exportar imágenes PSD con Aspose.PSD para .NET API. Todo lo que necesita es un objeto de la clase apropiada de [Opciones de Imagen](https://reference.aspose.com/psd/net/aspose.psd.imageoptions). Mediante el uso de estas clases, puede exportar fácilmente cualquier imagen creada, editada o simplemente cargada con Aspose.PSD para .NET a cualquier formato admitido.
## **Combinar Imágenes**
Este ejemplo utiliza la clase Graphics y muestra cómo combinar dos o más imágenes en una sola imagen completa. Para demostrar la operación, el ejemplo crea una nueva PsdImage y dibuja imágenes en la superficie del lienzo utilizando el método Draw Image expuesto por la clase Graphics. Usando la clase Graphics, se pueden combinar dos o más imágenes de tal manera que la imagen resultante se vea como una imagen completa sin espacio entre las partes de la imagen y sin páginas. El tamaño del lienzo debe ser igual al tamaño de la imagen resultante. A continuación se muestra una demostración de código que muestra cómo usar el método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) de la clase [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) para combinar imágenes en una sola imagen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **Expandir y Recortar Imágenes**
La API de Aspose.PSD le permite expandir o recortar una imagen durante el proceso de conversión de imágenes. El desarrollador necesita crear un rectángulo con coordenadas X e Y y especificar el ancho y la altura de la caja rectangular. Las coordenadas X, Y y el ancho, la altura del rectángulo representarán la expansión o el recorte de la imagen cargada. Si es necesario expandir o recortar la imagen durante la conversión de imágenes, realice los siguientes pasos:

1. Cree una instancia de la clase [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) y cargue la imagen existente.
1. Cree una instancia de la clase ImageOption.
1. Cree una instancia de la clase [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) e inicialice las coordenadas X, Y y el ancho, la altura del rectángulo.
1. Llame al método [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) de la clase RasterImage mientras pasa el nombre del archivo de salida, las opciones de imagen y el objeto de rectángulo como parámetros.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **Leer y Escribir Datos XMP en Imágenes**
XMP (Plataforma de Metadatos Extensible) es un estándar ISO. XMP estandariza un modelo de datos, un formato de serialización y propiedades centrales para la definición y procesamiento de metadatos extensibles. También proporciona pautas para incrustar información XMP en una imagen popular como JPEG, sin afectar su legibilidad por aplicaciones que no admiten XMP. Con la API de Aspose.PSD para .NET, los desarrolladores pueden leer o escribir metadatos XMP en imágenes. Este artículo demuestra cómo se pueden leer metadatos XMP de una imagen y escribir metadatos XMP en imágenes.
### **Crear Metadatos XMP, Escribirlos y Leerlos Desde un Archivo**
Con la ayuda del espacio de nombres Xmp, el desarrollador puede crear un objeto de metadatos XMP y escribirlo en una imagen. El siguiente fragmento de código le muestra cómo usar los paquetes XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage y DublinCorePackage contenidos en el espacio de nombres [Xmp](https://reference.aspose.com/psd/net/aspose.psd.xmp).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.cs" >}}
## **Exportar Imágenes en un Entorno Multihilo**
Aspose.PSD para .NET ahora admite la conversión de imágenes en un entorno multihilo. Aspose.PSD para .NET garantiza el rendimiento optimizado de las operaciones durante la ejecución del código en un entorno multihilo. Todas las clases de [opciones de imagen](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) (por ejemplo, Opciones Bmp, Opciones Tiff, Opciones Jpeg, etc.) en Aspose.PSD para .NET implementan la interfaz IDisposable. Por lo tanto, es imprescindible que el desarrollador deseche adecuadamente el objeto de clase de opciones de imagen en caso de que se establezca la propiedad Origen. El siguiente fragmento de código demuestra dicha funcionalidad.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.cs" >}}


Aspose.PSD ahora admite la propiedad SyncRoot mientras se trabaja en un entorno multihilo. El desarrollador puede usar esta propiedad para sincronizar el acceso al flujo de origen. El siguiente fragmento de código demuestra cómo se puede utilizar la propiedad SyncRoot.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SyncRoot-SyncRoot.cs" >}}
