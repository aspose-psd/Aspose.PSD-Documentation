---
title: 이미지 변환
type: docs
weight: 20
url: /ko/java/converting-images/
---

## **이미지를 흑백 및 그레이 스케일로 변환**
가끔은 인쇄 또는 아카이빙 목적으로 컬러 이미지를 흑백 또는 그레이 스케일로 변환해야 할 수도 있습니다. 이 기사에서는 이를 위해 Aspose.PSD for Java API를 사용하여 아래에 설명된 두 가지 방법으로 이를 달성하는 방법을 보여줍니다.

- 이진화 (Binarization)
- 그레이 스케일링 (Grayscaling)

### **이진화 (Binarization)**
이진화의 개념을 이해하기 위해서는 이진 이미지를 정의하는 것이 중요합니다. 이진 이미지란 각 픽셀에 대해 두 가지만 가능한 값이 있는 디지털 이미지를 말합니다. 일반적으로 이진 이미지에 사용되는 두 색은 흑색과 흰색이지만 어떤 두 색상이든 사용할 수 있습니다. 이진화는 이미지를 이진 수준으로 변환하는 과정으로, 각 픽셀이 단일 비트(0 또는 1)로 저장되어 0은 색상이 없음을 나타내고 1은 색상이 존재함을 의미합니다. Aspose.PSD for Java API는 현재 두 가지 이진화 방법을 지원합니다.

#### **고정 임계값을 사용한 이진화**
다음 코드 조각은 고정 임계값 이진화를 이미지에 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}

#### **Otsu 임계값을 사용한 이진화**
다음 코드 조각은 Otsu 임계값 이진화를 이미지에 적용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}

### **그레이 스케일링 (Grayscaling)**
그레이 스케일링은 연속된 톤 이미지를 불연속한 회색 음영 이미지로 변환하는 과정입니다. 다음 코드 조각은 그레이 스케일링을 사용하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}

## **GIF 이미지 레이어를 TIFF 이미지로 변환**
PSD 이미지의 레이어를 다른 래스터 이미지 형식으로 추출하고 변환해야 하는 경우가 있습니다. Aspose.PSD API는 PSD 이미지의 레이어를 다른 래스터 이미지 형식으로 추출 및 변환하는 기능을 지원합니다. 우선 이미지의 인스턴스를 생성하고 로컬 디스크에서 PSD 이미지를 로드한 다음, Layer 속성에서 각 레이어를 반복하게 됩니다. 이후 블록을 TIFF 이미지로 변환합니다. 다음 코드 조각은 PSD 이미지의 레이어를 TIFF 이미지로 변환하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}

... (이어지는 부분은 생략)
