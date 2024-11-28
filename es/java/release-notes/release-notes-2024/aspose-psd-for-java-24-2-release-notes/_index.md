---
title: Notas de la versión de Aspose.PSD para Java 24.2
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-24-2-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión para [Aspose.PSD para Java 24.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.2/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                    | **Categoría** |
|:------------|:-------------------------------------------------------------------------------|:-------------|
| PSDJAVA-584 | Manejar la propiedad de ángulo para PatternFillSettings.                         | Característica |
| PSDJAVA-585 | Soporte de escala vertical y horizontal para TextLayer.                         | Característica |
| PSDJAVA-589 | [AI Format] Implementar la representación correcta del fondo en el formato AI basado en PDF. | Característica |
| PSDJAVA-590 | Cambiar el mecanismo de distorsión en warp.                                      | Mejora        |
| PSDJAVA-591 | Acelerar el warp.                                                               | Mejora        |
| PSDJAVA-592 | Excepción "Error al cargar la imagen." al abrir un documento.                    | Error         |
| PSDJAVA-593 | Corregir el guardado de archivos psd con patrón de trazo.                        | Error         |
| PSDJAVA-594 | El estilo del texto es incorrecto en un objeto inteligente al usar ReplaceContents. | Error         |
| PSDJAVA-595 | [AI Format] Corregir la representación de Curva Cúbica en el archivo AI.         | Error         |

## **Cambios en la API pública**
# **APIs agregadas:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- T:com.aspose.psd.fileformats.psd.layers.FillLayer
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.getFillType
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.FillLayer.update
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.getAngle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PtFlResource.setAngle(double)

# **APIs eliminadas:**

- T:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.createInstance(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.getFillType
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.replaceNonTransparentColors(int)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.filllayers.FillLayer.update

## **Ejemplos de uso:**

** PSDJAVA-584. Manejar la propiedad de ángulo para PatternFillSettings**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/PatternFillLayerWide_0.psd";
        String archivoSalida = "src/main/resources/PatternFillLayerWide_0_salida.psd";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage imagen = (PsdImage) Image.load(archivoFuente, psdLoadOptions)) {
            FillLayer capaRelleno = (FillLayer) imagen.getLayers()[1];
            PatternFillSettings configRelleno = (PatternFillSettings) capaRelleno.getFillSettings();
            configRelleno.setAngle(70.0);
            capaRelleno.update();
            imagen.save(archivoSalida, new PsdOptions());
        }

        try (PsdImage imagen = (PsdImage) Image.load(archivoSalida, psdLoadOptions)) {
            FillLayer capaRelleno = (FillLayer) imagen.getLayers()[1];
            PatternFillSettings configRelleno = (PatternFillSettings) capaRelleno.getFillSettings();

            assertAreEqual(70.0, configRelleno.getAngle());
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

** PSDJAVA-585. Soporte de escala vertical y horizontal para TextLayer**

{{< highlight java >}}

        String src = "src/main/resources/1719_src.psd";
        String output = "src/main/resources/out_1719.png";

        try (PsdImage psdImage = (PsdImage) Image.load(src)) {
            psdImage.save(output, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-589. [AI Format] Implementar la representación correcta del fondo en el formato AI basado en PDF**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/pineapples.ai";
        String rutaSalida = "src/main/resources/pineapples.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            imagen.save(rutaSalida, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-590. Cambiar el mecanismo de distorsión en warp**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/crow_grid.psd";
        String archivoSalida = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(archivoFuente, opt)) {
            PngOptions opcionesPng = new PngOptions();
            opcionesPng.setCompressionLevel(9);
            opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(archivoSalida, opcionesPng);
        }

{{< /highlight >}}

** PSDJAVA-591. Acelerar el warp**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/output.psd";
        String archivoSalida = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        long inicioTiempo = System.currentTimeMillis();

        try (PsdImage img = (PsdImage) Image.load(archivoFuente, opt)) {
            PngOptions opcionesPng = new PngOptions();
            opcionesPng.setCompressionLevel(9);
            opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(archivoSalida, opcionesPng);
        }

        long finTiempo = System.currentTimeMillis();
        int tiempoEnSeg = (int) (finTiempo - inicioTiempo);

        if (tiempoEnSeg > 100000) {
            throw new RuntimeException("El tiempo de procesamiento es demasiado largo");
        }

{{< /highlight >}}

** PSDJAVA-592. Excepción "Error al cargar la imagen." al abrir un documento**

{{< highlight java >}}

        String archivoFuente1 = "src/main/resources/PRODUCT.ai";
        String archivoSalida1 = "src/main/resources/PRODUCT.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente1)) {
            imagen.save(archivoSalida1, new PngOptions());
        }

        String archivoFuente2 = "src/main/resources/Dolota.ai";
        String archivoSalida2 = "src/main/resources/Dolota.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente2)) {
            imagen.save(archivoSalida2, new PngOptions());
        }

        String archivoFuente3 = "src/main/resources/ARS_novelty_2108_out_01(1).ai";
        String archivoSalida3 = "src/main/resources/ARS_novelty_2108_out_01(1).png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente3)) {
            imagen.save(archivoSalida3, new PngOptions());
        }

        String archivoFuente4 = "src/main/resources/bit_gear.ai";
        String archivoSalida4 = "src/main/resources/bit_gear.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente4)) {
            imagen.save(archivoSalida4, new PngOptions());
        }

        String archivoFuente5 = "src/main/resources/test.ai";
        String archivoSalida5 = "src/main/resources/test.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente5)) {
            imagen.save(archivoSalida5, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-593. Corregir el guardado de archivos psd con patrón de trazo**

{{< highlight java >}}

    public static void main(String[] args) {
        String archivoFuente = "src/main/resources/StrokeShapePattern.psd";
        String archivoSalida = "src/main/resources/StrokeShapePattern_output.psd";

        Rectangle nuevosLimitesPatron = new Rectangle(0, 0, 4, 4);
        UUID guid = UUID.randomUUID();
        String nuevoNombrePatron = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
        int[] nuevoPatron = new int[]
                {
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getWhite().toArgb(), Color.getWhite().toArgb(), Color.getAqua().toArgb(),
                        Color.getAqua().toArgb(), Color.getRed().toArgb(), Color.getRed().toArgb(), Color.getAqua().toArgb(),
                };

        try (PsdImage imagen = (PsdImage) Image.load(archivoFuente)) {
            ShapeLayer capaForma = (ShapeLayer) imagen.getLayers()[1];
            PatternFillSettings configRellenoInternoTrazo = (PatternFillSettings) capaForma.getFill();

            PattResource recursoPatt;
            for (LayerResource recursoGlobalCapa : imagen.getGlobalLayerResources()) {
                if (recursoGlobalCapa instanceof PattResource) {
                    recursoPatt = (PattResource) recursoGlobalCapa;
                    PattResourceData elementoPatron = recursoPatt.getPatterns()[0]; // Datos del patrón interno del trazo

                    elementoPatron.setPatternId(guid.toString());
                    elementoPatron.setName(nuevoNombrePatron);
                    elementoPatron.setPattern(nuevoPatron, nuevosLimitesPatron);

                    break;
                }
            }

            configRellenoInternoTrazo.setPatternName(nuevoNombrePatron);
            configRellenoInternoTrazo.setPatternId(guid.toString() + "\0");

            capaForma.update();

            imagen.save(archivoSalida);
        }

        // Verificar los datos modificados.
        try (PsdImage imagen = (PsdImage) Image.load(archivoSalida)) {
            ShapeLayer capaForma = (ShapeLayer) imagen.getLayers()[1];
            PatternFillSettings configRellenoInternoTrazo = (PatternFillSettings) capaForma.getFill();

            assertAreEqual(guid.toString().toUpperCase(), configRellenoInternoTrazo.getPatternId());
            assertAreEqual(nuevoNombrePatron, configRellenoInternoTrazo.getPatternName() + "\0");
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

** PSDJAVA-594. El estilo del texto es incorrecto en un objeto inteligente al usar ReplaceContents**

{{< highlight java >}}

        String archivoEntrada = "src/main/resources/source.psd";
        String salida2 = "src/main/resources/salida.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setLoadEffectsResource(true);

        try (PsdImage imagenPsd = (PsdImage) Image.load(archivoEntrada, psdLoadOptions)) {
            SmartObjectLayer objetoInteligente = (SmartObjectLayer) imagenPsd.getLayers()[1];

            try (PsdImage imagenObjetoInteligente = (PsdImage) objetoInteligente.loadContents(psdLoadOptions)) {
                objetoInteligente.replaceContents(imagenObjetoInteligente);
            }

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            imagenPsd.save(salida2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-595. [AI Format] Corregir la representación de Curva Cúbica en el archivo AI**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/Typography.ai";
        String rutaSalida = "src/main/resources/Typography.png";

        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            imagen.save(rutaSalida, new PngOptions());
        }

{{< /highlight >}}