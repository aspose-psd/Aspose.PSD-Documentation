---
title: JPEG 이미지 조작
type: docs
weight: 30
url: /ko/net/manipulating-jpeg-images/
---

## **ExifData 클래스 사용하여 Jpeg EXIF 태그 읽기 및 수정하기**
거의 모든 디지털 카메라(스마트폰 포함), 스캐너 및 이미지를 처리하는 다른 시스템들은 이미지를 EXIF(교환 가능한 이미지 파일) 정보와 함께 저장합니다. 카메라 설정 및 장면 정보는 이미지 파일에 카메라에 의해 기록됩니다. EXIF 데이터는 또한 셔터 속도, 사진 촬영 날짜 및 시간, 초점 거리, 노출 보정, 측광 패턴 및 플래시 사용 유무를 포함합니다. Aspose.Imaging API는 주어진 이미지에서 매우 쉽고 간단하게 EXIF 정보를 추출할 수 있도록 하였습니다. 개발자들은 이미지에 EXIF 데이터를 작성하거나 기존 정보를 필요에 따라 수정할 수 있습니다. Aspose.PSD는 EXIF 데이터를 읽고 쓰고 수정하기 위한 [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) 클래스를 제공하며, [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) 네임스페이스는 해당 과정에서 사용되는 관련 열거형을 포함합니다.
### **EXIF 데이터 읽기**
Aspose.PSD API는 주어진 이미지에서 EXIF 데이터를 읽는 방법을 제공합니다. 아래 제공된 단계는 이미지에서 ExifData 클래스를 사용하여 EXIF 정보를 읽는 방법을 설명합니다.

- 로드된 PSD 이미지를 Load 팩토리 메서드를 사용하여 로드합니다.
- PSD 리소스 중에서 Jpeg 썸네일을 찾습니다.
- ExifData 클래스의 인스턴스를 추출합니다.

필요한 정보를 가져와 콘솔에 출력합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


또는 다음 코드 스니펫을 사용하여 특정 정보를 얻을 수도 있습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **EXIF 데이터 작성 및 수정**
Aspose.PSD API를 사용하여 개발자들은 이미지의 새로운 EXIF 정보를 작성하고 기존의 EXIF 데이터를 수정할 수 있습니다. 쓰기 및 수정 과정 모두 이미지를 로드하고 ExifData 클래스의 인스턴스에 EXIF 데이터를 가져와야 합니다. 그런 다음 ExifData 클래스에서 노출된 속성에 알맞게 값을 설정할 수 있습니다. 조작할 이미지는 일반적으로 PSD 서머리 이미지인 Jpeg 또는 Tiff 이미지여야 합니다. 사용법을 보여주는 샘플 코드는 다음과 같습니다:



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **PSD 리소스에서 썸네일 추출하기**
썸네일은 전체 프레임 대신 사진의 중요한 부분을 표시하는 데 사용되는 크기가 줄어든 이미지입니다. 일부 이미지 파일(특히 디지털 카메라로 촬영된 이미지)에는 파일에 내장된 썸네일 이미지가 있습니다. Aspose.PSD API를 사용하여 PSD 리소스에 포함된 썸네일을 추출하고 별도로 디스크에 저장할 수 있습니다. 썸네일 리소스에는 썸네일 데이터를 검색할 수 있는 ExifData.[Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) 속성이 있습니다. 아래 제공된 코드 스니펫은 이를 사용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


위에서 설명한 방법을 사용하여 썸네일을 다른 지원되는 파일 형식에 저장하실 수 있습니다. 썸네일 데이터를 BMP 및 PNG과 같은 다른 이미지 형식으로 내보내려는 경우 다른 이미지 내보내기 옵션을 사용하실 수 있습니다.


### **JFIF 세그먼트에서 썸네일 추출하기**
PSD 썸네일 리소스의 ExifData 또는 JFIF 세그먼트에서 썸네일을 추출하는 것도 가능합니다. 다음 코드는 JFIF 또는 ExifData 세그먼트에서 썸네일 데이터 추출하는 방법을 보여줍니다:


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


위에서 설명한 방법을 사용하여 썸네일을 다른 지원되는 파일 형식에 저장하실 수 있습니다. 썸네일 데이터를 BMP 및 PNG과 같은 다른 이미지 형식으로 내보내려는 경우 다른 이미지 내보내기 옵션을 사용하실 수 있습니다.
### **JFIF 세그먼트에 썸네일 추가하기**
아래 코드 스니펫은 로드된 PSD 이미지의 JFIF 세그먼트에 썸네일 이미지를 추가하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

