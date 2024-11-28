---
title: Aspose.PSD for Java 24.6 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-24-6-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 24.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.6/) için sürüm notlarını içermektedir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                          | **Kategori** |
|:------------ |:------------------------------------------------------------------------------------------------------------------|:------------ |
| PSDJAVA-628  | Gradyan haritası katmanının desteklenmesi uygulaması                                                             | Özellik      |
| PSDJAVA-629  | [AI Formatı] XPacket Metadata'in AI Formatına destek eklenmesi                                                   | Özellik      |
| PSDJAVA-630  | Şişirme, Sıkıştırma ve Bigesme türlerinin uygulanması                                                             | Özellik      |
| PSDJAVA-631  | Rgb ve Lab modları, ArtBoard Katmanları içeren dosyada 3 kanaldan az veya 4 kanaldan fazla içeremez              | Hata         |
| PSDJAVA-632  | İşlem bölgesi üstünün pozitif olması gerekmektedir. Belirli bir dosyanın işlenmesinde (Parametre 'areaToProcess') | Hata         |
| PSDJAVA-633  | Kaydetmeden sonra genişletilmiş kanvas görüntüsü kırpılır. Veri kaybolur ancak Önizleme doğru görünür                | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

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

# **Kaldırılan API'ler:**

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

## **Kullanım örnekleri:**

**PSDJAVA-628. Gradyan haritası katmanının desteklenmesi uygulaması**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/gradient_map_src.psd";
        String outputFile = "src/main/resources/gradient_map_src_output.psd";

        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            // Gradyan haritası ayar katmanı ekle.
            GradientMapLayer layer = im.addGradientMapAdjustmentLayer();
            layer.getGradientSettings().setReverse(true);

            im.save(outputFile);
        }

        // Kaydedilen değişiklikleri kontrol et
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
            assertAreEqual("Özel", gradientSettings.getGradientName());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objeler eşit değil.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-629. [AI Formatı] AI Formatına XPacket Metadata desteği ekle**

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
        String expectedUnit = "Piksel";
        double expectedHeight = 768;
        double expectedWidth = 1366;

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // Xmp Metadata eklendi.
            var xmpMetaData = image.getXmpData();

            assertIsNotNull(xmpMetaData);

            // Artık AI dosyalarının Xmp Paketlerine erişebiliriz.
            var basicPackage = (XmpBasicPackage) xmpMetaData.getPackage(Namespaces.XmpBasic);
            XmpPackage package_ = xmpMetaData.getPackages()[4];
            // Ve bu paketlerin içeriğine erişebiliriz.
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
        assertAreEqual(expected, actual, "Objeler eşit değil.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("Test nesnesi null.");
        }
    }

{{< /highlight >}}

**PSDJAVA-630. Şişirme, Sıkıştırma ve Bigesme tiplerinin uygulanması**

{{< highlight java >}}

    String[] dosyalar = {"Twist", "Squeeze", "Squeeze_vert", "Inflate"};

    for (String onEk : dosyalar) {
        String kaynakDosya = "src/main/resources/" + onEk + ".psd";
        String ciktiDosya = "src/main/resources/" + onEk + "_export.png";

        PsdLoadOptions psdYuklemeSecenekleri = new PsdLoadOptions();
        psdYuklemeSecenekleri.setAllowWarpRepaint(true);
        psdYuklemeSecenekleri.setLoadEffectsResource(true);
        try (PsdImage psdResim = (PsdImage) Image.load(kaynakDosya, psdYuklemeSecenekleri)) {
            PngOptions pngSecenekleri = new PngOptions();
            pngSecenekleri.setColorType(PngColorType.TruecolorWithAlpha);
            psdResim.save(ciktiDosya, pngSecenekleri);
        }
    }

{{< /highlight >}}

**PSDJAVA-631. Rgb ve Lab modları, ArtBoard Katmanları içeren dosyada 3 kanalın altında veya 4 kanalın üstünde olamaz**

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/Rgb5Channels.psb";
    String ciktiDosya = "src/main/resources/Rgb5Channels_output.psd";

    try (PsdImage resim = (PsdImage) Image.load(kaynakDosya)) {
        // Burada istisna olmamalı
        resim.save(ciktiDosya);
    }

{{< /highlight >}}

**PSDJAVA-632. İşlemenin üst işlem alanı pozitif olmalıdır. Belirli bir dosyanın işlenmesinde (Parametre 'areaToProcess')**

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/BANNERS_2_Intel-Gamer_psak.psd";
    String ciktiDosya = "src/main/resources/BANNERS_2_Intel-Gamer_psak_out.psd";
    PsdLoadOptions psdYuklemeSecenekleri = new PsdLoadOptions();
    psdYuklemeSecenekleri.setLoadEffectsResource(true);
    psdYuklemeSecenekleri.setAllowWarpRepaint(true);
    try (PsdImage resim = (PsdImage) PsdImage.load(kaynakDosya, psdYuklemeSecenekleri)) {
        resim.save(ciktiDosya);
        // İstisnanın olmaması gerekmektedir
    }

{{< /highlight >}}

**PSDJAVA-633. Genişletilmiş kanvas görüntüsü kaydedildikten sonra kırpılır. Veri kaybolur ancak Önizleme doğru görünür**

{{< highlight java >}}

    String kaynakDosya = "src/main/resources/bigfile.psd";

    String ciktiDosya = "src/main/resources/bigfile_output.psd";
    String ciktiResim = "src/main/resources/bigfile.png";

    PsdLoadOptions yuklemeSecenekleri = new PsdLoadOptions();
    yuklemeSecenekleri.setLoadEffectsResource(true);
    yuklemeSecenekleri.setUseDiskForLoadEffectsResource(true);

    try (var psdResim = (PsdImage) Image.load(kaynakDosya, yuklemeSecenekleri)) {
        PsdOptions psdSecenekler = new PsdOptions();
        psdSecenekler.setCompressionMethod(CompressionMethod.RLE);
        // Burada hata olmamalı
        psdResim.save(ciktiDosya, psdSecenekler);
    }

    try (var psdResim = (PsdImage) Image.load(ciktiDosya, yuklemeSecenekleri)) {
        psdResim.resize(psdResim.getWidth() / 10, psdResim.getHeight() / 10);

        PngOptions pngSecenekleri = new PngOptions();
        pngSecenekleri.setColorType(PngColorType.TruecolorWithAlpha);
        // Burada hata olmamalı
        psdResim.save(ciktiResim, pngSecenekleri);
    }

{{< /highlight >}}