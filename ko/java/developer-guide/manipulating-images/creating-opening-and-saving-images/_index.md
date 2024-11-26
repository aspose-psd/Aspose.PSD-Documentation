---
title: 이미지 만들기, 열기 및 저장하기
type: docs
weight: 30
url: /ko/java/creating-opening-and-saving-images/
---

## **이미지 파일 만들기**
Aspose.PSD for Java을 사용하면 개발자가 고유한 이미지를 만들 수 있습니다. Image 클래스에서 노출된 정적 Create 메서드를 사용하여 새 이미지를 만들 수 있습니다. 원하는 출력 이미지 형식을 위해 ImageOptions 네임스페이스 중 하나의 클래스의 적절한 개체를 공급하기만 하면 됩니다. 이미지 파일을 만들려면 먼저 ImageOptions 네임스페이스 중 하나의 클래스의 인스턴스를 만듭니다. 이러한 클래스들은 출력 이미지 형식을 결정합니다. 아래는 ImageOptions 네임스페이스에서 몇 가지 클래스입니다 (현재 PSD 파일 형식 패밀리만 지원됨을 유의하십시오):

PsdOptions은 PSD 파일을 만들 시 옵션을 설정합니다. 이미지 파일은 출력 경로를 설정하거나 스트림을 설정하여 만들 수 있습니다.
### **경로 설정으로 만들기**
ImageOptions 네임스페이스에서 PsdOptions를 만들고 다양한 속성을 설정합니다. 설정해야 하는 가장 중요한 속성은 Source 속성입니다. 이 속성은 이미지 데이터가 어디에 있는지를 지정합니다(파일 또는 스트림). 아래 예제에서는 소스가 파일입니다. 속성을 설정한 후에는 속성을 지정하고 폭과 높이 매개변수와 함께 정적 Create 메서드 중 하나에 개체를 전달합니다. 폭과 높이는 픽셀로 정의됩니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **스트림 사용하여 만들기**
스트림을 사용하여 이미지를 만드는 프로세스는 경로를 사용하는 것과 동일합니다. 유일한 차이점은 StreamSource 인스턴스를 만들어 스트림 개체를 생성하고 Source 속성에 할당해야 한다는 점입니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **이미지 파일 열기**
개발자는 다양한 목적으로 기존 PSD 이미지 파일을 열거나 이미지에 효과를 추가하거나 기존 파일을 다른 형식으로 변환하는 등의 작업을 할 수 있습니다. 무슨 목적으로 하든 Aspose.PSD는 기존 파일을 열기 위해 두 가지 표준 방법을 제공합니다: 파일로부터 또는 스트림으로부터.
### **디스크에서 열기**
이미지 파일을 Image 클래스에 의해 노출된 정적 Load 메서드에 경로와 파일 이름을 매개변수로 전달하여 엽니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **스트림 사용하여 열기**
때로는 열어야 하는 이미지가 스트림으로 저장되어 있습니다. 이러한 경우 Load 메서드의 오버로드된 버전을 사용합니다. 이 메서드는 이미지를 열기 위해 Stream 개체를 인수로 받습니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **레이어로 이미지 로드**
이 문서에서는 이미지로 레이어를 로드하는 Aspose.PSD의 사용법을 보여줍니다. Aspose.PSD API는 이 목표를 달성하기 위한 효율적이고 쉽게 사용할 수 있는 방법을 노출합니다. Aspose.PSD는 PsdImage 클래스의 AddLayer 메서드를 노출하여 이미지를 PSD 파일에 레이어로 추가할 수 있습니다.

PSD로 이미지를 레이어로 로드하는 단계는 다음과 같습니다:

- 지정된 너비와 높이를 가진 PsdImage 클래스의 이미지 인스턴스를 만듭니다.
- Image 클래스에 의해 노출된 팩토리 메서드 Load를 사용하여 이미지로 PSD 파일을로드합니다.
- Layer 클래스의 인스턴스를 만들고 PSD 이미지 레이어를 할당합니다.
- PsdImage 클래스에서 노출된 AddLayer 메서드를 사용하여 생성된 레이어를 추가합니다.
- 결과를 저장합니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}
## **이미지 파일 저장**
Aspose.PSD를 사용하면 이미지 파일을 처음부터 만들 수 있습니다. 기존 이미지 파일을 편집하는 수단도 제공합니다. 이미지가 만들어지거나 수정된 후 파일은 일반적으로 디스크에 저장됩니다. Aspose.PSD는 이미지를 경로를 지정하거나 Stream 개체를 사용하여 디스크에 저장하는 방법을 제공합니다.
### **디스크에 저장하기**
이미지 클래스는 이미지 개체를 나타냅니다. 따라서 이 클래스는 이미지 파일을 만들고 로드하고 저장하는 데 필요한 모든 도구를 제공합니다. 이미지를 저장하기 위해 Image 클래스의 Save 메서드를 사용합니다. Save 메서드의 오버로드된 버전 중 하나는 파일 위치를 문자열로 수락합니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **스트림으로 저장하기**
Save 메서드의 다른 오버로드 버전은 Stream 개체를 인수로 받아 이미지 파일을 스트림에 저장합니다.

이미지가 Image 클래스의 초기화 중에 제공된 경로 또는 스트림으로 자동 저장되도록 Image 클래스의 초기화 중에 제공된 CreateOptions 중 하나를 지정하여 이미지가 작성된 경우, Save 메서드를 호출하여 매개변수를 수락하지 않는 Save 메서드를 사용하면 됩니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **없는 글꼴 대체 설정**
개발자는 기존 PSD 이미지 파일을 로드하고 여러 목적으로 사용할 수 있습니다. 예를 들어 PSD 문서를 래스터 이미지(파일 형식을 PNG, JPG 및 BMP로)로 저장할 때 기본 글꼴 이름을 설정할 수 있습니다. 이 기본 글꼴은 모든 누락된 글꼴(현재 운영 체제에서 찾을 수 없는 글꼴)에 대한 대체로 사용해야 합니다. 이미지가 수정된 후 파일은 디스크에 저장됩니다.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}


