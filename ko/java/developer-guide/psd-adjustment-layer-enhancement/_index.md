---
title: PSD 개선을 위한 조정 레이어 사용
weight: 100
type: docs
description: Aspose.PSD를 통한 Java에서 조정 레이어 사용 예시
keywords: [조정 레이어, 사진 향상, 곡선 조정, 레벨 개선, 반전, 사진 필터, psd api, java, 코드 샘플]
url: ko/java/adjustment-layer-enhancement/
---

## **개요**

이 문서에서는 Aspose.PSD를 이용하여 Java에서 조정 레이어를 편집하는 방법을 탐색합니다. 조정 레이어는 이미지 편집에서 중요한 기능으로, 이미지에 비파괴적인 변경을 적용할 수 있습니다. Aspose.PSD는 이미지의 다양한 측면을 수정할 수 있는 포괄적인 조정 레이어 클래스를 제공합니다.

조정 레이어의 편집을 보여주기 위해 PSD 이미지를 로드하고 해당 레이어에 다양한 조정을 적용하는 샘플 코드 스니펫을 제공할 것입니다.

다음 코드 스니펫에서는 PsdImage.load() 메서드를 사용하여 PSD 이미지를 로드하고 시작합니다. 그런 다음 출력 PNG 파일을 저장하기 위한 옵션을 설정합니다. PngOptions 클래스를 사용하여 출력 이미지의 색상 유형을 지정할 수 있습니다.

다음으로, PSD 이미지의 각 레이어를 반복하고 isAssignable() 메서드를 사용하여 해당 유형을 확인합니다. 레이어가 특정 유형인 경우, cast() 메서드를 사용하여 해당 유형으로 형변환하고 원하는 조정을 적용합니다. 예를 들어, BrightnessContrastLayer의 밝기 및 대비를 조정하거나 LevelsLayer의 레벨을 수정하거나 CurvesLayer에 곡선 포인트를 추가하는 작업을 수행합니다.

각 레이어에 대해 해당하는 다른 조정을 적용하기 위해 추가 코드를 추가할 수 있습니다. Aspose.PSD는 [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) 등 다양한 조정 레이어 클래스를 제공합니다.

마지막으로, PsdImage 클래스의 save() 메서드를 사용하여 수정된 이미지를 저장합니다.

이것은 Java에서 Aspose.PSD를 사용하여 조정 레이어를 편집하는 기본적인 개요를 제공합니다. 요구 사항에 맞게 조정을 사용자 정의하고 API 문서에서 사용 가능한 다양한 옵션을 탐색할 수 있습니다.

완전한 예시를 아래에서 확인해 주세요.

## **예시**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
