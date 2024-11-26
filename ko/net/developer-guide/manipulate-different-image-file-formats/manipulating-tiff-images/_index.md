---
title: TIFF 이미지 조작
type: docs
weight: 50
url: /ko/net/manipulating-tiff-images/
---

## **다른 설정으로 프레임 추가**
TIFF는 매우 유연한 형식이며 다른 프레임을 다른 치수, 압축 및 기타 설정으로 추가할 수 있습니다. Aspose.PSD API를 사용하면 복합 문서 작성에 도움이 되도록 어떤 크기의 TIFF 프레임이든 추가할 수 있습니다. 모든 프레임을 동일하게 만들기 위해 추가 프로세스 중에 프레임을 조정해야하는 경우 다음 단계를 수행하십시오:

- 원하는 옵션으로 새 빈 프레임을 만들거나 CreateFrameFrom 메서드를 사용하여 출력 옵션이 지정된 소스 프레임을 복사합니다.
- Resize 메서드를 사용하여 원본 프레임/이미지를 원하는 치수로 조정합니다.
- 소스 프레임/이미지 픽셀을 새 프레임에 추가합니다.
- 새 프레임을 출력 TIFF 이미지에 추가합니다.
## **PSD 이미지의 레이어를 다중 페이지 TIFF 파일 형식으로 내보내기**
PSD 이미지 레이어를 다중 페이지 TIFF 파일 형식으로 내보내야하는 경우가 있습니다. 이 문서에서는 Aspose.PSD for .NET API를 사용하여 이 작업을 수행하는 방법을 보여줍니다. 먼저, 디스크에서 PSD 이미지를 로드합니다. 그런 다음 PSD 이미지 레이어를 반복하고 해당 레이어에서 TiffFrame을 생성합니다. 마지막으로 생성된 Tiff 이미지를 디스크의 단일 파일로 저장합니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}
## **TiffOptions 구성**
개발자는 [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) 클래스의 다양한 속성을 조정하여 원하는 결과를 얻을 수 있습니다. 이 문서에서는 결과 이미지 속성을 제어하는 4 가지 주요 속성에 중점을 둘 것입니다.

아래에 나열된 이러한 속성은 다음과 같습니다.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

빈 TiffOptions 구조체를 초기화할 때마다 각 옵션이 기본값으로 설정됩니다. 예를 들어, 압축은 '없음'으로 설정되고, BitsPerSample은 1로 설정되며, Photometric은 MinIsWhite로 설정됩니다. 이 형식으로 저장하면 최종 이미지가 흑백이 되며 이는 해당 옵션 조합에 대한 예상 동작입니다. 원하는 색상 결과를 얻으려면 상기 모든 속성을 배색 공간에 해당하는 값으로 설정하거나 본 문서의 나중에 설명된 미리 설정된 설정으로 TiffOptions 구조체를 초기화할 수 있습니다. 아래에는 원하는 결과를 얻기 위해 설정할 수 있는 예상 변수 값에 대한 설명이 포함된 표가 제공되어 있습니다. 참고로, TIFF 파일 형식으로 로드/생성된 이미지를 저장하려면 TiffOptions를 통해 4개의 열 모두를 설정해야합니다.

| **TiffOptions.Photometric** | **TiffOptions.Compression** | **TiffOptions.BitsPerSample** | **TiffOptions.Predictor** |
| :- | :- | :- | :- |
|Palette|LZW/압축 해제|1/4/8/16 (팔레트, 컬러 모드) 단일 채널만|없음|
|MinIsWhite/MinIsBlack|LZW/압축 해제|1/4/8/16 (그레이 스케일 모드) 단일 채널만|없음|
|Palette|LZW/압축 해제|8 (팔레트, 컬러 모드) 단일 채널만|수평 (LZW에서 동일한 패턴으로 압축이 더 많이 구현됨)|
|MinIsWhite/MinIsBlack|LZW/압축 해제|8 (그레이 스케일 모드) 단일 채널만|수평 (LZW에서 동일한 패턴으로 압축이 더 많이 구현됨)|
|RGB|LZW/압축 해제|[8,8,8] (3 RGB 채널)|없음/수평|
|RGB|LZW/압축 해제|[8,8,8,8] (3 RGB 채널 및 추가 알파 채널은 TiffOptions.AlphaStorage를 통해 설정 가능) 사실 추가 채널 수는 지원되지만 각 채널은 [8,8,8,8,8,8]과 같이 8비트 크기여야 합니다.|없음/수평|
모든 4개의 속성은 이미지 형식을 TIFF 형식으로 저장하려면 TiffOptions를 통해 설정해야 합니다. 서로 다른 조합을 사용할 때 일부 뷰어(Windows 사진 뷰어포함)는 제공하는 제한된 지원 때문에 최종 이미지를 렌더링을 거부할 수 있습니다. 이 경우 테스트를 위해 다른 뷰어를 선택해야 합니다.
### **TiffOptions 클래스의 미리 설정된 설정**
TiffOptions 인스턴스의 설정 오류를 피하고 사용자를 지원하기 위해 Aspose.PSD for .NET API는 [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat) 유형 매개변수를 허용하는 또 다른 생성자를 노출했습니다. TiffExpectedFormat 열거형에서 선택한 값에 따라 API는 원하는 결과를 생성하도록 TiffOptions 인스턴스에 필수적인 속성을 자동으로 구성합니다. 샘플 코드로 넘어가기 전에 여기서 TiffExpectedFormat 필드와 사용법을 더 잘 이해하기 위해 해당 필드 및 세부 정보 목록을 제공합니다.


