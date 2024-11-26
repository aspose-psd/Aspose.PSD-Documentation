---
title: Adobe Photoshop 포맷 조작
type: docs
weight: 20
url: /ko/net/manipulating-adobe-photoshop-formats/
---

## **PSD 레이어를 다른 레이어로 합치기**

## **이미지 PSD로 내보내기**
PSD, 포토샵 문서,는 Adobe Photoshop에서 이미지를 처리하는 데 사용하는 기본 파일 형식입니다. Aspose.PSD를 사용하면 파일을 PSD로 로드, 편집하고 저장하여 Photoshop에서 열고 편집할 수 있습니다. 이 문서에서는 이미지를 PSD로 저장하는 방법을 보여주며 이 형식으로 저장할 때 사용할 수 있는 일부 설정을 설명합니다. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)는 이미지를 PSD로 내보내기 위해 사용되는 [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 네임스페이스의 특수화된 클래스입니다. PSD로 내보내려면 기존 이미지 파일(예: 섬네일)에서 로드된 Image 클래스의 인스턴스를 만들거나 처음부터 생성합니다. 이 문서는 처음부터 이미지를 만드는 방법을 설명합니다. 생성되고 픽셀 데이터가 채워진 후 Image 클래스의 Save 메서드를 사용하여 이미지를 저장하고 두 번째 인수로 PsdOptions 객체를 제공합니다. 고급 변환을 위해 PsdOptions 클래스의 여러 속성을 설정할 수 있습니다. 일부 속성은 ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) 및 Version입니다. Aspose.PSD는 CompressionMethod 열거형을 통해 다음 압축 방법을 지원합니다:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

다음 색상 모드는 [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes) 열거형을 통해 지원됩니다:

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB

PSD v4.0, v5.0 및 그 이상을 위한 섬네일 리소스나 PSD v4.0 이상을 위한 격자 및 가이드 리소스와 같은 추가 리소스를 추가할 수 있습니다. 아래의 코드는 처음부터 Image 파일을 생성하고 픽셀을 채운 후 RLE 압축 및 그레이스케일 색상 모드로 PSD에 저장합니다. 다음 코드 스니펫은 이미지를 PSD로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}

## **PSD 레이어에 이미지 가져오기**
이 문서에서는 Aspose.PSD를 사용하여 PSD 레이어에 이미지를 추가하거나 가져오는 방법을 보여줍니다. Aspose.PSD API는이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 방법을 노출합니다. Aspose.PSD는 Layer 클래스의 [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) 메서드를 노출하여 PSD 파일에 이미지를 추가/가져오는 데 사용합니다. DrawImage 메서드는 PSD 파일에 이미지를 추가/가져오기 위해 위치 및 이미지 값을 필요로합니다. PSD 레이어에 이미지를 가져오는 단순한 단계는 다음과 같습니다:

- Image 클래스에서 노출된 Load 팩토리 메서드를 사용하여 PSD 파일로 이미지를 로드
- Png, Jpeg, Tiff, Gif, Bmp, Psd 또는 j2k 파일로부터 스트림으로 Layer 클래스의 인스턴스를 생성
- AddLayer 메서드를 사용하여 Psd에 Layer 추가
- 결과 저장

다음 코드 스니펫은 PSD 레이어에 이미지를 가져오는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

## **PSD 레이어에서 색상 교체**
이 문서에서는 Aspose.PSD를 사용하여 PSD 레이어에 이미지를 추가하거나 가져오는 방법을 보여줍니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 방법을 노출합니다. Aspose.PSD는 Layer 클래스의 DrawImage 메서드를 노출하여 PSD 파일에 이미지를 추가/가져오는 데 사용합니다. DrawImage 메서드는 PSD 파일에 이미지를 추가/가져오기 위해 위치 및 이미지 값을 필요로합니다. PSD 레이어에 이미지를 가져오는 단순한 단계는 다음과 같습니다:

- Image 클래스에서 노출된 Load 팩토리 메서드를 사용하여 PSD 파일로 이미지를 로드
- Layer 클래스의 인스턴스를 생성하고 해당 PSD 이미지 레이어를 할당
- 추가할 이미지를 로드하거나 처음부터 생성한 후 Layer. DrawImage 메서드를 호출하면서 위치와 이미지 인스턴스 지정
- 결과 저장

다음 코드 스니펫은 PSD 레이어에 이미지를 가져오는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}

## **PSD 파일에서 썸네일 생성**
PSD는 Adobe의 포토샵 애플리케이션의 기본 문서 형식입니다. Adobe Photoshop(버전 5.0 이상)은 JFIF 썸네일을 사용하는 초기 28바이트 헤더로 구성된 이미지 리소스 블록에 미리보기 표시용 섬네일 정보를 저장합니다. Aspose.PSD API는 PSD 파일의 리소스에 액세스할 수 있는 사용하기 쉬운 메커니즘을 제공합니다. 이러한 리소스에는 어플리케이션 요구에 따라 검색하고 디스크로 저장할 수 있는 섬네일 리소스가 포함되어 있습니다. 아래의 코드는 PSD 파일에서 썸네일을 생성하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}

