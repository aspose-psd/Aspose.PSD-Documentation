---
title: Note sulla release di Aspose.PSD per Java 21.5
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-21-5-note-sulla-release/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla release di [Aspose.PSD per Java 21.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-per-java-21-5/) {{% /alert %}}

{{% alert color="info" %}}
Questa è una release intermedia di Aspose.PSD per Java.
Presenta alcuni problemi noti. Quindi, se hai bisogno di una versione stabile, dovresti utilizzare [Aspose.PSD 20.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.9/) fino a quando non verrà rilasciato Aspose.PSD 21.6.
Questa release include tutte le funzionalità di Aspose.PSD .Net (incluso Smart Object) dal 20.9 e le funzionalità elencate di seguito.
{{% /alert %}} 

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-340|Supporto per il ridimensionamento dei layer di forma con percorsi vettoriali quando viene ridimensionato solo un layer|Funzionalità|
|PSDJAVA-341|Supporto per il ridimensionamento dei layer di forma con percorsi vettoriali|Funzionalità|
|PSDJAVA-342|Stringa di testo troncata|Bugs|

# **Modifiche all'API pubblica**
# **API Aggiunte:**
- M:com.aspose.psd.CmykColor.isEquals(com.aspose.psd.CmykColor,com.aspose.psd.CmykColor)
- M:com.aspose.psd.Color.isEquals(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.ColorPaletteHelper.getCloseImagePalette(com.aspose.psd.RasterImage,com.aspose.psd.Rectangle,int,boolean)
- ...

# **API Rimosse:**
- M:com.aspose.psd.coreexceptions.imageformats.BmpImageException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.RleCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- M:com.aspose.psd.coreexceptions.compressors.LzwCompressorException.#ctor(java.lang.String,java.lang.RuntimeException)
- ...

# **Esempi d'uso:**

**PSDJAVA-340. Supporto per il ridimensionamento dei layer di forma con percorsi vettoriali quando solo un layer viene ridimensionato**

{{< highlight java >}}
    // Questo esempio mostra come ridimensionare i layer con un Vogk e risorsa del percorso vettoriale nell'immagine PSD
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

**PSDJAVA-341. Supporto per il ridimensionamento dei layer di forma con percorsivettoriali**

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

**PSDJAVA-342. Stringa di testo troncata**

{{< highlight java >}}
    String srcFile = "grinched-regular-font.psd";
    String output = "output_grinched-regular-font.psd.png";

    // Imposta il percorso dei font
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