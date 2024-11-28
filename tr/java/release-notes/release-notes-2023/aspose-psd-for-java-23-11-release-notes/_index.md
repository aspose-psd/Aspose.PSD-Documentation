---
title: Aspose.PSD for Java 23.11 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-23-11-release-notes/
---

{{% alert color="primary" %}}Bu sayfa, [Aspose.PSD for Java 23.11](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.11/) için sürüm notlarını içermektedir.{{% /alert %}}

| **Anahtar**    | **Özet**                                                                                                | **Kategori** |
|:---------------|:--------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-551    | LMskResource'un Desteklenmesi                                                                          |    Özellik   |
| PSDJAVA-552    | [AI Format] PDF tabanlı AI dosyasının Aspose.PSD ile işlenme yeteneğinin eklenmesi                      |    Özellik   |
| PSDJAVA-553    | [AI Format] 'cm' PostScript işlemcisine destek eklenmesi                                              |    Özellik   |
| PSDJAVA-554    | Yeni eğim türlerinin eklenmesi: Dalga, üst kabuk, alt kabuk                                           |    Özellik   |
| PSDJAVA-555    | Dikey eğim desteğinin eklenmesi                                                                       |    Özellik   |
| PSDJAVA-556    | TextLayer.GetFonts() çağrısında 'Anahtar' parametresi için 'Değer boş olamaz. (Parametre 'anahtar')' System.ArgumentNullException hatası |      Hata     |

