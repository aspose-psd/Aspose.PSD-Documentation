---
title: Manipular formatos de Adobe Photoshop
type: docs
weight: 20
url: /es/net/manipulando-formatos-de-adobe-photoshop/
---

## **Combinar capas PSD en otras capas**

## **Exportar imagen a PSD**
PSD, documento de Photoshop, es el formato de archivo predeterminado utilizado por Adobe Photoshop para trabajar con imágenes. Aspose.PSD le permite cargar, editar y guardar archivos en PSD para que puedan abrirse y editarse en Photoshop. Este artículo muestra cómo guardar un archivo en PSD con Aspose.PSD, y también discute algunas de las configuraciones que se pueden usar al guardar en este formato. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) es una clase especializada en el espacio de nombres de [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) utilizada para exportar imágenes a PSD. Para exportar a PSD, cree una instancia de la clase Image, ya sea cargada desde un archivo de imagen existente (por ejemplo, miniaturas) o creada desde cero. Este artículo explica cómo hacerlo. En los ejemplos a continuación, se crea una imagen desde cero. Una vez creada y poblados los datos de píxeles, guarde la imagen utilizando el método Save de la clase Image y suministre un objeto PsdOptions como segundo argumento. Varias propiedades de la clase PsdOptions se pueden configurar para una conversión avanzada. Algunas de las propiedades son ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) y Version. Aspose.PSD admite los siguientes métodos de compresión a través de la enumeración CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Los siguientes modos de color son compatibles a través de la enumeración [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

Se pueden agregar recursos adicionales, como recursos de miniaturas para PSD v4.0, v5.0 y superiores, o recursos de cuadrícula y guía para PSD v4.0 y superiores. El código a continuación crea un archivo de imagen desde cero, popula los píxeles y lo guarda en PSD con compresión RLE y modo de color en escala de grises. El siguiente fragmento de código le muestra cómo exportar una imagen a PSD.

## **Importar imagen a capa PSD**
Este artículo demuestra el uso de Aspose.PSD para agregar o importar una imagen a una capa PSD. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto el método [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) de la clase Layer para agregar/importar una imagen en un archivo PSD. El método DrawImage necesita valores de ubicación e imagen para agregar/importar una imagen en un archivo PSD. Los pasos para importar una imagen en una capa PSD son tan simples como los siguientes:

- Cargue un archivo PSD como una imagen utilizando el método de fábrica Load expuesto por la clase Image.
- Cree una instancia de la clase Layer a partir del stream con archivos Png, Jpeg, Tiff, Gif, Bmp, Psd o j2k.
- Agregue la capa a Psd utilizando el método AddLayer
- Guarde los resultados.

El siguiente fragmento de código le muestra cómo importar la imagen a la capa PSD.

## **Reemplazo de color en capas PSD**
Este artículo demuestra el uso de Aspose.PSD para agregar o importar una imagen a una capa PSD. Las API de Aspose.PSD han expuesto métodos eficientes y fáciles de usar para lograr este objetivo. Aspose.PSD ha expuesto el método DrawImage de la clase Layer para agregar/importar una imagen en un archivo PSD. DrawImage necesita valores de ubicación e imagen para agregar/importar una imagen en un archivo PSD. Los pasos para importar una imagen a una capa PSD son tan simples como los siguientes:

- Cargue un archivo PSD como una imagen utilizando el método de fábrica Load expuesto por la clase Image.
- Cree una instancia de la clase Layer y asigne la capa de la imagen PSD a ella.
- Cargue la imagen que necesita ser agregada o cree una desde cero.
- Llame al método Layer.DrawImage especificando la ubicación y la instancia de la imagen.
- Guarde los resultados.

El siguiente fragmento de código le muestra cómo importar una imagen a una capa PSD.

## **Creación de miniaturas a partir de archivos PSD**
PSD es el formato de documento nativo de la aplicación Adobe Photoshop. Adobe Photoshop (versión 5.0 y posterior) almacena información de miniaturas para visualización previa en un bloque de recursos de imagen que consta de un encabezado inicial de 28 bytes, seguido de una miniatura JFIF en orden RGB (rojo, verde, azul). La API de Aspose.PSD proporciona un mecanismo fácil de usar para acceder a los recursos del archivo PSD. Estos recursos también incluyen el recurso de miniatura que a su vez puede ser recuperado y guardado en disco según las necesidades de la aplicación. El siguiente fragmento de código le muestra cómo crear miniaturas a partir de archivos PSD.

## **Creación de archivos PSD indexados**
Aspose.PSD para .NET API puede crear archivos PSD indexados desde cero. Este artículo muestra cómo utilizar las clases PsdOptions y [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) para crear un PSD indexado mientras se dibujan algunas formas sobre el lienzo recién creado. Los siguientes simples pasos son necesarios para crear un archivo PSD indexado.

- Cree una instancia de PsdOptions y configure su origen.
- Establezca la propiedad ColorMode de PsdOptions en ColorModes.Indexed.
- Cree una nueva paleta de colores del espacio RGB y establézcala como propiedad Palette de PsdOptions.
- Establezca la propiedad CompressionMethod en el algoritmo de compresión requerido.
- Cree una nueva imagen PSD llamando al método PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Dibuje gráficos u realice otras operaciones según sea necesario.
- Llame al método PsdImage.Save para comprometer todos los cambios.

El siguiente fragmento de código le muestra cómo crear archivos PSD indexados.

## **Exportar capa PSD a imagen de mapa de bits**
Aspose.PSD para .NET le permite exportar capas en un archivo PSD a imágenes de mapa de bits. Utilice el método [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) para exportar la capa a la imagen. El siguiente código de ejemplo carga un archivo PSD y exporta cada una de sus capas a una imagen PNG utilizando Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Una vez que todas las capas se exporten a imágenes PNG, puede abrirlas con su visor de imágenes favorito. El siguiente fragmento de código le muestra cómo exportar una capa PSD a una imagen de mapa de bits.

## **Actualizar capa de texto en archivo PSD**
Aspose.PSD para .NET le permite manipular el texto en la capa de texto de un archivo PSD. Utilice la clase [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) para actualizar el texto en la capa PSD. El siguiente fragmento de código carga un archivo PSD, accede a la capa de texto, actualiza el texto y guarda el archivo PSD con un nuevo nombre utilizando el método [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index).

## **Detectar archivo PSD aplanado**
Aspose.PSD para .NET le permite detectar si un archivo PSD dado está aplanado o no. La propiedad IsFlatten se ha introducido en la clase Aspose.PSD.FileFormats.Psd.PsdImage para lograr esta funcionalidad. El siguiente fragmento de código carga un archivo PSD y accede a la propiedad [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten).

## **Combinar capas PSD**
Este artículo muestra cómo combinar capas en un archivo PSD al convertir un archivo PSD a JPG con Aspose.PSD. En el ejemplo a continuación, se carga un archivo PSD existente pasando la ruta del archivo al método estático Load de la clase Image. Una vez cargado, convierta/transforme la imagen a PsdImage. Cree una instancia de la clase JpegOptions y configure varias propiedades. Ahora llame al método Save de la instancia PsdImage. El siguiente fragmento de código le muestra cómo combinar capas PSD.

## **Compatibilidad en escala de grises con alfa para PSD**
Este artículo muestra cómo admitir una escala de grises con alfa para un archivo PSD al convertir un archivo PSD a PNG con Aspose.PSD. En el ejemplo a continuación, se carga un archivo PSD existente pasando la ruta del archivo al método estático Load de la clase Image. Una vez cargado, convierta/transforme la imagen a PsdImage. Cree una instancia de la clase PngOptions y configure sus varias propiedades. Configure la propiedad [ColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) en TruecolorWithAlpha. Ahora llame al método Save de la instancia PngOptions. El siguiente fragmento de código le muestra cómo convertir a PNG en escala de grises con alfa.