---
title: 이미지 자르기, 회전 및 크기 조정
type: docs
weight: 40
url: /ko/net/crop-rotate-and-resize-images/
---

## **이미지 자르기**
이미지 자르기는 일반적으로 이미지의 외부 부분을 제거하여 구도를 개선하는 것을 말합니다. 자르기는 또한 이미지의 특정 부분에 초점을 맞추기 위해 이미지의 일부를 잘라내는 데 사용될 수 있습니다. Aspose.PSD API 는 이미지 자르기를 위해 두 가지 다른 방법을 지원합니다: 시프트와 직사각형.
### **시프트에 의한 자르기**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스는 왼쪽, 오른쪽, 위 및 아래를 나타내는 4 개의 정수 값을 받아들이는 Crop 메서드의 오버로드된 버전을 제공합니다. 이 네 가지 값에 기초하여, Crop 메서드는 이미지 경계를 이미지 중앙쪽으로 이동시키고 외부 부분을 제거합니다. 아래 코드 스니펫은 시프트로 이미지를 자르는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **직사각형에 의한 자르기**
[RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) 클래스는 직사각형 클래스의 인스턴스를 받아들이는 Crop 메서드의 다른 오버로드된 버전을 제공합니다. 원하는 경계를 직사각형 객체에 제공하여 이미지의 어떤 부분이든 잘라낼 수 있습니다. 아래 코드 스니펫은 직사각형에 의해 이미지를 잘라내는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **이미지 회전 및 뒤집기**
Aspose.PSD for .NET은 복잡한 작업을 수행하는 간단한 방법을 제공하기 때문에 사용하기 쉬운 라이브러리입니다. 예를 들어, 이미지를 회전해야 하는 애플리케이션의 경우 Aspose.PSD for .NET은 이미지를 회전하기 위한 RotateFlip 메서드를 제공합니다. 이미지 형식에 관계없이 라이브러리는 이미지에 특정한 회전 및 뒤집기 절차를 수행할 수 있습니다.
### **이미지 회전**
Image.RotateFlip 메서드를 사용하면 이미지를 90/180/270도 회전하고 이미지를 수평 또는 수직으로 뒤집을 수 있습니다. Image.RotateFlip 메서드는 이미지에 적용할 회전 및 뒤집기 유형을 지정하는 RotateFlipType 매개변수를 받습니다. 회전 및 뒤집기를 수행하는 단계는 아래와 같이 간단합니다.

1. Image 클래스가 노출하는 팩터리 메서드 Load를 사용하여 이미지를 로드합니다.
1. 적절한 RotateFlipType을 지정하는 Image.RotateFlip 메서드를 호출합니다.
1. 결과를 저장합니다.

다음 코드 예제는 Image의 RotateFlip 속성 및 RotateFlipType 열거형을 설정하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **특정 각도로 이미지 회전**
Aspose.PSD for .NET API는 이미지를 특정 각도로 회전하려는 사용자를 지원하기 위해 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate 메서드를 노출합니다. [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip 메서드와 달리, [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate 메서드는 세 개의 매개변수를 받습니다:

1. 회전 각도: 이미지를 회전할 각도를 지정하는 float 형식의 매개변수. 양수 값은 이미지를 시계 방향으로 회전하며, 음수 값은 반시계 방향으로 회전합니다.
1. 비율을 조정: 부울 형식의 매개변수로, 이미지 크기가 회전된 사각형(꼭짓점)의 투영에 따라 변경되어야 하는지 여부를 지정합니다. false로 설정하면 이미지 크기는 변경되지 않고 내부 이미지 내용만 회전됩니다.
1. 배경색: 회전된 이미지의 배경에 채워질 색상을 지정하는 Color 형식의 매개변수.

다음 코드 스니펫은 [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate 메서드의 사용법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **이미지 크기 조정**
이 기사는 Aspose.PSD for .NET을 사용하여 이미지 크기 조정 작업을 수행하는 방법을 보여줍니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 메서드를 노출했습니다. Aspose.PSD for .NET은 기존 이미지 크기를 동적으로 조정할 수 있는 Image 클래스의 Resize 메서드를 노출했습니다. 응용 프로그램 요구 사항에 맞는 두 가지 Resize 메서드 오버로드가 있습니다.
### **간단한 크기 조정**
크기 조정을 수행하는 단계는 아래와 같이 간단합니다.

1. Image 클래스가 노출하는 팩터리 메서드 Load를 사용하여 이미지를 로드합니다.
1. 새 높이 및 너비를 지정하는 Image.Resize 메서드를 호출합니다.
1. 결과를 저장합니다.

다음 코드 예제는 이미지 크기를 조정하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **ResizeType 열거형으로 크기 조정**
Aspose.PSD API는 Image.Resize와 함께 사용할 수 있는 ResizeType 열거형을 노출했습니다. 아래 제공된 코드 스니펫은 ResizeType 열거형의 사용법을 보여주며, ResizeType 열거형 멤버에 대한 자세한 내용은 이 페이지의 맨 아래에서 찾을 수 있습니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



리사이즈를 적용한 후 품질 결과를 얻고자 한다면 ResizeType.LanczosResample을 항상 사용하는 것이 좋습니다. 이는 매우 품질 높은 결과물을 출력하지만 ResizeType.NearestNeighbourResample보다 작동 속도가 느릴 수 있습니다. 반면 ResizeType.NearestNeighbourResample 알고리즘은 이미지 품질에 타협하면서 빠른 리사이징에 사용되며, 성능이 요구되는 썸네일 생성 또는 실시간 유사 프로세스에 유용할 수 있습니다.
## **비율에 맞게 이미지 리사이즈**
이미지를 리사이즈하려면 Image.Resize 메서드에 새 높이 및 너비 값을 매개변수로 전달해야하지만 이 경우 종횡비를 직접 계산해야 합니다. 이미지의 너비 또는 높이가 변경되면 이미지가 새 크기로 채워지거나 축소됩니다. 이미지의 너비와 높이의 변경이 비례적이지 않으면 늘어나거나 왜곡된 결과를 초래할 수 있습니다. 이 기사는 Aspose.PSD for .NET API를 사용하여 이미지의 높이 또는 너비를 전달하면 API가 다른 비례 값 자동으로 계산하도록 허용하는 방법을 보여줍니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **ResizeType 열거형**
ResizeType은 선택한 필터에 따라 이미지에 수행할 리사이징의 유형을 결정합니다.

[ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype) 열거형의 멤버

|**멤버 이름**|**값**|**설명**|
| :- | :- | :- |
|LeftTopToLeftTop|0|새 이미지의 왼쪽 상단 점은 원본 이미지의 왼쪽 상단 점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|RightTopToRightTop|1|새 이미지의 오른쪽 상단 점은 원본 이미지의 오른쪽 상단 점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|RightBottomToRightBottom|2|새 이미지의 오른쪽 하단 점은 원본 이미지의 오른쪽 하단 점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|LeftBottomToLeftBottom|3|새 이미지의 왼쪽 하단 점은 원본 이미지의 왼쪽 하단 점과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|CenterToCenter|4|새 이미지의 중앙은 원본 이미지의 중심과 일치합니다. 필요한 경우 자르기가 발생합니다.|
|LanczosResample|5|7x7 마스크를 사용하여 Lanczos 알고리즘을 사용한 리샘플링.|
|NearestNeighbourResample|6|가장 가까운 이웃 알고리즘을 사용한 리샘플링.|
