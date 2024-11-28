---
title: Aspose.PSD for Java 19.4 - 릴리스 노트
type: docs
weight: 20
url: /ko/java/aspose-psd-for-java-19-4-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 Aspose.PSD for Java 19.4의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

|**키**|**요약**|**카테고리**|
| :- | :- | :- |
|PSDJAVA-1|JPEG/PNG 등 이미지 파일을 직접 로드하지 않고 PsdImage로 로드하는 기능 추가(Aspose.PSD에서 지원하지 않음)|기능|
|PSDJAVA-2|RGB 색상 모드 지원(채널당 16비트, 각 색상당 64비트)|기능|
|PSDJAVA-3|레이어 벡터 마스크 및 텍스트 레이어 사용자 지정 회전/뒤집기 지원|기능|
|PSDJAVA-4|모든 아시아 문자가 제대로 렌더링되지 않음|버그|
|PSDJAVA-5|\r\n 기호가 잘못 해석되어 이중 줄 바꿈으로 해석됨|버그|
|PSDJAVA-6|라인 브레이크를 포함하는 문자열로 텍스트 레이어를 업데이트하면 PSD 파일이 읽을 수 없게 됨|버그|
|PSDJAVA-7|탭 기호가 포함된 문자열로 텍스트 레이어를 업데이트하면 처리가 예외로 실패함|버그|
# **퍼블릭 API 변경**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **제거된 API:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
(중략)
# **사용 예시:**

**PSDJAVA-1. JPEG/PNG 등 이미지 파일을 PsdImage로 직접 로드하는 기능 추가(Aspose.PSD에서 지원하지 않음)**

{{< highlight java >}}

(중략)

{{< /highlight >}}

(이하 생략)