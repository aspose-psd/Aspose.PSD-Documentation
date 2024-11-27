---
title: Aspose.PSD за Java 24.6 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-for-java-24-6-release-notes/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) {{% /alert %}}

| **Ключ**     | **Резюме**                                                                                                      | **Категория** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | Добавяне на поддръжка на слой за картографиране на градиенти                                                                          | Функционалност      |
| PSDJAVA-629 | [Формат AI] Добавяне на поддръжка на метаданни XPacket към формата AI                                                         | Функционалност      |
| PSDJAVA-630 | Добавяне на типовете изкривяване Inflate, Squeeze и Twist                                                               | Функционалност      |
| PSDJAVA-631 | Rgb and Lab modes не могат да съдържат по-малко от 3 канала и повече от 4 канала във файла с ArtBoard Layers | Проблем      |
| PSDJAVA-632 | Горният край на областта за обработка трябва да бъде положителен. (Параметър 'areaToProcess') при обработката на конкретен файл         | Проблем          |
| PSDJAVA-633 | Разширеното изображение отива извън платното след запазването. Данните се загубват, но прегледът изглежда правилен               | Проблем          |

## **Промени в общественото API**
# **Добавени API:**

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

# **Премахнати API:**

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

## **Примери за използване:**

**PSDJAVA-628. Добавяне на поддръжка на слой за картографиране на градиенти**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/gradient_map_src.psd";
        String outputFile = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            // Добавяне на слой за корекция на картографиране на градиенти.
            GradientMapLayer layer = im.addGradientMapAdjustmentLayer();
            layer.getGradientSettings().setReverse(true);

            im.save(outputFile);
        }

        // Проверка на запазените промени
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
        assertAreEqual(expected, actual, "Обектите не са равни.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [Формат AI] Добавяне на поддръжка на метаданни XPacket към формата AI**

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
            // Метаданните Xmp бяха добавени.
            var xmpMetaData = image.getXmpData();

            assertIsNotNull(xmpMetaData);

            // Вече можем да получим достъп до пакети Xmp на AI файловете.
            var basicPackage = (XmpBasicPackage) xmpMetaData.getPackage(Namespaces.XmpBasic);
            XmpPackage package_ = xmpMetaData.getPackages()[4];
            // Имаме достъп и до съдържанието на тези пакети.
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
        assertAreEqual(expected, actual, "Обектите не са равни.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("Тестовият обект е нулев.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Добавяне на типовете изкривяване Inflate, Squeeze и Twist**

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

**PSDJAVA-631. Rgb and Lab modes не могат да съдържат по-малко от 3 канала и повече от 4 канала във файла с ArtBoard Layers**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Rgb5Channels.psb";
    String outputFile = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // Тук не трябва да има изключение
        image.save(outputFile);
    }

{{< /highlight >}}

**PSDJAVA-632. Горният край на областта за обработка трябва да бъде положителен. (Параметър 'areaToProcess') при обработката на конкретен файл**

{{< highlight java >}}

    String sourceFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String outputFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);
    try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        image.save(outputFile);
        // Не би трябвало да има изключение
    }

{{< /highlight >}}

**PSDJAVA-633. Разширеното изображение отива извън платното след запазването. Данните се загубват, но прегледът изглежда правилен**

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
        // Тук не би трябвало да има грешка
        psdImage.save(outputFile, psdOptions);
    }

    try (var psdImage = (PsdImage) Image.load(outputFile, loadOptions)) {
        psdImage.resize(psdImage.getWidth() / 10, psdImage.getHeight() / 10);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        // Тук не би трябвало да има грешка
        psdImage.save(outputPicture, pngOptions);
    }

{{< /highlight >}}