## **색인 PSD 파일 생성**
Aspose.PSD for .NET API를 사용하면 처음부터 색인 PSD 파일을 만들 수 있습니다. 이 문서는 PsdOptions 및 [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) 클래스의 사용법을 보여주며 새로 생성된 캔버스 위에 모양을 그리는 중에 색인 PSD를 만드는 방법을 설명합니다. 색인 PSD 파일을 만드는 데 필요한 간단한 단계는 다음과 같습니다:

- PsdOptions의 인스턴스를 만들고 소스를 설정
- PsdOptions의 ColorMode 속성을 ColorModes.Indexed로 설정
- RGB 공간에서의 색상 팔레트를 만들고 PsdOptions의 Palette 속성으로 설정
- 필요한 압축 알고리즘을 CompressionMethod 속성에 설정
- PsdImage.Create 메서드를 호출하여 새 PSD 이미지 생성
- 요구 사항에 따라 그래픽을 그리거나 다른 작업 수행
- PsdImage.Save 메서드를 호출하여 모든 변경 사항 저장

다음 코드 스니펫은 색인 PSD 파일을 만드는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}

## **PSD 레이어를 래스터 이미지로 내보내기**
Aspose.PSD for .NET을 사용하면 PSD 파일의 레이어를 래스터 이미지로 내보낼 수 있습니다. PSD 레이어를 이미지로 내보내려면 [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) 메서드를 사용하세요. 다음 샘플 코드는 PSD 파일을 로드하고 각 레이어를 PNG 이미지로 내보내기 위해 Aspose.PSD.FileFormats.Psd.Layers.Layer.Save를 사용합니다. 모든 레이어를 PNG 이미지로 내보낸 후 이를 좋아하는 이미지 뷰어를 사용하여 열 수 있습니다. 다음 코드 스니펫은 PSD 레이어를 래스터 이미지로 내보내는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}

## **PSD 파일에서 텍스트 레이어 업데이트**
Aspose.PSD for .NET을 사용하면 PSD 파일의 텍스트 레이어의 텍스트를 조작할 수 있습니다. PSD 파일의 텍스트 레이어를 업데이트하려면 [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) 클래스를 사용하십시오. 다음 코드 스니펫은 PSD 파일을 로드하고 텍스트 레이어에 액세스한 다음 텍스트를 업데이트하고 [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer/methods/updatetext/index) 메서드를 사용하여 새 이름으로 PSD 파일을 저장합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}

## **평탄화된 PSD 감지**
Aspose.PSD for .NET을 사용하면 주어진 PSD 파일이 평탄화되었는지 여부를 감지할 수 있습니다. 이 기능을 달성하기 위해 Aspose.PSD.FileFormats.Psd.PsdImage 클래스에 IsFlatten 속성이 소개되었습니다. 다음 코드 스니펫은 PSD 파일을 로드하고 [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/isflatten) 속성에 액세스합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}

## **PSD 레이어를 병합**
이 문서는 PSD 파일의 레이어를 병합하여 PSD 파일을 JPG로 변환하는 방법을 보여줍니다. 아래 예제에서는 기존 PSD 파일을 Image 클래스의 정적 Load 메서드에 파일 경로를 전달하여 로드합니다. 로드된 후 이미지를 PsdImage로 변환하거나 캐스트합니다. JpegOptions 클래스의 인스턴스를 만들고 다양한 속성을 설정합니다. 이제 PsdImage 인스턴스의 Save 메서드를 호출합니다. 다음 코드 스니펫은 PSD 레이어를 병합하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}

## **PSD에 알파와 함께 그레이스케일 지원**
이 문서는 Aspose.PSD를 사용하여 PSD 파일을 PNG로 변환하는 동안 알파와 함께 그레이스케일을 지원하는 방법을 보여줍니다. 아래 예에서 기존 PSD 파일은 Image 클래스의 정적 Load 메서드에 파일 경로를 전달하여 로드됩니다. 로드된 후 이미지를 PsdImage로 변환하거나 캐스트합니다. PngOptions 클래스의 인스턴스를 만들고 다양한 속성을 설정합니다. ColorType 속성을 TruecolorWithAlpha로 설정하세요. 이제 PngOptions 인스턴스의 Save 메서드를 호출합니다. 다음 코드 스니펫은 알파로 그레이스케일 PNG로 변환하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}

## **PSD 레이어 지원**
이 문서는 PSD 레이어에 **Blur**, **Inner Glow**, **Outer Glow** 등 다양한 효과를 지원하는 방법을 보여줍니다. 다음 코드 스니펫은 레이어 효과를 지원하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}

## **레이어 생성 날짜 및 시간 지원**
이 문서는 PSD 레이어의 생성 날짜 및 시간을 지원하는 방법을 보여줍니다. 다음 코드 스니펫은 레이어 생성 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LayerCreationDateTime-LayerCreationDateTime.cs" >}}

## **시트 색상 강조 지원**
이 문서는 PSD 이미지를 로드한 다음 시트 색상을 변경하고 강조하는 방법을 보여줍니다. 코드 스니펫을 제공하였습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SheetColorHighlighting-SheetColorHighlighting.cs" >}}