---
title: 중앙값 및 Wiener 필터 적용
type: 문서
weight: 10
url: /ko/net/applying-median-and-wiener-filters/
---

## **중앙값 및 Wiener 필터 적용**
중앙값 필터는 종종 노이즈를 제거하기 위해 사용되는 비선형 디지털 필터링 기술로, 노이즈 감소는 후속 처리 결과를 개선하기 위한 전형적인 전처리 단계입니다. Wiener 필터는 첨가 노이즈와 흐림에 의해 손상된 이미지에 대한 MSE(평균 제곱 오차) 최적 정상 선형 필터입니다. Aspose.PSD를 통해 .NET API 개발자는 이미지에서 노이즈를 제거하는 중앙값 필터를 적용하고 가우스 Wiener 필터를 이미지에 적용할 수 있습니다. 이 문서에서는 중앙값 필터와 가우스 Wiener 필터를 이미지에 적용하는 방법을 보여줍니다.
### **중앙값 필터 적용**
Aspose.PSD는 [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) 클래스를 제공하여 [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)에 필터를 적용합니다. 아래 제공된 코드 조각은 래스터 이미지에 중앙값 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **가우스 Wiener 필터 적용**
Aspose.PSD는 [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) 클래스를 제공하여 [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)에 필터를 적용합니다. 아래 제공된 코드 조각은 래스터 이미지에 가우스 Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **컬러 이미지에 대한 가우스 Wiener 필터 적용**
Aspose.PSD는 [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)를 컬러 이미지에도 제공합니다. 아래 제공된 코드 조각은 컬러 이미지에 가우스 Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **모션 Wiener 필터 적용**
Aspose.PSD는 [MotionWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) 클래스를 이용하여 [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage)에 필터를 적용합니다. 아래 제공된 코드 조각은 래스터 이미지에 모션 Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **이미지에 교정 필터 적용**
이 문서에서는 Aspose.PSD for .NET을 사용하여 이미지에 교정 필터를 적용하는 방법을 보여줍니다. Aspose.PSD API는 효율적이고 사용하기 쉬운 방법을 노출하여 이 목표를 달성할 수 있습니다. Aspose.PSD for .NET은 [BilateralSmoothingFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)와 [SharpenFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) 클래스를 노출하고 있습니다. BilateralSmoothingFilterOptions 클래스는 크기로 정수가 필요합니다. Resize를 수행하는 단계는 다음과 같습니다.

1. Image 클래스가 노출하는 factory 메소드 Load를 사용하여 이미지를 로드합니다.
1. 이미지를 RasterImage로 변환합니다.
1. BilateralSmoothingFilterOptions 및 SharpenFilterOptions 클래스의 인스턴스를 생성합니다.
1. RasterImage.Filter 메소드를 호출하면서 이미지 경계를 지정하고 BilateralSmoothingFilterOptions 클래스의 인스턴스를 지정합니다.
1. RasterImage.Filter 메소드를 호출하면서 이미지 경계를 지정하고 SharpenFilterOptions 클래스의 인스턴스를 지정합니다.
1. 명암을 조정합니다.
1. 밝기를 설정합니다.
1. 결과를 저장합니다.


## **Bradley 임계값 알고리즘 사용하기**
이미지 임계처리는 그래픽 애플리케이션에서 사용됩니다. 이미지의 임계값을 정의하고 Bradley 임계처리를 사용하는 방법을 Aspose.PSD API를 통해 가능합니다. 다음 코드 조각은 임계값을 정의하고 Bradley의 임계값 알고리즘을 호출하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
