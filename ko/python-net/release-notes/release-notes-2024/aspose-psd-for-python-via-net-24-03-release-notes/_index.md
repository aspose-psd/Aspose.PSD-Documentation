---
title: Aspose.PSD for Python via .NET 24.3 - 릴리스 노트
type: docs
weight: 10
url: /ko/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**      | **개요**                                                          | **카테고리**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI 형식] 대형 다중페이지 AI 이미지의 로딩 시간 감소         | 개선 |
| PSDPYTHON-45 | 8 비트에서 16 비트로 변환한 PSD 파일이 읽을 수 없게 되었습니다 |     버그     |
| PSDPYTHON-46 | 8 비트에서 32 비트로 변환한 PSD 파일이 읽을 수 없게 되었습니다 |     버그     |
| PSDPYTHON-47 | [AI 형식] AI 파일에서 Short Curve 렌더링 수정                 |     버그     |



## **공개 API 변경사항**
# **추가된 API:**
- 없음

# **제거된 API:**
- 없음


## **사용 예시:**

**PSDPYTHON-42. [AI 형식] 대형 다중페이지 AI 이미지의 로딩 시간 감소**

{{< highlight python >}}
   # 샘플 없음
{{< /highlight >}}

**PSDPYTHON-45. 8 비트에서 16 비트로 변환한 PSD 파일이 읽을 수 없게 되었습니다**

{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(outputFile, psdOptions16)

        with PsdImage.load(outputFile) as image:
            psdImage16 = cast(PsdImage, image)

            testResource = as_of(psdImage16.global_layer_resources[5], Lr16Resource)
            if testResource is not None:
                # is ok
                pass
            else:
                raise Exception("잘못된 글로벌 리소스, 첫 번째 리소스는 Lr16Resource여야 합니다")
{{< /highlight >}}

**PSDPYTHON-46. 8 비트에서 32 비트로 변환한 PSD 파일이 읽을 수 없게 되었습니다**


{{< highlight python >}}
        sourceFile = "test_smart_layer.psd"
        outputFile = "export.psd"

        with PsdImage.load(sourceFile) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(outputFile, psdOptions32)

        with PsdImage.load(outputFile) as image:
            psdImage32 = cast(PsdImage, image)

            testResource = as_of(psdImage32.global_layer_resources[5], Lr32Resource)
            if testResource is not None:
                # is ok
                pass
            else:
                raise Exception("잘못된 글로벌 리소스, 첫 번째 리소스는 Lr32Resource여야 합니다")
{{< /highlight >}}

**PSDPYTHON-47. [AI Format] AI 파일에서 Short Curve 렌더링 수정**

{{< highlight python >}}
        sourceFile = "shortCurve.ai"
        outputFilePath = "shortCurve.png"

        with AiImage.load(sourceFile) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}
