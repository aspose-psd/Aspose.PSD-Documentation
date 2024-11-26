---
title: PSD 향상을 위한 조정 레이어 사용
weight: 100
type: docs
description: Aspose.PSD를 통해 조정 레이어를 사용하는 예제 (C#)
keywords: [조정 레이어, 사진 향상, 곡선 조정, 레벨 향상, 반전, 사진 필터, psd api, C#, 씨샵, 코드 샘플]
url: ko/net/adjustment-layer-enhancement/
---

## 개요

이 문서에서는 Aspose.PSD for C#에서 조정 레이어를 편집하는 방법을 살펴봅니다. 조정 레이어는 이미지 편집에서 강력한 기능으로, 이미지에 파괴적인 변경 없이 변경 내용을 만들 수 있도록 해줍니다. Aspose.PSD는 이미지의 다양한 측면을 수정할 수 있는 조정 레이어 클래스 세트를 제공합니다.

조정 레이어를 편집하는 방법을 보여주기 위해 PSD 이미지를로드하고 레이어에 다양한 조정을 적용하는 샘플 코드 스니펫을 사용할 것입니다.

아래 코드 스니펫에서는 `PsdImage.Load()` 메서드를 사용하여 PSD 이미지를로드합니다. 그런 다음 출력 PNG 파일을 저장하기 위한 옵션을 설정합니다. `PngOptions` 클래스를 사용하여 출력 이미지의 색상 유형을 지정할 수 있습니다.

다음으로, PSD 이미지의 각 레이어를 반복하고 `IsAssignable()` 메서드를 사용하여 해당 유형을 확인합니다. 특정 유형의 레이어인 경우 `Cast()` 메서드를 사용하여 해당 유형으로 캐스트하고 원하는 조정을 적용합니다. 예를 들어 `BrightnessContrastLayer`의 밝기와 명암을 조정하거나 `LevelsLayer`의 레벨을 수정하거나 `CurvesLayer`에 곡선 포인트를 추가하는 등의 작업을 수행합니다.

각각의 레이어에 다른 조정을 적용하는 추가 코드를 추가할 수 있습니다. Aspose.PSD는 [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer) 등과 같은 폭넓은 범위의 조정 레이어 클래스를 제공합니다.

마지막으로, `PsdImage` 클래스의 `Save()` 메서드를 사용하여 수정된 이미지를 저장합니다.

이 코드는 Aspose.PSD for C#에서 조정 레이어를 편집하는 방법에 대한 기본 개요를 제공합니다. 요구 사항에 맞게 조정을 맞춤화하고 API 문서에서 제공하는 다양한 옵션을 살펴볼 수 있습니다.

## 예시

다음은 Aspose.PSD for C#를 사용하여 조정 레이어를 사용하는 방법을 보여주는 코드 샘플입니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

더 자세한 정보 및 예제는 [Aspose.PSD for C# 문서](https://docs.aspose.com/psd/net/)를 방문하십시오.
