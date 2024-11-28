---
title: Fill Layers 지원
type: docs
weight: 90
url: /ko/net/support-of-fill-layers/
---

## **패턴으로 레이어 채우기**
이 문서는 [PSD](https://wiki.fileformat.com/image/psd/) 레이어를 패턴으로 채우는 방법을 보여줍니다. 패턴은 이미지, 색상, 그림자 또는 선 등을 사용하여 이미지 영역을 채우는 데 사용되는 것입니다. 패턴을 추가하려면 Aspose.PSD.FileFormats.Psd.Layers.FillLayer를 사용하십시오. 아래 코드 스니펫은 PSD 파일을 로드하고 [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 클래스에 액세스하여 [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) 속성을 사용하여 패턴을 설정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

또한 [Aspose.PSD](https://products.aspose.com/psd/net)이 [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 및 [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings)을 사용하여 패턴을 렌더링하는 다른 예제가 있습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}

## **그라데이션으로 레이어 채우기**
이 문서에서는 PSD 레이어를 채우는 데 그라데이션 채우기를 사용하는 방법을 설명합니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이면서 사용하기 쉬운 방법을 제공합니다. Aspose.PSD는 GradientColorPoint 및 GradientTransparencyPoint 클래스를 노출하여 레이어에 그라데이션 효과를 추가했습니다.

PSD 레이어를 그라데이션으로 채우기 위한 단계는 다음과 같습니다:
- [Image](https://reference.aspose.com/net/psd/aspose.psd/image) 클래스에서 노출된 팩토리 메서드 [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index)를 사용하여 이미지로 PSD 파일을로드합니다.
- [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 개체의 설정 속성을 설정합니다.
- 필요한 색상 및 색상 위치를 갖는 [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) 목록을 만듭니다.
- 필요한 투명도 및 투명도 지점의 위치를 갖는 투명도 점 목록을 만듭니다.
- [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) 메서드를 호출합니다.
- 결과를 저장합니다.

다음 코드 스니펫은 PSD 레이어를 그라데이션으로 채우는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

또한 [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 및 [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings)을 사용하여 PSD 레이어를 그라데이션으로 채우는 데 [GradientFillSettings.GradientType](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype) 속성을 사용하는 또 다른 예제가 있습니다. Aspose.PSD는 GradientType 열거형을 통해 다음과 같은 그라데이션 유형을 지원합니다:
- **GradientType.Linear:** 선형 그라데이션에서 색상은 시작 색조부터 끝까지 직선으로 변화합니다.
- **GradientType.Radial:** 원형 그라데이션에서 색상은 시작 지점에서 원형으로 퍼져나옵니다.
- **GradientType.Angle:** 각도 그라데이션은 시작 지점을 중심으로 반시계방향으로 회전합니다.
- **GradientType.Reflected:** 반사 그라데이션에서 색상은 시작 지점을 중심으로 양쪽에 거울로 반영됩니다.
- **GradientType.Diamond:** 다이아몬드 그라데이션은 시작 지점에서 다이아몬드 모양을 만듭니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}

## **그라데이션 채움 레이어의 스케일 속성 지원**
이 문서에서는 .NET에서 Aspose.PSD를 사용하여 그라데이션 채움 레이어를 조절하는 방법을 설명합니다. 이를 위해 [IGradientFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings)에 **Scale** 속성이 추가되었습니다. 아래는 **Scale** 속성 사용을 보여주는 코드입니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}

## **색상으로 레이어 채우기**
이 문서에서는 [PSD](https://wiki.fileformat.com/image/psd/) 레이어를 색상으로 채우는 방법을 설명합니다. PSD 레이어에 색상을 추가하려면 [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) 클래스를 사용하십시오. 아래 코드 스니펫은 PSD 파일을 로드하고 Fill 레이어 클래스에 액세스하여 [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings) 속성을 사용하여 색상을 설정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
