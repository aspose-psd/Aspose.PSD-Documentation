---
title: Median 및 Wiener 필터 적용
type: docs
weight: 10
url: /ko/java/applying-median-and-wiener-filters/
---

## **Median 및 Wiener 필터 적용**
중간값 필터는 종종 잡음을 제거하기 위해 사용되는 비선형 디지털 필터링 기술로, 이러한 잡음 감소는 후속 처리 결과를 향상시키기 위한 전처리 단계입니다. Wiener 필터는 첨가 잡음 및 흐림으로 손상된 이미지에 대해 MSE(평균 제곱 오차) 최적 정적 선형 필터입니다. Aspose.PSD for Java API 개발자는 중간값 필터를 적용하여 이미지의 잡음을 줄이고 이미지에 Gauss Wiener 필터를 적용할 수 있습니다. 이 문서에서는 중간값 필터와 Gauss Wiener 필터가 이미지에 적용되는 방법을 보여줍니다.

### **Median 필터 적용**
Aspose.PSD는 MedianFilterOptions 클래스를 제공하여 RasterImage에 필터를 적용합니다. 아래 제공된 코드 스니펫은 래스터 이미지에 중간값 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}

### **Gauss Wiener 필터 적용**
Aspose.PSD는 GaussWienerFilterOptions 클래스를 제공하여 RasterImage에 필터를 적용합니다. 아래 제공된 코드 스니펫은 래스터 이미지에 Gauss Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}

### **컬러 이미지에 Gauss Wiener 필터 적용**
Aspose.PSD는 컬러 이미지에 대한 GaussWienerFilterOptions도 제공합니다. 아래 제공된 코드 스니펫은 컬러 이미지에 Gauss Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}

### **모션 Wiener 필터 적용**
Aspose.PSD는 MotionWienerFilterOptions 클래스를 제공하여 RasterImage에 필터를 적용합니다. 아래 제공된 코드 스니펫은 래스터 이미지에 모션 Wiener 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}

## **이미지에 보정 필터 적용**
이 문서는 이미지에 보정 필터를 적용하는 Aspose.PSD for Java의 사용법을 보여줍니다. Aspose.PSD API는 효율적이고 쉽게 사용할 수 있는 방법을 제공하여 이 목표를 달성할 수 있습니다. Aspose.PSD for Java는 BilateralSmoothingFilterOptions 및 SharpenFilterOptions 클래스를 필터링 용으로 노출시켰습니다. BilateralSmoothingFilterOptions 클래스는 크기로 정수를 필요로 합니다. 리사이즈를 수행하는 단계는 아래와 같이 간단합니다:

1. Image 클래스에 의해 노출된 팩토리 메서드 Load를 사용하여 이미지를 불러옵니다.
1. 이미지를 RasterImage로 변환합니다.
1. BilateralSmoothingFilterOptions 및 SharpenFilterOptions 클래스의 인스턴스를 생성합니다.
1. RasterImage.Filter 메서드를 호출하면서 이미지 경계로 사각형을 지정하고 BilateralSmoothingFilterOptions 클래스 인스턴스를 지정합니다.
1. RasterImage.Filter 메서드를 호출하면서 이미지 경계로 사각형을 지정하고 SharpenFilterOptions 클래스 인스턴스를 지정합니다.
1. 대비를 조절합니다.
1. 밝기를 설정합니다.
1. 결과를 저장합니다.

다음 코드 스니펫은 보정 필터를 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}

## **Bradley 임계값 알고리즘 사용**
이미지의 임계값을 지정하는 것은 그래픽 애플리케이션에서 사용됩니다. 이미지의 임계값을 지정하는 목표는 픽셀을 "어두운" 또는 "밝은"으로 분류하는 것입니다. Aspose.PSD API를 사용하여 이미지를 변환하는 동안 Bradley 임계값을 사용할 수 있습니다. 아래 코드 스니펫은 임계값 값을 정의하고 Bradley's 임계값 알고리즘을 호출하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
