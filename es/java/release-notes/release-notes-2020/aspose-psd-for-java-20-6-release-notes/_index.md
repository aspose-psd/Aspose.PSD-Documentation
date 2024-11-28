---
title: Notas de la Versión de Aspose.PSD para Java 20.6
type: docs
weight: 50
url: /es/java/aspose-psd-para-java-20-6-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-216|Soporte de LnkEResource (Recurso de Capa de Objeto Inteligente)|Característica|
|PSDJAVA-219|Soporte de britResource (Recurso de Capa de Ajuste de Brillo/Contraste)|Característica|
|PSDJAVA-222|Mover la configuración DefaultReplacementFont a la clase ImageOptionsBase|Mejora|
|PSDJAVA-217|El redimensionamiento de archivos PSD no funciona correctamente si hay una máscara en la capa de ajuste con límites vacíos|Error|
|PSDJAVA-218|La imagen PSD en modo RGB de 16 bits/ canal solo actualiza las capas en vista previa|Error|
|PSDJAVA-220|Los cambios en la máscara de capa PSD se descartan al guardar|Error|
|PSDJAVA-221|Orden incorrecto de la capa después de agregar un Grupo de Capas vacío|Error|
|PSDJAVA-223|Excepción al cargar un archivo PSD específico con el recurso LnkE compuesto y la propiedad adobeStockLicenseState|Error|
|PSDJAVA-224|La conversión de un archivo AI a formato Jpeg2000 no funciona|Error|
|PSDJAVA-225|El Grupo de Capas con un modo de mezcla que no es de "Pasar a través" no se renderiza|Error|
|PSDJAVA-226|Excepción de referencia nula al intentar convertir un archivo PSD específico en una imagen|Error|
|PSDJAVA-227|Excepción de desbordamiento al intentar abrir un archivo PSD específico|Error|

# **Cambios en la API Pública:**
# **APIs Añadidas:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **APIs Eliminadas:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Ejemplos de Uso:**

**PSDJAVA-216: Soporte de LnkEResource (Recurso de Capa de Objeto Inteligente)**

{{< highlight java >}}

 // Un ejemplo de enlazar diferentes tipos de activos (imágenes rasterizadas, bibliotecas de CC) a PSD.

// También se considera la API de LnkeResource.

// Una clase que mantiene métodos en el ámbito local

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("El ejemplo de soporte de LnkEResource funciona incorrectamente.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Este ejemplo demuestra cómo obtener y establecer propiedades del Psd LnkE

    // Resource que contiene información sobre un archivo externo vinculado.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Carga un PSD predefinido

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Buscar LnkeResource entre los recursos de capa global

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Verificar propiedades de LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.LIFE);

                    // Actualizar propiedades de LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Asegurarse de que LnkeResource sea compatible

            assertIsTrue(lnkeResource != null);

            // Guardar una copia del PSD cargado

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Cargar la copia guardada

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Convertir PSD a formato de archivo PNG (con canal alfa para transparencia)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Este ejemplo muestra cómo obtener y establecer propiedades del Recurso LnkE de forma programática.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Este ejemplo muestra cómo obtener y establecer propiedades del Recurso LnkE de forma programática.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Este ejemplo muestra cómo obtener y establecer propiedades del Recurso LnkE de forma programática.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (La característica está disponible en Photoshop CC 2015)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: Soporte de britResource (Recurso de Capa de Ajuste de Brillo/Contraste)**

{{< highlight java >}}

 // Este ejemplo muestra cómo puede cambiar programáticamente la Capa de Brillo/Contraste de la Imagen PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_salida.psd";

// Carga un documento de Photoshop que contiene una capa de ajuste de Brillo/Contraste

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Buscar britResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Verificar propiedades de recurso

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource fue leído incorrectamente");

                    }

                    // Actualizar propiedades de recurso

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Guardar una copia del PSD actualizado

                    psdImage.save(dstPath, new PsdOptions());

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

**PSDJAVA-217: El redimensionamiento de archivos PSD no funciona correctamente si hay una máscara en la capa de ajuste con límites vacíos**

{{< highlight java >}}

 // Un ejemplo de redimensionar una imagen que contiene una máscara de capa decapa de ajuste con límites vacíos. El programa carga un PSD predefinido solo para verificar que no haya excepciones.

final int escala = 2; // coeficiente arbitrario

String[] nombres = {

        "UnaRegularYUnaAjusteConVectorYmáscaraDeCapa",

        "CapaDeNivelesConMáscaraDeCapadeRGB",

        "CapaDeNivelesConMáscaraDeCapadeCMYK",

};

for (String nombre : nombres)

