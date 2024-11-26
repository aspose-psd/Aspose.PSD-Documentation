---
title: 그래픽을 사용하여 이미지 그리기
type: docs
weight: 20
url: /ko/net/drawing-images-using-graphics/
---

## **그래픽을 사용하여 이미지 그리기**
Aspose.PSD 라이브러리를 사용하면 선, 직사각형, 원과 같은 간단한 모양 뿐만 아니라 다각형, 곡선, 호 및 베지어 모양과 같은 복잡한 모양도 그릴 수 있습니다. Aspose.PSD 라이브러리는 Aspose.PSD 네임스페이스에 속한 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스를 사용하여 이러한 모양을 생성합니다. Graphics 객체는 이미지의 표면을 변경하여 다양한 그리기 작업을 수행하는 데 책임이 있습니다. [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스는 모양을 향상시키기 위해 다양한 도우미 객체를 사용합니다:

·         Pens: 선을 그리거나 모양의 윤곽선을 정의하거나 기하학적 표현을 렌더링합니다.

·         Brushes: 영역이 채워지는 방식을 정의합니다.

·         Fonts: 문자의 모양을 정의합니다.
### **Graphics 클래스로 그리기**
아래는 [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스의 사용을 보여주는 코드 예제입니다. 예제 소스 코드는 간단하고 이해하기 쉽도록 여러 부분으로 나뉘어 있습니다. 단계별로 예제를 통해 다음을 보여줍니다:

1. 이미지 생성.
1. Graphics 객체 생성 및 초기화.
1. 표면 지우기.
1. 타원 그리기.
1. 채워진 다각형 그리고 이미지 저장.
### **프로그래밍 샘플**
#### **이미지 만들기**
먼저 Creating Files에서 설명된 방법 중 하나를 사용하여 이미지를 만드세요.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Graphics 객체 생성 및 초기화**
그런 다음 Image 객체를 Graphics 객체의 생성자에 전달하여 Graphics 객체를 만들고 초기화하세요.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **표면 지우기**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스 Clear 메서드를 호출하고 매개변수로 색상을 전달하여 그래픽 표면을 지우세요. 이 메서드는 전달된 색상으로 그래픽 표면을 채웁니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **타원 그리기**
[Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) 클래스에는 여러 모양을 그리고 채울 수 있는 많은 메서드가 노출되어 있습니다. Aspose.PSD for .NET API 참조에서 메서드의 전체 목록을 확인할 수 있습니다. Graphics 클래스에서는 DrawEllipse 메서드의 다양한 오버로드 버전이 노출되어 있습니다. 이 메서드는 첫 번째 인수로 Pen 객체를 받습니다. 후속 매개변수는 타원 주위의 경계 사각형을 정의하기 위해 전달됩니다. 이 예제에서는 원하는 색상으로 Pen 객체를 사용하여 타원을 그리기 위해 두 번째 매개변수로 Rectangle 객체를 수용하는 버전을 사용하세요.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **채워진 다각형 그리기**
다음으로 LinearGradientBrush 및 점 배열을 사용하여 다각형을 그리세요. Graphics 클래스에서는 여러 오버로드 된 버전의 FillPolygon() 메서드가 노출되어 있습니다. 이들 중 모든 메서드는 채움의 특성을 정의하는 Brush 객체를 첫 번째 인수로 받습니다. 두 번째 매개변수는 점 배열입니다. 참고로 배열의 매 두 연속 점은 다각형의 변을 지정합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **그래픽을 사용하여 이미지 그리기: 완전한 소스**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

모든 IDisposable을 구현하고 관리되지 않는 리소스에 액세스하는 클래스는 올바르게 폐기되도록 Using 문에서 인스턴스화됩니다.

