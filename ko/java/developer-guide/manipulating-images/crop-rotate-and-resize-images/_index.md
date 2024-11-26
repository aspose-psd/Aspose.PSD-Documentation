---
title: 이미지 자르기, 회전 및 크기 조정
type: docs
weight: 40
url: /ko/java/crop-rotate-and-resize-images/
---

## **이미지 자르기**
이미지 자르기는 일반적으로 이미지의 외부 부분을 잘라내어 구도를 개선하는 것을 의미합니다. 자르기는 또한 이미지의 특정 영역에 초점을 맞추기 위해 이미지의 일부를 잘라내는 데 사용될 수 있습니다. Aspose.PSD API는 이미지 자르기를 위해 두 가지 다른 방법을 지원합니다: 이동 및 사각형.
### **이동으로 자르기**
RasterImage 클래스는 좌, 우, 위 및 아래를 나타내는 4개의 정수 값을 인수로받는 Crop 메서드의 오버로드된 버전을 제공합니다. 이 네 가지 값에 따라 Crop 메서드는 이미지 경계를 이미지의 중심쪽으로 이동시키면서 외부 부분을 삭제합니다. 아래 코드 스니펫은 이동으로 이미지를 자르는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **사각형으로 자르기**
RasterImage 클래스는 사각형 클래스의 인스턴스를 인수로받는 Crop 메서드의 다른 오버로드된 버전을 제공합니다. 사각형 객체에 원하는 경계를 제공하여 이미지의 어떤 부분이든 잘라낼 수 있습니다. 아래 코드 스니펫은 사각형으로 이미지를 자르는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **이미지 회전 및 뒤집기**
Java용 Aspose.PSD는 복잡한 작업을 수행할 수 있는 간단한 방법을 제공하기 때문에 쉽게 사용할 수 있는 라이브러리입니다. 예를 들어, 이미지를 회전해야 하는 경우 Aspose.PSD for Java는 이미지를 회전하기 위해 RotateFlip 메서드를 제공했습니다. 이미지 형식과 관계없이 라이브러리는 특정 회전 및 뒤집기 절차를 수행할 수 있습니다.
### **이미지 회전**
Image.RotateFlip 메서드를 사용하면 이미지를 90/180/270도 회전하고 이미지를 수평 또는 수직으로 뒤집을 수 있습니다. Image.RotateFlip 메서드는 이미지에 적용할 회전 및 뒤집기 유형을 지정하는 RotateFlipType 매개변수를 사용합니다. 회전 및 뒤집기를 수행하기 위한 단계는 아래와 같이 간단합니다.

1. Image 클래스에서 노출된 팩토리 메서드 Load를 사용하여 이미지를 로드합니다.
1. 적절한 RotateFlipType을 지정하면서 Image.RotateFlip 메서드를 호출합니다.
1. 결과를 저장합니다.

다음 코드 예제는 Image의 RotateFlip 속성 및 RotateFlipType 열거형 설정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **특정 각도로 이미지 회전**
Aspose.PSD for Java API는 특정 각도로 이미지를 회전하려는 사용자를 위해 RasterImage.Rotate 메서드를 노출합니다. RasterImage.RotateFlip 메서드와 달리, RasterImage.Rotate 메서드는 세 가지 매개변수를​​받습니다:

1. 회전 각도: 이미지를 회전해야 하는 회전 각도를 지정하는 부동 소수점형 매개변수입니다. 양수 값은 이미지를 시계 방향으로 회전하고 음수 값은 반시계 방향으로 회전합니다.
1. 비례 조정: 부울 형식 매개변수는 이미지 크기가 회전된 사각형 (코너 포인트)의 투영에 따라 변경되어야 하는지 여부를 지정합니다. false로 설정하면 이미지 크기는 변경되지 않고 내부 이미지 콘텐츠만 회전됩니다.
1. 배경 색상: Color 형식의 매개변수는 회전된 이미지의 배경에 채울 색상을 지정합니다.

