---
title: Convertir imágenes
type: docs
weight: 20
url: /es/java/convertir-imagenes/
---

## **Convertir imágenes a blanco y negro y escala de grises**
A veces puede ser necesario convertir imágenes a color a blanco y negro o escala de grises para imprimir o archivar. Este artículo demuestra el uso de Aspose.PSD para la API de Java para lograr esto mediante dos métodos como se indica a continuación.

- Binzarización
- Escala de grises
### **Binarización**
Para entender el concepto de binarización, es importante definir una imagen binaria; una imagen digital que solo puede tener dos valores posibles para cada píxel. Normalmente, los dos colores utilizados para una imagen binaria son negro y blanco, aunque se pueden usar cualquier par de colores. La binarización es el proceso de convertir una imagen en bi-nivel, lo que significa que cada píxel se almacena como un solo bit (0 o 1) donde 0 denota la ausencia de color y 1 significa la presencia de color. Aspose.PSD para Java API actualmente admite dos métodos de binarización.
#### **Binarización con umbral fijo**
El siguiente fragmento de código le muestra cómo se puede aplicar la binarización con umbral fijo a una imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}
#### **Binarización con umbral de Otsu**
El siguiente fragmento de código le muestra cómo se puede aplicar la binarización con umbral de Otsu a una imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}
### **Escala de grises**
La escala de grises es el proceso de convertir una imagen de tonos continuos a una imagen con tonos de grises discontinuos. El siguiente fragmento de código le muestra cómo utilizar la escala de grises.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}
## **Convertir capas de imagen GIF a imagen TIFF**
A veces es necesario extraer y convertir capas de una imagen PSD a otro formato de imagen de mapa de bits para satisfacer una necesidad de la aplicación. La API de Aspose.PSD admite la funcionalidad de extraer y convertir capas de una imagen PSD a otro formato de imagen de mapa de bits. En primer lugar, crearemos una instancia de imagen y cargaremos la imagen PSD desde el disco local, luego iteraremos cada capa en la propiedad de Layer. Luego convertiremos el bloque en una imagen TIFF. El siguiente fragmento de código le muestra cómo convertir las capas de imagen PSD en imágenes TIFF.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}
## **Convertir PSD CMYK a TIFF CMYK**
Usando Aspose.PSD para Java, los desarrolladores pueden convertir un archivo PSD CMYK a formato tiff CMYK. Este artículo muestra cómo exportar / convertir un archivo PSD CMYK a formato tiff CMYK con Aspose.PSD. Usando Aspose.PSD para Java, puede cargar imágenes PSD y luego puede establecer varias propiedades utilizando la clase TiffOptions y guardar o exportar la imagen. El siguiente fragmento de código le muestra cómo lograr esta funcionalidad.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}
## **Exportar imágenes**
Junto con un conjunto de rutinas de procesamiento de imágenes, Aspose.PSD proporciona clases especializadas para convertir formatos de archivo PSD a otros formatos. Utilizando esta biblioteca, la conversión de imágenes PSD es muy simple e intuitiva. A continuación se muestran algunas clases especializadas para este propósito en el espacio de nombres ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

Es fácil exportar imágenes PSD con la API de Aspose.PSD para Java. Todo lo que necesita es un objeto de la clase apropiada del espacio de nombres ImageOptions. Usando estas clases, puede exportar fácilmente cualquier imagen creada, editada o simplemente cargada con Aspose.PSD para Java a cualquier formato compatible.
## **Combina Imágenes**
Este ejemplo utiliza la clase Graphics y muestra cómo combinar dos o más imágenes en una sola imagen completa. Para demostrar la operación, el ejemplo crea una nueva PsdImage y dibuja imágenes en la superficie del lienzo utilizando el método Draw Image expuesto por la clase Graphics. Usando la clase Graphics, dos o más imágenes pueden combinarse de tal manera que la imagen resultante se verá como una imagen completa sin espacio entre las partes de la imagen y sin páginas. El tamaño del lienzo debe ser igual al tamaño de la imagen resultante. A continuación se muestra una demostración de código que muestra cómo usar el método Draw Image de la clase Graphics para combinar imágenes en una sola imagen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}
## **Expandir y recortar imágenes**
La API de Aspose.PSD le permite expandir o recortar una imagen durante el proceso de conversión de imagen. El desarrollador necesita crear un rectángulo con coordenadas X y Y y especificar el ancho y alto de la caja del rectángulo. Las coordenadas X, Y y Ancho, Altura del rectángulo representarán la expansión o recorte de la imagen cargada. Si es necesario expandir o recortar la imagen durante la conversión de imagen, realice los siguientes pasos:

1. Cree una instancia de la clase RasterImage y cargue la imagen existente.
1. Cree una instancia de la clase ImageOption.
1. Cree una instancia de la clase Rectangle e inicialice las coordenadas X, Y y el ancho, altura del rectángulo.
1. Llame al método Save de la clase RasterImage pasando el nombre de archivo de salida, las opciones de imagen y el objeto de rectángulo como parámetros.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}
## **Leer y Escribir Datos XMP en Imágenes**
XMP (Plataforma de Metadatos Extensible) es un estándar ISO. XMP estandariza un modelo de datos, un formato de serialización y propiedades básicas para la definición y procesamiento de metadatos extensibles. También proporciona pautas para incrustar información XMP en imágenes populares como JPEG, sin alterar su legibilidad por aplicaciones que no admiten XMP. Con la API de Aspose.PSD para Java, los desarrolladores pueden leer o escribir metadatos XMP en imágenes. Este artículo demuestra cómo se pueden leer los metadatos XMP de una imagen y escribir metadatos XMP en las imágenes.
### **Crear metadatos XMP, escribirlos y leer desde archivo**
Con la ayuda del espacio de nombres XMP, el desarrollador puede crear un objeto de metadatos XMP y escribirlo en una imagen. El siguiente fragmento de código le muestra cómo usar los paquetes XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage y DublinCorePackage contenidos en el espacio de nombres XMP.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}
## **Exportar imágenes en un entorno multiproceso**
Aspose.PSD para Java ahora admite la conversión de imágenes en un entorno multiproceso. Aspose.PSD para Java garantiza el rendimiento optimizado de las operaciones durante la ejecución de código en un entorno multiproceso. Todas las clases de opciones de imagen (por ej., BmpOptions, TiffOptions, JpegOptions, etc.) en Aspose.PSD para Java implementan la interfaz IDisposable. Por lo tanto, es imprescindible que el desarrollador deseche adecuadamente el objeto de la clase de opciones de imagen en caso de que se establezca la propiedad Source. El siguiente fragmento de código demuestra dicha funcionalidad.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ExportImagesinMultiThreadEnv-ExportImagesinMultiThreadEnv.java" >}}



Aspose.PSD ahora admite la propiedad SyncRoot mientras se trabaja en un entorno multiproceso. El desarrollador puede usar esta propiedad para sincronizar el acceso a la secuencia de origen. El siguiente fragmento de código demuestra cómo se puede usar la propiedad SyncRoot.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SyncRoot-SyncRoot.java" >}}
