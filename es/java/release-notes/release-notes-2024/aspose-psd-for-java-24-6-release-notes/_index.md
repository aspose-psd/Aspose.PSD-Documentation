---
title: Notas de la versión de Aspose.PSD para Java 24.6
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-24-6-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                                      | **Categoría** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | Implementar soporte de capa de mapa de degradado                                                                   | Característica|
| PSDJAVA-629 | [Formato AI] Agregar soporte de metadatos de paquete X a AI formato                                                  | Característica|
| PSDJAVA-630 | Implementar tipos de deformación Inflate, Squeeze y Twist                                                           | Característica|
| PSDJAVA-631 | Los modos Rgb y Lab no pueden contener menos de 3 canales y más de 4 canales en el archivo con capas de ArtBoard    | Error        |
| PSDJAVA-632 | El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de archivos específicos | Error        |
| PSDJAVA-633 | La imagen ampliada sobre el lienzo se recorta después de guardarla. Los datos se pierden pero la vista previa se ve correcta | Error        |

## **Cambios en la API pública**
# **APIs añadidas:**

- M:com.aspose.psd.fileformats.ai.AiImage.getXmpData
- M:com.aspose.psd.fileformats.psd.PsdImage.addGradientMapAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.setGradientSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.GradientMapLayer.getGradientSettings
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getExpansionCount
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setExpansionCount(short)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToInt(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.intToNoiseColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.StrModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelRGB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GradientHelper.IntModelHSB
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientName(java.lang.String)

# **APIs removidas:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientName(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB

## **Ejemplos de uso:**

**PSDJAVA-628. Implementar soporte de capa de mapa de degradado**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/gradient_map_src.psd";
        String archivoSalida = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(archivoFuente)) {
            // Agregar capa de ajuste de mapa de degradado.
            GradientMapLayer capa = im.addGradientMapAdjustmentLayer();
            capa.getGradientSettings().setReverse(true);

            im.save(archivoSalida);
        }

        // Verificar cambios guardados
        try (PsdImage im = (PsdImage) Image.load(archivoSalida)) {
            GradientMapLayer capaMapaDegradado = (GradientMapLayer) im.getLayers()[1];
            GradientFillSettings ajustesDegradado = (GradientFillSettings) capaMapaDegradado.getGradientSettings();

            assertAreEqual(0.0, ajustesDegradado.getAngle());
            assertAreEqual((short) 4096, ajustesDegradado.getInterpolation());
            assertAreEqual(true, ajustesDegradado.getReverse());
            assertAreEqual(false, ajustesDegradado.getAlignWithLayer());
            assertAreEqual(false, ajustesDegradado.getDither());
            assertAreEqual(GradientType.Linear, ajustesDegradado.getGradientType());
            assertAreEqual(100, ajustesDegradado.getScale());
            assertAreEqual(0.0, ajustesDegradado.getHorizontalOffset());
            assertAreEqual(0.0, ajustesDegradado.getVerticalOffset());
            assertAreEqual("Custom", ajustesDegradado.getGradientName());
        }
    }

    static void assertAreEqual(Object esperado, Object actual) {
        assertAreEqual(esperado, actual, "Los objetos no son iguales.");
    }

    static void assertAreEqual(Object esperado, Object actual, String mensaje) {
        if (!esperado.equals(actual)) {
            throw new IllegalArgumentException(mensaje);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [Formato AI] Agregar soporte de metadatos XPacket a AI formato**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/ai_one.ai";

        String claveHerramientaCreador = ":CreatorTool";
        String claveNPaginas = "xmpTPg:NPages";
        String claveUnidad = "stDim:unit";
        String claveAltura = "stDim:h";
        String claveAnchura = "stDim:w";

        String herramientaCreadorEsperada = "Adobe Illustrator CC 22.1 (Windows)";
        String nPaginasEsperadas = "1";
        String unidadEsperada = "Pixels";
        double alturaEsperada = 768;
        double anchuraEsperada = 1366;

        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            // Se agregaron metadatos Xmp.
            var metadatosXmp = imagen.getXmpData();

            assertIsNotNull(metadatosXmp);

            // Ahora podemos acceder a los paquetes Xmp de los archivos AI.
            var paqueteBasico = (XmpBasicPackage) metadatosXmp.getPackage(Namespaces.XmpBasic);
            XmpPackage paquete = metadatosXmp.getPackages()[4];
            // Y tenemos acceso al contenido de estos paquetes.
            var herramientaCreador = paqueteBasico.get_Item(claveHerramientaCreador).toString();
            var nPaginas = paquete.get_Item(claveNPaginas);
            var unidad = paquete.get_Item(claveUnidad);
            var altura = Double.parseDouble(paquete.get_Item(claveAltura).toString());
            var anchura = Double.parseDouble(paquete.get_Item(claveAnchura).toString());

            assertAreEqual(herramientaCreador, herramientaCreadorEsperada);
            assertAreEqual(nPaginas, nPaginasEsperadas);
            assertAreEqual(unidad, unidadEsperada);
            assertAreEqual(altura, alturaEsperada);
            assertAreEqual(anchura, anchuraEsperada);
        }
    }

    static void assertAreEqual(Object esperado, Object actual) {
        assertAreEqual(esperado, actual, "Los objetos no son iguales.");
    }

    static void assertAreEqual(Object esperado, Object actual, String mensaje) {
        if (!esperado.equals(actual)) {
            throw new IllegalArgumentException(mensaje);
        }
    }

    static void assertIsNotNull(Object objetoPrueba) {
        if (objetoPrueba == null) {
            throw new RuntimeException("El objeto de prueba es nulo.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Implementar tipos de deformación Inflate, Squeeze y Twist**

{{< highlight java >}}

    String[] archivos = {"Twist", "Squeeze", "Squeeze_vert", "Inflate"};

    for (String prefijo : archivos) {
        String archivoFuente = "src/main/resources/" + prefijo + ".psd";
        String archivoSalida = "src/main/resources/" + prefijo + "_export.png";

        PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
        opcionesCargaPsd.setAllowWarpRepaint(true);
        opcionesCargaPsd.setLoadEffectsResource(true);
        try (PsdImage imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCargaPsd)) {
            PngOptions opcionesPng = new PngOptions();
            opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);
            imagenPsd.save(archivoSalida, opcionesPng);
        }
    }

{{< /highlight >}}

**PSDJAVA-631. Los modos Rgb y Lab no pueden contener menos de 3 canales y más de 4 canales en el archivo con capas de ArtBoard**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/Rgb5Channels.psb";
    String archivoSalida = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage imagen = (PsdImage) Image.load(archivoFuente)) {
        // Aquí no debería haber excepciones
        imagen.save(archivoSalida);
    }