아래 코드 스니펫은 RasterImage.Rotate 메서드의 사용 예시를 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **이미지 크기 조정**
본 문서는 Aspose.PSD for Java를 사용하여 이미지 크기 조정 작업을 수행하는 방법을 보여줍니다. Aspose.PSD API는 이러한 목표를 달성하기 위해 효율적이고 사용하기 쉬운 메서드를 노출했습니다. Java용 Aspose.PSD는 이미지 크기를 실시간으로 조정하는 데 사용할 수 있는 Image 클래스의 Resize 메서드를 제공합니다. 응용 프로그램 요구에 맞게 Resize 메서드의 두 가지 오버로드가 있습니다.
### **간단한 크기 조정**
크기 조정을 수행하는 단계는 다음과 같습니다:

1. Image 클래스가 노출하는 Load 팩토리 메서드를 사용하여 이미지를 로드합니다.
1. Image.Resize 메서드를 호출하면서 새 높이 및 너비를 지정합니다.
1. 결과를 저장합니다.

다음 코드 예제는 이미지 크기를 조정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **ResizeType 열거형으로 크기 조정**
Aspose.PSD API는 Image.Resize와 함께 사용할 수 있는 ResizeType 열거형을 노출했습니다. 아래 코드 스니펫은 ResizeType 열거형의 사용법을 보여주며, ResizeType 열거형 멤버의 자세한 정보는 이 페이지 하단에서 확인할 수 있습니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}

크기를 조정한 후 품질 결과를 얻고자 한다면 언제나 ResizeType.LanczosResample을 사용하는 것이 좋습니다. 이 방법은 품질 높은 결과물을 출력하나 ResizeType.NearestNeighbourResample에 비해 작업 시간이 느릴 수 있습니다. 반면 ResizeType.NearestNeighbourResample 알고리즘은 이미지 품질에 조금 희생함으로써 빠르게 크기를 조정하는 데 사용됩니다. 이 방법은 섬네일 생성 또는 성능이 필요한 실시간 작업과 같은 프로세스에서 유용할 수 있습니다.
## **이미지 비율에 맞춰 크기 조정**
새로운 높이와 너비 값을 Image.Resize 메서드의 매개변수로 전달하여 이미지의 크기를 조정할 수 있지만, 이 경우 종횡비를 직접 계산해야 합니다. 이미지의 너비 또는 높이가 변경되면 이미지가 새 크기를 채우기 위해 확대되거나 축소됩니다. 이미지의 너비와 높이 변경이 비율적으로 이루어지지 않으면 늘어난 이미지 또는 왜곡된 결과를 가져올 수 있습니다. 본 문서는 Java용 Aspose.PSD API를 사용하여 새로운 높이 또는 너비를 전달하면서 이미지 크기를 자동으로 계산하도록 허용하여 이미지 크기를 조정하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType 열거형**
ResizeType는 선택된 필터를 기반으로 이미지에서 수행할 크기 조정 유형을 결정합니다.

ResizeType 열거형 멤버

|**멤버 이름**|**값**|**설명**|
| :- | :- | :- |
|LeftTopToLeftTop|0|새 이미지의 왼쪽 상단 지점이 원본 이미지의 왼쪽 상단 지점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|RightTopToRightTop|1|새 이미지의 오른쪽 상단 지점이 원본 이미지의 오른쪽 상단 지점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|RightBottomToRightBottom|2|새 이미지의 오른쪽 하단 지점이 원본 이미지의 오른쪽 하단 지점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|LeftBottomToLeftBottom|3|새 이미지의 왼쪽 하단 지점이 원본 이미지의 왼쪽 하단 지점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|CenterToCenter|4|새 이미지의 중앙이 원본 이미지의 중앙과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|LanczosResample|5|7x7 마스크를 사용하는 Lanczos 알고리즘을 사용하여 재샘플링합니다.|
|NearestNeighbourResample|6|가장 가까운 이웃 알고리즘을 사용하여 재샘플링합니다.|

