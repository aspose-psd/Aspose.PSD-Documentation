---
title: Stroke Effect With Color Fill
type: docs
weight: 60
url: /ko/net/stroke-effect-with-color-fill/
---

## **색 채우기 스트로크 효과**
이 문서에서는 색 채우기 스트로크 효과를 렌더하는 방법을 보여줍니다. 스트로크 효과는 레이어 및 모양에 테두리 및 외곽선을 추가하는 데 사용됩니다. 이를 사용하여 단색 선, 다채로운 그라데이션, 그리고 패턴이 있는 테두리를 만들 수 있습니다.

색 채우기 스트로크 효과를 렌더하는 단계는 다음과 같습니다:

- [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource) 속성 설정.
- [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions)를 정의하고 Image 클래스에 의해 노출된 Load 팩토리 메서드를 사용하여 PSD 파일을 이미지로 로드.
- [**ColorFillSetting**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings)의 설정 속성 설정.
- 결과 저장.

다음 코드 스니펫은 색 채우기 스트로크 효과를 렌더하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
