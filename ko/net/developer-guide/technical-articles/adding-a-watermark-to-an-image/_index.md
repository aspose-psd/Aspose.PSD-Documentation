---
title: 이미지에 워터마크 추가하기
type: docs
weight: 30
url: /ko/net/adding-a-watermark-to-an-image/
---

## **이미지에 워터마크 추가하기**
이 문서에서는 Aspose.PSD를 사용하여 이미지에 워터마크를 추가하는 방법을 설명합니다. 이미지에 워터마크를 추가하는 것은 이미지 처리 응용 프로그램에서 흔한 요구 사항입니다. 이 예제에서는 Graphics 클래스를 사용하여 이미지 표면에 문자열을 그리는 방법을 보여줍니다.

### **워터마크 추가**
작업을 표시하기 위해 디스크에서 BMP 이미지를로드하고 Graphics 클래스의 DrawString 메서드를 사용하여이미지 표면에 워터마크로 문자열을 그립니다. PngOptions 클래스를 사용하여 이미지를 PNG 형식으로 저장합니다. 아래는 이미지에 워터마크를 추가하는 방법을 보여주는 코드 예제입니다. 코드 예제는 쉽게 따르도록 여러 부분으로 나누어졌습니다. 예제는 다음과 같은 단계로 보여줍니다:

1. [이미지 로드](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2).
2. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 객체 생성 및 초기화.
3. 글꼴 및 [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush) 객체 생성 및 초기화.
4. Graphics 클래스 [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) 메서드를 사용하여 문자열을 워터마크로 그리기.
5. 이미지를 PNG로 저장.

다음 코드 조각은 이미지에 워터마크를 추가하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **대각선 워터마크 추가**
이미지에 대각선 워터마크를 추가하는 것은 위에서 설명한 수평 워터마크를 추가하는 것과 유사하지만 약간의 차이가 있습니다. 작업을 표시하기 위해 디스크에서 JPG 이미지를로드하고 [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) 클래스의 개체를 사용하여 변환을 추가하고 Graphics 클래스의 DrawString 메서드를 사용하여 이미지 표면에 워터마크로 문자열을 그립니다. 아래는 이미지에 대각선 워터마크를 추가하는 방법을 보여주는 코드 예제입니다. 코드 예제는 쉽게 이해할 수 있도록 여러 부분으로 나누어졌습니다. 예제는 다음과 같은 단계로 보여줍니다:

1. 이미지 로드.
2. Graphics 객체 생성 및 초기화.
3. 글꼴 및 SolidBrush 객체 생성 및 초기화.
4. [SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef) 객체에서 이미지 크기 가져오기.
5. Matrix 클래스의 인스턴스를 만들고 복합 변환을 수행합니다.
6. 변환을 Graphics 개체에 할당합니다.
7. [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat) 객체 생성 및 초기화.
8. Graphics 클래스의 DrawString 메서드를 사용하여 문자열을 워터마크로 그리기.
9. 결과 이미지 저장.

다음 코드 조각은 이미지에 대각선 워터마크를 추가하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
