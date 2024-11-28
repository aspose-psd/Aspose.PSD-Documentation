---
title: 브라이트니스 대비 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/brightness-contrast/
---

# 자바에서 포토샵 밝기/대비 조정 레이어 작업

이 문서에서는 Aspose.PSD for Java® 라이브러리를 사용하여 Adobe® Photoshop® 문서에 밝기/대비 조정을 적용할 것입니다. 또한, 이런 종류의 조정 레이어에 관련된 라이브러리 기능에 대해 더 알아볼 것입니다.

하지만 먼저 이론 부터 알아보겠습니다.

밝기/대비 조정 레이어는 이미지의 밝기와 대비를 변경합니다. 그 정확한 의미는 무엇일까요? 밝기를 높이면 색상 값이 흰색까지 밝아지고, 반대로 밝기를 줄이면 색상 값이 검정색까지 어둡게 됩니다. 대비를 높이면 밝은 색과 어두운 색 사이의 차이가 커지고, 대비를 줄이면 그 차이가 줄어듭니다; 이는 밝은 색이 더 밝아지고 어두운 색이 더 어둡다는 것을 의미합니다.

## 컬러 모드 지원

라이브러리는 RGB, CMYK 또는 Lab 색상 모드의 이미지에 밝기/대비 조정 레이어를 추가할 수 있습니다.

## 현재 및 레거시 동작

현재 라이브러리 구현 (작성 시점의 v20.6)은 최신 포토샵 알고리즘을 사용하며 그림자부터 강조까지의 전체 토널 범위를 보존하지만 아직 레거시 동작을 지원하지 않습니다. 이는 라이브러리가 최신 버전의 포토샵(CS4 이상)에서 만든 문서의 밝기/대비 조정 레이어를 지원한다는 것을 의미합니다. 그러나 필요한 경우 [포토샵 밝기/대비 조정 레이어의 레거시 구현](https://forum.aspose.com/c/psd)을 포럼에서 요청할 수 있습니다.

## 밝기와 대비 조정

이제 우리는 밝기/대비 조정 레이어의 고수준 API가 어떻게 작동하는 지 설명하겠습니다 (미리 말하지만, API는 직관적입니다). PsdImage 클래스에는 밝기 및 대비 조정 게이트웨이인 BrightnessContrastLayer 클래스를 인스턴스화하는 팩토리 메서드(addBrightnessContrastAdjustmentLayer)가 있습니다. BrightnessContrastLayer 클래스에는 밝기와 대비 속성에 액세스하고 값을 변경할 수 있는 일종의 게터와 세터 쌍이 있습니다.

![|PSD의 밝기/대비 조정 레이어 예제](brightness-contrast-psd-adjustment-layer-figure-1.png)

따라서, 예를 들어 개 이미지(a)의 밝기를 조정하고 대비를 조정한 다음에 밝기1 및 대비2를 조정하여 더 생생하게 보이는 이미지(c)를 얻기 위해 해당 인수를 사용한 팩토리 메서드만 사용합니다:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

참고:

1. 밝기 값은 -150에서 150 사이여야 합니다.
2. 대비 값은 -50에서 100 사이여야 합니다.

자세한 내용은 [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) 문서를 참조하십시오.

## 결론

이 문서에서는 밝기/대비 조정 레이어에 대한 간단한 개요를 얻었으며, 팩토리 메서드를 사용하여 이미지의 밝기와 대비를 조정하는 방법을 배웠습니다.

더 많은 정보를 얻으려면 Aspose.PSD for Java의 [조정 레이어 API 시리즈](/ko/java/layer-types/adjustment-layer/)를 확인하시기 바랍니다.
