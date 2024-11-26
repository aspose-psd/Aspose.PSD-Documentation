---
title: 노출 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/exposure/
---

# 자바에서 포토샵 노출 조정 레이어 다루기

이 문서에서는 Aspose.PSD for Java - PSD 파일 형식 조작 라이브러리를 사용하여 Adobe® Photoshop® 문서에 노출 조정 레이어를 추가하는 방법을 알아볼 것입니다. 이 라이브러리는 자체 이미지 처리 알고리즘을 사용하기 때문에 포토샵 편집기가 설치되어 있지 않아도 작동합니다. 우리는 또한 라이브러리 노출 조정 API와 관련된 세부 정보를 학습했습니다.

## API 개요

노출 조정 레이어는 노출 조정에 관련된 다음 속성을 다루는 [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) 클래스를 통해 구성됩니다.

- 사진이 얼마나 많은 빛을 가지고 있는지를 정의합니다. 전체 히스토그램을 검은 색에 상대적으로 압축하거나 늘려서 주로 하이라이트에 영향을 줍니다.
- 노출 보정이 그림자에 주로 영향을 줍니다.
- 감마 보정. 이미지 휘도를 보정합니다.

## 올바른 노출

노출 보정 및 관련 속성을 수정하는 것은 클래스의 몇 가지 속성을 변경하는 것만큼 간단합니다. 라이브러리의 이미지를 인식 가능하도록 라이브러리의 이미지에 노출 조정을 적용하려면 (a) 라이브러리의 소형 사진에 미세 조정을 적용하고, 인간의 눈에 인식 가능하도록 만들어야 합니다.

![노출 조정 레이어 예시](exposure-adjustment-layer-figure-1.png)

전체 조정은 주로 감마 보정을 통해 이뤄집니다. 그러나 노출 및 보정도 약간 조정됩니다. 이미 언급된 속성에 적절한 값을 설정하기만 하면 됩니다:

```java
ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
exposureLayer.setExposure(-0.03f);
exposureLayer.setOffset(-0.0005f);
exposureLayer.setGammaCorrection(1.85f);
```

노출은 -20.0에서 20.0 사이 여야 하며, 오프셋 값은 -0.5에서 0.5 범위에 있어야 하며, 감마 보정 값은 9.99에서 0.01 사이여야 합니다.

자세한 내용은 [노출 조정 레이어 API 참조](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer)를 참조하십시오.

## 결론

이 문서에서는 PSD 파일에 노출 조정 레이어를 추가하여 이미지를 밝게 하는 방법 및 일부 API 세부 정보를 고려했습니다.
