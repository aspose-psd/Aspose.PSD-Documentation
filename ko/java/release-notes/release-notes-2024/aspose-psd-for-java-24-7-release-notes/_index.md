---
title: Aspose.PSD for Java 24.7 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} 이 페이지는 [Aspose.PSD for Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) 의 릴리스 노트를 포함합니다. {{% /alert %}}

| **키**        | **요약**                                                                                          | **카테고리** |
|:--------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635  | AI 문서를 열 때 "이미지 로드 실패." 예외 발생                                                | 버그         |
| PSDJAVA-636  | 출력 PDF 파일에서 텍스트가 잘못 렌더링 됨                                                  | 버그         |
| PSDJAVA-637  | 리눅스에서 주어진 파일에 대한 이미지 내보내기 실패 수정                                     | 버그         |
| PSDJAVA-638  | Aspose.Drawing 사용 시 폰트 로드 수정                                                       | 버그         |
| PSDJAVA-639  | 대용량 JPEG를 사용하여 스마트 객체 레이어를 생성할 때 "산술 연산이 오버플로우로 인해 결과가 발생했습니다" | 버그         |
| PSDJAVA-640  | AI 파일을 JPG 파일로 변환할 수 없음                                                         | 버그         |

## **공개 API 변경**
# **추가된 API:**

- 없음

# **제거된 API:**

- 없음

## **사용 예시:**

**PSDJAVA-635. AI 문서 열 때 "이미지 로드 실패." 예외 발생**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. 출력 PDF 파일에서 텍스트가 잘못 렌더링 됨**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. 리눅스에서 주어진 파일에 대한 이미지 내보내기 실패 수정**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Aspose.Drawing 사용 시 폰트 로드 수정**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- 업데이트 전 설치된 글꼴 수: " + installedFonts.getFamilies().length);
        System.out.println("- 플랫폼: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- 'Arial'에 대한 Adobe 글꼴 이름을 가져와서 글꼴 캐시를 새로고침합니다: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- 업데이트 후 설치된 글꼴 수: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 대용량 JPEG를 사용하여 스마트 객체 레이어를 생성할 때 "산술 연산이 오버플로우로 인해 결과가 발생했습니다"**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. AI 파일을 JPG 파일로 변환할 수 없음**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
