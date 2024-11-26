---
title: 커브 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/curves/
---

# 자바에서 포토샵 커브 조정 레이어 작업

이 기사의 목표는 Adobe® 포토샵® 문서에서 **커브 조정 레이어를 다룰 때** 라이브러리 Aspose.PSD for Java의 기능을 보여주는 것입니다. 이 라이브러리는 완전 자체 자립형입니다. 따라서 포토샵 사진 편집기를 설치하지 않고 작동합니다. [모든 기능 목록](https://docs.aspose.com/psd/java/features/)은 여기서 확인할 수 있습니다. 이제 커브로 돌아가겠습니다.

## API 개요

커브 도구는 히트라이트가 우측 상단에 그림자가 우측 하단에 있는 그래프의 대각선 선(커브)로 표현할 수 있습니다.

이 라이브러리는 커브 작업을 위한 API를 제공합니다. 구체적으로 [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer) 클래스를 이용합니다. 그러나 이 클래스는 커브 작업을 위한 **두 가지 완전히 다른 접근 방식**을 가지고 있습니다. 따라서 한 번에 두 가지 중 하나의 모드로 편집할 수 있습니다:

- 연속(커브를 구부리는 지점에 점들로 표시)
- 이산(점선으로 표시되는 커브)

그러므로 라이브러리는 [연속](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) 및 [이산 관리자](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager)를 이용하여 커브를 수정할 수 있습니다. 다음으로는 특정 예제를 통해 각각을 사용하는 방법을 설명하겠습니다.

## 커브 연속 관리자를 이용하여 색조 및 톤 조정

[커브 연속 관리자](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager)는 **연속 커브의 구부리는 점들**을 구성하며 (RGB) 복합 채널과 각각의 색상 채널에 대해 작동합니다. 시연을 위해 어두운 오케스트라 이미지에 몇 가지 커브 조정 (a)이 적용되어 따뜻한 색이 들어간 밝은 이미지(b)를 얻습니다:

![커브 조정 레이어 그림 1](curves-psd-adjustment-layer-figure-1.png)

두 관리자가 있기 때문에 얻기 전에 (이 경우에는 연속 관리자) 명시적으로 선택하는 것이 필요합니다. 그 후, 원하는 색상 채널 (복합 RGB, 각각의 빨강, 파랑)에 원하는 좌표에 커브 점을 직접 추가할 수 있습니다. 앞서 한 것과 같은 곡선 모양을 재현하기 위해:

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

좌표의 원점은 왼쪽 하단에 있습니다. 점의 최대 좌표 값은 데이터 형식(byte)에 제한되어 있으며 255(부호 있는 유형의 경우 127)와 같습니다.

[사용할 수 있는](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) 몇 가지 다른 메서드도 있습니다.

## 커브 이산 관리자를 사용하여 톤 조절

커브 이산 관리자는 커브 점을 위치시키는 것도 가능하며 (사실 색조와 톤을 변경함), 그러나 그 방식이 다릅니다. 첫째, **커브는 점**이나 점들로 구성됩니다 (실선이 아님). 둘째, 이 관리자는 **그래프의 모든 곳에 점을 놓지 않습니다**. 대신에 이 점을 각각 255에서 0사이의 값의 범위로 위나 아래로 **이동**합니다. 기본적으로 커브 점 값은 45도 각도로 정렬되어있습니다.

그것을 염두에 두면, "Negative (RBG)" 포토샵 사전 설정(a)을 재현하고 이를 계곡의 회색 이미지(b)에 적용하여 최종적으로 계곡의 부정적 표현(c)을 얻는 것은 쉽습니다.

![커브 조정 레이어 그림 2](curves-psd-adjustment-layer-figure-2.png) 먼저, 사용하기 위해 해당 관리자를 선택하고 (이 경우에는 이산 관리자) 각 커브 점의 값을 255부터 0까지 내려가는 순서로 설정하여 곡선을 형성하면 됩니다:

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

이 관리자는 커브를 관리하기 위한 몇 가지 [다른 메서드](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager)도 제공합니다.

## 결론

이 기사에서는 두 가지 완전히 다른 방법 (연속 및 이산 관리자)을 사용하여 포토샵 문서에서 커브 조정 레이어를 다루는 방법을 배웠습니다.
