---
title: Creación, Apertura y Guardado de Archivos PSD
type: docs
weight: 10
url: /es/creacion-apertura-y-guardado-de-archivos-psd/
---

## **Exportar Imagen a PSD**
PSD, documento de PhotoShop, es el formato de archivo predeterminado utilizado por Adobe PhotoShop para trabajar con imágenes. Aspose.PSD te permite cargar, editar y guardar archivos en PSD para que puedan ser abiertos y editados en PhotoShop. Este artículo muestra cómo guardar un archivo en PSD con Aspose.PSD, y también discute algunos de los ajustes que se pueden utilizar al guardar en este formato. PsdOptions es una clase especializada en el espacio de nombres ImageOptions utilizada para exportar imágenes a PSD. Para exportar a PSD, crea una instancia de la clase Image, ya sea cargada desde un archivo de imagen existente (por ejemplo, miniaturas) o creada desde cero. Este artículo explica cómo hacerlo. En los ejemplos a continuación, se crea una imagen desde cero. Una vez creada y poblados los datos de píxeles, guarda la imagen usando el método Save de la clase Image y suministra un objeto PsdOptions como segundo argumento. Se pueden establecer varias propiedades de la clase PsdOptions para una conversión avanzada. Algunas de las propiedades son Modo de Color, Método de Compresión y Versión. Aspose.PSD soporta los siguientes métodos de compresión a través de la enumeración CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Los siguientes modos de color son soportados a través de la enumeración ColorModes:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Se pueden agregar recursos adicionales, como recursos de miniatura para PSD v4.0, v5.0 y superiores, o recursos de cuadrícula y guía para PSD v4.0 y superiores. El código a continuación crea un archivo BMP desde cero, poblados los píxeles y lo guarda en PSD con compresión RLE y modo de color en escala de grises. El siguiente fragmento de código te muestra cómo exportar una imagen a PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importar imagen a capa PSD**
Este artículo demuestra el uso de Aspose.PSD para añadir o importar una imagen a una capa PSD. Las APIs de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto el método DrawImage de la clase Layer para añadir/importar una imagen a un archivo PSD. El método DrawImage necesita valores de ubicación e imagen para añadir/importar una imagen a un archivo PSD. Los pasos para importar una imagen a una capa PSD son tan simples como se muestra a continuación:

- Carga un archivo PSD como una imagen usando el método de fábrica Load expuesto por la clase Image.
- Crea una instancia de la clase Layer y asigna la capa de imagen PSD a ella.
- Carga la imagen que necesita ser añadida o crea una desde cero.
- Llama al método Layer.DrawImage especificando la ubicación y la instancia de imagen.
- Guarda los resultados.


El siguiente fragmento de código te muestra cómo importar una imagen a una capa PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Creación de Miniaturas desde Archivos PSD**
PSD es el formato de documento nativo de la aplicación Adobe Photoshop. Adobe Photoshop (versión 5.0 y posteriores) almacena información de miniatura para la visualización previa en un bloque de recursos de imagen que consta de un encabezado inicial de 28 bytes, seguido de una miniatura JPEG en orden RGB (rojo, verde, azul). La API de Aspose.PSD proporciona un mecanismo fácil de usar para acceder a los recursos del archivo PSD. Estos recursos también incluyen el recurso de miniatura que a su vez puede ser obtenido y guardado en disco según las necesidades de la aplicación. El siguiente fragmento de código te muestra cómo crear miniaturas desde archivos PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Creación de Archivos PSD Indexados**
Aspose.PSD para la API de Java puede crear archivos PSD indexados desde cero. Este artículo demuestra el uso de las clases PsdOptions y PsdImage para crear un PSD indexado mientras dibuja algunas formas sobre el lienzo recién creado. Los siguientes pasos simples son necesarios para crear un archivo PSD indexado.

- Crea una instancia de PsdOptions y establece su fuente.
- Establece la propiedad ColorMode de PsdOptions en ColorModes.Indexed.
- Crea una nueva paleta de colores a partir del espacio RGB y establécela como propiedad Palette de PsdOptions.
- Establece la propiedad CompressionMethod en el algoritmo de compresión requerido.
- Crea una nueva image PSD llamando al método PsdImage.Create.
- Dibuja gráficos u realiza otras operaciones según sea necesario.
- Llama al método PsdImage.Save para confirmar todos los cambios.



El siguiente fragmento de código te muestra cómo crear archivos PSD indexados.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Exportar Capa PSD a Imagen Rasterizada**
Aspose.PSD para Java te permite exportar capas en un archivo PSD a imágenes rasterizadas. Por favor utiliza el método Save de la clase Aspose.PSD.FileFormats.Psd.Layers.Layer para exportar la capa a imagen. El siguiente código de ejemplo carga un archivo PSD y exporta cada una de sus capas a una imagen PNG usando Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Una vez que todas las capas son exportadas a imágenes PNG, puedes abrirlas usando tu visor de imágenes favorito. El siguiente fragmento de código te muestra cómo exportar una capa PSD a una imagen rasterizada.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Ejemplos-src-main-java-com-aspose-psd-ejemplos-ModificaryConvertirImágenes-PSD-ExportarPSDCapaaImagenRasterizada-ExportarPSDCapaaImagenRasterizada.java" >}}
