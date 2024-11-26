---
title: Aspose.PSD for Java 20.2 - 릴리스 노트
type: docs
weight: 20
url: /ko/java/aspose-psd-for-java-20-2-release-notes/
---

{{% alert color="primary" %}} 이 페이지에는 [Aspose.PSD for Java 20.2](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.2/)의 릴리스 노트가 포함되어 있습니다. {{% /alert %}}

|**키**|**요약**|**범주**|
| :- | :- | :- |
|PSDJAVA-96|텍스트 레이어에서 다른 색상 텍스트 렌더링 능력 개선|기능|
|PSDJAVA-97|clbl 리소스 지원 (레이어 리소스에 블렌드 클리핑 요소 정보 포함)|기능|
|PSDJAVA-100|blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터 포함)|기능|
|PSDJAVA-101|Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 레이어 그룹 내보내기 능력|기능|
|PSDJAVA-105|lspf 리소스 지원 (레이어 보호 설정에 대한 설정 포함)|기능|
|PSDJAVA-106|infx 리소스 지원 (내부 요소 블렌딩에 대한 데이터 포함)|기능|
|PSDJAVA-99|PsdImage 및 Layer의 리팩토링을 통한 변형 동작 변경 (하나의 레이어를 별도로 변형시 레이어 마스크에 대한 올바른 크기 조정/회전/자르기)|향상|
|PSDJAVA-98|일부 전역 설정에서 AI 이미지 래스터 이미지를 열 수 없는 문제|버그|
|PSDJAVA-102|레이어에 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없어지는 문제|버그|
|PSDJAVA-103|PSD 파일 로드 중 System.ArgumentException 발생|버그|
|PSDJAVA-104|레이어에 대해 변형 메서드를 사용한 후 저장된 레이어의 올바르지 않은 바운드나 마스크|버그|

# **공개 API 변경사항**
# **이 API는 일시적으로 비활성화되었으며 다음 릴리스에서 켜질 것입니다:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.생성자(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.생성자(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.saveData(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.생성자(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)

` `**적합한 종속성이 있는 경우 v19.4를 사용하십시오.**
# **추가된 API:**
- M:com.aspose.psd.Color.op_Equality(com.aspose.psd.Color,com.aspose.psd.Color)
- M:com.aspose.psd.Color.op_Inequality(com.aspose.psd.Color,com.aspose.psd.Color)
- ...
- (API 추가 내용 생략)

## **제거된 API:**
- F:com.aspose.psd.xmp.types.derived.RenditionClass.DefinedValues
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- ...
- (API 제거 내용 생략)

# **사용 예시:**
**PSDJAVA-96. 텍스트 레이어에서 다른 색상 텍스트 렌더링 능력 향상**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-97. clbl 리소스 지원 (레이어 리소스에 블렌드 클리핑 요소 정보 포함)**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-100. blwh 리소스 지원 (블랙 & 화이트 조정 레이어 데이터 포함)**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**(나머지 내용들도 위와 같이 한국어로 번역)****PSDJAVA-101. Jpeg/Png/Tiff/Gif/Bmp/Jpeg2000/Psd/Psb/Pdf로 레이어 그룹 내보내기 능력**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-105. lspf 리소스 지원 (레이어 보호 설정에 대한 설정 포함)**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-106. infx 리소스 지원 (내부 요소 블렌딩에 대한 데이터 포함)**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-99. PsdImage 및 Layer의 리팩토링을 통한 변형 동작 변경 (하나의 레이어를 별도로 변형시 레이어 마스크에 대한 올바른 크기 조정/회전/자르기)**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-98. 일부 전역 설정에서 AI 이미지 래스터 이미지를 열 수 없는 문제**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-102. 레이어에 FlipRotate 작업을 수행한 후 PSD 이미지가 읽을 수 없어지는 문제**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-103. PSD 파일 로드 중 System.ArgumentException 발생**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}

**PSDJAVA-104. 레이어에 대해 변형 메서드를 사용한 후 저장된 레이어의 올바르지 않은 바운드나 마스크**

{{< highlight java >}}
    // 코드 내용
{{< /highlight >}}