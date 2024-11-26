---
title: 이미지 변환
type: docs
weight: 20
url: /ko/net/converting-images/
---

## **흑백 및 그레이스케일로 이미지 변환하기**
가끔은 인쇄 또는 아카이빙 목적으로 컬러 이미지를 흑백 또는 그레이스케일로 변환해야 할 때가 있습니다. 이 문서에서는 Aspose.PSD for .NET API를 사용하여 이를 달성하기 위해 아래에 설명된 두 가지 방법을 보여줍니다.

- 이진화
- 그레이스케일링
### **이진화**
이진화 개념을 이해하기 위해서는 먼저 이진 이미지를 정의하는 것이 중요합니다; 즉, 각 픽셀에 대해 두 가지 가능한 값만 가질 수 있는 디지털 이미지입니다. 일반적으로 이진 이미지에 사용되는 두 색은 검정과 흰색이지만 다른 두 색상을 사용할 수도 있습니다. 이진화는 이미지를 이진레벨로 변환하는 과정으로, 각 픽셀이 색상의 부재를 나타내는 단일 비트(0 또는 1)로 저장되는 의미합니다. Aspose.PSD for .NET API는 현재 두 가지 이진화 방법을 지원합니다.
#### **고정 임계값을 사용한 이진화**
다음 코드 스니펫에서는 이미지에 고정 임계값 이진화를 적용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **오츠 임계값을 사용한 이진화**
다음 코드 스니펫에서는 이미지에 오츠 임계값 이진화를 적용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **그레이스케일링**
그레이스케일링은 연속된 음영의 이미지를 불연속한 회색 음영의 이미지로 변환하는 과정입니다. 다음 코드 스니펫에서 그레이스케일링을 사용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **GIF 이미지 레이어를 TIFF 이미지로 변환하기**
PSD 이미지의 레이어를 추출하고 다른 래스터 이미지 형식으로 변환하여 애플리케이션 요구 사항을 충족해야 할 때가 있습니다. Aspose.PSD API는 PSD 이미지의 레이어를 추출하고 다른 래스터 이미지 형식으로 변환하는 기능을 지원합니다. 먼저 이미지의 인스턴스를 만들고 로컬 디스크에서 PSD 이미지를 로드한 다음, 각 레이어를 Layer 속성에서 반복한 다음 해당 블록을 TIFF 이미지로 변환합니다. 다음 코드 스니펫에서 PSD 이미지 레이어를 TIFF 이미지로 변환하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **CMYK PSD를 CMYK TIFF로 변환하기**
Aspose.PSD for .NET을 사용하면 개발자는 CMYK PSD 파일을 CMYK tiff 형식으로 변환할 수 있습니다. 이 문서에서는 Aspose.PSD를 사용하여 CMYK PSD 파일을 CMYK tiff 형식으로 내보내거나 변환하는 방법을 보여줍니다. Aspose.PSD for .NET을 사용하면 PSD 이미지를 로드한 다음 [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) 클래스를 사용하여 다양한 속성을 설정하고 이미지를 저장하거나 내보낼 수 있습니다. 다음 코드 스니펫에서 이 기능을 어떻게 구현하는지 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **이미지 내보내기**
Aspose.PSD는 PSD 파일 형식을 다른 형식으로 변환하기 위한 전문화된 클래스를 제공합니다. 이 라이브러리를 사용하면 PSD 이미지 변환이 매우 간단하고 직관적입니다. 아래는 [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 네임스페이스 내의 이러한 목적을 위한 특수 클래스 몇 가지입니다.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

Aspose.PSD for .NET API를 사용하면 PSD 이미지를 다른 형식으로 쉽게 내보낼 수 있습니다. [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 네임스페이스에서 적절한 클래스의 객체만 있으면, Aspose.PSD for .NET으로 생성, 편집 또는로드된 이미지를 지원하는 형식으로 쉽게 내보낼 수 있습니다.
## **이미지 결합하기**
이 예제는 Graphics 클래스를 사용하여 두 개 이상의 이미지를 하나의 완전한 이미지로 결합하는 방법을 보여줍니다. 작업을 설명하기 위해, 예제는 새로운 PsdImage를 만들고 Graphics 클래스에서 노출된 Draw Image 메서드를 사용하여 캔버스 표면에 이미지를 그립니다. Graphics 클래스를 사용하면 두 개 이상의 이미지를 결합할 수 있어 최종 이미지가 이미지 부분 사이에 공간도 없이 페이지도 없이 완전한 이미지로 보이게 할 수 있습니다. 캔버스 크기는 결과 이미지의 크기와 동일해야 합니다. 아래는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) 메서드를 사용하여 이미지를 결합하는 방법을 보여주는 코드 예시입니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **이미지 확장 및 자르기**
Aspose.PSD API를 사용하면 이미지 변환 과정 중 이미지를 확장하거나 자를 수 있습니다. 개발자는 X, Y 좌표로 사각형을 생성하고 사각형 상자의 너비와 높이를 지정해야 합니다. 사각형의 X, Y 및 너비, 높이는 로드된 이미지의 확장 또는 자르기를 나타냅니다. 이미지 변환 중 이미지를 확장하거나 자를 경우 다음 단계를 수행하십시오:

1. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스의 인스턴스를 생성하고 기존 이미지를 로드합니다.
1. ImageOption 클래스의 인스턴스를 만듭니다.
1. [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) 클래스의 인스턴스를 생성하고 사각형의 X, Y, 너비, 높이를 초기화합니다.
1. RasterImage 클래스의 [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) 메서드를 호출할 때 출력 파일 이름, 이미지 옵션 및 사각형 객체를 매개 변수로 전달하십시오.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **이미지에 XMP 데이터 읽기 및 쓰기**
XMP(Extensible Metadata Platform)은 ISO 표준입니다. XMP는 데이터 모델, 직렬화 형식 및 확장 가능한 메타데이터의 정의 및 처리를 표준화합니다. 인기 있는 이미지인 JPEG와 같은 이미지에 XMP 정보를 포함하는 가이드 라인을 제공하여 XMP를 지원하지 않는 애플리케이션에서도 해당 이미지의 가독성을 해치지 않습니다. Aspose.PSD for .NET API를 사용하면 개발자는 이미지에 XMP 메타데이터를 읽거나 쓸 수 있습니다. 이 문서에서는 이미지에서 XMP 메타데이터를 읽고 이미지에 XMP 메
