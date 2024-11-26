---
title: Aspose.PSD for Java 23.9 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/)에 대한 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

| **키**       | **개요**                                                                    | **카테고리** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | 새 조정 레이어에 대한 마스크 생성 구현                                    |    기능     |
| PSDJAVA-528 | 클립된 레이어 블렌딩 옵션으로 그룹 블렌딩 지원 추가                      |    기능     |
| PSDJAVA-529 | 16비트 색상 모드의 PSD 파일은 조정 레이어에 마스크를 적용하지 않음         |      버그    |
| PSDJAVA-530 | 텍스트 레이어에서 괄호가 잘못 렌더링됨                                 |      버그    |
| PSDJAVA-531 | 텍스트 레이어에서 스타일 업데이트를 할 수 없음                             |      버그    |
| PSDJAVA-532 | CMYK로 PSD 파일을 내보낸 후 내보낸 PSD에서 색상이 깨짐                     |      버그    |
| PSDJAVA-533 | 특정 PSB 파일이 "사각형에 공통 처리 영역이 없습니다"라는 예외를 발생      |      버그    |
| PSDJAVA-534 | 이미지 로드 실패 . OverflowException: 산술 작업으로 오버플로우 발생       |      버그    |

## **공개 API 변경**
# **추가된 API:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **제거된 API:**

- 없음

## **사용 예시:**

** PSDJAVA-527. 새 조정 레이어에 대한 마스크 생성 구현**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "객체가 동일하지 않습니다.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. 클립된 레이어 블렌딩 옵션으로 그룹 블렌딩 지원 추가**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-529. 16비트 색상 모드의 PSD 파일은 조정 레이어에 마스크를 적용하지 않음 **

{{< highlight java >}}
	String sourceFile = "src/main/resources/source.psd";
    String outputPng = "src/main/resources/current.png";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-530. 텍스트 레이어에서 괄호가 잘못 렌더링됨 **

{{< highlight java >}}
    String file = "src/main/resources/file1.psd";
    String output = "src/main/resources/output_1235.png";

    try (PsdImage psdImage = (PsdImage) Image.load(file)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getTextData().updateLayerData();

                PsdOptions imageOptions = new PsdOptions(psdImage);
                psdImage.save(output, imageOptions);
            }
        }
    }
{{< /highlight >}}


** PSDJAVA-531. 텍스트 레이어에서 스타일을 업데이트할 수 없음 **

{{< highlight java >}}
    String sourceFile = "src/main/resources/Example_FontSize.psd";
    String outputFile = "src/main/resources/output_Example_FontSize.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        TextLayer l1 = (TextLayer) psdImage.getLayers()[4];
        TextLayer l2 = (TextLayer) psdImage.getLayers()[5];

        ITextPortion[] textItems1 = l1.getTextData().producePortions(new String[]{"text1", "text2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion item : textItems1) {
            l1.getTextData().addPortion(item);
        }

        ITextPortion[] textItems2 = l2.getTextData().producePortions(new String[]{"text layer 1", "text layer 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion item : textItems2) {
            l2.getTextData().addPortion(item);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        psdImage.save(outputFile);
    }
{{< /highlight >}}


** PSDJAVA-532. CMYK로 PSD 파일을 내보낸 후 내보낸 PSD에서 색상이 깨짐 **

{{< highlight java >}}
    String sourceFile = "src/main/resources/canyon.psd";
    String outputFilePng = "src/main/resources/output_canyon.png";

    MemoryStream outputStream = new MemoryStream();

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        psdImage.save(outputStream.toOutputStream());
    }

    outputStream.setPosition(0);
    try (PsdImage psdImage = (PsdImage) Image.load(outputStream.toInputStream())) {
        psdImage.save(outputFilePng, new PngOptions());
    }

    outputStream.close();
{{< /highlight >}}


** PSDJAVA-533. 특정 PSB 파일이 "사각형에 공통 처리 영역이 없습니다"라는 예외를 발생 **

{{< highlight java >}}
    String input = "src/main/resources/1619_src.psb";
    String output = "src/main/resources/1619_output.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage img = (PsdImage) Image.load(input, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        img.save(output, pngOptions);
    }
{{< /highlight >}}


** PSDJAVA-534. 이미지 로드 실패 . OverflowException: 산술 작업으로 오버플로우 발생.**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage im = (PsdImage)PsdImage.load(sourceFile))
    {
        Layer layer = im.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)layer.getResources()[0];

        assertAreEqual("自定", grdmResource.getGradientName());
    }

}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "객체가 동일하지 않습니다.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}
