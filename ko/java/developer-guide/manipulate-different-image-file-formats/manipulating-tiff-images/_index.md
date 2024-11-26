---
title: TIFF 이미지 조작
type: docs
weight: 40
url: /ko/java/manipulating-tiff-images/
---

## **다른 설정으로 프레임 추가**
TIFF는 매우 유연한 형식이며, 다른 크기, 압축 및 기타 설정으로 다른 프레임을 추가할 수 있습니다. Aspose.PSD API를 사용하면 복잡한 문서를 작성하는 데 도움이 되는 임의의 크기의 TIFF 프레임을 추가할 수 있습니다. 프레임을 추가하는 동안 모든 프레임을 동일하게 만들기 위해 조정해야 하는 경우 다음 단계를 수행합니다:

- 원하는 옵션으로 새 빈 프레임을 생성하거나 CreateFrameFrom 메서드를 사용하여 출력 옵션이 지정된 원본 프레임을 복사합니다.
- Resize 메서드를 사용하여 원본 프레임/이미지를 원하는 크기로 조정합니다. 
- 소스 프레임/이미지 픽셀을 새 프레임에 추가합니다.
- 새 프레임을 출력 TIFF 이미지에 추가합니다.

## **PSD 이미지 레이어를 멀티페이지 TIFF 파일 형식으로 내보내기**
가끔 PSD 이미지 레이어를 멀티페이지 TIFF 파일 형식으로 내보내야 하는 경우가 있습니다. 이 문서에서는 Java API를 사용하여 이 작업을 수행하는 방법을 보여줍니다. 먼저, 디스크에서 PSD 이미지를 로드합니다. 그런 다음 PSD 이미지 레이어를 반복하고 해당 레이어에서 TiffFrame을 작성합니다. 마지막으로 생성된 TIFF 이미지를 디스크의 단일 파일로 저장합니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}


## **TiffOptions 구성**


개발자는 Tiffoptions 클래스의 다양한 속성을 조정하여 원하는 결과를 얻을 수 있습니다. 이 문서에서는 결과 이미지 속성을 제어하는 4가지 주요 속성에 중점을 둡니다.

아래에 나열된 이러한 속성은 다음과 같습니다.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

빈 Tiffoptions 구조체를 초기화할 때마다 각 옵션은 기본값으로 설정됩니다. 예를 들어 압축은 None으로 설정되고, BitsPerSample은 1로 설정되며, Photometric은 MinIsWhite로 설정됩니다. 이 형식으로 저장하면 최종 이미지가 흑백으로 표시되며, 이는 해당 옵션 조합의 예상 동작입니다. 색상 결과를 얻으려면 상기 언급된 모든 속성을 원하는 색상 공간에 해당하는 값으로 설정해야 하거나 이 문서에서 나중에 설명되는 미리 정의된 설정으로 Tiffoptions 구조체를 초기화할 수 있습니다. 아래에 제시된 표는 원하는 결과를 얻기 위해 설정할 수 있는 예상 매개변수 값을 설명하는 표입니다. 주의: 불러온/생성된 이미지를 TIFF 파일 형식으로 저장하려면 Tiffoptions를 통해 4개의 열을 모두 설정해야 합니다.


|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|Palette|LZW/압축되지 않음|1/4/8/16 (팔레트, 컬러 모드) 단일 채널만|없음|
|MinIsWhite/MinIsBlack|LZW/압축되지 않음|1/4/8/16 (그레이 스케일 모드) 단일 채널만|없음|
|Palette|LZW/압축되지 않음|8 (팔레트, 컬러 모드) 단일 채널만|수평 (LZW에서 동일한 패턴에 대해 더 많은 압축 효과 달성)|
|MinIsWhite/MinIsBlack|LZW/압축되지 않음|8 (그레이 스케일 모드) 단일 채널만|수평 (LZW에서 동일한 패턴에 대해 더 많은 압축 효과 달성)|
|RGB|LZW/압축되지 않음|[8,8,8] (3개의 RGB 채널)|없음/수평|
|RGB|LZW/압축되지 않음|[8,8,8,8] (3개의 RGB 채널 및 TiffOptions.AlphaStorage를 통해 추가 알파 채널 설정 가능) 사실상 추가 채널 수는 지원되지만 각 채널은 [8,8,8,8,8,8]과 같이 8비트 크기여야 합니다.|없음/수평|
모든 4가지 속성은 이미지 형식을 Tiff 형식으로 저장하기 위해 TiffOptions를 통해 설정되어야 합니다. 서로 다른 조합을 사용할 때 일부 뷰어(Windows 사진 뷰어를 포함하여)는 제한된 지원으로 인해 결과 이미지를 렌더링하지 않을 수 있습니다. 이 경우 테스트에 다른 뷰어를 선택하십시오.
### **TiffOptions 클래스를 위한 미리 정의된 설정**
사용자들을 지원하고 Tiffoptions 인스턴스의 잘못된 구성을 피하기 위해 Aspose.PSD for Java API는 TiffExpectedFormat 유형의 매개변수를 수용하는 다른 생성자를 노출시켰습니다. TiffExpectedFormat 열거형에서 선택한 값에 따라 API는 원하는 결과를 생성하기 위해 Tiffoptions 인스턴스의 모든 필수 속성을 자동으로 구성합니다. 샘플 코드로 이동하기 전에 TiffExpectedFormat 필드의 목록과 사용 방법을 더 잘 이해하기 위해 아래에 TiffExpectedFormat 필드 및 자세한 정보가 제공됩니다.


