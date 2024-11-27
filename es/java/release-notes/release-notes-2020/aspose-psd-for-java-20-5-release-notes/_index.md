---
title: Notas de la versión de Aspose.PSD para Java 20.5
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-20-5-notas-de-lanzamiento/
---

{{% alert color="primary" %}} Esta página contiene las notas de la versión de [Aspose.PSD para Java 20.5](https://downloads.aspose.com/psd/java/nuevos-lanzamientos/aspose.psd-para-java-20.5/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-188|Soporte para progreso de conversión de documentos|Funcionalidad|
|PSDJAVA-197|Soporte de imagen PSD de modo de color en escala de grises con 16 bits por canal ahorro|Funcionalidad|
|PSDJAVA-198|Soporte de Recurso Nvrt (Recurso de Capa de Ajuste de Inversión)|Funcionalidad|
|PSDJAVA-200|Soporte de Máscaras de Capa para Grupos de Capas|Funcionalidad|
|PSDJAVA-195|Corregir el guardado de imagen PSD con modo de color en escala de grises de 16 bits por canal al formato PSD de 16 bits por canal RGB|Error|
|PSDJAVA-196|Corregir el guardado de imagen PSD con modo de color en escala de grises de 16 bits por canal al formato PSD de escala de grises de 8 bits por canal|Error|
|PSDJAVA-199|El alineamiento de texto a través de ITextPortion no funciona para idiomas de derecha a izquierda. El archivo de salida está dañado.|Error|
|PSDJAVA-201|Excepción al intentar abrir un archivo Psd en particular con Color Lab y 8 bit/canal|Error|
# **Cambios en la API Pública**
# **APIs Agregadas:**
- Ninguna
## **APIs Eliminadas:**
- Ninguna
# **Ejemplos de uso:**

**PSDJAVA-188. Soporte para progreso de conversión de documentos**

{{< highlight java >}}

 // Un ejemplo de uso del controlador de progreso para operaciones de carga y guardado.

// El programa utiliza diferentes opciones de guardado para activar eventos de progreso.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Crear un controlador de progreso que escribe información de progreso en la consola

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s de %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Cargando Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Vincular el controlador de progreso para mostrar el progreso de carga

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Cargar PSD usando opciones de carga específicas

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Guardando Apple.psd en formato PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Hacer que la imagen de salida tenga color y no sea transparente

    pngOptions.setColorType(PngColorType.Truecolor);

    // Vincular el controlador de progreso para mostrar el progreso de guardado

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Convertir PSD a PNG con características específicas

    image.save(outputStream, pngOptions);

    System.out.println("---------- Guardando Apple.psd en formato PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Hacer que el PSD de salida sea en color

    psdOptions.setColorMode(ColorModes.Rgb);

    // Establecer un canal para cada color (rojo, verde y azul) más un canal compuesto

    psdOptions.setChannelsCount((short)4);

    // Vincular el controlador de progreso para mostrar el progreso de guardado

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Guardar una copia de PSD con características específicas

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Soporte de imagen PSD con modo de color en escala de grises con 16 bits por canal**

{{< highlight java >}}

 // Un ejemplo de aplicación de diferentes combinaciones de modos de color, bits por canal, conteo de canales

// y compresiones para capas específicas.

// Hacer que un método sea accesible desde el ámbito local

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Cargar un PSD en escala de grises de 16 bits predefinido

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Dibujar un borde interior gris alrededor del perímetro de la capa

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Guardar una copia de PSD con características específicas

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Cargar el PSD guardado

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Convertir el PSD guardado en una imagen PNG en escala de grises

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // aquí no debería haber excepción

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_sin_capas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_sin_capas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_sin_capas", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Soporte del Recurso Nvrt (Recurso de Capa de Ajuste de Inversión)**

{{< highlight java >}}

 // Un ejemplo de cómo encontrar el Recurso Nvrt de una capa de ajuste de inversión.

String inPsdFilePath = "CapaDeAjusteDeInversion.psd";

NvrtResource nvrtResource = null;

// Cargar un PSD predefinido que contiene una capa de ajuste de inversión

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Intentar encontrar un recurso de la capa de ajuste de inversión

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Se encontró el Recurso Nvrt

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Soporte de Máscaras de Capa para Grupos de Capas**

{{< highlight java >}}

 // Un ejemplo de soporte de máscaras de capa para grupos de capas. El programa carga y guarda PSD

// a diferentes formatos de salida sin lanzar excepciones.

String srcFile = "psdnet595.psd";

String outputPng = "salida.png";

String outputPsd = "salida.psd";

// Cargar un PSD predefinido que contiene máscaras de capa para grupos de capas

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Convertir el PSD cargado a PNG

    input.save(outputPng, new PngOptions());

    // Guardar una copia del PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Corregir el guardado de imagen PSD con modo de color en escala de grises de 16 bits por canal al formato PSD de 16 bits por canal RGB**

{{< highlight java >}}

 // Un ejemplo de convertir un PSD en escala de grises de 16 bits en uno RGB de 16 bits y luego de regreso a

// imagen en escala de grises de 16 bits pero con una imagen ráster.

String sourceFilePath = "escalaDeGrises5x5.psd";

String exportFilePath = "salida_rgb16bits5x5.psd";

String pngExportPath = "salida_rgb16bits5x5.png";

// Cargar un PSD en escala de grises de 16 bits predefinido

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Dibujar un borde interior gris alrededor del perímetro de la capa

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Guardar una copia de PSD con el modo de color cambiado a RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Cargar el PSD guardado

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Convertir el PSD guardado en una imagen PNG en escala de grises

    image1.save(pngExportPath, pngOptions); // aquí no debería haber excepción

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Corregir el guardado de imagen PSD con modo de color en escala de grises de 16 bits por canal al formato PSD de escala de grises de 8 bits por canal**

{{< highlight java >}}

 // Un ejemplo de convertir un PSD en escala de grises de 16 bits en uno de escala de grises de 8 bits y luego a

// una imagen de ráster de escala de grises de 8 bits.

String sourceFilePath = "escalaDeGrises16bit.psd";

String exportFilePath = "salida_escalaDeGrises16bit.psd";

String pngExportPath = "salida_escalaDeGrises16bit.png";

// Cargar un PSD en escala de grises de 16 bits predefinido

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Dibujar un borde interior gris alrededor del perímetro de la capa

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Guardar una copia de PSD con el recuento de canales cambiado a 8 bits

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Cargar el PSD guardado

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Convertir el PSD guardado en una imagen PNG en escala de grises

    image1.save(pngExportPath, pngOptions); // aquí no debería haber excepción

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. El alineamiento de texto a través de ITextPortion no funciona para idiomas de derecha a izquierda. El archivo de salida está dañado.**

{{< highlight java >}}

 // Un ejemplo de alinear una capa de texto RTL a través de ITextPortion. El programa modifica

// una capa de texto RTL existente en un PSD cargado y guarda una copia del documento modificado.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiSalida.psd";

// Cargar un PSD predefinido que contiene una capa de texto RTL

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Obtener porciones de texto de la capa

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Cambiar el alineamiento del texto

    portions[0].getParagraph().setJustification(2);

    // Aplicar cambios a la capa

    layer.getTextData().updateLayerData();

    // Guardar una copia modificada del PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Excepción al intentar abrir un archivo Psd en particular con Color Lab y 8 bit/canal**

{{< highlight java >}}

 // Un ejemplo de soporte de un documento de Photoshop de 8 bits en el modo de color LAB.

String srcFile = "SinTítulo-1.psd";

String outputFilePsd = "salida.psd";

// Cargar un PSD de 8 bits predefinido en el modo de color LAB

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // Guardar una copia del PSD cargado

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}