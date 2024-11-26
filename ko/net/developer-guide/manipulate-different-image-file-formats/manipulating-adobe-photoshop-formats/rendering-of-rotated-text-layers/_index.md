---
title: 회전된 텍스트 레이어의 렌더링
type: docs
weight: 40
url: /ko/net/rendering-of-rotated-text-layers/
---

## **회전된 텍스트 레이어의 렌더링**
Aspose.PSD는 회전된 텍스트 레이어의 렌더링 기능을 제공합니다. 아래 예에서는 PSD 파일이 이미지 클래스의 정적 Load 메서드에 파일 경로를 전달하여 로드됩니다. 이제 [PsdImage](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage) 인스턴스의 [Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) 메서드를 호출합니다.

다음 코드 조각은 회전된 [텍스트 레이어](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer)를 렌더링하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenderingOfRotatedTextLayer-RenderingOfRotatedTextLayer.cs" >}}
## **회전된 벡터 마스크 및 텍스트 레이어**
Aspose.PSD는 벡터 마스크와 텍스트 레이어를 회전하는 기능을 제공합니다. Aspose.PSD는 벡터 마스크와 텍스트 레이어를 회전하기 위해 RotateFlip 메서드를 노출하였습니다. 레이어를 회전하는 단계는 아래와 같이 간단합니다:

- Image 클래스가 노출하는 Load 팩토리 메서드를 사용하여 PSD 파일을 이미지로 로드합니다.
- 필요한 [RotateFlipType](https://reference.aspose.com/psd/net/aspose.psd/rotatefliptype)를 설정합니다.
- [RotateFlip](https://reference.aspose.com/psd/net/aspose.psd/image/methods/rotateflip) 메서드를 호출합니다.
- 결과를 저장합니다.

다음 코드 조각은 벡터 마스크와 텍스트 레이어를 회전하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfRotateLayer-SupportOfRotateLayer.cs" >}}
