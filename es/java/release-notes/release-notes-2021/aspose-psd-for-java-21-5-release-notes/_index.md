---
title: Notas de la versión Aspose.PSD para Java 21.5
type: docs
weight: 40
url: /es/java/aspose-psd-para-java-21-5-notas-de-version/
---

{{% alert color="primary" %}} Esta página contiene notas de versión para [Aspose.PSD para Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd. for-java-21.5/) {{% /alert %}}

{{% alert color="info" %}}
Esta es una versión intermedia de Aspose.PSD para Java.
Tiene algunos problemas conocidos. Por lo tanto, si necesita una versión estable, debería usar [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) hasta que se lance Aspose.PSD 21.6.
Esta versión incluye todas las funciones de Aspose.PSD .Net (Incluyendo Smart Object) desde la versión 20.9 y las funciones enumeradas a continuación.
{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-340|Soportar el redimensionamiento de capas de forma con rutas vectoriales cuando solo se redimensiona una capa|Función|
|PSDJAVA-341|Soportar el redimensionamiento de capas de forma con rutas vectoriales|Función|
|PSDJAVA-342|Cadena de texto truncada|Error|

# **Cambios en la API pública**
# **APIs agregadas:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M:com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- M:com.aspose.psd.ColorPaletteHelper.hasTransparentColors(com.aspose.psd.IColorPalette)
<!-- More APIs... -->

# **APIs eliminadas:**
- M:com.aspose.psd.coreexceptions.imageformats.BmpImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.RleCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.LzwCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
<!-- More APIs... -->

# **Ejemplos de uso:**

**PSDJAVA-340. Soportar el redimensionamiento de capas de forma con rutas vectoriales cuando solo se redimensiona una capa**

{{< highlight java >}}
    // Este ejemplo muestra cómo redimensionar capas con un recurso Vogk y una ruta vectorial en la imagen PSD
    float scaleX = 0.45f;
    float scaleY = 1.60f;
    String dataDir = "PSDNET862_1";
    String sourceFileName = Paths.get(dataDir, "vectorShapes.psd").toString();
    PsdImage image = (PsdImage) Image.load(sourceFileName);
    try {
        for (int layerIndex = 1; layerIndex < image.getLayers().length; layerIndex++, scaleX += 0.25f, scaleY -= 0.25f) {
            Layer layer = image.getLayers()[layerIndex];
            int newWidth = (int) Math.round(layer.getWidth() * scaleX);
            int newHeight = (int) Math.round(layer.getHeight() * scaleY);
            layer.resize(newWidth, newHeight);

            String outputName = String.format("resized_%1$s_%2$s_%2$s", layerIndex, scaleX, scaleY);
            String outputPath = Paths.get(dataDir, outputName + ".psd").toString();
            String outputPngPath = Paths.get(dataDir, outputName + ".png").toString();
            image.save(outputPath, new PsdOptions(image));
            PngOptions options = new PngOptions();
            options.setColorType(PngColorType.TruecolorWithAlpha);
            image.save(outputPngPath, options);
        }
    } finally {
        image.dispose();
    }
{{< /highlight >}}
<!-- More usages... -->**PSDJAVA-341. Soportar el redimensionamiento de capas de forma con rutas vectoriales**

{{< highlight java >}}
    String sourceFileName = "vectorShapes.psd";
    String outputFileName = "out_vectorShapes.psd";
    String dataDir = "PSDNET758_1";
    String sourcePath = Paths.get(dataDir, sourceFileName).toString();
    String outputPath = Paths.get(dataDir, outputFileName).toString();
    PsdImage psdImage = (PsdImage) Image.load(sourcePath);
    try {
        for (Layer layer : psdImage.getLayers())
        {
            layer.resize(layer.getWidth() * 5 / 4, layer.getHeight() / 2);
        }

        psdImage.save(outputPath);
        PngOptions options = new PngOptions();
        options.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outputPath + ".png", options);
    } finally {
        psdImage.dispose();
    }
{{< /highlight >}}

**PSDJAVA-342. Cadena de texto truncada**

{{< highlight java >}}
    String srcFile = "grinched-regular-font.psd";
    String output = "output_grinched-regular-font.psd.png";

    // Establecer la ruta de las fuentes
    List<String> fonts = new ArrayList<>();
    fonts.addAll(Arrays.asList(FontSettings.getDefaultFontsFolders()));
    fonts.add("Fonts\\");
    FontSettings.setFontsFolders(fonts.toArray(new String[0]), true);

    PsdImage image = (PsdImage) Image.load(srcFile);
    try {
        image.save(output, new PngOptions());
    } finally {
        image.dispose();
    }
{{< /highlight >}}