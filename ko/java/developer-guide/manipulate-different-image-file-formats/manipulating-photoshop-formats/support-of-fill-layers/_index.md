---
title: 채우기 레이어 지원
type: docs
weight: 50
url: /ko/java/support-of-fill-layers/
---


## **색 채우기로 채우기 레이어 지원**
이 문서에서는 PSD 레이어를 색상으로 채우는 방법을 보여줍니다. Aspose.PSD.FileFormats.Psd.Layers.FillLayer를 사용하여 PSD 레이어에 색상을 추가하십시오. 다음 코드 스니펫은 PSD 파일을 로드하고 FillLayer 클래스에 액세스하여 FillLayer.FillSettings 속성을 사용하여 색상을 설정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **그라디언트 채우기로 채우기 레이어 지원**
이 문서에서는 PSD 레이어를 그라디언트로 채우는 방법을 보여줍니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 방법을 제공합니다. Aspose.PSD는 GradientColorPoint 및 GradientTransparencyPoint 클래스를 노출하여 레이어에 그라디언트 효과를 추가했습니다.

PSD 레이어를 그라디언트로 채우는 단계는 다음과 같습니다:

- Image 클래스에 의해 노출된 factory 메소드 Load를 사용하여 이미지로 PSD 파일을 로드합니다.
- FillLayer 객체의 설정 속성을 설정합니다.
- 필요한 색상 및 색상 위치로 ColorPoints 목록을 생성합니다.
- 필요한 불투명도와 불투명도 위치로 transparencyPoints 목록을 생성합니다.
- FillLayer.Update 메소드를 호출합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 PSD 레이어에 그라디언트 채우기를 추가하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **색 채우기로 스트로크 효과**
이 문서에서는 색 채우기로 스트로크 효과를 렌더링하는 방법을 보여줍니다. 스트로크 효과는 레이어 및 모양에 테두리를 추가하는 데 사용됩니다. 단색 선, 다채로운 그라디언트 및 패턴 테두리를 만드는 데 사용할 수 있습니다.

색 채우기로 스트로크 효과를 렌더링하는 단계는 다음과 같습니다:

- LoadEffectsResource 속성 설정.
- Image 클래스에 의해 노출된 factory 메소드 Load를 사용하여 이미지로 PSD 파일을 로드하고 PsdLoadOptions를 정의합니다.
- ColorFillSetting의 설정 속성을 설정합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 색 채우기로 스트로크 효과를 렌더링하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}


