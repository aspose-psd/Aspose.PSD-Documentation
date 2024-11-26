---
title: GraphicsPath를 사용하여 이미지 그리기
type: docs
weight: 30
url: /ko/net/drawing-images-using-graphicspath/
---

## **GraphicsPath를 사용하여 이미지 그리기**
[GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) 클래스는 그래픽 경로를 생성하고 유지하는 역할을 담당합니다. GraphicsPath에는 이미지에 대한 참조가 없으며 이미지 자체를 변경하지 않습니다. 대신 그래픽 클래스가 그릴 수 있는 경로를 설명하는 메타데이터를 포함하는 객체로 볼 수 있습니다. GraphicsPath 클래스는 도형을 사용합니다. 각 도형은 연결된 선과 곡선의 일렬 또는 기하학적 모양 기본요소로 구성됩니다. 각 모양은 모양 세그먼트로 분할될 수 있습니다. GraphicsPath 객체에 다양한 도형 또는 모양을 추가, 제거 및 변경할 수 있습니다. GraphicsPath가 완전히 설명된 후에는 해당하는 Graphics 클래스 메서드(DrawPath 및 Fill Paths)를 사용하여 경로를 그리거나 채울 수 있습니다. Graphics 클래스는 각 모양 세그먼트를 가져와 최종 이미지를 생성합니다.
### **GraphicsPath 클래스를 사용한 그리기**
아래는 [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) 클래스를 사용하는 예제입니다. 예제 소스 코드는 간단하고 쉽게 따라갈 수 있도록 여러 부분으로 나뉘어져 있습니다. 단계별로 예제를 통해 다음을 보여줍니다:

- 이미지 생성
- Graphics 객체 초기화
- 표면 지우기
- [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) 인스턴스 생성
- 도형 생성
- 도형에 모양 추가
- 모양 배열 만들기
- 경로 그리기
- 경로 채우기


### **GraphicsPath를 사용한 이미지 그리기: 프로그래밍 샘플**
#### **GraphicsPath: 이미지 생성**
파일 생성 중 설명된 방법 중 하나를 사용하여 이미지를 생성합니다.
#### **GraphicsPath: Graphics 객체 초기화**
Graphics 객체를 만들고 초기화하려면 Image 객체를 생성자에 전달하세요.
#### **GraphicsPath: 표면 지우기**
Graphics 표면을 지우려면 Graphics 클래스의 Clear 메서드를 호출하고 매개변수로 색상을 전달하세요. 이 메서드는 전달된 색상으로 Graphics 표면을 채웁니다.
#### **GraphicsPath: GraphicsPath 인스턴스 생성**
GraphicsPath 인스턴스를 생성하고 GraphicsPath를 기본값인 대체로 설정합니다. 이 모드는 닫힌 도형의 내부를 채우는 방법을 결정합니다. 다른 가능한 GraphicsPath 값은 Winding입니다.
#### **GraphicsPath: 도형 생성**
Figure 클래스의 인스턴스를 만듭니다. 앞에서 설명한대로 Figure에는 Shapes이 포함될 수 있으며 shapes는 Aspose.PSD.Shapes 네임스페이스에 있습니다.
#### **GraphicsPath: 도형에 모양 추가**
Figure 클래스에 노출된 Add Shapes 메서드를 사용하여 도형에 모양을 추가할 수 있습니다. 아래 코드 예제에서 Figure 개체에 여러 모양이 추가됩니다.
#### **GraphicsPath: 배열에 도형 추가**
GraphicsPath 클래스에 포함된 AddFigures 메서드를 사용하여 여러 도형을 GraphicsPath 객체에 추가할 수 있습니다. 이 메서드는 도형 배열을 매개변수로 사용합니다.
#### **GraphicsPath: 경로 그리기**
Graphics 클래스에 노출된 DrawPath 메서드를 사용하여 GraphicsPath를 그립니다. 이 메서드는 두 개의 매개변수를 받습니다. 첫 번째 매개변수는 Pen 클래스의 객체로, 경로의 색상, 너비 및 스타일을 결정합니다. 두 번째 매개변수는 경로 자체를 나타내는 GraphicsPath 클래스의 객체입니다.
#### **GraphicsPath: 경로 채우기**


경로를 채울 수 있습니다. Graphics 클래스에서 노출된 Fill Paths 메서드에 GraphicsPath 객체를 전달하여 경로를 채울 수 있습니다. Fill Paths 메서드는 현재 경로에 설정된 채우기 모드(대체 또는 winding)에 따라 경로를 채웁니다. 경로에 열린 도형이 있는 경우 해당 도형이 닫혀있는 것처럼 경로가 채워집니다.

Fill Paths 메서드는 두 개의 매개변수를 받습니다. 첫 번째 매개변수는 Aspose.PSD.Brushes 네임스페이스의 브러시 클래스의 객체입니다. 두 번째 매개변수는 경로 자체입니다. 이 예제를 위해 상자 모양의 브러시인 HatchBrush를 사용하세요. 이 브러시는 사선 모양, 전경색 및 배경색을 가진 직사각형 브러시입니다. HatchBrush 개체를 Fill Paths 메서드로 전달하기 전에 해당 프로퍼티를 설정하세요.
### **GraphicsPath: 전체 소스**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.cs" >}}



IDisposable을 구현하는 모든 클래스는 Dispose가 올바르게 처리되도록 Using 문에서 인스턴스화됩니다.
