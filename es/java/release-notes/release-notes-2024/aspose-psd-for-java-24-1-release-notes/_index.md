---
title: Notas de Lanzamiento de Aspose.PSD para Java 24.1
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-24-1-notas-de-lanzamiento/
---

{{% alert color="primary" %}} Esta página contiene notas de lanzamiento de [Aspose.PSD para Java 24.1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) {{% /alert %}}

| **Clave**   | **Resumen**                                                                                    | **Categoría** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [Formato AI] Agregar manejo básico para imágenes AI de varias páginas.                         | Característica |
| PSDJAVA-579 | El efecto de Texto Warp no se aplica al texto.                                                  | Error        |
| PSDJAVA-580 | Renderización incorrecta de máscara en el archivo específico.                                  | Error        |
| PSDJAVA-581 | Excepción de Referencia Nula en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor. | Error |
| PSDJAVA-582 | [Formato AI] Arreglar el uso de memoria en AiExporterUtils.                                      | Error        |

## **Cambios en la API Pública**
# **APIs Agregadas:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getUseVectorColor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setUseVectorColor(boolean)
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
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getDither
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getFillType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getHorizontalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getReverse
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getScale
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getVerticalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setVerticalOffset(double)

# **APIs Eliminadas:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getScale
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getVerticalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setVerticalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColorPoints
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getTransparencyPoints
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColorPoints(com.aspose.psd.fileformats.psd.layers.IGradientColorPoint[])
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setTransparencyPoints(com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint[])
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB

## **Ejemplos de Uso:**

** PSDJAVA-576. [Formato AI] Agregar manejo básico para imágenes AI de varias páginas**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/tresPaginas.ai";
        String pngSalidaPrimeraPagina = "src/main/resources/salidaPrimeraPagina.png";
        String pngSalidaSegundaPagina = "src/main/resources/salidaSegundaPagina.png";
        String pngSalidaTerceraPagina = "src/main/resources/salidaTerceraPagina.png";

        // Cargar la imagen AI.
        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            // Por defecto, el ActivePageIndex es 0.
            // Por lo tanto, si guarda la imagen AI sin cambiar esta propiedad, se renderizará y guardará la primera página.
            imagen.save(pngSalidaPrimeraPagina, new PngOptions());

            // Cambiar el índice de página activo a la segunda página.
            imagen.setActivePageIndex(1);

            // Guardar la segunda página de la imagen AI como una imagen PNG.
            imagen.save(pngSalidaSegundaPagina, new PngOptions());

            // Cambiar el índice de página activo a la tercera página.
            imagen.setActivePageIndex(2);

            // Guardar la tercera página de la imagen AI como una imagen PNG.
            imagen.save(pngSalidaTerceraPagina, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. El efecto de Texto Warp no se aplica al texto**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/texto_warp.psd";
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

** PSDJAVA-580. Renderización incorrecta de máscara en el archivo específico**

{{< highlight java >}}

        String archivoFuente1 = "src/main/resources/problema_mascara.psd";
        String archivoFuente2 = "src/main/resources/puh_softLight3_1.psd";
        String archivoSalida1 = "src/main/resources/exportacion_mascara.png";
        String archivoSalida2 = "src/main/resources/exportacion_puh.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(archivoFuente1, opt)) {
            PngOptions opcionesPng = new PngOptions();
            opcionesPng.setCompressionLevel(9);
            opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(archivoSalida1, opcionesPng);
        }

        try (PsdImage img = (PsdImage) Image.load(archivoFuente2, opt)) {
            PngOptions opcionesPng = new PngOptions();
            opcionesPng.setCompressionLevel(9);
            opcionesPng.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(archivoSalida2, opcionesPng);
        }

{{< /highlight >}}

** PSDJAVA-581. Excepción de Referencia Nula en Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor**

{{< highlight java >}}

        String carpetaFuentes = "src/main/resources/Fuentes";
        FontSettings.setFontsFolders(new String[]{carpetaFuentes}, true);

        String archivoEntrada = "src/main/resources/1.psd";
        String archivoSalida = "src/main/resources/salida_1855.png";
        try (PsdImage imagenPsd = (PsdImage) Image.load(archivoEntrada)) {
            imagenPsd.save(archivoSalida, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [Formato AI] Arreglar el uso de memoria en AiExporterUtils**

{{< highlight java >}}

        String archivoFuente = "src/main/resources/tresPaginas.ai";
        String pngSalidaPrimeraPagina = "src/main/resources/salidaPrimeraPagina.png";
        String pngSalidaSegundaPagina = "src/main/resources/salidaSegundaPagina.png";
        String pngSalidaTerceraPagina = "src/main/resources/salidaTerceraPagina.png";

        final double LimiteMemoria = 700;
        double memoriaUtilizada = Double.MAX_VALUE;

        // Cargar la imagen AI.
        try (AiImage imagen = (AiImage) Image.load(archivoFuente)) {
            // Guardar la primera página de la imagen AI como una imagen PNG.
            imagen.save(pngSalidaPrimeraPagina, new PngOptions());

            // Cambiar el índice de página activo a la segunda página.
            imagen.setActivePageIndex(1);

            // Guardar la segunda página de la imagen AI como una imagen PNG.
            imagen.save(pngSalidaSegundaPagina, new PngOptions());

            // Cambiar el índice de página activo a la tercera página.
            imagen.setActivePageIndex(2);

            // Guardar la tercera página de la imagen AI como una imagen PNG.
            imagen.save(pngSalidaTerceraPagina, new PngOptions());
        }

        System.gc();

        memoriaUtilizada = (double) (Runtime.getRuntime().totalMemory() - Runtime.getRuntime().freeMemory()) / (1024.0 * 1024.0);

        if (memoriaUtilizada > LimiteMemoria) {
            throw new RuntimeException("El uso de memoria es demasiado grande.