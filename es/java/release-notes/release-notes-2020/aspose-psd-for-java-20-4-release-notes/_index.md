---
title: Aspose.PSD para Java 20.4 - Notas de la versión
type: docs
weight: 30
url: /es/java/aspose-psd-para-java-20-4-notas-de-la-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión para [Aspose.PSD para Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-156|Soporte del recurso 'Vector Origination Data'|Característica|
|PSDJAVA-171|Soporte de lclrResource (Configuración de color de capa)|Característica|
|PSDJAVA-157|Soporte de propiedades de datos de LengthRecord. (Operaciones de trayecto (operaciones booleanas), índice de la forma en la capa, conteo de registros de nodos de bezier)|Característica|
|PSDJAVA-158|Soporte del color de fondo del recurso de Sección de Imagen #1010|Característica|
|PSDJAVA-161|Adición de capas de relleno en tiempo de ejecución|Característica|
|PSDJAVA-168|Soporte de la información de borde del recurso de Sección de Imagen #1009|Característica|
|PSDJAVA-169|Soporte de capas en archivos de formato AI|Característica|
|PSDJAVA-163|Soporte de Lectura y Edición del Efecto de capa de superposición de degradado|Característica|
|PSDJAVA-164|Renderizado del Efecto de capa de superposición de degradado|Característica|
|PSDJAVA-149|Error de Aspose.PSD para java al obtener la propiedad textData.items de la capa de texto|Error|
|PSDJAVA-166|Corregir el guardado de imagen PSD con ColorMode en escala de grises y 16 bits por canal a formato PSD en escala de grises|Error|
|PSDJAVA-167|Corregir el guardado de imagen PSD con ColorMode en escala de grises y 16 bits por canal a formato PNG|Error|
|PSDJAVA-159|Los cambios en la propiedad GradientOverlayEffect.BlendMode no se muestran en Photoshop|Error|
## Cambios en la API pública
## API añadidas:
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(flotante)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(flotante,flotante)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(corto,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(largo)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(largo)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## APIs eliminadas:
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# Ejemplos de uso:

**PSDJAVA-156. Soporte del recurso 'Vector Origination Data'**

{{< highlight java >}}

 /*

Un ejemplo de lectura y modificación de un recurso de 'Vector Origination Data'.

*/

// Mantener los métodos en el ámbito local para mayor simplicidad

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("VogkResource no encontrado.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Cargar un archivo PSD que contiene un recurso VOGK predefinido

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Encontrar el primer VogkResource en los recursos de la capa predefinida

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Verificar las propiedades del recurso predefinido

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource no se leyó correctamente.");

    }

    // Modificar algunas propiedades del recurso Vogk

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Guardar una copia modificada del archivo PSD cargado en la ruta

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Soporte de lclrResource (Ajuste de color de capa)**

{{< highlight java >}}

 /*

Un ejemplo de uso del Color de Capa para resaltar visualmente las capas. Por ejemplo, puede

actualizar algunas capas en PSD y luego resaltar por color la capa a la que desea atraer

la atención.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // El recurso lcrl siempre está presente en la lista de recursos de archivo psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("El Color de Capa se leyó incorrectamente");

                }

                // Inversión de colores de la hoja de estilo. Configurar el resaltado de color de la capa.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// En el archivo los colores de las capas resaltadas están en este orden

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Red,

        SheetColorHighlightEnum.Orange,

        SheetColorHighlightEnum.Yellow,

        SheetColorHighlightEnum.Green,

        SheetColorHighlightEnum.Blue,

        SheetColorHighlightEnum.Violet,

        SheetColorHighlightEnum.Gray,

        SheetColorHighlightEnum.NoColor

};

// Cargar un archivo PSD que contiene un recurso Lclr predefinido

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Cargar un archivo PSD recién guardado

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Invertir colores

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Soporte de propiedades de datos de LengthRecord. (Operaciones de trayecto (operaciones booleanas), índice de la forma en la capa, conteo de registros de nodos de bezier)**

{{< highlight java >}}

 /*

Un ejemplo de cambiar las operaciones del trayecto al trabajar con formas. El programa lee

registros de trayecto de vector predefinidos (LengthRecord) y cambia sus operaciones de trayecto, luego guarda

una copia modificada del documento como un nuevo archivo PSD.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Cargar un archivo PSD que contiene un recurso vsms predefinido

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Encontrar el primer recurso VsmsResource en los recursos de la capa predefinida

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Cambiar la forma en que se combinan las formas

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Guardar una copia modificada del archivo PSD cargado en la ruta

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Soporte del color de fondo del recurso de Sección de Imagen #1010**

{{< highlight java >}}

 /*

Un ejemplo de lectura y modificación de un recurso de color de fondo.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Cargar un archivo PSD que contiene un recurso de color de fondo predefinido

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Recurso de Color de Fondo no encontrado");

    }

    // Actualizar el color del recurso de color de fondo

    backgroundColorResource.setColor(Color.getDarkRed());

    // Guardar una copia modificada del archivo PSD cargado en la ruta

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-161. Adición de capas de relleno en tiempo de ejecución**

{{< highlight java >}}

 /*

Un ejemplo de adición de capas de relleno de diferentes tipos a un documento de Photoshop.

*/

String outPsdFilePath = "output.psd";

// Crear un documento de Photoshop con un lienzo vacío

PsdImage psdImage = new PsdImage(100, 100);

try

{

    // Agregar capas de relleno de diferentes tipos a PSD

    FillLayer colorFillLayer = FillLayer.createInstance(FillType.Color);

    colorFillLayer.setDisplayName("Capa de Relleno de Color");

    psdImage.addLayer(colorFillLayer);

    FillLayer gradientFillLayer = FillLayer.createInstance(FillType.Gradient);

    gradientFillLayer.setDisplayName("Capa de Relleno de Degradado");

    psdImage.addLayer(gradientFillLayer);

    FillLayer patternFillLayer = FillLayer.createInstance(FillType.Pattern);

    patternFillLayer.setDisplayName("Capa de Relleno de Patrón");

    patternFillLayer.setOpacity((byte)50);

    psdImage.addLayer(patternFillLayer);

    // Guardar una copia modificada del archivo PSD cargado en la ruta

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-168. Soporte del recurso de Sección de Imagen #1009 Información de borde**

{{< highlight java >}}

 /*

Un ejemplo de lectura, modificación y guardado de un archivo PSD que contiene un recurso de información de borde.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Cargar un archivo PSD que contiene un recurso de imagen predefinido

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    ResourceBlock[] imageResources = psdImage.getImageResources();

    // Encontrar el primer recurso de información de borde en los recursos de imagen

    BorderInformationResource borderInfoResource = null;

    for (ResourceBlock imageResource : imageResources)

    {

        if (imageResource instanceof BorderInformationResource)

        {

            borderInfoResource = (BorderInformationResource)imageResource;

            break;

        }

    }

    // Actualizar algunas propiedades del recurso de información de borde

    borderInfoResource.setWidth(0.1);

    borderInfoResource.setUnit(Physical