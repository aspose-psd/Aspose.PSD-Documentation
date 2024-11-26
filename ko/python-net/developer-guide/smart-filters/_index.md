---
title: Aspose.PSD를 이용한 Python에서 Smart Filter 조작
weight: 100
type: docs
description: PSD 파일에서 Smart Filters 사용 예제
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, python, code sample]
url: ko/python-net/smart-filters/
---

## **개요**

Aspose.PSD for Python에서 Smart Filters를 적용하는 3가지 방법이 있습니다.

## **직접적인 필터 적용**
이 코드 샘플에서는 Aspose.PSD for Python에서 Smart Filters를 직접 적용하는 예제를 볼 수 있습니다.

먼저, 코드는 원본 이미지의 소스 PSD 파일, 원본 이미지의 출력 파일 및 업데이트된 이미지의 출력 파일을 지정합니다.

다음으로, 코드는 Image.load() 메서드를 사용하여 PSD 이미지를 로드하고 PsdImage 객체로 캐스팅합니다.

원본 이미지는 save() 메서드를 사용하여 지정된 출력 파일 이름으로 저장됩니다.

SmartFilter에 SmartFilter을 적용하는 SharpenSmartFilter 객체가 생성됩니다.

그런 다음 코드는 im.layers[1]을 사용하여 PSD 이미지에서 일반 레이어를 검색합니다.

그런 다음 루프를 사용하여 sharpenFilter를 일반 레이어에 세 번 적용합니다.

마지막으로, update된 이미지는 출력 파일 이름을 지정하여 save() 메서드를 사용하여 저장됩니다.

이 코드는 Aspose.PSD for Python에서 Smart Filters를 직접적으로 적용하는 방법을 보여줍니다. 적절한 필터 객체를 사용하고 원하는 레이어에 적용함으로써 이미지에 원하는 효과를 얻을 수 있습니다.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Smart Objects에 Smart Filters 조작**

먼저, 코드는 원본 이미지의 소스 PSD 파일, 원본 이미지의 출력 파일 및 업데이트된 이미지의 출력 파일을 지정합니다.

PSD 이미지는 Image.load() 메서드를 사용하여 로드한 다음 PsdImage 객체로 캐스팅됩니다.

원본 이미지는 save() 메서드를 사용하여 지정된 출력 파일 이름으로 저장됩니다.

다음으로, 코드는 PSD 이미지의 두 번째 레이어를 SmartObjectLayer 객체로 캐스팅하여 스마트 오브젝트 레이어를 나타냅니다.

그런 다음, 코드는 스마트 필터를 편집합니다. 이 예에서는 두 종류의 Smart Filters(GaussianBlurSmartFilter 및 AddNoiseSmartFilter)를 사용하는 방법을 보여줍니다.

GaussianBlurSmartFilter에 대해서는 코드가 반경, 블렌드 모드, 불투명도 및 활성화 여부를 포함한 필터 값을 업데이트합니다.

AddNoiseSmartFilter에 대해서는 코드가 노이즈 분포를 NoiseDistribution.UNIFORM으로 설정합니다.

다음으로, 코드는 두 개의 새 필터 항목을 스마트 오브젝트 레이어에 추가합니다: 또 다른 GaussianBlurSmartFilter 및 AddNoiseSmartFilter입니다.

새 필터를 추가한 후, update_resource_values() 메서드를 사용하여 변경 사항을 적용합니다.

마지막으로, 코드는 레이어 및 해당 레이어의 마스크에 필터를 직접 적용하는 방법을 보여줍니다. 각각 apply() 및 apply_to_mask() 메서드를 사용합니다.

update된 이미지는 출력 파일 이름을 지정하여 save() 메서드를 사용하여 저장됩니다.

이 코드 샘플을 따르면 Aspose.PSD for Python에서 Smart Filters를 다루는 방법을 알 수 있습니다. 라이브러리는 다양한 스마트 필터를 제공하며, 각각의 속성 및 메서드를 사용자 정의하여 이미지에 원하는 효과를 얻을 수 있습니다.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **레이어 마스크에 Smart Filters 적용**

마스크에 Smart Filters 적용: 강력한 이미지 편집 기술

Smart filters는 이미지 편집 소프트웨어에서 인기 있는 기능으로 사용자가 이미지에 다양한 필터와 효과를 적용할 수 있게 합니다. Smart filters를 사용하여 달성할 수 있는 흥미로운 기술 중 하나는 마스크에 적용하는 것입니다. 이 기사에서는 Smart filters를 마스크에 적용하는 방법을 탐구하고 이미지 편집 분야에서의 사용법을 논의하겠습니다.

마스크란 무엇인가? Smart filters를 마스크에 적용하기 전에 먼저 마스크가 무엇인지 이해해 봅시다. 이미지 편집에서 마스크는 이미지의 특정 영역의 투명도를 결정하는 회색 이미지입니다. 마스크를 사용하면 이미지의 특정 부분에 필터, 조정 또는 효과를 선택적으로 적용할 수 있으며 다른 영역을 변경하지 않은 상태로 남길 수 있습니다.

마스크에 Smart Filters 적용: 마스크에 Smart filters를 적용할 때 필터는 마스크로 지정된 영역에만 적용됩니다. 이를 통해 이미지의 어느 부분이 필터에 영향을 받는지를 정확하게 제어할 수 있습니다. 마스크를 조작함으로써 필터의 효과의 강도와 범위를 결정할 수 있습니다.

이전 예제 및 메서드를 확인하세요: [API 참조 Smart Filter를 마스크에 적용](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