{{< /highlight >}}

**PSDJAVA-632. El área de procesamiento superior debe ser positiva. (Parámetro 'areaToProcess') en el procesamiento de archivos específicos**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String archivoSalida = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions opcionesCargaPsd = new PsdLoadOptions();
    opcionesCargaPsd.setLoadEffectsResource(true);
    opcionesCargaPsd.setAllowWarpRepaint(true);
    try (PsdImage imagen = (PsdImage) PsdImage.load(archivoFuente, opcionesCargaPsd)) {
        imagen.save(archivoSalida);
        // No debería haber excepción
    }

{{< /highlight >}}

**PSDJAVA-633. La imagen ampliada sobre el lienzo se recorta después de guardarla. Los datos se pierden pero la vista previa se ve correcta**

{{< highlight java >}}

    String archivoFuente = "src/main/resources/bigfile.psd";
    String archivoSalida = "src/main/resources/bigfile_output.psd";
    String imagenSalida = "src/main/resources/bigfile.png";

    PsdLoadOptions opcionesCarga = new PsdLoadOptions();
    opcionesCarga.setLoadEffectsResource(true);
    opcionesCarga.setUseDiskForLoadEffectsResource(true);

    try (var imagenPsd = (PsdImage) Image.load(archivoFuente, opcionesCarga)) {
        PsdOptions opcionesPsd = new PsdOptions();
        opcionesPsd.setCompressionMethod(CompressionMethod.RLE);
        // No debería haber errores aquí
        imagenPsd.save(archivoSalida, opcionesPsd);
    }

    try (var imagenPsd = (PsdImage) Image.load(archivoSalida, opcionesCarga)) {
        imagenPsd.resize(imagenPsd.getWidth() / 10, imagenPsd.getHeight() / 10);

        PngOptions opcionesPng = new PngOptions();
        opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);
        // No debería haber errores aquí
        imagenPsd.save(imagenSalida, opcionesPng);
    }

{{< /highlight >}}