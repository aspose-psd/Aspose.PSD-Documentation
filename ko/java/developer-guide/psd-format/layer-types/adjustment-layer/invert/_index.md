---
title: 레이어 타입 조정 레이어 반전
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/invert/
---

# Java에서 Photoshop 반전 조정 레이어 작업

이 기사에서는 Java에서 프로그래밍 방식으로 Photoshop 문서의 이미지를 부정 이미지로 바꾸는 방법을 보여줍니다. 이를 위해 Aspose.PSD for Java라는 PSD 파일 형식 조작 라이브러리를 사용할 것입니다.

색상 반전 API를 사용하면 이미지에 **부정적인 효과를 추가** 할 수 있습니다. 이미 [곡선 조정 레이어를 사용하여 이미지 색상을 반전하는 방법] (/psd/java/layer-types/adjustment-layer/curves/)을 보았을 수 있습니다. 그러나 오늘은 Invert 조정 레이어를 사용하여 작업을 더 빨리하고 쉽게 할 수 있는 방법을 고려할 것입니다.

## API 개요

**Invert 조정 레이어 API**는 레이어 클래스 자체로 구성되어 있으며 [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer)입니다. 이 클래스에는 자체의 공개 멤버가 없으며 부모 클래스인 ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer))에서 모든 공개 멤버를 상속받기 때문에 사용이 간단해집니다. 이미지를 부정으로 만들려면 PSD 파일에 추가하면 됩니다.

## 이미지 색상 반전

따라서 명백하게 보일지라도 우리가 **이미지에 Invert 조정 레이어를 적용하는 방법**을 명확히 보여드립니다. 우주 비행사의 이미지 (a)에 부정 효과를 만들기 위해 이미지에 Invert 조정 레이어를 추가하세요 (b).

![반전 조정 레이어 예시 전후](invert-adjustment-layer-figure-1.png)

이미지의 색상을 **반전시키려면** PSD에 Invert 조정 레이어를 추가하세요:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

그게 다입니다! 이 유형의 조정 레이어를 구성할 특정 속성은 없습니다.

## 결론

이 기사에서는 Aspose.PSD for Java의 Invert 조정 레이어 API에 대해 배웠습니다. 이 조정 레이어의 API는 공개 멤버를 선언하지 않기 때문에 부정 이미지를 얻는 데 편리한 도구입니다.