- TiffExpectedFormat.Default: Default를 설정하면 Tiffoptions 클래스의 기본 생성자와 유사하게 작동하며, 압축이 설정되지 않고 BitsPerPixel이 1로 설정되어 흑백 결과를 생성합니다. 다른 형식별 속성을 수동으로 설정해야 하는 경우 이 필드를 사용하는 것이 좋습니다.
- TiffExpectedFormat.TiffCcitRle: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장할 때 RLE 인코딩에 특정한 형식.
- TiffExpectedFormat.TiffCcittFax3: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장할 때 CCITT Fax3 인코딩에 특정한 형식.
- TiffExpectedFormat.TiffCcittFax4: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장할 때 CCITT Fax4 인코딩에 특정한 형식.
- TiffExpectedFormat.TiffDeflateBW: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장할 때 Deflate 압축에 특정한 형식.
- TiffExpectedFormat.TiffDeflateRGB: RGB(컬러) TIFF 형식으로 결과를 저장할 때 Deflate 압축에 특정한 형식.
- TiffExpectedFormat.TiffJpegRGB: RGB(컬러) TIFF 형식으로 결과를 저장할 때 Jpeg 압축에 특정한 형식.
- TiffExpectedFormat.TiffJpegYCBCR: YCBCR(컬러) TIFF 형식으로 결과를 저장할 때 Deflate 압축에 특정한 형식.
- TiffExpectedFormat.TiffLzwBW: 1 BitsPerPixel(흑백) TIFF 형식으로 결과를 저장할 때 LZW 압축에 특정한 형식.
- TiffExpectedFormat.TiffLzwRGB: RGB(컬러) TIFF 형식으로 결과를 저장할 때 LZW 압축에 특정한 형식.
- TiffExpectedFormat.TiffLzwRGBA: RGBA(투명도 있는 컬러) TIFF 형식으로 결과를 저장할 때 LZW 압축에 특정한 형식.
- TiffExpectedFormat.TiffNoCompressionBW: 1 BitsPerPixel(흑백)으로 결과를 저장할 때 압축되지 않은 TIFF 형식에 특정한 형식.
- TiffExpectedFormat.TiffNoCompressionRGB: RGB(컬러)로 결과를 저장할 때 압축되지 않은 TIFF 형식에 특정한 형식.
- TiffExpectedFormat.TiffNoCompressionRGBA: RGBA(투명도 있는 컬러)로 결과를 저장할 때 압축되지 않은 TIFF 형식에 특정한 형식.



다음 코드 스니펫은 Tiffoptions 클래스의 인스턴스를 생성할 때 TiffExpectedFormat 필드의 사용법을 설명합니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.java" >}}

## **Deflate 및 Adobe Deflate 압축 지원**
TIFF(Tagged Image File Format) 파일 형식은 파일에 정수 값으로 저장된 압축 유형을 포함하여 다양한 유형의 압축을 지원합니다. 그 중 하나인 이러한 압축 방법 중 하나는 Adobe Deflate(이전에는 Deflate로 알려져 있음)입니다. Aspose.PSD for Java API는 TIFF 이미지를 내보내고 생성할 때 이러한 압축 방법을 지원합니다.
### **Deflate 압축으로 TIFF 이미지 저장**
로드된 이미지를 Deflate/Adobe Deflate 압축을 사용하여 TIFF로 변환하는 것은 간답합니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFWithDeflateCompression-TIFFWithDeflateCompression.java" >}}
### **Adobe Deflate 압축을 사용한 TiffImage 생성**
아래 예시는 Aspose.PSD for Java API를 사용하여 Adobe Deflate 압축 방법을 이용해 처음부터 이미지를 생성하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-TIFFwithAdobeDeflateCompression-TIFFwithAdobeDeflateCompression.java" >}}
### **TIFF 이미지 압축**
Aspose.PSD for Java API를 사용하면 PSD 이미지를 TIFF 이미지 형식으로 변환하거나 결과 TIFF 이미지의 압축을 변경할 수 있습니다. API는 이미지를 최상의 압축 비율을 얻도록 소스 데이터 크기를 줄여서 TIFF 이미지의 프레임으로 저장하거나 이미지를 가장 낮은 데이터 크기로 압축하여 아카이빙 목적으로 사용할 수도 있습니다. 압축 알고리즘에 관계없이 이미지 압축은 소스 데이터 크기를 줄여서 수행되어야 합니다. 최상의 압축 비율을 얻기 위해 색인 색상 공간을 사용할 수 있습니다. 아래 제공된 코드 스니펫은 16개의 인덱스 색상만 사용하여 최상의 압축을 수행합니다. 그러나 소스 색상은 약간 패턴화됩니다.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-CompressingTiff-CompressingTiff.java" >}}
