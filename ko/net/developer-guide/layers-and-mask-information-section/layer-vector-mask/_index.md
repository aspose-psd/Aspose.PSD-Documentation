---
title: 레이어 벡터 마스크
type: docs
weight: 10
url: /ko/net/layer-vector-mask/
---

## **레이어 벡터 마스크 개요**
벡터 마스크는 레이어의 내용을 자르는 해상도에 독립적인 경로입니다. 벡터 마스크는 일반적으로 픽셀 기반 도구로 생성된 것보다 정확합니다. 핀 또는 모양 도구를 사용하여 벡터 마스크를 생성합니다.

Aspose.PSD는 벡터 마스크의 렌더링 및 적용을 지원합니다. 벡터 마스크를 편집하는 방법은 벡터 경로를 편집함으로써 이루어집니다.
## **Aspose.PSD의 벡터 경로**
Aspose.PSD에서 벡터 경로에 액세스하려면 [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) 및 [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) 자원을 통해 제공되며, 이들은 [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource)의 하위 클래스입니다.

![할 일:이미지 대체 텍스트](layer-vector-mask_0.png)

## **벡터 경로 편집 방법**
### **벡터 경로 구조**
경로를 조작하기 위한 기본 구조는 [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord)입니다. 그러나 편리성을 위해 다음 솔루션이 제안됩니다.

벡터 경로의 쉬운 편집을 위해 [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 클래스를 사용해야 하며, 이 클래스에는 VectorPathDataResource에서 파생된 자원의 벡터 데이터를 편리하게 편집하는 메서드가 포함되어 있습니다.

VectorPath 유형의 개체를 만들어 시작합니다.

편리를 위해, [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 정적 메서드를 사용하면 입력 레이어에서 벡터 리소스를 찾아 그를 기반으로 한 VectorPath 개체를 만들 수 있습니다.

모든 편집을 마친 후, 변경된 VectorPath 개체를 [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 정적 메서드를 사용하여 레이어에 적용할 수 있습니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

VectorPath 유형에는 [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 요소 목록이 포함되어 있으며, 하나 이상의 모양으로 구성된 전체 벡터 이미지를 설명합니다.

![할 일:이미지 대체 텍스트](layer-vector-mask_1.png)

각 PathShape은 별도의 베지어 점(점) 세트로 구성된 벡터 도형입니다.

점은 도형을 구성하는 포인트로서 [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 유형의 객체입니다.

![할 일:이미지 대체 텍스트](layer-vector-mask_2.png)

다음 코드 예제에서 도형과 점에 액세스하는 방법을 보여줍니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **모양을 만드는 방법**
모양을 편집하려면 [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 목록에서 기존 모양을 가져오거나 [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) 인스턴스를 생성하고 해당 목록에 추가하여 새로운 모양을 추가해야 합니다.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **점(포인트)을 추가하는 방법**
PathShape.Points 속성을 사용하여 모양의 포인트를 일반 List의 요소로 조작할 수 있으며, 예를 들어 모양 포인트를 추가할 수 있습니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}

베지어 점에는 앵커 포인트와 두 개의 제어 포인트가 포함됩니다.

![할 일:이미지 대체 텍스트](layer-vector-mask_3.png)

앵커 포인트와 제어 포인트가 동일한 값인 경우 해당 노드는 예각을 가집니다.

Photoshop에서 발생하는 것과 유사하게 앵커 포인트 위치를 변경하려면 BezierKnot에 Shift 메서드가 있습니다.

다음 코드 예제는 전체 베지어 점을 Y 좌표를 통해 수직으로 이동하는 방법을 보여줍니다:

PathShape.Points 속성을 사용하여 모양의 포인트를 일반 List의 요소로 조작할 수 있으며, 예를 들어 모양 포인트를 추가할 수 있습니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **PathShape 속성**
PathShape 편집은 노드 편집으로 제한되지 않으며, 이 유형에는 다른 속성도 있습니다.
### **경로 작업(부울 작업)**
PathOperations 속성은 여러 모양이 어떻게 혼합되는지를 정의하는 부울 연산이라고 불립니다.

다음과 같은 가능한 값이 있습니다:

- 0 = 중첩된 모양 제외(XOR 연산).
- 1 = 모양 결합(OR 연산).
- 2 = 앞 모양 뺌(NOT 연산).
- 3 = 모양 영역 교차(AND 연산).

![할 일:이미지 대체 텍스트](layer-vector-mask_4.png)
### **IsClosed 속성**
또한 PathShape.IsClosed 속성을 사용하여 모양의 첫 번째와 마지막 점이 연결되었는지를 확인할 수 있습니다.

|**닫힌 모양**|**열린 모양**|
| :- | :- |
|![할 일:이미지 대체 텍스트](layer-vector-mask_5.png)|![할 일:이미지 대체 텍스트](layer-vector-mask_6.png)|
### **FillColor 속성**
어떤 도형도 고유한 색상을 가질 수 있으므로 VectorPath.FillColor 속성을 사용하여 전체 벡터 경로의 색상을 변경할 수 있습니다.

PathShape.Points 속성을 사용하여 모양의 포인트를 일반 List의 요소로 조작할 수 있으며, 예를 들어 모양 포인트를 추가할 수 있습니다:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **여기에서 VectorDataProvider 및 관련 클래스의 소스 코드를 찾을 수 있습니다:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}

