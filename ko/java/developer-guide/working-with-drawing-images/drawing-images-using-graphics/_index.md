---
title: 그래픽을 사용하여 이미지 그리기
type: docs
weight: 20
url: /ko/java/drawing-images-using-graphics/
---

## **그래픽을 사용하여 이미지 그리기**

Aspose.PSD 라이브러리를 사용하면 선, 직사각형, 원과 같은 간단한 모양뿐만 아니라 다각형, 곡선, 호 및 베지어 모양과 같은 복잡한 모양을 그릴 수 있습니다. Aspose.PSD 라이브러리는 Aspose.PSD 네임스페이스에 속하는 Graphics 클래스를 사용하여 이러한 모양을 생성합니다. Graphics 객체는 이미지의 표면을 변경하여 다양한 그리기 작업을 수행하는 역할을 합니다. Graphics 클래스는 다양한 도우미 객체를 사용하여 모양을 향상시킵니다:

- Pens: 선을 그리거나 모양의 윤곽 또는 다른 기하학적 표현을 렌더링합니다.
- Brushes: 영역을 채우는 방법을 정의합니다.
- Fonts: 텍스트 문자의 모양을 정의합니다.

### **Graphics 클래스로 그리기**

아래는 Graphics 클래스 사용을 보여주는 코드 예제입니다. 예제 소스 코드는 단순하고 따르기 쉽도록 각 부분으로 분할되었습니다. 여러 예제는 다음을 보여줍니다:

1. 이미지 생성
1. Graphics 객체 생성 및 초기화
1. 표면 지우기
1. 타원 그리기
1. 채워진 다각형 그리기 및 이미지 저장

### **프로그래밍 샘플**

#### **이미지 생성**

Creating Files에서 설명된 방법을 사용하여 이미지를 생성하는 것으로 시작하십시오.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}

#### **Graphics 객체 생성 및 초기화**

그런 다음 Image 객체를 그 생성자에 전달하여 Graphics 객체를 생성하고 초기화합니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}

#### **표면 지우기**

Graphics 클래스의 Clear 메서드를 호출하고 매개 변수로 색상을 전달하여 Graphics 표면을 지우십시오. 이 메서드는 전달된 색상으로 Graphics 표면을 채웁니다.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

#### **타원 그리기**

Graphics 클래스에는 모양을 그리고 채우는 데 사용할 수 있는 많은 메서드가 노출되어 있음을 알 수 있습니다. Aspose.PSD for Java API 참조에서 모든 메서드의 전체 목록을 확인할 수 있습니다. Graphics 클래스에 의해 노출된 DrawEllipse 메서드의 여러 오버로드된 버전이 있음을 발견할 수 있습니다. 이 메서드는 첫 번째 인수로 Pen 객체를 수락합니다. 나중의 매개변수는 타원 주변의 경계 직사각형을 정의하기 위해 전달됩니다. 이 예제를 위해 원하는 색상으로 Pen 객체를 사용하여 타원을 그리기 위해 두 번째 매개변수로 Rectangle 객체를 수락하는 버전을 사용하십시오.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}

#### **채워진 다각형 그리기**

그런 다음 LinearGradientBrush 및 점 배열을 사용하여 다각형을 그립니다. Graphics 클래스에는 여러 오버로드된 FillPolygon 메서드가 노출되어 있습니다. 이들은 모두 채우기의 특성을 정의하는 Brush 객체를 첫 번째 인수로 수락합니다. 두 번째 매개변수는 점 배열입니다. 배열에서 모든 연속된 두 점이 다각형의 한 변을 지정함을 주의하십시오.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

### **그래픽을 사용하여 이미지 그리기: 전체 소스**

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

모든 IDisposable을 구현하고 관리되지 않은 리소스에 액세스하는 클래스는 올바르게 폐기되도록 [Using 문] (https://docs.microsoft.com/ko/dotnet/csharp/language-reference/keywords/using)에서 인스턴스화됩니다.

