---
title: 이미지에 워터마크 추가하기
type: docs
weight: 20
url: /ko/java/adding-a-watermark-to-an-image/
---

## **이미지에 워터마크 추가하기**
이 문서에서는 Aspose.PSD를 사용하여 이미지에 워터마크를 추가하는 방법에 대해 설명합니다. 이미지에 워터마크를 추가하는 것은 이미지 처리 애플리케이션에서 흔한 요구 사항입니다. 이 예제는 Graphics 클래스를 사용하여 이미지 표면에 문자열을 그리는 방법을 보여줍니다.
### **워터마크 추가하기**
작업을 설명하기 위해 디스크에서 BMP 이미지를 로드하고 Graphics 클래스의 DrawString 메서드를 사용하여 이미지 표면에 워터마크로 문자열을 그릴 것입니다. PngOptions 클래스를 사용하여 이미지를 PNG 형식으로 저장할 것입니다. 아래는 이미지에 워터마크를 추가하는 방법을 보여주는 코드 예제입니다. 예제 소스 코드는 쉽게 따를 수 있도록 여러 부분으로 분할되어 있습니다. 단계별로 예제는 다음을 보여줍니다:

1. 이미지 로드
1. Graphics 객체 생성 및 초기화
1. Font 및 SolidBrush 객체 생성 및 초기화
1. Graphics 클래스의 DrawString 메서드를 사용하여 워터마크로 문자열 그리기
1. PNG로 이미지 저장

다음 코드 조각은 이미지에 워터마크를 추가하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.java" >}}
### **대각선 방향 워터마크 추가하기**
이미지에 대각선 워터마크를 추가하는 것은 위에서 설명한 수평 워터마크를 추가하는 것과 유사하지만 몇 가지 차이가 있습니다. 작업을 설명하기 위해 디스크에서 JPG 이미지를 로드하고 Matrix 클래스의 객체를 사용하여 변환을 추가하고 Graphics 클래스의 DrawString 메서드를 사용하여 이미지 표면에 워터마크로 문자열을 그릴 것입니다. 아래는 이미지에 대각선 워터마크를 추가하는 방법을 보여주는 코드 예제입니다. 예제 소스 코드는 쉽게 따를 수 있도록 여러 부분으로 분할되어 있습니다. 단계별로 예제는 다음을 보여줍니다:

1. 이미지 로드
1. Graphics 객체 생성 및 초기화
1. Font 및 SolidBrush 객체 생성 및 초기화
1. SizeF 객체에 이미지 크기 가져오기
1. Matrix 클래스의 인스턴스 생성 및 복합 변환 수행
1. 변환을 Graphics 객체에 할당
1. StringFormat 객체 생성 및 초기화
1. Graphics 클래스의 DrawString 메서드를 사용하여 워터마크로 문자열 그리기
1. 결과 이미지 저장

다음 코드 조각은 이미지에 대각선 워터마크를 추가하는 방법을 보여줍니다.





{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.java" >}}