## **Halka Açık API Değişiklikleri**
# **Eklenen API'lar:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent1
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent2
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent4
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorSpace
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getFlag
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent1(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent2(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent3(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent4(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorSpace(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setOpacity(short)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.TypeToolKey
- T:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.CMYK
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.GrayScale
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.HSB
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.Lab
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB

# **Kaldırılan API'lar:**

- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **Kullanım örnekleri:**

** PSDJAVA-551. LMskResource'un Desteklenmesi**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/sourceFile.psd";
        String outputPsd = "src/main/resources/sourceFile_output.psd";

        // 16-bit görüntü yükle.
        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            // LmskResource'u bul.
            LmskResource lmskResource = new LmskResource();
            for (LayerResource res : image.getGlobalLayerResources()) {
                if (res instanceof LmskResource) {
                    lmskResource = (LmskResource) res;
                    break;
                }
            }

            // LmskResource özelliklerini kontrol et.
            assertAreEqual(lmskResource.getColorSpace(), ColorSpace.RGB);
            assertAreEqual(lmskResource.getColorComponent1(), 65535);
            assertAreEqual(lmskResource.getColorComponent2(), 0);
            assertAreEqual(lmskResource.getColorComponent3(), 0);
            assertAreEqual(lmskResource.getColorComponent4(), 0);
            assertAreEqual(lmskResource.getOpacity(), (short) 45);
            assertAreEqual(lmskResource.getFlag(), (byte) 128);

            // LmskResource özelliklerini değiştir.
            lmskResource.setColorSpace(ColorSpace.HSB);
            lmskResource.setColorComponent1(7854);
            lmskResource.setColorComponent2(10);
            lmskResource.setColorComponent3(15484);
            lmskResource.setOpacity((short) 85);

            // Görüntüyü kaydet.
            image.save(outputPsd);
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

** PSDJAVA-552. [AI Format] PDF tabanlı AI dosyasının Aspose.PSD ile işlenme yeteneğinin eklenmesi**

{{< highlight java >}}

    String sourceFile = "src/main/resources/ai_one.ai";
    String outputPng = "src/main/resources/ai_one_output.psd";

    // PDF tabanlı AI görüntüsünü yükle.
    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        // AI görüntüsünü PNG görüntüsü olarak kaydet.
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}

** PSDJAVA-553. [AI Format] 'cm' PostScript işlemcisine destek eklenmesi**

{{< highlight java >}}

    String sourceFile = "src/main/resources/ai_two.ai";
    String outputPng = "src/main/resources/ai_two_output.png";

    // AI görüntüsünü yükle.
    try (AiImage image = (AiImage)Image.load(sourceFile)) {
        // AI görüntüsünü PNG olarak kaydet.
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}


** PSDJAVA-554. Yeni eğim türlerinin eklenmesi: Dalga, üst kabuk, alt kabuk**

{{< highlight java >}}

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setAllowWarpRepaint(true);
    loadOptions.setLoadEffectsResource(true);

    PngOptions saveOptions = new PngOptions();
    saveOptions.setColorType(PngColorType.TruecolorWithAlpha);

    String sourceFileFish = "src/main/resources/1752_warp_fish.psd";
    String sourceFileRise = "src/main/resources/1752_warp_rise.psd";
    String sourceFileWave = "src/main/resources/1752_warp_wave.psd";

    String outputFileFish = "src/main/resources/1752_output_fish.png";
    String outputFileRise = "src/main/resources/1752_output_rise.png";
    String outputFileWave = "src/main/resources/1752_output_wave.png";

    try (PsdImage psdImage = (PsdImage)Image.load(sourceFileFish, loadOptions)) {
        psdImage.save(outputFileFish, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage)Image.load(sourceFileRise, loadOptions)) {
        psdImage.save(outputFileRise, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage)Image.load(sourceFileWave, loadOptions)) {
        psdImage.save(outputFileWave, saveOptions);
    }

{{< /highlight >}}


** PSDJAVA-555. Dikey eğim desteğinin eklenmesi**

{{< highlight java >}}

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setAllowWarpRepaint(true);
    loadOptions.setLoadEffectsResource(true);

    PngOptions saveOptions = new PngOptions();
    saveOptions.setColorType(PngColorType.TruecolorWithAlpha);

    String sourceFileArcLower = "src/main/resources/1797_warp_arc_lower_v.psd";
    String sourceFileArcUpper = "src/main/resources/1797_warp_arc_upper_v.psd";
    String sourceFileArch = "src/main/resources/1797_warp_arch_v.psd";
    String sourceFileBulge = "src/main/resources/1797_warp_bulge_v.psd";
    String sourceFileFlag = "src/main/resources/1797_warp_flag_v.psd";
    String sourceFileFish = "src/main/resources/1797_warp_fish_v.psd";
    String sourceFileRise = "src/main/resources/1797_warp_rise_v.psd";
    String sourceFileWave = "src/main/resources/1797_warp_wave_v.psd";

    String outputFileArcLower = "src/main/resources/1797_warp_arc_lower_v.png";
    String outputFileArcUpper = "src/main/resources/1797_warp_arc_upper_v.png";
    String outputFileArch = "src/main/resources/1797_warp_arch_v.png";
    String outputFileBulge = "src/main/resources/1797_warp_bulge_v.png";
    String outputFileFlag = "src/main/resources/1797_warp_flag_v.png";
    String outputFileFish = "src/main/resources/1797_output_fish_v.png";
    String outputFileRise = "src/main/resources/1797_output_rise_v.png";
    String outputFileWave = "src/main/resources/1797_output_wave_v.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcLower, loadOptions)) {
        psdImage.save(outputFileArcLower, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcUpper, loadOptions)) {
        psdImage.save(outputFileArcUpper, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArch, loadOptions)) {
        psdImage.save(outputFileArch, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileBulge, loadOptions)) {
        psdImage.save(outputFileBulge, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileFlag, loadOptions)) {
        psdImage.save(outputFileFlag, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileFish, loadOptions)) {
        psdImage.save(outputFileFish, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileRise, loadOptions)) {
        psdImage.save(outputFileRise, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileWave, loadOptions)) {
        psdImage.save(outputFileWave, saveOptions);
    }

{{< /highlight >}}


** PSDJAVA-556. TextLayer.GetFonts() çağrısında 'Anahtar' boş olamaz. (Parametre 'anahtar')' System.ArgumentNullException hatası**

{{< highlight java >}}

    String src = "src/main/resources/SimpleText.psd";

    FontSettings.removeFontCacheFile();

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getFonts();
            }
        }
    }

{{< /highlight >}}