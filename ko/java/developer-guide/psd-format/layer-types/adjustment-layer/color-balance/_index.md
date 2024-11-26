---
title: 색상 균형 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/color-balance/
---

# 자바로 포토샵 색상 균형 조정 레이어 작업

이 문서에서는 자바에서 PSD 파일 형식의 이미지의 **색상 균형을 조정**하는 방법에 대해 알아볼 것입니다. 포토샵 문서를 조작하기 위한 도구상자인 Aspose.PSD for Java라는 특별한 라이브러리를 사용할 것입니다.

이 라이브러리는 PSD 파일 형식을 다루므로 포토샵 편집기에서 사용 가능한 거의 [모든 기능](https://docs.aspose.com/psd/java/features/)을 포함하고 있으며 **색상 균형 조정 레이어**도 이에 포함됩니다.

색상 균형 조정 레이어를 사용하면 그림자, 중간 음영 및 하이라이트의 주요 (RGB) 및 보색 (CMY) 색상 간의 균형을 변화시키는 것이 가능해지며, 이를 간단하고 빠르게 수행할 수 있게 됩니다.

## 색상 균형 조정

앞서 언급한 대로 Aspose.PSD for Java의 색상 균형 조정 레이어는 **기본 색과 보색 사이의 균형을 맞추는 작업**입니다. 이는 각 색상 쌍 (청록/빨강, 마젠타/초록, 노랑/파랑)에 대한 세 가지 스케일이 있는데, 해당하는 값이 해당 색상으로 이동하면 해당 색삭장의 강도가 증가하고 그 반대로 감소합니다. 또한, 그 세 가지 쌍은 각각 톤 범위 영역 (그림자, 중간 음영 및 하이라이트)에 고유하므로 이러한 조정의 유연성이 향상됩니다.

그래서, 이러한 지식을 실무에 적용해 보겠습니다. 예를 들어 여성의 얼굴 사진인 붉은 사진 (b)를 선택했습니다. 얼굴이 매우 붉다는 것을 고치기 위해 **색상 균형 조정 레이어를 추가**하여 기본적으로 빨간색을 줄이고 청록을 늘릴 것입니다 (a) 더 자연스러운 얼굴(c)으로 보이도록합니다. 이 이미지로 작업할 것이 많지만 이 글에서는 이것으로 마칠 것입니다.

![색상 균형 조정 레이어 예시](color-balance-adjustment-layer-example-figure-1.png) 색상 균형 조정 레이어의 API는 평면 디자인을 갖고 있습니다. 따라서 당신이 필요한 모든 것은 [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) 클래스입니다. 먼저 기본 밝기를 유지해야 합니다. 그 후, 그림자에 조금의 녹색과 더 많은 노랑을 추가하고, 중간 음영에는 더 많은 청록과 약간의 파랑을 추가하며, 하이라이트에는 더 많은 청록과 약간의 마젠타와 파랑을 추가하십시오.

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

이제 원하는 그림이 나왔습니다! 정말 간단하지 않습니까?

_각 색상 쌍의 값은 포토샵 편집기와 마찬가지로 **-100에서 100 범위**에 있어야 한다는 것에 주의하십시오. 즉, 빨간색 부의 값은 음수이며 기본 색은 양수여야 합니다._

자세한 기술적 세부 사항을 확인하려면 [색상 균형 조정 레이어에 대한 API 참조](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer)를 확인하십시오.

## 결론

이 문서에서는 Aspose.PSD for Java 라이브러리를 사용하여 자바에서 이미지의 색상 균형을 프로그래밍 방식으로 조정하는 방법을 고려했습니다. 이 라이브러리에는 포토샵 문서에서 색상 균형 조정 레이어를 다루는 데 필요한 완전한 API가 포함되어 있습니다.
