---
title: Aspose.PSD for Java 21.6 - 릴리스 노트
type: docs
weight: 40
url: /ko/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

|**키**|**개요**|**카테고리**|
| :- | :- | :- |
|PSDJAVA-351|그룹의 클리핑 마스크가 정확하게 렌더링되지 않음|버그|
|PSDJAVA-352|레이어 그룹의 일반 또는 벡터 마스크가 렌더링시 무시됨|버그|
|PSDJAVA-353|저장시 비활성화 된 벡터 레이어 마스크를 가진 PSD 이미지는 벡터 마스크를 활성화 함|버그|
|PSDJAVA-354|255자 이상의 텍스트를 포함하는 TextLayer를 생성할 때 예외 발생|버그|

# **공개 API 변경**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음

# **사용 예시:**

**PSDJAVA-351. 그룹의 클리핑 마스크가 정확하게 렌더링되지 않음**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. 레이어 그룹의 일반 또는 벡터 마스크가 렌더링시 무시됨**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. 저장 중 비활성화 된 벡터 레이어 마스크를 가진 PSD 이미지는 벡터 마스크를 활성화 함**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. 255자 이상의 텍스트를 포함하는 TextLayer를 생성할 때 예외 발생**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
