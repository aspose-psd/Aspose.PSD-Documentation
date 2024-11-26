---
title: 채널 믹서 조정 레이어
type: docs
weight: 30
url: /ko/java/layer-types/adjustment-layer/channel-mixer/
---

# 자바에서 포토샵 채널 믹서 조정 레이어 사용하기

오늘은 자바를 사용하여 프로그래밍적으로 포토샵 문서에서 색상 채널을 혼합하는 방법을 살펴보겠습니다. 포토샵 편집기는 자바 스크립팅을 지원하지 않기 때문에, Aspose.PSD for Java라는 특별한 PSD 파일 형식 조작 라이브러리를 사용할 것입니다.

**API를 사용하여 색상 채널을 다룰 수 있는** 이 라이브러리에는 여러 가지 방법이 있지만, 이 글에서는 채널 믹서 조정 레이어에 초점을 맞출 것입니다.

채널 믹서 조정 레이어 API를 통해 **색상 채널을 다루어 틴 이미지를 만들거나 다양한 창의적인 색상 효과를 만들거나 심지어 이미지를 흑백으로 변환**할 수 있습니다. 다음으로, 존재하는 포토샵 문서에 채널 믹서 조정을 적용하는 방법을 Aspose.PSD for Java를 사용하여 살펴보겠지만, 먼저 전체 API 기능에 대해 이야기해야 합니다.

## API 개요

채널 믹서 조정 레이어를 만드는 것에는 특별한 점이 없습니다. [기본 팩토리 메소드](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--)를 통해 추가할 수 있으며, 이 메소드는 ChannelMixerLayer 클래스의 인스턴스를 반환합니다. 이 클래스에는 그레이 출력 채널을 위한 모노크롬 옵션 및 출력 채널을 가져오는 메소드와 같은 일반적인 기능이 포함되어 있습니다. 특정 출력 채널은 [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) 또는 [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel) 중 하나일 수 있습니다. [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel)의 유형은 이미지의 [색상 모드](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--)에 따라 다릅니다.

## 이미지를 흑백으로 만들기

이제 기존의 포토샵 문서에 채널 믹서 조정 레이어를 적용하는 예제를 살펴보겠습니다. 이 종류의 조정 레이어는 아직 프리셋을 지원하지 않으므로, **블랙 앤 화이트 (RGB) 포토샵 프리셋**을 다시 만들겠습니다. 이 프리셋은 번졸이 피어나는 나무의 이미지에 적용될 것입니다. 결과적으로, 적외선 사진 효과를 얻고자 합니다.

![채널 믹서 조정 레이어 예](channel-mixer-adjustment-psd-layer-figure-1.png) 우선, 블랙 앤 화이트 (RGB) 포토샵 프리셋을 다시 만들기 위해서는 모노크롬 플래그를 활성화하고 그레이 출력 채널에 대해 각 색상(빨강, 녹색, 파랑)에 적합한 raw 값 설정이 필요합니다:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

코드가 작동하려면 이미지가 RGB 색상 모드여야 합니다(빨강, 녹색, 파랑 믹서 채널 클래스로의 캐스트 때문에). CMYK 색상 모드도 지원되지만 해당 색상 모드를 가진 이미지에 대해서만 가능합니다.

각 색상의 값 및 Constant 속성은 -200에서 200 사이의 값이어야 함을 주의하세요.

## 결론

본 문서에서는 Aspose.PSD for Java의 채널 믹서 API를 사용하여 색상 채널에서 색상을 조정하고 이미지를 흑백으로 변환하는 방법에 대해 살펴보았습니다.