JPEG 형식 사양으로 인해 다른 세그먼트 데이터와 함께 썸네일 이미지는 65,545 바이트를 초과할 수 없습니다. 대형 이미지를 썸네일로 설정해야 하는 경우 예외가 발생할 수 있습니다.


### **EXIF 세그먼트에 썸네일 추가하기**
아래 코드 스니펫에서는 로드된 PSD 이미지의 EXIF 세그먼트에 썸네일 이미지를 추가하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


이 경우 Aspose.PSD API는 썸네일 이미지 크기를 추정할 수 없지만 전체 EXIF 데이터 세그먼트 크기를 확인할 수 있습니다. 이 값은 65,535 바이트를 초과할 수 없습니다.
## **Jpeg EXIF 태그를 읽고 수정하기 위해 JpegExifData 클래스 사용하기**
Aspose.PSD API는 Jpeg 이미지 형식에 대해 독점적인 [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) 클래스를 제공하여 EXIF 정보를 검색하고 업데이트할 수 있습니다. 본 문서는 JpegExifData 클래스를 사용하여 동일한 결과를 달성하는 방법을 보여줍니다. Aspose.PSD.Exif.JpegExifData 클래스는 Jpeg 이미지를 위한 EXIF 데이터 컨테이너로 작용하며 아래에서 설명하는 방법으로 표준 Jpeg EXIF 태그를 검색하는 수단을 제공합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **전체 EXIF 태그 목록**
위의 코드 스니펫은 Aspose.PSD.Exif.JpegExifData 클래스가 제공하는 속성을 사용하여 몇 가지 EXIF 태그를 읽습니다. 이러한 속성의 전체 목록은 여기에서 확인하실 수 있습니다. 다음 코드는 [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) 클래스를 사용하여 모든 EXIF 태그를 읽습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **JPEG 이미지의 방향 자동 보정하기**


사진은 카메라가 90°, 180°, 270° 또는 없음(보통 방향)으로 회전한 상태로 촬영될 수 있습니다. 대부분의 디지털 카메라는 JEPG 이미지의 EXIF 태그로 방향 정보를 저장합니다. 이 정보를 사용하여 이미지의 방향을 자동으로 보정하여 이미지를 수정할 수 있습니다. Aspose.PSD APIs는 .NET용 JpegImage 클래스의 AutoRotate 메서드를 제공하여 JPEG 이미지의 방향을 자동으로 보정하는 기능을 제공합니다. Aspose.PSD를 사용하여 JPEG 이미지의 방향을 자동으로 보정하는 방법은 다음과 같습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.cs" >}}
## **JPEG-LS의 CMYK 및 YCCK 지원**


Aspose.PSD for .NET API는 JPEG-LS에서 CMYK 및 YCCK 색상 모델을 지원합니다. 아래 코드 스니펫은 JPEG-LS에 대한 해당 지원을 사용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportForJPEG_LSWithCMYK-SupportForJPEG_LSWithCMYK.cs" >}}
## **JPEG-LS 이미지에서 2-7비트 매수 지원**


Aspose.PSD for .NET API는 2-7비트 매수 JPEG-LS 이미지를 지원합니다. 아래 코드 스니펫은 JPEG-LS에 대한 해당 지원을 사용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-SupportFor2-7BitsJPEG-SupportFor2_7BitsJPEG.cs" >}}
## **JPEG 이미지의 ColorType 및 CompressionType 설정하기**




Aspose.PSD for .NET API는 JPEG 이미지 파일에 대한 Color Type 및 Compression Type을 설정할 수 있으며 이를 그레이스케일 및 프로그레시브로 설정할 수 있습니다. 다음 코드 스니펫은 해당 지원을 사용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ColorTypeAndCompressionType-ColorTypeAndCompressionType.cs" >}}





아래 코드 스니펫에서는 로드된 PSD 이미지의 EXIF 세그먼트에 썸네일 이미지를 추가하는 방법을 보여줍니다.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

이 경우 Aspose.PSD API는 썸네일 이미지 크기를 추정할 수 없지만 전체 EXIF 데이터 세그먼트 크기를 확인할 수 있습니다. 이 값은 65,535 바이트를 초과할 수 없습니다.
