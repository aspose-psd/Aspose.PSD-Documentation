---
title: GraphicsPath를 사용하여 이미지 그리기
type: 문서
weight: 30
url: /ko/java/drawing-images-using-graphicspath/
---

## **GraphicsPath를 사용하여 이미지 그리기**
GraphicsPath 클래스는 그래픽 경로를 생성하고 유지하는 역할을 합니다. GraphicsPath에는 이미지에 대한 참조가 없으며 이미지 자체를 변경하지 않고, 대신 Graphics 클래스가 그릴 수있는 경로를 설명하는 메타데이터를 포함하는 객체로 볼 수 있습니다. GraphicsPath 클래스는 각 도형을 사용합니다. 각 도형은 연결된 선 및 곡선의 시퀀스 또는 기하학적 모양 원시로 구성된 도형입니다. 각 모양은 모양 세그먼트로 분할 될 수 있습니다. GraphicsPath 객체에 다양한 도형이나 모양을 추가, 제거 및 변경할 수 있습니다. GraphicsPath가 완전히 설명되면 해당 Graphics 클래스 메서드 (DrawPath 및 Fill Paths)를 사용하여 경로를 그리거나 채울 수 있습니다. Graphics 클래스는 각 모양 세그먼트를 가져와 최종 이미지를 생성하는 데 사용합니다.

### **GraphicsPath 클래스를 사용한 그리기**
아래 예는 GraphicsPath 클래스 사용을 보여주는 예제입니다. 예제 소스 코드는 단순하고 따르기 쉽도록 여러 부분으로 분할되었습니다. 예제는 다음을 보여줍니다.

- 이미지 생성
- Graphics 객체 초기화
- 표면 지우기
- GraphicsPath의 인스턴스 생성
- 도형 생성
- 도형에 모양 추가
- 도형 배열 생성
- 경로 그리기
- 경로 채우기

### **GraphicsPath를 사용한 이미지 그리기: 프로그래밍 샘플**
#### **GraphicsPath: 이미지 생성**
Creating Files에 설명된 메서드 중 하나를 사용하여 이미지를 생성합니다.
#### **GraphicsPath: Graphics 객체 초기화**
Graphics 객체를 생성하고 초기화하기 위해 Image 개체를 생성자에 전달합니다.
#### **GraphicsPath: 표면 지우기**
Graphics 표면을 Clear 메서드를 호출하여 지웁니다. Color를 매개 변수로 전달하면 Graphics 표면을 해당 색상으로 채웁니다.
#### **GraphicsPath: GraphicsPath의 인스턴스 생성**
GraphicsPath의 인스턴스를 생성하고 기본적으로 Alternate로 설정합니다. 이 모드는 닫힌 도형의 내부를 어떻게 채울지 결정합니다. 다른 가능한 GraphicsPath 값은 Winding입니다.
#### **GraphicsPath: 도형 생성**
Figure 클래스의 인스턴스를 생성합니다. 앞에서 설명한대로 Figure에는 Shapes가 포함되며 모양은 Aspose.PSD.Shapes 네임스페이스에 있습니다.
#### **GraphicsPath: 도형에 모양 추가**
Figure 클래스가 노출하는 Add Shapes 메서드를 사용하여 도형에 모양을 추가할 수 있습니다. 아래 코드 예제에서 Figure 개체에 여러 모양이 추가됩니다.
#### **GraphicsPath: 도형 배열에 도형 추가**
여러 도형을 AddFigures 메서드를 사용하여 GraphicsPath 객체에 추가할 수 있습니다. 이 메서드는 매개 변수로 도형 배열을 허용합니다.
#### **GraphicsPath: 경로 그리기**
Graphics 클래스가 노출하는 DrawPath 메서드를 사용하여 GraphicsPath를 그립니다. 이 메서드는 두 개의 매개 변수를 받습니다. 첫 번째 매개 변수는 Pen 클래스의 객체로, 경로의 색상, 너비 및 스타일을 결정합니다. 두 번째 매개 변수는 경로 자체를 나타내는 GraphicsPath 클래스의 객체입니다.
#### **GraphicsPath: 경로 채우기**
GraphicsPath 객체를 Fill Paths 메서드에 전달하여 경로를 채울 수 있습니다. Fill Paths 메서드는 현재 경로에 대해 설정된 채우기 모드 (대체 또는 와인딩)에 따라 경로에 채우기를 수행합니다. 경로에 열린 도형이 포함되어 있으면 해당 도형이 닫힌 것처럼 경로가 채워집니다.

Fill Paths 메서드는 두 개의 매개 변수를 받습니다. 첫 번째 매개 변수는 Aspose.PSD.Brushes 네임스페이스에서 모든 브러시 클래스의 객체입니다. 두 번째 매개 변수는 경로 자체입니다. 이 예제를 위해 HatchBrush를 사용하십시오. 이는 무늬 스타일, 전경 색상 및 배경 색상을 가진 직사각형 브러시입니다. HatchBrush 개체를 Fill Paths 메서드에 전달하기 전에 속성을 설정하십시오.
### **GraphicsPath: 전체 소스**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphicsPath-DrawingUsingGraphicsPath.java" >}}

모든 IDisposable을 구현하는 클래스는 올바르게 삭제되도록 Using 문에서 인스턴스화됩니다.

