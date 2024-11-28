---
title: Aspose.PSD برای جاوا 24.6 - یادداشت‌های نسخه
type: docs
weight: 40
url: /fa/java/aspose-psd-for-java-24-6-release-notes/
---

{{% alert color="primary" %}} این صفحه حاوی یادداشت‌های نسخه برای [Aspose.PSD برای جاوا 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) می‌باشد {{% /alert %}}

| **کلید**     | **خلاصه**                                                                                                      | **دسته** |
|:------------|:-----------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-628 | پیاده‌سازی پشتیبانی از لایه نقشه‌ی گرادیان                                                                      | ویژگی      |
| PSDJAVA-629 | [فرمت AI] اضافه کردن پشتیبانی از متا داده XPacket به فرمت AI                                             | ویژگی      |
| PSDJAVA-630 | پیاده‌سازی انواع تورم Inflate، فشرده سازی Squeeze و رنگین Squeeze از نوع وارپ                                                                 | ویژگی      |
| PSDJAVA-631 | حالت‌های Rgb و Lab نمی‌توانند کمتر از ۳ کانال و بیشتر از ۴ کانال را در فایل‌های دارای لایه‌های ArtBoard جای دهند | اشکال     |
| PSDJAVA-632 | بالای محدوده پردازش باید مثبت باشد. ('areaToProcess' پارامتر) در پردازش فایل خاص                   | اشکال     |
| PSDJAVA-633 | بریده شدن تصویر گسترده بیش از تصویر کانونی پس از ذخیره شدن. داده از بین می‌رود اما پیش‌نمایش صحیح است            | اشکال     |

## **تغییرات API عمومی**
# **API‌های اضافه شده:**

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

# **API‌های حذف شده:**

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

## **مثال‌های استفاده:**

**PSDJAVA-628. پیاده‌سازی پشتیبانی از لایه نقشه‌ی گرادیان**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/gradient_map_src.psd";
        String outputFile = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            // افزودن لایه تنظیم نقشه‌ی گرادیان.
            GradientMapLayer layer = im.addGradientMapAdjustmentLayer();
            layer.getGradientSettings().setReverse(true);

            im.save(outputFile);
        }

        // بررسی تغییرات ذخیره شده
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
        assertAreEqual(expected, actual, "اشیاء مساوی نیستند.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [فرمت AI] اضافه کردن پشتیبانی از متا داده XPacket برای فرمت AI**

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
            // متا داده Xmp اضافه شد.
            var xmpMetaData = image.getXmpData();

            assertIsNotNull(xmpMetaData);

            // حالا می‌توانیم به بسته‌های Xmp فایل‌های AI دسترسی پیدا کنیم.
            var basicPackage = (XmpBasicPackage) xmpMetaData.getPackage(Namespaces.XmpBasic);
            XmpPackage package_ = xmpMetaData.getPackages()[4];
            // و دسترسی به محتوای این بسته‌ها داریم.
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
        assertAreEqual(expected, actual, "اشیاء مساوی نیستند.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("اشیاء آزمون تهی هستند.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. پیاده‌سازی انواع تورم Inflate، فشرده سازی Squeeze و رنگین Squeeze از نوع وارپ**

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

**PSDJAVA-631. حالت‌های Rgb و Lab نمی‌توانند کمتر از ۳ کانال و بیشتر از ۴ کانال را در فایل‌های دارای لایه‌های ArtBoard جای دهند**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Rgb5Channels.psb";
    String outputFile = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // اینجا باید هیچ اشکالی وجود نداشته باشد
        image.save(outputFile);
    }

{{< /highlight >}}

**PSDJAVA-632. بالای محدوده پردازش باید مثبت باشد. ('areaToProcess' پارامتر) در پردازش فایل خاص**

{{< highlight java >}}

    String sourceFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String outputFile = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);
    try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        image.save(outputFile);
        // نباید خطا وجود داشته باشد
    }

{{< /highlight >}}

**PSDJAVA-633. تصویر گسترده بیشتر از تصویر کانونی پس از ذخیره شدن بریده می‌شود. داده از بین می‌رود اما پیش‌نمایش صحیح است**

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
        // اینجا نباید هیچ خطایی وجود داشته باشد
        psdImage.save(outputFile, psdOptions);
    }

    try (var psdImage = (PsdImage) Image.load(outputFile, loadOptions)) {
        psdImage.resize(psdImage.getWidth() / 10, psdImage.getHeight() / 10);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        // اینجا نباید هیچ خطایی وجود داشته باشد
        psdImage.save(outputPicture, pngOptions);
    }

{{< /highlight >}}