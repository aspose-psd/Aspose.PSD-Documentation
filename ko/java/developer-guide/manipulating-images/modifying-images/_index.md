---
title: 이미지 수정
type: docs
weight: 50
url: /ko/java/modifying-images/
---

## **러스터 이미지에 대한 디더링**
디더링은 실제로 이미지를 생성하는 점의 패턴을 변화시킴으로써 새로운 색상과 음영의 환상을 만들어내는 기술입니다. 이미지의 색상 범위를 256(또는 그 이하) 가지로 줄이는 가장 흔한 수단입니다. Aspose.PSD는 Dither 메서드를 소개하여 RasterImage 클래스에 대한 디더링 지원을 제공합니다. 이 메서드는 두 개의 매개변수를 받습니다. 첫 번째는 FloydSteinbergDithering 및 ThresholdDithering 두 가지 옵션 중 하나가 적용될 DitheringMethod 유형입니다. Dither 메서드의 두 번째 매개변수는 정수 형식의 BitCount입니다. BitCount는 디더링 결과의 샘플링 크기를 정의합니다. 기본 값은 흑백을 나타내는 1이며, 허용되는 값은 각각 2, 4 및 256개의 색상을 생성하는 1, 4, 8입니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **밝기, 대조 및 감마 조정**
디지털 이미지에서의 색상 조정은 대부분의 이미지 처리 라이브러리가 제공하는 핵심 기능 중 하나입니다. 색상 조정은 다음과 같이 분류할 수 있습니다.

1. 밝기는 색상의 밝고 어두움을 나타냅니다. 이미지의 밝기를 높이면 모든 색상이 밝아지고, 밝기를 감소시키면 모든 색상이 어두워집니다.
1. 대조는 이미지 내 개체 또는 세부사항을 더 명확하게 만드는 것을 의미합니다. 이미지의 대비를 높이면 빛과 어두운 영역 사이의 차이가 증가하여 빛나는 영역이 더 밝아지고 어두운 영역이 더 어두워집니다. 대비를 줄이면 더 밝은 영역과 더 어두운 영역이 대략적으로 동일해지지만 전반적인 이미지가 더 균일해집니다.
1. 감마는 이미지에서 개체를 조명하는 간접 광 조명의 대비와 밝기를 최적화합니다.
### **밝기 조정**
Aspose.PSD for Java API는 이미지의 밝기를 조절하는 데 사용할 수 있는 RasterImage 클래스의 AdjustBrightness 메서드를 제공합니다. 매개변수로 정수 값을 전달하여 이미지 밝기를 조절할 수 있습니다. 더 높은 매개변수 값은 더 밝은 이미지를 나타냅니다. 여기에는 원본 이미지와 비교를 위한 조정된 이미지가 있습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **대비 조정**
RasterImage 클래스가 노출한 AdjustContrast 메서드를 사용하여 이미지의 대비를 조절할 수 있습니다. 매개변수로 float 값을 전달함으로써 이미지의 대비를 조절할 수 있습니다.

최고 매개변수 값은 주어진 이미지에서 더 높은 대비를 나타냅니다. 여기에는 원본 이미지와 비교를 위한 조정된 이미지가 있습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **감마 조정**
RasterImage 클래스가 노출한 AdjustGamma 메서드에는 두 가지 버전이 있습니다. 오버로드 중 하나는 하나의 float 값을 수용하고 빨강, 파랑 및 녹색 채널 계수에 대한 감마 보정을 수행합니다. 반면 다른 오버로드는 각 색상 계수를 개별적으로 나타내는 세 개의 float 매개변수를 수용합니다. 다음 코드 예제는 이미지에서 AdjustGamma를 수행하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **이미지 블러 처리**
이 문서는 이미지에 블러 효과를 적용하는 방법을 보여줍니다. Aspose.PSD API는이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 메서드를 노출시켰습니다. Aspose.PSD for Java는 이미지의 블러 효과를 만들기 위해 GaussianBlurFilterOptions 클래스를 노출했습니다. GaussianBlurFilterOptions 클래스는 이미지에 블러 효과를 만들기 위해 반지름과 시그마 값을 필요로 합니다. 리사이징을 수행하는 단계는 아래와 같이 간단합니다:

1. Image 클래스가 노출하는 Load 팩토리 메서드를 사용하여 이미지를 로드합니다.
1. 이미지를 RasterImage로 변환합니다.
1. GaussianBlurFilterOptions 클래스의 기본 생성자를 사용하거나 생성자에서 반지름 및 시그마 값을 제공합니다.
1. GaussianBlurFilterOptions 클래스 인스턴스와 사각형을 이미지 경계로 지정하면서 RasterImage.Filter 메서드를 호출합니다.
1. 결과를 저장합니다.

다음 코드 예제는 이미지에 블러 효과를 만드는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **이미지 투명성 확인**
이 문서는 이미지 투명성을 확인하기 위해 Aspose.PSD for Java를 사용하는 방법을 보여줍니다. 이미지의 투명성을 확인하는 단계는 다음과 같이 간단합니다:

1. Image 클래스가 노출하는 Load 팩토리 메서드를 사용하여 이미지를 로드합니다.
1. 이미지 불투명도를 확인하고 불투명도가 0이면 이미지가 투명한 것입니다.
1. 다음 코드 예제는 이미지가 투명한지 여부를 확인하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **손실 압축 GIF 컴프레서 구현**
Aspose.PSD for Java를 사용하면 개발자가 픽셀 차이를 설정할 수 있습니다. GIF의 압축은 이미지 내 픽셀 문자열 "사전"에 기반합니다. 일반 인코더는 이미지에서 정확히 일치하는 픽셀 문자열 중 가장 긴 문자열을 사전에서 찾습니다. 손실 압축기는 이미지의 픽셀과 "충분히 유사한" 가장 긴 픽셀 문자열을 선택합니다. 아래는 해당 기능의 코드 안내입니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **바이큐빅 리샘플링 구현**
리샘플링은 이미지의 픽셀 차원을 변경하는 것을 의미합니다. 다운샘플링하는 경우 픽셀을 제거하고 이미지에서 정보와 세부 사항을 삭제합니다. 업샘플링하는 경우 픽셀을 추가합니다. Photoshop은 보간을 사용하여이러한 픽셀을 추가합니다. 이 문서는 Aspose.PSD for Java를 사용하여 바이큐빅 리샘플링을 수행하는 방법을 보여줍니다.

아래는 해당 기능의 코드 안내입니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **색상 반전 조정 레이어**
이 문서는 Aspose.PSD for Java를 사용하여 **색상 반전 조정 레이어**를 수행하는 방법을 보여줍니다. 조정 레이어는 대부분 색상 보정을 위해 사용되는 특수한 종류의 레이어입니다. 자신의 콘텐츠를 갖는 대신에 그 아래의 레이어에서 정보를 조정합니다. 색상 반전 조정 레이어는 이미지의 색상을 반전시켜 사진 부정 효과를 만듭니다.

아래는 해당 기능의 코드 안내입니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}

