---
title: Aspose.PSD에서 다른 색상 모드 간 변환
type: docs
weight: 50
url: /ko/net/psd-convert-between-different-color-modes/
---

이 문서에서 Aspose.PSD의 지원하는 색상 모드에 대해 알아볼 수 있습니다.

예를 들어, Aspose.PSD는 8에서 16비트 픽셀로의 변환과 그 반대 변환을 지원합니다. CMYK ICC-프로필 변환 및 다른 비트 깊이 유형으로의 대화식 변환도 가능합니다. 여기에서는 PSD 파일에서 그레이스케일로 변환하는 방법의 예시를 볼 수 있습니다.

## **CMYK, RGB, 그레이스케일에서 그레이스케일 색상 모드로 변환하기**
다음 샘플 코드는 포토샵을 사용하지 않고 CMYK, RGB 또는 그레이스케일 변환을 하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdImage-Saving16BitGrayscalePsdImage.cs" >}}

## **16비트 포토샵 이미지를 8비트 그레이스케일 모드로 변환하기**
하지만 16비트 그레이스케일 포토샵 이미지를 8비트 그레이스케일 모드로 변환해야 할 경우 어떻게 할까요? 다음 코드 스니펫을 사용해야 합니다. 8비트는 PSD 파일에서 흔한 비트 깊이입니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitGrayscale-Saving16BitGrayscalePsdTo8BitGrayscale.cs" >}}

## **그레이스케일을 RGB로 변환하기**
다른 복잡한 경우는 그레이스케일 PSD 이미지를 RGB 이미지로 변환해야 할 때입니다.

그레이스케일 이미지는 채널이 하나뿐이지만, RGB 이미지는 R(빨강), G(초록), B(파랑) 세 가지 채널이 있습니다. Aspose.PSD는 그레이스케일을 RGB로 변환할 수 있습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-Saving16BitGrayscalePsdTo8BitRgb-Saving16BitGrayscalePsdTo8BitRgb.cs" >}}
