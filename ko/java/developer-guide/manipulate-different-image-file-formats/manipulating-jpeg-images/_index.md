---
title: JPEG 이미지 조작
type: docs
weight: 20
url: /ko/java/manipulating-jpeg-images/
---

## **ExifData 클래스를 사용하여 JPEG EXIF 태그 읽고 수정하기**


거의 모든 디지털 카메라(스마트폰 포함), 스캐너 및 이미지를 처리하는 기타 시스템은 이미지에 EXIF(교환 가능 이미지 파일) 정보를 저장합니다. 카메라 설정 및 씬 정보가 이미지 파일에 의해 카메라에 의해 기록됩니다. EXIF 데이터에는 또한 셔터 속도, 촬영 일시 및 시간, 초점 거리, 노출 보정, 측광 패턴 및 플래시 사용 여부도 포함됩니다. Aspose.Imaging API를 사용하면 주어진 이미지에서 EXIF 정보를 매우 쉽고 간단한 방법으로 추출할 수 있습니다. 개발자는 또한 이미지에 EXIF 데이터를 작성하거나 기존 정보를 필요에 따라 수정할 수 있습니다. Aspose.Imaging은 EXIF 데이터를 읽기, 쓰기 및 수정하기 위한 ExifData 클래스를 제공하며, Aspose.PSD.Exif.Enums 네임스페이스에는 프로세스에서 사용되는 관련 열거형이 포함되어 있습니다.
### **EXIF 데이터 읽기**
Aspose.PSD API는 주어진 이미지에서 EXIF 데이터를 읽는 방법을 제공합니다. 아래 제공된 단계는 이미지에서 EXIF 정보를 읽는 ExifData 클래스의 사용법을 보여줍니다.

- 팩토리 메서드 Load를 사용하여 PSD 이미지 로드.
- PSD 리소스 중 JPEG 썸네일 찾기.
- ExifData 클래스의 인스턴스 추출.

필요한 정보를 가져와 콘솔에 작성합니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



또는 아래 코드 스니펫을 사용하여 특정 정보를 얻을 수도 있습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **EXIF 데이터 쓰기 및 수정**
Aspose.PSD API를 사용하면 개발자가 이미지의 새로운 EXIF 정보를 작성하고 기존 EXIF 데이터를 수정할 수 있습니다. 쓰기 및 수정의 두 프로세스는 이미지 로드 및 ExifData 클래스의 인스턴스로 EXIF 데이터를 가져오는 것을 요구합니다. 그런 다음 ExifData 클래스가 노출하는 속성에 액세스하여 해당 속성을 설정할 수 있습니다. 조작을 위한 이미지는 일반적으로 PSD 썸네일인 JPEG 또는 TIFF 이미지여야 합니다. 사용법을 보여주는 샘플 코드는 다음과 같습니다:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **PSD 리소스로부터 썸네일 추출**
썸네일은 전체 프레임 대신 사진의 중요한 부분을 표시하는 데 사용되는 사진의 줄인 크기 버전입니다. 일부 이미지 파일(특히 디지털 카메라로 촬영된 이미지)에는 파일에 포함된 썸네일 이미지가 있습니다. Aspose.PSD API를 사용하면 PSD 리소스 썸네일을 추출하고 디스크에 별도로 저장할 수 있습니다. 썸네일 리소스는 썸네일 데이터를 검색할 수 있는 ExifData.Thumbnail 속성을 포함하고 있습니다. 아래 제공된 코드 스니펫은 사용 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



상기 접근 방법을 사용하여 썸네일을 다른 지원되는 파일 형식으로 저장합니다. BMP 및 PNG과 같은 다른 이미지 내보내기 옵션을 사용하여 썸네일 데이터를 내보내고 싶은 경우에는 이용하십시오.


### **JFIF 세그먼트로부터 썸네일 추출**
PSD 썸네일 리소스의 JFIF 또는 ExifData 세그먼트에서 썸네일을 추출하는 것도 가능합니다. 아래 코드를 통해 JFIF 또는 ExifData 세그먼트에서 썸네일 데이터를 추출하는 방법을 볼 수 있습니다:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



