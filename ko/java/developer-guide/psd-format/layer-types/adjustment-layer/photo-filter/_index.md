---
title: 사진 필터 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/photo-filter/
---

# 자바에서 포토샵 사진 필터 조정 레이어 사용하기

오늘은 Aspose.PSD for Java를 사용하여 기존의 포토샵 문서에 사진 필터 조정 레이어를 적용하는 방법을 살펴볼 것입니다. 이 라이브러리는 PSD 파일 형식을 조작하기 위한 라이브러리입니다.

**사진 필터 조정 레이어 API**는 색상 밸런스를 조정하여 이미지의 색조를 변경합니다. 결과 이미지는 실제 카메라 필터를 사용한 후처리한 것과 동일하게 보일 것입니다. 라이브러리의 사진 필터 조정 레이어 API는 미리 정의된 필터가 없는 Photoshop과 약간 다르지만, 다른 측면 모두 동일합니다. 이는 색조를 설정하고 강도(밀도)를 변경하거나 광도 보존 옵션을 사용할 수 있다는 것을 의미합니다.

## API 개요

사진 필터 조정 레이어 API는 상당히 간단하게 사용할 수 있습니다. 이 조정 레이어의 진입점 역할을 하는 [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) 클래스와 색상, 밀도, 광도 보존 등의 세 가지 공개 속성이 포함되어 있습니다.

## 색상 밸런스 조정

말할 것이 크게 없으므로, 바로 **사진 필터를 사용한 색상 밸런스 조정의 예시**를 살펴보겠습니다. 이미지에 온도가 따뜻한 필터를 수동으로 추가하여 더욱 즐거운 따뜻한 톤의 이미지를 얻기 위해 사슴 조각상 이미지에 필터를 적용할 것입니다.

![사진 필터 조정 레이어 예시](photo-filter-adjustment-layer-figure-1.png)

먼저, [팩토리 메소드](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-)는 [다른 조정 레이어들](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers)과 다르다는 것을 주목해야 합니다. 이는 인자 없이 기본 메소드가 없기 때문입니다. 따라서 로드된 포토샵 문서에 사진 필터 조정 레이어를 추가하려면 [색상](https://reference.aspose.com/psd/java/com.aspose.psd/Color)을 인자로 전달하는 단일 인자가 필요합니다. 따라서 온도 필터 효과를 재현하려면 주황색을 인자로 팩토리 메소드에 전달한 다음, 해당 세터를 사용하여 밀도를 설정하면 됩니다:

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

밀도 속성은 기본값인 100을 갖고, 광도 보존 속성의 기본값은 true입니다(이것이 이 옵션을 명시적으로 활성화하지 않는 이유입니다).

## 결론

본 문서에서는 Aspose.PSD for Java의 사진 필터 조정 레이어 API 사용법을 살펴보았습니다. 이 도구는 사용하기 쉽고 이미지에 변수 밀도의 색조를 추가할 수 있습니다. 전체 이미지의 색상 밸런스를 빠르게 조정하는 방법입니다.
