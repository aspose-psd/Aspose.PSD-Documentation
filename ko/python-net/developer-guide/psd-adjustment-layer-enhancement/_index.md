---
title: PSD 향상을 위한 조정 레이어 사용
weight: 100
type: docs
description: Aspose.PSD for Python을 사용한 조정 레이어의 예시
keywords: [조정 레이어, 사진 향상, 곡선 조정, 레벨 향상, 반전, 사진 필터,  psd API, Python, 코드 샘플]
url: ko/python-net/adjustment-layer-enhancement/
---

## **개요**

이 기사에서는 Aspose.PSD를 사용한 Python에서 조정 레이어를 편집하는 방법을 알아볼 것입니다. 조정 레이어는 이미지 편집에서의 강력한 기능으로, 이미지를 비파괴적으로 변경할 수 있게 해줍니다. Aspose.PSD는 다양한 이미지 측면을 수정할 수 있는 조정 레이어 클래스 세트를 제공합니다.

조정 레이어의 편집을 설명하기 위해, PSD 이미지를 로드하고 레이어에 다양한 조정을 적용하는 샘플 코드 스니펫을 사용할 것입니다. 

아래 코드 스니펫에서는 PsdImage.load() 메서드를 사용하여 PSD 이미지를 불러오고, 출력 PNG 파일의 옵션을 설정합니다. PngOptions 클래스를 사용하면 출력 이미지의 색상 유형을 지정할 수 있습니다.

다음으로, PSD 이미지의 각 레이어를 반복하고 is_assignable() 메서드를 사용하여 해당 유형을 확인합니다. 레이어가 특정 유형이면 cast() 메서드를 사용하여 해당 유형으로 캐스팅하고 원하는 조정을 적용합니다. 예를 들어, BrightnessContrastLayer의 밝기와 대비를 조절하거나, LevelsLayer의 수준을 수정하거나, CurvesLayer에 곡선 점을 추가하는 등의 작업을 수행합니다.

다른 조정을 각각의 레이어에 적용하기 위해 추가 코드를 추가할 수 있습니다. Aspose.PSD는 [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) 등과 같은 다양한 조정 레이어 클래스를 제공합니다.

마지막으로, PsdImage 클래스의 save() 메서드를 사용하여 수정된 이미지를 저장합니다.

이 코드는 Aspose.PSD를 사용한 Python에서 조정 레이어를 편집하는 기본적인 개요를 제공합니다. 요구 사항에 맞게 조정을 사용자 정의하고 API 문서에서 제공하는 다양한 옵션을 탐색할 수 있습니다.

전체 예시를 확인하세요.

## **예시**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
