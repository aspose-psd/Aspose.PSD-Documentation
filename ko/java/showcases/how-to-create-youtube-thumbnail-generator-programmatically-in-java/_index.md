---
title: 자바에서 YouTube 섬네일 생성기를 프로그래밍 방식으로 생성하는 방법
type: docs
weight: 10
url: /ko/java/how-to-create-youtube-thumbnail-generator-programmatically-in-java/
---

## **소개**
이 문서의 목적은 [Aspose.PSD for Java](https://products.aspose.com/psd/java)의 일부 복합 도구 API 사용을 실제 예제로 보여주는 것입니다. 이 기사에서는 **DW Documentary** 채널을 위한 **YouTube 섬네일을 생성하는 단순한 자바 프로그램**을 작성하고 설명할 것입니다. 이 채널은 섬네일이 꽤 표준적이어서 몇 가지 인기 있는 Aspose.PSD for Java의 복합 도구 사용법을 설명해줍니다 (예: [그림자 효과](/psd/ko/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), 방사형 그라디언트 채우기, 텍스트 및 모양 그리기):

![할 일:이미지 대체 텍스트](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **핵심 동작**
단순한 자바 프로그램은 캡션과 이미지를 입력으로 받아들입니다. Aspose.PSD for Java를 사용하여 그 입력으로부터 **인메모리 Photoshop 문서 (PSD)가 생성**됩니다. 이후, 프로그램은 문서를 PSD에서 PNG 파일 형식으로 변환하여 1280x720 픽셀 크기의 YouTube 섬네일을 얻습니다. 출력 이미지는 다음과 유사합니다:

![할 일:이미지 대체 텍스트](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **기술 요구 사항**
이 기사의 코드를 실행하는 데 성공하려면 다음 기술이 필요합니다:

- Java 6+
- [Aspose.PSD for Java](/psd/ko/java/installation/) (최신)

## **시작하기**
이미 언급했듯이, 프로그램은 섬네일 생성을 위해 인메모리 PSD를 사용합니다. 그러므로, 우리는 **PSD 문서를 생성**해야 합니다:

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

위의 YouTube 섬네일을 자세히 살펴보면 다음과 같은 여러 구성 요소로 구성되어 있음을 알 수 있습니다:

1. 배경 이미지 (인쇄된 마스크)
2. 방사형 PSD 그라디언트 (오른쪽 상단 부분을 강조)
3. 그림자 효과가 적용된 로고
4. 캡션 및 간단한 그리기 (파란색 사각형)

다음 섹션에서 Aspose.PSD for Java를 사용하여 각 구성 요소를 구현하는 방법을 자세히 살펴봅시다.

## **1. 배경 이미지 추가**
레이어의 순서가 중요합니다. 따라서 다른 레이어를 가리지 않도록 배경 이미지를 먼저 추가해야 합니다. 현재 래스터 파일 형식만 지원됩니다. 

### **1.1. Photoshop 레이어에 배경 이미지 추가**
PSD에 **래스터 이미지를 추가**하려면 계층 생성 중에 입력 스트림을 전달해야 합니다 (더 많은 [래스터 이미지 로딩 예제](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images) 참조):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

### **1.2. 배경 이미지를 캔버스에 맞추기**
다음 두 가지 작업(크기 조정, 위치 설정)은 **이미지 크기가 캔버스 크기와 다른 경우** 유용하지만, 이 기사의 이미지는 캔버스와 같은 크기이기 때문에 다르지 않습니다 (이런 경우가 항상 그렇지 않을 것으로 가정합니다).

로드된 이미지가 **캔버스 크기에 맞는지 확인**하십시오 ([크기 조정 예제](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages) 참조):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

크기 조정 후 이미지 위치가 변경됩니다. 따라서, 이미지의 위치를 초기화하여 크기 조정된 이미지를 왼쪽 상단 모서리로 이동하십시오:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}

## **2. 방사형 그라디언트 추가**
방사형 그라디언트를 추가하는 두 가지 방법이 있습니다:

- 기존 레이어에 대한 [그라디언트 오버레이 효과](/psd/ko/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163)使用하기 (현재 레이어에 바인딩되는 그라디언트 효과 및 콘텐츠에 적용)
- 새로운 [그라디언트 채우기 레이어](/psd/ko/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill) 추가하기 (독립적인 그라디언트의 구성을 유지하는 별도 레이어)

이 예제에서는 그라디언트 오버레이 효과를 사용하는 것으로 충분합니다. 그러나 이 기사를 더 흥미롭게하고 유용하게 만들기 위해 **그라디언트 채우기 레이어가 사용**됩니다. 왜냐하면 모든 레이어 효과가 유사하게 적용되기 때문이며 다음 섹션에서 다른 레이어 효과를 사용합니다.

### **2.1. 방사형 그라디언트 채우기 레이어 추가**
새로운 그라디언트 채우기 레이어를 추가하는 프로세스는 다음 2 단계로 구성됩니다:

1. 그라디언트 채우기 설정을 **선언**해야 합니다. 사전 정의된 구성이 없는 경우 필요한 최소 구성은 다음과 같습니다 (그라디언트 유형, 스케일, 색상 및 투명도 포인트가 필수 속성임):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

위의 설정은 가장자리를 투명하게 하고 중앙이 짙은 파란색인 방사형 그라디언트를 선언합니다. 그라디언트 위치는 기본적으로 캔버스의 중앙에 있습니다.

그라디언트 채우기를 반전하고 약간 오른쪽 상단 모서리로 이동하려면 해당 선택적 속성을 사용하세요:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

2. 구성이 완료되면 PSD에 그라디언트 채우기 레이어와 해당 설정을 추가합니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}

## **로그로티프와 그림자 추가하기**
**드롭 그림자**는 개체 주위의 윤곽에 사용자 정의 그림자를 추가할 수 있는 효과입니다 (이미지, 텍스트 등).
### **3.1. Photoshop 레이어에 로고 추가**
1.1. 섹션에서 사용한 것과 동일한 방법을 사용하여 PSD에 로고를 추가할 수 있습니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
### **3.2. 로고 위치 조정**
로드된 이미지는 기본적으로 왼쪽 상단에 근접합니다. 그러나 채널에서 원본 YouTube 섬네일과 유사하게 보이기 위해 일부 **여백을 추가**해야 합니다. 따라서 이미지 위치는 레이어의 가장자리에서 멀어져야 합니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
### **3.3. 로고에 드롭 그림자 효과 추가**
밝은 배경 이미지가 사용된 경우 로고가 보이지 않을 수 있습니다. 따라서 로고에 **드롭 그림자 효과를 추가**하는 것이 좋습니다. 블렌딩 옵션 속성을 통해 로고에 그림자를 추가합니다 ([그림자 예제](/psd/ko/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect) 참조):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-9.java" >}}

드롭 그림자 효과는 기본 구성 때문에 필수 속성이 없습니다 (Photoshop의 것처럼 보입니다). 그러나 위의 그림자는 투명한 테두리를 가진 테두리가 흐리게 보이도록 수정되었습니다.        

## **4. 텍스트 및 모양 그리기 추가**
### **3.1. 그래픽 레이어 만들기**
그림은 일반 레이어로 직접 지원되지 않습니다. 따라서 레이어 옆에 사용되는 **그림 API를 제공**하기 위해 그래픽 엔진을 사용합니다 ([그림 예제](/psd/ko/java/drawing-images-using-graphics/) 참조):

```java
Layer graphicLayer = psdImage.addRegularLayer();
Graphics graphics = **new** Graphics(graphicLayer);
```

### **3.2. 여러 줄 텍스트 그리기**
경험 많은 독자는 텍스트 레이어를 사용하여 텍스트를 추가하는 것이 훨씬 더 좋다고 말할 수 있습니다. 그러나 이 경우에는 텍스트 편집이 필요하지 않기 때문에 PSD는 매번 새로 생성됩니다; [텍스트 API](https://docs.aspose.com/display/psdnet/Working+With+Text+Layers)는 폰트 사용자 정의를 아직 지원하지 않습니다(v20.6시점). 원하는 폰트를 쉽게 **지정하여 텍스트를 그릴 수** 있지만 텍스트 라인 수에 따라 자동으로 높이가 변하는 사각형을 만드는 것은 조금 더 어렵습니다. 모든 라인의 정확한 높이를 먼저 계산해야 합니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-10.java" >}}

여기서 1.15는 라인 높이를, 3은 텍스트 간격을 나타냅니다.

### **3.3. 사각형 그리기**
사각형은 그림자 브러시와 함께 그리는 것도 쉽습니다 (그리기할 영역과 색상 범위를 설정하기만 하면 됩니다). 텍스트의 높이가 알려진 경우 사각형의 크기 및 위치가 계산됩니다. **변형된 직사각형을 그리려면** **psd에 채워진 사각형을 그리세요** (프레임만 그리는 것이 아님) 모든 것을 포함하여 그림 엔진의 해당 메서드를 호출합니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-11.java" >}}

이때 40, 15, 25은 들여쓰기를 나타냅니다.

## **결과**
따라서 섬네일의 모양이 완성되었습니다. 이제 섬네일을 래스터 파일 형식(PNG 등)으로 **내보내기** 위해 시간이 됐습니다:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-12.java" >}}

## **결론**
이 기사에서는 DW Documentary 채널을 위한 YouTube 섬네일 생성기를 만들고, 그림자 효과, 방사형 그라디언트 채우기, 텍스트 그리기와 모양 그리기와 같은 인기 있는 복합 도구 사용법을 설명했습니다.

## **전체 예시**
[Aspose.PSD SDK 다운로드](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator.java" >}}