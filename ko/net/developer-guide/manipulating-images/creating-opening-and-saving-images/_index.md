---
title: 이미지 만들기, 여는 방법 및 저장하기
type: 문서
weight: 30
url: /ko/net/creating-opening-and-saving-images/
---

## **이미지 파일 만들기**
Aspose.PSD for .NET을 사용하면 개발자는 자체 이미지를 만들 수 있습니다. Image 클래스에 의해 노출된 정적 Create 메서드를 사용하여 새 이미지를 만들 수 있습니다. 원하는 출력 이미지 형식을 위해 ImageOptions 네임스페이스 중 하나의 클래스 개체를 제공하면 됩니다. 이미지 파일을 만들려면 먼저 ImageOptions 네임스페이스 중 하나의 클래스의 인스턴스를 만들어야 합니다. 이러한 클래스는 출력 이미지 형식을 결정합니다. ImageOptions 네임스페이스에서 일부 클래스는 다음과 같습니다 (현재 PSD 파일 형식 패밀리만 작성되는 것에 유의하십시오):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions)는 PSD 파일을 생성하는 옵션을 설정합니다. 이미지 파일은 출력 경로를 설정하거나 스트림을 설정하여 만들 수 있습니다.
### **경로 설정으로 만들기**
[ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) 네임스페이스에서 PsdOptions를 만들고 다양한 속성을 설정합니다. 설정해야 할 가장 중요한 속성은 Source 속성입니다. 이 속성은 이미지 데이터가 어디에 있는지 지정합니다 (파일에 있는지 또는 스트림에 있는지). 아래 예시에서는 소스가 파일입니다. 속성을 설정한 후 해당 개체를 폭(width) 및 높이(height) 매개변수와 함께 정적 [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) 메서드 중 하나로 전달하십시오. 폭과 높이는 픽셀로 정의됩니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **스트림을 사용하여 만들기**
스트림을 사용하여 이미지를 만드는 과정은 경로를 사용하는 것과 동일합니다. 유일한 차이점은 [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource)의 인스턴스를 생성해야 한다는 것입니다. 이를 위해 Stream 객체를 전달하여 StreamSource의 생성자에 할당하고 Source 속성에 할당하십시오.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **이미지 파일 열기**
개발자는 다양한 목적으로 Aspose.PSD for .NET API를 사용하여 PSD 이미지 파일을 열 수 있습니다. 이미지에 효과를 추가하거나 기존 파일을 다른 형식으로 변환하는 등의 목적에 사용할 수 있습니다. Aspose.PSD는 파일을 열기 위해 두 가지 표준 방법을 제공합니다: 파일로부터 또는 스트림으로부터.
### **디스크에서 열기**
Image 클래스에 의해 노출되는 정적 Load 메서드에 이미지 파일의 경로 및 파일 이름을 매개변수로 전달하여 이미지 파일을 엽니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **스트림 사용하여 열기**
열어야 할 이미지가 스트림으로 저장된 경우도 있습니다. 이러한 경우에는 Load 메서드의 오버로드된 버전을 사용하십시오. 이는 이미지를 열기 위해 Stream 객체를 인수로 수락합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **레이어로 이미지 로드**
이 기사는 이미지를 레이어로 로드하기 위한 Aspose.PSD 사용법을 보여줍니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이고 사용하기 쉬운 방법을 노출하고 있습니다. Aspose.PSD는 PsdImage 클래스의 AddLayer 메서드를 노출하여 PSD 파일에 이미지를 레이어로 추가합니다.

PSD에 이미지를 레이어로 로드하는 단계는 다음과 같습니다:

- 지정된 폭과 높이를 가진 PsdImage 클래스의 이미지 인스턴스를 만드십시오.
- Image 클래스에 의해 노출된 Load 팩토리 메서드를 사용하여 이미지로 PSD 파일을 로드하십시오.
- Layer 클래스의 인스턴스를 만들고 PSD 이미지 레이어를 할당하십시오.
- PsdImage 클래스에 의해 노출된 AddLayer 메서드를 사용하여 생성된 레이어를 추가하십시오.
- 결과를 저장하십시오.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **스트림으로부터 레이어로 이미지 로드**
이 기사는 Aspose.PSD를 사용하여 스트림으로부터 이미지를 레이어로 로드하는 방법을 보여줍니다. 이미지를 스트림으로부터 로드하려면 이미지를 포함하는 스트림 개체를 Layer 클래스 생성자에 전달하면 됩니다. PsdImage 클래스에 의해 노출된 AddLayer 메서드를 사용하여 생성된 레이어를 추가하고 결과를 저장하십시오.


다음은 샘플 코드입니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **이미지 파일 저장하기**
Aspose.PSD를 사용하면 처음부터 이미지 파일을 만들 수 있습니다. 기존 이미지 파일을 편집하는 수단도 제공합니다. 이미지가 만들어지거나 수정된 후 파일은 일반적으로 디스크에 저장됩니다. Aspose.PSD는 이미지를 경로를 지정하거나 Stream 객체를 사용하여 디스크에 저장하는 메서드를 제공합니다.
### **디스크에 저장하기**
Image 클래스는 이미지 개체를 나타내므로 Image 클래스는 이미지를 만들고 로드하고 저장하는 데 필요한 모든 도구를 제공합니다. 이미지를 저장하려면 Image 클래스의 Save 메서드를 사용하십시오. Save 메서드의 오버로드된 버전 중 하나는 파일 위치를 문자열로 수락합니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **스트림에 저장하기**
Save 메서드의 다른 오버로드된 버전은 Stream 개체를 인수로 수락하고 이미지 파일을 스트림에 저장합니다.

이미지를 Image 생성자 내의 CreateOptions 중 하나를 지정하여 생성한 경우 Image 클래스의 초기화 중에 제공된 경로 또는 스트림으로 이미지가 자동으로 저장되며 매개변수를 수락하지 않는 Save 메서드를 호출하면 됩니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **누락된 글꼴 대체 설정**
개발자는 Aspose.PSD for .NET API를 사용하여 다양한 목적으로 기존 PSD 이미지 파일을 로드할 수 있습니다. 예를 들어 PSD 문서를 래스터 이미지(여기서는 PNG, JPG 및 BMP 형식)로 저장할 때 누락된 글꼴에 대한 기본 글꼴 이름을 설정할 수 있습니다. 이 기본 글꼴은 모든 누락된 글꼴(현재 운영 체제에 포함되어 있지 않은 글꼴)에 대한 대체로 사용될 것입니다. 이미지가 수정된 후 결과는 디스크에 저장될 것입니다.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
