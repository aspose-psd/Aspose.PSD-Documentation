---
title: 블랙 앤 화이트 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/levels/
---

## Java에서 Photoshop 레벨 조정 레이어 작업

이 문서에서는 Java에서 프로그래밍 방식으로 [PSD 파일 형식](/psd/ko/java/psd-format/)의 사진의 음조 범위 및 색상 밸런스를 조정하는 방법에 대해 알아보겠습니다. 우리는 Adobe® Photoshop® 사진 편집기 자체를 사용하지 않습니다. 대신에 Photoshop 문서를 조작하는 데 독립적으로 작동하는 Java용 Aspose.PSD 라이브러리를 사용합니다.

Java용 Aspose.PSD는 우리가 원하는대로 사진을 편집하는 데 충분한 [도구를 지원합니다](/psd/ko/java/manipulating-images/), 그러나 우리는 **레벨 조정 레이어 API를 사용**하여 작업하는 것이 가장 간단하고 빠른 방법 중 하나라는 것을 확인할 수 있습니다.

## API 개요

현재 구현 중인 (작성 시점의 20.6) 레벨 조정 레이어 API**는 Photoshop 레벨의 기본 기능을 모두 지원**하며, 총합 채널 (RGB) 및 각 기본 컬러 채널 (빨강, 녹색 및 파랑)을위한 입력 및 출력 레벨을 조정합니다.

레벨 조정 레이어의 API는 직관적입니다. [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) 클래스는 레벨 조정에 대한 진입점입니다. 색상 채널에 액세스하는 데 사용되는 몇 가지 메서드를 포함하고 있습니다: getMasterChannel 및 getChannel(int). 두 메서드 모두 조작을 위한 입력 및 출력 레벨을 액세스하는 [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel)을 반환합니다. 차이점은 getMasterChannel이 복합 컬러 채널 (RGB)을 조정하는 데 사용되는 반면, getChannel은 색상 채널 (빨강, 녹색 또는 파랑)에 해당하는 인덱스로 액세스합니다.

## 색 모드와의 호환성

Photoshop 레벨에 따르면 레벨 조정 레이어**는 대부분의 색 모드와 호환**됩니다. 따라서 그레이스케일 (회색 채널), RGB (RGB, 빨강, 녹색 및 파랑 채널), CMYK (CMYK, 청색, 마젠타, 노랑 및 검정 채널), 듀오톤 (단색 채널) 및 LAB (밝기, a 및 b 채널) 색 모드의 이미지에 대해 레벨을 조정할 수 있습니다.

## 음조 범위 조정

간단히 말하면, 음조 보정은 중간 톤을 더 잘 분배하기 위해 그림의 그림자와 하이라이트를 매핑하는 것입니다. 일반적으로, **올바르게 수행되면 이미지를 더 대비있게 만듭니다**. 예를 들어, 강아지 사진 (b)을 촬영 한 뒤 음조 범위 (a - 명확성을 위해 Photoshop 레벨 창에서 캡처 된 스크린샷)를 조정하여 사진을 더 대비 있게 만들어 봅시다 (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levels Layer Figure 1](levels-adjustment-figure-1.png)|

이미지의 **전체 음조 범위를 조정**하려면 마스터 채널의 입력 레벨을 설정해야 합니다:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

그림자의 경우 입력 레벨은 0에서 253까지, 중간 톤의 경우 9.99에서 0.01까지, 하이라이트의 경우 2에서 255까지의 범위에 있어야 합니다. 출력 레벨의 범위는 0에서 255 사이여야 합니다.

더 많은 예시가 필요하신가요? [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java)나 [knowledge base](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers)에서 찾아볼 수 있습니다.

## 결론

요약하면, Java용 Aspose.PSD는 거의 모든 색 모드와 호환되는 이미지의 음조 범위 및 색상 밸런스를 변경하기 위한 편리하고 간단한 API를 제공합니다. 라이브러리의 레벨 조정 레이어 API는 Photoshop 레벨과 유사하여, 이전에 라이브러리와 작업해 본 적이 없더라도 쉽게 시작할 수 있습니다.
