---
title: Aspose.PSD에서 C#의 스마트 필터 조작
weight: 100
type: docs
description: PSD 파일에서 Smart Filters 사용 예제
keywords: [smart filter, add noise, gauss blur, sharpen, filter, psd filter, psd api, C#, csharp, code sample]
url: ko/net/smart-filters/
---

## 개요

Aspose.PSD에서 C#에 스마트 필터를 적용하는 세 가지 방법이 있습니다.

### 직접 필터 적용

이 예제는 Aspose.PSD에서 C#에 스마트 필터를 직접 적용하는 방법을 보여줍니다.

먼저 원본 이미지의 출시 파일과 업데이트된 이미지의 출력 파일을 지정합니다.

다음으로 `Image.Load` 메서드를 사용하여 PSD 이미지를 로드하고 `PsdImage` 객체로 캐스트합니다.

지정된 출력 파일 이름을 사용하여 원본 이미지를 `Save` 메서드를 사용하여 저장합니다.

적용할 스마트 필터를 나타내는 `SharpenSmartFilter` 개체를 만듭니다.

`psdImage.Layers[1]`을 사용하여 PSD 이미지에서 일반 레이어를 검색합니다.

반복문을 사용하여 일반 레이어에 `sharpenFilter`를 세 번 적용합니다.

마지막으로 지정된 출력 파일 이름을 사용하여 업데이트된 이미지를 `Save` 메서드를 사용하여 저장합니다.

이 코드는 Aspose.PSD에서 C#에 직접 스마트 필터를 적용하는 방법을 보여줍니다. 적절한 필터 객체를 사용하고 원하는 레이어에 적용함으로써 이미지에 원하는 효과를 얻을 수 있습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### 스마트 오브젝트 내의 스마트 필터 조작

이 예제는 스마트 오브젝트 내부에서 스마트 필터를 조작하는 방법을 보여줍니다.

먼저 원본 이미지의 출시 파일과 업데이트된 이미지의 출력 파일을 지정합니다.

`Image.Load` 메서드를 사용하여 PSD 이미지를 로드하고 `PsdImage` 객체로 캐스트합니다.

지정된 출력 파일 이름을 사용하여 원본 이미지를 `Save` 메서드를 사용하여 저장합니다.

PSD 이미지의 두 번째 레이어를 `SmartObjectLayer` 객체로 캐스트합니다.

스마트 필터를 편집합니다. 이 예제는 `GaussianBlurSmartFilter`와 `AddNoiseSmartFilter`와 작업하는 방법을 보여줍니다.

`GaussianBlurSmartFilter`의 경우 반지름, 블렌드 모드, 불투명도 및 활성 상태와 같은 필터 값을 업데이트합니다.

`AddNoiseSmartFilter`의 경우 노이즈 분포를 `NoiseDistribution.UNIFORM`으로 설정합니다.

스마트 오브젝트 레이어에 새로운 필터 항목을 추가합니다: 다른 `GaussianBlurSmartFilter`와 `AddNoiseSmartFilter`.

`UpdateResourceValues` 메서드를 사용하여 변경사항을 적용합니다.

레이어와 레이어의 마스크에 필터를 직접 적용하고 `Apply` 및 `ApplyToMask` 메서드를 사용하여 마스크에 적용합니다.

지정된 출력 파일 이름을 사용하여 업데이트된 이미지를 `Save` 메서드를 사용하여 저장합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### 레이어 마스크에 스마트 필터 적용

스마트 필터는 여러 필터와 효과를 적용할 수 있는 강력한 이미지 편집 도구입니다. 한 가지 흥미로운 기술은 마스크에 적용하여 필터에 영향받는 영역을 정밀하게 제어하는 것입니다.

마스크는 일부 이미지 영역의 투명도를 결정하고 선택적으로 필터, 조정 또는 효과를 적용합니다.

마스크에 스마트 필터를 적용할 때 필터는 마스크에 지정된 영역에만 적용됩니다. 이 정밀한 제어를 통해 필터의 강도와 범위를 조작할 수 있습니다.

더 자세한 정보 및 예제는 [Aspose.PSD for C# 문서](https://docs.aspose.com/psd/net/)를 참조하십시오.