상기 접근 방법을 사용하여 썸네일을 다른 지원되는 파일 형식으로 저장합니다. BMP 및 PNG과 같은 다른 이미지 내보내기 옵션을 사용하여 썸네일 데이터를 내보내고 싶은 경우에는 이용하십시오.
### **JFIF 세그먼트에 썸네일 추가**
다음 코드 스니펫은 로드된 PSD 이미지의 JFIF 세그먼트에 썸네일 이미지를 추가하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

JFIF 형식 사양으로 인해 다른 세그먼트 데이터와 함께 썸네일 이미지는 65,545바이트를 초과할 수 없습니다. 큰 이미지를 썸네일로 설정해야 하는 경우 예외가 발생할 수 있습니다.


### **EXIF 세그먼트에 썸네일 추가**
다음 코드 스니펫은 로드된 PSD 이미지의 EXIF 세그먼트에 썸네일 이미지를 추가하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

이 경우 Aspose.PSD API는 썸네일 이미지 크기를 추정할 수 없지만 전체 EXIF 데이터 세그먼트의 크기를 확인할 수 있습니다. 이 크기는 65,535바이트를 초과할 수 없습니다.
## **JpegExifData 클래스를 사용하여 JPEG EXIF 태그 읽고 수정하기**
Aspose.PSD API는 JPEG 이미지 포맷에 독점적인 JpegExifData 클래스를 제공하여 EXIF 정보를 검색하고 업데이트할 수 있습니다. 이 문서에서는 JpegExifData 클래스의 사용법을 보여줍니다. Aspose.PSD.Exif.JpegExifData 클래스는 JPEG 이미지를 위한 EXIF 데이터 컨테이너로 작동하며 표준 JPEG EXIF 태그를 검색하는 방법을 아래에서 설명합니다:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **전체 EXIF 태그 목록**
상기 코드 조각은 Aspose.PSD.Exif.JpegExifData 클래스가 제공하는 속성을 사용하여 몇 가지 EXIF 태그를 읽습니다. 이러한 속성의 전체 목록은 여기에서 볼 수 있습니다. 다음 코드는 System.Reflection.PropertyInfo 클래스를 사용하여 모든 EXIF 태그를 읽습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-.jpeg-read-all-exiftags-read-all-exiftaglist.java-" >}}
## **JPEG 이미지의 자동 방향 보정**
사진은 카메라를 90°, 180°, 270° 또는 회전하지 않은 방향으로 촬영할 수 있습니다. 대부분의 디지털 카메라는 JPEG 이미지의 EXIF 태그로 방향 정보를 저장합니다. 이 정보를 사용하여 이미지의 방향을 올바르게 조정하기 위해 자동 회전을 수행할 수 있습니다. Aspose.PSD API는 JPEG 이미지의 방향을 자동으로 보정하기 위한 JpegImage 클래스의 AutoRotate 메서드를 제공합니다. 아래에서 Aspose.PSD for Java API와 함께 AutoRotate 메서드를 사용하는 방법을 안내합니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **CMYK 및 YCCK를 사용한 JPEG-LS 지원**


Aspose.PSD for Java API는 JPEG-LS에서 CMYK 및 YCCK 색상 모델을 지원합니다. 아래 코드 스니펫은 JPEG-LS 지원을 사용하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-.jpeg-support-for-jpegls-with-cmyk-support-for-jpegls-with-cmyk.java-" >}}
## **JPEG-LS 이미지에서 2-7비트 샘플 지원**


Aspose.PSD for Java API는 2-7비트 샘플 JPEG-LS 이미지를 지원합니다. 아래 코드 스니펫은 JPEG-LS 지원을 사용하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-.jpeg-support-for-2-and-7-bitsjpeg-support-for-2-and-7-bitsjpeg.java-" >}}
## **JPEG 이미지용 ColorType 및 CompressionType 설정**




Aspose.PSD for Java API는 JPEG 이미지의 Color Type 및 Compression Type을 지원하고 회색조 및 프로그레시브로 설정할 수 있습니다. 아래 코드 스니펫은 해당 지원을 사용하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-.jpeg-colortype-andcompressiontype-colortypeandcompressiontype.java-" >}}





