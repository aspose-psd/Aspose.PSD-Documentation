---
title: PNG 이미지 조작
type: docs
weight: 40
url: /ko/net/manipulating-png-images/
---

## **PNG 이미지에 투명도 지정**
PNG 형식으로 이미지를 저장하는 장점 중 하나는 PNG가 투명 배경을 가질 수 있다는 것입니다. Aspose.PSD for .NET은 PNG 이미지 및 래스터 이미지에 대한 투명도를 지정할 수 있는 기능을 제공합니다. 아래 섹션에서 이를 보여줍니다. Aspose.PSD for .NET API는 새 PNG 이미지를 생성하거나 기존 이미지를 PNG 형식으로 변환할 때 투명한 색상을 설정할 수 있습니다. 이를 위해 Aspose.PSD for .NET API에는 [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) 속성 및 [PngColorType](https://reference.aspose.com/psd/net/aspose.psd.fileformats.png/pngcolortype) 열거형이 노출되어 있어 PNG 이미지에서 투명하게 렌더링할 색상을 지정할 수 있습니다. 아래 제공된 코드 스니펫은 기존 PSD 이미지를 가져와 원하는 색상을 투명하게 지정한 후 PNG 이미지로 변환하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **PNG 이미지의 해상도 설정**
Aspose.PSD for .NET은 PNG를 포함한 모든 이미지 형식의 해상도를 설정할 수 있는 ResolutionSetting 클래스를 노출합니다. 이 기사에서는 Aspose.PSD for .NET API를 사용하여 PNG 이미지 형식의 수평 및 수직 해상도 매개변수를 설정하는 방법을 보여줍니다. 아래 코드 스니펫은 기존 PSD 이미지를로드하고 해상도를 변경한 다음 PNG 형식으로 변환하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **PNG 파일 압축**
포터블 네트워크 그래픽(PNG)은 비트맵을 네트워크를 통해 전송하기 위한 무손실 압축 형식입니다. 어떤 프로그램에서 이미지를 PNG 파일로 저장할 때 0에서 최대 수준까지 압축 수준을 선택하라는 요청을 받을 수 있습니다. 이 값을 설정하면 실제로 파일 크기가 압축되지만 이미지 품질은 떨어지지 않습니다. 이 기사에서는 Aspose.PSD API가 PNG 파일 크기를 제어하는 방법을 설명합니다. Aspose.PSD API를 사용하여 PNG 파일 형식의 압축 수준을 설정할 수 있으며, 이를 위해 PngOptions 클래스에 int 형 [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) 속성이 있습니다. 이 속성은 0부터 9까지의 값 (9가 최대 압축)을 수용합니다. 아래 제공된 코드 스니펫은 Aspose.PSD for .NET API를 사용하여 압축 수준을 설정하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **PNG 이미지에 비트 단위 지정**
이미징에서의 비트 단위란 비트맵 이미지에서 단일 픽셀의 색상을 나타내는 데 사용되는 비트의 수입니다. 다른 모든 비트맵 형식과 마찬가지로, PNG 색상 깊이도 1비트(2색), 2비트(4색), 4비트(16색) 및 8비트(256색)와 같이 비트로 표현됩니다. Aspose.PSD for .NET API를 사용하여 PngOptions 클래스에서 제공하는 [BitDepth](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/bitdepth) 속성을 사용하여 PNG 이미지에 대한 비트 단위를 설정할 수 있습니다. 현재 BitDepth 속성은 회색조와 인덱스 색상 유형에 대해 1, 2, 4 또는 8비트로 설정할 수 있습니다. 다른 모든 색상 유형에 대해서는 8비트만 지원됩니다. 아래 제공된 코드 스니펫은 PNG 이미지에 대한 비트 단위를 설정하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **PNG 이미지에 필터 방법 적용**
이미징에서의 비트 단위란 비트맵 이미지에서 단일 픽셀의 색상을 나타내는 데 사용되는 비트의 수입니다. 다른 모든 비트맵 형식과 마찬가지로, PNG 색상 깊이도 1비트(2색), 2비트(4색), 4비트(16색) 및 8비트(256색)와 같이 비트로 표현됩니다. Aspose.PSD for .NET API를 사용하여 PngOptions 클래스에서 제공하는 BitDepth 속성을 사용하여 PNG 이미지의 비트 단위를 설정할 수 있습니다. 현재 BitDepth 속성은 회색조 및 인덱스 색상 유형에 대해 1, 2, 4 또는 8비트로 설정할 수 있습니다. 다른 모든 색상 유형에 대해서는 8비트만 지원됩니다. 아래 제공된 코드 스니펫은 PNG 이미지에 대한 비트 단위를 설정하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **투명 PNG 이미지의 배경색 변경**
PNG 형식 이미지는 투명 배경을 가질 수 있습니다. Aspose.PSD for .NET은 투명 배경을 가진 PNG 이미지의 배경색을 변경할 수 있는 기능을 제공합니다. Aspose.PSD for .NET API를 사용하여 투명 PNG 이미지의 배경색을 설정하거나 변경할 수 있습니다. 아래 제공된 코드 스니펫은 투명 PNG 이미지의 배경색을 설정/변경하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
