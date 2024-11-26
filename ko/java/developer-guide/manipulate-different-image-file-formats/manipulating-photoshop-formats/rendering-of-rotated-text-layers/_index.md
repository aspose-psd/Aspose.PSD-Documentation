---
title: 회전된 텍스트 레이어의 렌더링
type: docs
weight: 30
url: /ko/java/rendering-of-rotated-text-layers/
---

## **회전된 텍스트 레이어의 렌더링**
Aspose.PSD는 회전된 텍스트 레이어의 렌더링 기능을 제공합니다. 아래 예제에서는 기존 PSD 파일을 이미지 클래스의 정적 Load 메서드에 파일 경로를 전달하여 로드합니다. 이제 PsdImage 인스턴스의 Save 메서드를 호출합니다.

다음 코드 스니펫은 회전된 텍스트 레이어를 렌더링하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.java" >}}
## **회전된 벡터 마스크 및 텍스트 레이어**
Aspose.PSD는 회전된 벡터 마스크 및 텍스트 레이어를 회전시키는 기능을 제공합니다. Aspose.PSD는 벡터 마스크 및 텍스트 레이어를 회전시키기 위해 RotateFlip 메서드를 노출했습니다. 레이어를 회전하는 단계는 다음과 같이 간단합니다:

- Image 클래스가 노출하는 팩토리 메서드 Load를 사용하여 이미지로 PSD 파일을 로드합니다.
- 필요한 RotateFlipType을 설정합니다.
- RotateFlip 메서드를 호출합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 벡터 마스크 및 텍스트 레이어를 회전하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.java" >}}