{

    String rutaArchivoFuente = nombre + ".psd";

    String rutaArchivoDestino = "salida_" + rutaArchivoFuente;

    String rutaPngDestino = "salida_" + nombre + ".png";

    // Cargar un PSD predefinido que contiene una máscara de capa de ajuste con límites vacíos

    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();

    opcionesCargaPsd.setLoadEffectsResource(true);

    PsdImage imagen = (PsdImage)Image.load(rutaArchivoFuente, opcionesCargaPsd);

    try

    {

        // Redimensionar la imagen

        imagen.resize(imagen.getWidth() * escala, imagen.getHeight() * escala);

        // Guardar una copia del PSD cargado

        imagen.save(rutaArchivoDestino, new PsdOptions());

        // Exportar PSD a formato de archivo PNG (con canal alfa para transparencia)

        PngOptions opcionesPng = new PngOptions();

        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

        imagen.save(rutaPngDestino, opcionesPng);

    }

    finally

    {

        imagen.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: La imagen PSD en modo RGB de 16 bits/canal solo actualiza las capas en vista previa**

{{< highlight java >}}

 // Un ejemplo de actualización de capas regulares para una imagen RGB de 16 bits. El programa dibuja algo

// en cada capa solo para asegurarse de que se actualice correctamente la capa completa.

String rutaArchivoFuente = "in.psd";

String rutaArchivoSalida = "salida.psd";

// Cargar un PSD predefinido en modo RGB de 16 bits

PsdImage imagen = (PsdImage)Image.load(rutaArchivoFuente);

try

{

    for (Layer capa : imagen.getLayers())

    {

        // Dibujar el nombre de la capa y un borde interno para la capa regular

        if (!(capa instanceof LayerGroup) && !(capa instanceof AdjustmentLayer) &&

                (capa.getWidth() > 100) && (capa.getHeight() > 100))

        {

            Graphics graficos = new Graphics(capa);

            graficos.drawString(capa.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graficos.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Guardar una copia del PSD cargado

    imagen.save(rutaArchivoSalida, new PsdOptions(imagen));

}

finally

{

    imagen.dispose();

}

{{< /highlight >}}

**PSDJAVA-220: Los cambios en la máscara de capa PSD se descartan al guardar**

{{< highlight java >}}

 // Una clase que mantiene métodos en el ámbito local

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("El ejemplo funciona incorrectamente.");

        }

    }

    // Obtiene el valor int convertido a bytes en orden big-endian.

    byte[] getBigEndianBytesInt32(int valor)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((valor >> 24) & 0x000000FF);

        bytes[1] = (byte)((valor >> 16) & 0x000000FF);

        bytes[2] = (byte)((valor >> 8) & 0x000000FF);

        bytes[3] = (byte)valor;

        return bytes;

    }

    // Obtiene el valor convertido de big-endian a Int32.

    int fromBigEndianToInt32(byte[] bytes, int indice)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (indice < 0 || indice + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("indice", "El índice está fuera del array de bytes.");

        }

        return ((bytes[indice] & 0xff) << 24) | ((bytes[indice + 1] & 0xff) << 16) |

                ((bytes[indice + 2] & 0xff) << 8) | (bytes[indice + 3] & 0xff);

    }

    // Obtiene una máscara de capa de ráster de la capa de una imagen de PSD y la guarda en un archivo

    void saveRasterMask(String rutaMascara, Layer capa)

    {

        LayerMaskDataShort datosMascara = (LayerMaskDataShort)capa.getLayerMaskData();

        FileStreamContainer contenedor = FileStreamContainer.createFileStream(rutaMascara, false);

        try

        {

            contenedor.write(getBigEndianBytesInt32(datosMascara.getTop()));

            contenedor.write(getBigEndianBytesInt32(datosMascara.getLeft()));

            contenedor.write(getBigEndianBytesInt32(datosMascara.getBottom()));

            contenedor.write(getBigEndianBytesInt32(datosMascara.getRight()));

            contenedor.writeByte(datosMascara.getDefaultColor());

            contenedor.writeByte((byte)datosMascara.getFlags());

            contenedor.write(getBigEndianBytesInt32(datosMascara.getImageData().length));

            contenedor.write(datosMascara.getImageData(), 0, datosMascara.getImageData().length);

        }

        finally

        {

            contenedor.dispose();

        }

    }

    // Añade una máscara de ráster del archivo a la capa y guarda la imagen en formato PSD

    void addRasterMask(Layer capa, String rutaOrigenMascara)

    {

        LayerMaskDataShort datosMascara = new LayerMaskDataShort();

        FileStreamContainer contenedor = FileStreamContainer.openFileStream(rutaOrigenMascara);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(contenedor.read(bytes), 22);

            datosMascara.setTop(fromBigEndianToInt32(bytes, 0));

            datosMascara.setLeft(fromBigEndianToInt32(bytes, 4));

            datosMascara.setBottom(fromBigEndianToInt32(bytes, 8));

            datosMascara.setRight(fromBigEndianToInt32(bytes, 12));

            datosMascara.setDefaultColor(bytes[16]);

            datosMascara.setFlags(bytes[17]);

            int longitudDatosImagen = fromBigEndianToInt32(bytes, 18);

            byte[] datos = new byte[longitudDatosImagen];

            assertAreEqual(datosMascara.getMaskRectangle().getWidth() *

                    datosMascara.getMaskRectangle().getHeight(), longitudDatosImagen);

            assertAreEqual(contenedor.read(datos), longitudDatosImagen);

            datosMascara.setImageData(datos);

        }

        finally

        {

            contenedor.dispose();

        }

        // Solo agregar LayerMaskData no es suficiente para guardar correctamente porque los canales no se actualizan;

        // layer.setLayerMaskData(mask); // Esto no agrega el canal de máscara

        // Agregar (o actualizar) la máscara

        capa.addLayerMask(datosMascara); // ¡Pero esto agrega/actualiza tanto la máscara como los canales!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Este ejemplo muestra cómo obtener, actualizar, quitar y añadir máscaras de capa de ráster en el archivo de Adobe® Photoshop® de forma programática.

PngOptions opcionesPng = new PngOptions();

opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

String rutaArchivoFuente = "FourWithMasks.psd";

PsdImage imagen = (PsdImage)Image.load(rutaArchivoFuente);

try

{

    Layer capa = imagen.getLayers()[2];

    // Obtener una máscara de ráster de la capa y guardarla en un archivo

    $.saveRasterMask("FourWithMasks2.msk", capa);

    // Cambiar la máscara de la capa (invertir) y guardar la imagen

    LayerMaskData mascara = capa.getLayerMaskData();

    byte[] datosMascara = mascara.getImageData();

    for (int i = 0; i < datosMascara.length; i++)

    {

        datosMascara[i] = (byte)~datosMascara[i];

    }

    // Solo cambiar LayerMaskData es suficiente para efecto de renderizado

    imagen.save("FourWithMasksUpdated2.png", opcionesPng);

    // Pero solo cambiar LayerMaskData no es suficiente para guardar correctamente porque los canales no se actualizan;

    capa.setLayerMaskData(mascara); // Esto tampoco funciona

    capa.addLayerMask(mascara); // ¡Pero esto actualiza tanto la máscaras como los canales!

    imagen.save("FourWithMasksUpdated2.psd");

    // Quitar una máscara de ráster de la capa y guardar la imagen

    capa.setLayerMaskData(null); // Solo quitar LayerMaskData es suficiente para efecto de renderizado pero no para guardar en el formato PSD

    imagen.save("FourWithMasksRemoved2.png", opcionesPng);

    capa.addLayerMask(null); // ¡Pero esto elimina tanto la máscara como el canal de máscara!

    imagen.save("FourWithMasksRemoved2.psd");

    // Añadir una máscara de ráster del archivo a la capa y guardar la imagen

    $.addRasterMask(capa, "raster.msk");

    imagen.save("FourWithMasksAdded2.png", opcionesPng);

    imagen.save("FourWithMasksAdded2.psd");

}

finally

{

    imagen.dispose();

}

{{< /highlight >}}

**PSDJAVA-221: Orden incorrecto de la capa después de agregar un Grupo de Capas vacío**

{{< highlight java >}}

 // Este ejemplo demuestra cómo agregar un grupo de capas anidadas a PSD de forma programática.

String rutaPsdDst = "salida.psd";

// Crear una imagen con un tamaño de 1x1 píxeles para trabajar

PsdImage psdImagen = new PsdImage(1, 1);

try

{

    // Agregar un grupo de capas principal ("true" significa abrir el grupo de capas al inicio)

    LayerGroup grupo1 = psdImagen.addLayerGroup("Grupo 1", 0, true);

    // Agregar un grupo de capas anidadas

    LayerGroup grupo2 = grupo1.addLayerGroup("Grupo 2", 0);

    if (grupo1.getLayers().length != 2)

    {

        throw new RuntimeException("El Grupo 1 debe contener dos capas del Grupo 2.");

    }

    // Verificar que no haya excepciones al guardar los grupos de capas creados

    psdImagen.save(rutaPsdDst);

}

finally

{

    psdImagen.dispose();

}

{{< /highlight >}}

**PSDJAVA-223: Excepción al cargar un archivo PSD específico con el recurso LnkE compuesto y la propiedad adobeStockLicenseState**

{{< highlight java >}}

 // Este ejemplo demuestra cómo leer y modificar el recurso de vínculo externo de Adobe® Photoshop®

// (LnkeResource) con múltiples fuentes de datos (imágenes, bibliotecas de CC) de forma programática.

// Una clase que mantiene métodos en el ámbito local

class LocalScopeExtension

{

    void assertIsTrue(boolean condición)

    {

        if (!condición)

        {

            throw new FormatException("El ejemplo funciona incorrectamente.");

        }

    }

    void assertAreEqual(Object actual, Object esperado)

    {

        assertIsTrue(actual != null && actual.equals(esperado));

    }

    void exampleOfComplexLnkEResourceSupport(String rutaPsdSrc, int longitud, int longitud2, Object[] valoresEsperadosFuenteDatos)

    {

        // Cargar un PSD predefinido que contiene un LayerResource con múltiples fuentes de datos

        PsdImage imagen = (