- TiffExpectedFormat.Default: Default를 설정하면 원하는 결과에 따라 수동으로 다른 형식별 속성이 설정되어야 하는 TiffOptions 클래스의 기본 생성자와 유사하게 작동합니다.
- TiffExpectedFormat.TiffCcitRle: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장하는 동안 RLE 인코딩에 특정된 형식입니다.
- TiffExpectedFormat.TiffCcittFax3: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장하는 동안 CCITT Fax3 인코딩에 특정된 형식입니다.
- TiffExpectedFormat.TiffCcittFax4: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장하는 동안 CCITT Fax4 인코딩에 특정된 형식입니다.
- TiffExpectedFormat.TiffDeflateBW: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장하는 동안 Deflate 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffDeflateRGB: RGB(컬러) TIFF 형식으로 결과를 저장하는 동안 Deflate 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffJpegRGB: RGB(컬러) TIFF 형식으로 결과를 저장하는 동안 Jpeg 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffJpegYCBCR: YCBCR(컬러) TIFF 형식으로 결과를 저장하는 동안 Jpeg 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffLzwBW: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장하는 동안 LZW 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffLzwRGB: RGB(컬러) TIFF 형식으로 결과를 저장하는 동안 LZW 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffLzwRGBA: RGBA(투명도가 포함된 컬러) TIFF 형식으로 결과를 저장하는 동안 LZW 압축에 특정된 형식입니다.
- TiffExpectedFormat.TiffNoCompressionBW: 1 BitsPerPixel(흑백)에 대해 결과를 저장하는 동안 압축되지 않은 TIFF 형식에 특정된 형식입니다.
- TiffExpectedFormat.TiffNoCompressionRGB: 컬러에 대해 결과를 저장하는 동안 압축되지 않은 TIFF 형식에 특정된 형식입니다.
- TiffExpectedFormat.TiffNoCompressionRGBA: RGBA(투명도가 포함된 컬러)에 대해 결과를 저장하는 동안 압축되지 않은 TIFF 형식에 특정된 형식입니다.


다음 코드 스니펫은 TiffOptions 클래스의 인스턴스를 만들 때 TiffExpectedFormat 필드를 사용하는 방법을 설명합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}
## **Deflate 및 Adobe Deflate 압축 지원**
TIFF(Tagged Image File Format) 파일 형식은 여러 유형의 압축을 지원하며, 압축 형식은 파일에 정수 값으로 저장됩니다. 그 중 하나인 압축 방법은 Adobe Deflate(이전에는 Deflate로 알려짐)입니다. Aspose.PSD for .NET API는 TIFF 이미지를 내보내고 생성할 때 이러한 압축 방법을 지원합니다.
### **Deflate 압축을 사용하여 TIFF에 이미지 저장**
로드된 이미지를 Deflate/Adobe Deflate 압축을 사용하여 TIFF로 변환하는 것은 다음과 같이 간단합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithDeflateCompression-TIFFwithDeflateCompression.cs" >}}
### **Adobe Deflate 압축으로 Tiff 이미지 생성**
아래 제공된 샘플은 Adobe Deflate 압축 방법을 사용하여 Aspose.PSD for .NET API를 사용하여 처음부터 이미지를 만드는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.cs" >}}
### **TIFF 이미지 압축**
Aspose.PSD for .NET API를 사용하여 PSD 이미지를 TIFF 이미지 형식으로 변환하고 결과 TIFF 이미지의 압축을 변경할 수 있습니다. API를 사용하여 이미지를 TIFF 이미지에 프레임으로 저장하여 이미지를 최소 데이터 크기로 압축하면서 아카이빙 목적으로 사용할 수도 있습니다. 모든 경우에 이미지 압축은 압축 알고리즘에 관계없이 소스 데이터 크기를 줄여서 수행되어야 합니다. 최상의 압축 비율을 얻기 위해 색인 색상 공간을 사용할 수 있습니다. 아래 제공된 코드 스니펫은 16가지 색인 색상을 사용하여 최상의 압축을 수행하며, 그러나 소스 색상은 약간 비틀릴 수 있습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.cs" >}}
