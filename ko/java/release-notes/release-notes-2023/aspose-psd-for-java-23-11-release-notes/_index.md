---
title: Aspose.PSD for Java 23.11 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-23-11-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 23.11](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.11/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

| **키**         | **요약**                                                                                                    | **카테고리** |
|:---------------|:-----------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-551    | LMskResource 지원                                                                                          |    기능     |
| PSDJAVA-552    | [AI 형식] PDF 기반 AI 파일을 렌더링할 수 있는 기능 추가                                                     |    기능     |
| PSDJAVA-553    | [AI 형식] "cm" PostScript 연산자 지원 추가                                                                  |    기능     |
| PSDJAVA-554    | 새로운 워프 유형 추가: Wave, shell up, shell down                                                           |    기능     |
| PSDJAVA-555    | 수직 워프 지원 추가                                                                                        |    기능     |
| PSDJAVA-556    | TextLayer.GetFonts() 호출시 'Value cannot be null. (Parameter 'key')' System.ArgumentNullException 발생        |      버그     |

## **공개 API 변경**
# **추가된 API:**

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

# **제거된 API:**

- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **사용 예시:**

** PSDJAVA-551. LMskResource 지원**

{{< highlight java >}}


    public static void main(String[] args) {
        String sourceFile = "src/main/resources/sourceFile.psd";
        String outputPsd = "src/main/resources/sourceFile_output.psd";

        // 16비트 이미지 로드
        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            // LmskResource 찾기
            LmskResource lmskResource = new LmskResource();
            for (LayerResource res : image.getGlobalLayerResources()) {
                if (res instanceof LmskResource) {
                    lmskResource = (LmskResource) res;
                    break;
                }
            }

            // LmskResource 속성 확인
            assertAreEqual(lmskResource.getColorSpace(), ColorSpace.RGB);
            assertAreEqual(lmskResource.getColorComponent1(), 65535);
            assertAreEqual(lmskResource.getColorComponent2(), 0);
            assertAreEqual(lmskResource.getColorComponent3(), 0);
            assertAreEqual(lmskResource.getColorComponent4(), 0);
            assertAreEqual(lmskResource.getOpacity(), (short) 45);
            assertAreEqual(lmskResource.getFlag(), (byte) 128);

            // LmskResource 속성 변경
            lmskResource.setColorSpace(ColorSpace.HSB);
            lmskResource.setColorComponent1(7854);
            lmskResource.setColorComponent2(10);
            lmskResource.setColorComponent3(15484);
            lmskResource.setOpacity((short) 85);

            // 이미지 저장
            image.save(outputPsd);
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "객체가 같지 않음.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}


** PSDJAVA-552. [AI 형식] PDF 기반 AI 파일을 Aspose.PSD로 렌더링하는 기능 추가**

{{< highlight java >}}


    String sourceFile = "src/main/resources/ai_one.ai";
    String outputPng = "src/main/resources/ai_one_output.psd";

    // PDF 기반 AI 이미지 로드
    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        // AI 이미지를 PNG 이미지로 저장
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}


** PSDJAVA-553. [AI 형식] "cm" PostScript 연산자 지원 추가 **

{{< highlight java >}}


    String sourceFile = "src/main/resources/ai_two.ai";
    String outputPng = "src/main/resources/ai_two_output.png";

    // AI 이미지 로드
    try (AiImage image = (AiImage)Image.load(sourceFile)) {
        // AI 이미지를 PNG 이미지로 저장
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}


** PSDJAVA-554. 새로운 워프 유형 추가: Wave, shell up, shell down **

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


** PSDJAVA-555. 수직 워프 지원 추가 **

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


** PSDJAVA-556. TextLayer.GetFonts() 호출시 'Value cannot be null. (Parameter 'key')' System.ArgumentNullException 발생 **

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