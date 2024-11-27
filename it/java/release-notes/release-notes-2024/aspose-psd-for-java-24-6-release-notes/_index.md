---
title: Note sulla versione di Aspose.PSD 24.6 per Java
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-24-6-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) {{% /alert %}}

| **Chiave**   | **Sommario**                                                                                                    | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | Implementare il supporto per il livello della mappa del gradiente                                                 | Funzionalità |
| PSDJAVA-629 | [Formato AI] Aggiungi il supporto per i metadati XPacket al formato AI                                             | Funzionalità |
| PSDJAVA-630 | Implementare i tipi di deformazione Inflate, Squeeze e Twist                                                       | Funzionalità |
| PSDJAVA-631 | Le modalità Rgb e Lab non possono contenere meno di 3 canali e più di 4 canali nel file con livelli ArtBoard     | Bug          |
| PSDJAVA-632 | L'area di elaborazione superiore deve essere positiva. (Parametro 'areaToProcess') durante l'elaborazione di un file specifico | Bug          |
| PSDJAVA-633 | L'immagine espansa oltre il canvas viene ritagliata dopo il salvataggio. I dati sono persi ma l'anteprima sembra corretta | Bug          |

## **Modifiche all'API pubblica**
# **API aggiunte:**

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

# **API rimosse:**

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

## **Esempi di utilizzo:**

**PSDJAVA-628. Implementare il supporto per il livello della mappa del gradiente**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/gradient_map_src.psd";
        String outputFile = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            // Aggiungi il livello di regolazione della mappa del gradiente.
            GradientMapLayer layer = im.addGradientMapAdjustmentLayer();
            layer.getGradientSettings().setReverse(true);

            im.save(outputFile);
        }

        // Controlla le modifiche salvate
        try (PsdImage im = (PsdImage) Image.load(outputFile)) {
            GradientMapLayer gradientMapLayer = (GradientMapLayer) im.getLayers()[1];
            GradientFillSettings gradientSettings = (GradientFillSettings) gradientMapLayer.getGradientSettings();

            assertAreEqual(0.0, gradientSettings.getAngle());
            assertAreEqual((short) 4096, gradientSettings.getInterpolation());
            assertAreEqual(true, gradientSettings.getReverse());
            assertAreEqual(false, gradientSettings.getAlignWithLayer());
            assertAreEqual(false, gradientSettings.getDither());
            assertAreEqual(GradientType.Linear, gradientSettings.getGradientType());
            assertAreEqual(100, gradientSettings.getScale());
            assertAreEqual(0.0, gradientSettings.getHorizontalOffset());
            assertAreEqual(0.0, gradientSettings.getVerticalOffset());
            assertAreEqual("Custom", gradientSettings.getGradientName());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [Formato AI] Aggiungi il supporto per i metadati XPacket al formato AI**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ai_one.ai";

        String creatorToolKey = ":CreatorTool";
        String nPagesKey = "xmpTPg:NPages";
        String unitKey = "stDim:unit";
        String heightKey = "stDim:h";
        String widthKey = "stDim:w";

        String expectedCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
        String expectedNPages = "1";
        String expectedUnit = "Pixels";
        double expectedHeight = 768;
        double expectedWidth = 1366;

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // I metadati Xmp sono stati aggiunti.
            var xmpMetaData = image.getXmpData();

            assertIsNotNull(xmpMetaData);

            // Ora possiamo accedere ai pacchetti Xmp dei file AI.
            var basicPackage = (XmpBasicPackage) xmpMetaData.getPackage(Namespaces.XmpBasic);
            XmpPackage package_ = xmpMetaData.getPackages()[4];
            // E abbiamo accesso al contenuto di questi pacchetti.
            var creatorTool = basicPackage.get_Item(creatorToolKey).toString();
            var nPages = package_.get_Item(nPagesKey);
            var unit = package_.get_Item(unitKey);
            var height = Double.parseDouble(package_.get_Item(heightKey).toString());
            var width = Double.parseDouble(package_.get_Item(widthKey).toString());

            assertAreEqual(creatorTool, expectedCreatorTool);
            assertAreEqual(nPages, expectedNPages);
            assertAreEqual(unit, expectedUnit);
            assertAreEqual(height, expectedHeight);
            assertAreEqual(width, expectedWidth);
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("L'oggetto di test è nullo.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Implementare i tipi di deformazione Inflate, Squeeze e Twist**

{{< highlight java >}}

    String[] files = {"Twist", "Squeeze", "Squeeze_vert", "Inflate"};

    for (String prefix : files) {
        String sourceFile = "src/main/resources/" + prefix + ".psd";
        String outputFile = "src/main/resources/" + prefix + "_export.png";

        PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
        psdLoadOptions.setAllowWarpRepaint(true);
        psdLoadOptions.setLoadEffectsResource(true);
        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
            psdImage.save(outputFile, pngOptions);
        }
    }

{{< /highlight >}}

**PSDJAVA-631. Le modalità Rgb e Lab non possono contenere meno di 3 canali e più di 4 canali nel file con livelli ArtBoard**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Rgb5Channels.psb";
    String outputFile = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // Qui non dovrebbe esserci alcuna eccezione
        image.save(outputFile);
    }

{{< /highlight >}}

**PSDJAVA-632. L'area di elaborazione superiore deve essere positiva. (Parametro 'areaToProcess') durante l'elaborazione di un file specifico**

{{< highlight java >}}

    String sourceFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String outputFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);
    try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        image.save(outputFile);
        // Non dovrebbe esserci eccezione
    }

{{< /highlight >}}

**PSDJAVA-633. L'immagine espansa oltre il canvas viene ritagliata dopo il salvataggio. I dati sono persi ma l'anteprima sembra corretta**

{{< highlight java >}}

    String sourceFile = "src/main/resources/bigfile.psd";

    String outputFile = "src/main/resources/bigfile_output.psd";
    String outputPicture = "src/main/resources/bigfile.png";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setUseDiskForLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);
        // Non dovrebbero esserci errori qui
        psdImage.save(outputFile, psdOptions);
    }

    try (var psdImage = (PsdImage) Image.load(outputFile, loadOptions)) {
        psdImage.resize(psdImage.getWidth() / 10, psdImage.getHeight() / 10);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        // Non dovrebbero esserci errori qui
        psdImage.save(outputPicture, pngOptions);
    }

{{< /highlight >}}