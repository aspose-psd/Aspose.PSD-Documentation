---
title: 이미지 수정
type: 문서
weight: 50
url: /ko/net/modifying-images/
---

## **래스터 이미지에 대한 디더링**
디더링은 실제 이미지를 생성하는 점의 패턴을 다르게하여 새로운 색상과 음영의 환상을 만드는 기술입니다. 이미지의 색상 범위를 256(또는 그 이하) 색상으로 줄이는 가장 일반적인 수단입니다. Aspose.PSD는 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스에 디더링 지원을 제공하며 FloydSteinbergDithering 및 ThresholdDithering 두 가지 옵션이 있는 DitheringMethod 유형의 매개 변수를 허용하는 Dither 메서드를 소개합니다. [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) 메서드의 두 번째 매개 변수는 정수형의 BitCount입니다. BitCount는 디더링 결과의 샘플링 크기를 정의합니다. 기본값은 흑백을 나타내는 1이며, 허용되는 값은 각각 2, 4 및 256개의 색상이 있는 팔레트를 생성하는 1, 4, 8입니다.

## **밝기, 대비 및 감마 조절**
디지털 이미지의 색상 조정은 대부분의 이미지 처리 라이브러리에서 제공하는 핵심 기능 중 하나입니다. 색상 조정은 다음과 같이 분류할 수 있습니다.

1. 밝기는 색상의 밝기 또는 어둡기를 나타냅니다. 이미지의 밝기를 높이면 모든 색상이 밝아지고, 밝기를 낮추면 모든 색상이 어두워집니다.
1. 대비는 이미지 내의 물체 또는 세부 사항을 더욱 분명하게 만드는 것을 의미합니다. 이미지의 대비를 높이면 밝고 어두운 영역 간의 차이가 커져서 밝은 영역이 더 밝고 어두운 영역이 더 어둡게 됩니다. 대비를 낮추면 밝은 영역과 어두운 영역이 대략 동일하지만 전체 이미지가 더 균일해집니다.
1. 감마는 이미지의 물체를 조명하는 간접 조명의 대조와 밝기를 최적화합니다.

### **밝기 조절**
Aspose.PSD for .NET API는 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스에 대한 이미지 밝기 조절을 위한 [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) 메서드를 제공하며 매개 변수로 정수 값을 전달하여 이미지 밝기를 조절할 수 있습니다. 가장 높은 매개 변수 값은 더 밝은 이미지를 나타냅니다. 여기에는 원본 이미지와 비교를 위한 결과 이미지가 포함되어 있습니다.

### **대비 조절**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스에서 노출된 [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) 메서드를 사용하여 이미지의 대비를 조정할 수 있습니다. 이는 매개 변수로 float 값을 전달하여 이미지의 대비를 조절하는 데 사용됩니다.

### **감마 조절**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스에서 노출된 [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) 메서드에는 두 가지 버전이 있습니다. 오버로드 중 하나는 하나의 float 값만 받아들이고 붉은색, 청색 및 녹색 채널 계수에 대한 감마 보정을 수행합니다. 다른 오버로드는 각 색상 계수를 개별적으로 나타내는 세 가지 float 매개 변수를 수용합니다. 다음 코드 예제는 이미지에서 AdjustGamma를 수행하는 방법을 보여줍니다.

## **이미지 흐리게하기**
이 문서는 이미지에 대한 흐림 효과를 수행하기 위해 Aspose.PSD for .NET을 사용하는 방법을 보여줍니다. Aspose.PSD API는이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 방법을 제공합니다. Aspose.PSD for .NET은 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 클래스를 공개하여 이미지에 흐림 효과를 만드는 방법을 제공합니다. [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 클래스는 이미지에서 흐리게 하는 데 필요한 반지름과 시그마 값을 필요로 합니다. Resize를 수행하는 단계는 다음과 같이 간단합니다:

1. Image 클래스가 노출하는 팩토리 메서드 Load를 사용하여 이미지를 로드합니다.
1. Image를 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)로 변환합니다.
1. 기본 생성자 또는 생성자에서 반지름 및 시그마 값을 제공하여 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) 클래스의 인스턴스를 작성합니다.
1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage)의 Filter 메서드를 호출하면서 사각형을 이미지 경계로 지정하고 [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd/imagefilters/filteroptions/gaussianblurfilteroptions) 클래스의 인스턴스를 지정합니다.
1. 결과를 저장합니다.

## **이미지 투명도 확인**
이 문서는 Aspose.PSD for .NET을 사용하여 이미지 투명도를 확인하는 방법을 보여줍니다. 이미지 투명도를 확인하는 단계는 다음과 같이 간단합니다:

1. Image 클래스가 노출하는 [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) 팩토리 메서드를 사용하여 이미지를 로드합니다.
1. 투명도가 제로이면 이미지가 투명합니다.
1. 다음 코드 예제는 이미지가 투명한지 여부를 확인하는 방법을 보여줍니다.

## **손실 GIF 압축기 구현**
Aspose.PSD for .NET을 사용하면 개발자가 픽셀 차이를 설정할 수 있습니다. GIF의 압축은 본질적으로 픽셀의 문자열 "사전"에 기반합니다. 일반 엔코더는 이미지의 픽셀과 정확히 일치하는 최장 픽셀 문자열을 사전에서 찾습니다. 손실 엔코더는 이미지의 픽셀과 "충분히 유사한" 가장 긴 픽셀 문자열을 선택합니다. 아래는 해당 기능의 코드 디모입니다.

## **바이큐빅 재샘플링 구현**
재샘플링은 이미지의 픽셀 차원을 변경하는 것을 의미합니다. 다운샘플링할 때는 픽셀을 제거하여 이미지에서 정보와 세부 사항을 삭제합니다. 업샘플링할 때는 픽셀을 추가합니다. 포토샵은 보간을 사용하여 이러한 픽셀을 추가합니다. 이 문서는 Aspose.PSD for .NET을 사용하여 바이큐빅 재샘플링을 수행하는 방법을 보여줍니다.

## **색상 밸런스 조정 레이어**
이 문서는 Aspose.PSD for .NET을 사용하여 이미지에 대한 **색상 밸런스 조정 레이어**를 수행하는 방법을 보여줍니다. 색상 밸런스 조정 레이어를 사용하면 이미지의 색조를 조절할 수 있습니다. 세 가지 색상 채널과 이에 상응하는 색상이 제시되며 이러한 쌍의 밸런스를 조절하여 사진의 외관을 변경할 수 있습니다.

## **반전 조정 레이어**
이 문서는 Aspose.PSD for .NET을 사용하여 **반전 조정 레이어**를 수행하는 방법을 보여줍니다. 조정 레이어는 대부분 색상 보정을 위해 사용되는 특수한 종류의 레이어이며, 그들 자체의 내용 대신에 하위 레이어의 정보를 조정합니다. 반전 조정 레이어는 이미지의 색상을 반전시켜 사진의 색상을 부정적으로 만듭니다.

