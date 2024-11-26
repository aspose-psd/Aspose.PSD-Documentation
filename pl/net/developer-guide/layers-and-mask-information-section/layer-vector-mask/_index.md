---
title: Warstwowy Mask Vector
type: docs
weight: 10
url: /pl/net/layer-vector-mask/
---

## **Omówienie maski wektorowej warstwy**
Maska wektorowa to ścieżka niezależna od rozdzielczości, która przycinają zawartość warstwy. Maseczki wektorowe są zazwyczaj bardziej dokładne niż te tworzone za pomocą narzędzi opartych na pikselach. Maseczki wektorowe tworzy się za pomocą narzędzi ołówka lub kształtów.

Aspose.PSD obsługuje renderowanie i stosowanie masek wektorowych. Możesz edytować maski wektorowe poprzez edycję Ścieżek Wektorowych.

## **Ścieżka wektorowa w Aspose.PSD**
Dostęp do ścieżek wektorowych w Aspose.PSD uzyskuje się dzięki zasobom [VsmsResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) i [VmskResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource), które są klasami pochodnymi od [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Jak edytować ścieżkę wektorową?**
### **Struktura ścieżki wektorowej**
Podstawową strukturą do manipulowania ścieżkami jest [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord). Dla Twojej wygody proponowane jest jednak następujące rozwiązanie.

Dla łatwej edycji ścieżek wektorowych powinieneś użyć klasy [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), która zawiera metody do wygodnej edycji danych wektorowych w zasobach pochodzących z VectorPathDataResource.

Rozpocznij od stworzenia obiektu typu VectorPath.

Dla wygody, możesz skorzystać ze statycznej metody [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), która znajdzie zasób wektorowy w warstwie wejściowej i stworzy obiekt VectorPath na jego podstawie.



Po wszystkich edycjach, możesz zastosować obiekt VectorPath ze zmianami z powrotem do warstwy za pomocą statycznej metody [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Typ VectorPath zawiera listę elementów [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) i opisuje cały obraz wektorowy, który może składać się z jednego lub więcej kształtów.

![todo:image_alt_text](layer-vector-mask_1.png)



Każdy kształt PathShape to figura wektorowa składająca się z oddzielnego zbioru węzłów Beziera (punktów).

Węzły są obiektami typu [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) będącymi w zasadzie punktami, z których jest budowana figura.

![todo:image_alt_text](layer-vector-mask_2.png)

Poniższy przykład kodu pokazuje, jak uzyskać dostęp do figury i punktów.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Jak utworzyć kształt?**
Aby edytować kształt, musisz uzyskać istniejący z listy [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), lub dodać nowy kształt, tworząc instancję [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) i dodając go do listy [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Jak dodać węzły (punkty)?**
Możesz manipulować punktami kształtu jako elementami standardowej Listy za pomocą właściwości PathShape.Points, na przykład, możesz dodać punkty kształtu:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}



BezierKnot zawiera punkt kotwicy i dwa punkty kontrolne.

![todo:image_alt_text](layer-vector-mask_3.png)

Jeśli punkty kotwicy i kontrolne mają te same wartości, wtedy węzeł będzie miała kąt ostry.

Aby zmienić położenie punktu kotwicy wraz z punktami kontrolnymi (podobnie jak ma to miejsce w Photoshopie), BezierKnot ma metodę Shift.

Poniższy przykład kodu demonstruje przesuwanie całego węzła beziera pionowo w górę według współrzędnej Y:

Możesz manipulować punktami kształtu jako elementami standardowej Listy za pomocą właściwości PathShape.Points, na przykład, możesz dodać punkty kształtu:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Właściwości PathShape**
Edycja PathShape nie ogranicza się jedynie do edytowania węzłów, ten typ ma również inne właściwości.
### **Operacje na ścieżce (Operacje logiczne)**
Właściwość [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) to tzw. operacja logiczna, zmieniając wartość której definiuje się, jak są mieszane wielokrotne kształty.

Możliwe są następujące wartości:

- 0 = ExcludeOverlappingShapes (operacja XOR).
- 1 = CombineShapes (operacja OR).
- 2 = SubtractFrontShape (operacja NOT).
- 3 = IntersectShapeAreas (operacja AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Właściwość IsClosed**
Dodatkowo, korzystając z właściwości PathShape.IsClosed, możemy określić, czy pierwszy i ostatni węzeł kształtu są połączone.

|**Kształt zamknięty**|**Kształt otwarty**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **Właściwość FillColor**
Żaden kształt nie może mieć swojego własnego koloru, dlatego możesz zmienić kolor całej ścieżki wektorowej za pomocą właściwości VectorPath.FillColor.

Możesz manipulować punktami kształtu jako elementami standardowej Listy za pomocą właściwości PathShape.Points, na przykład, możesz dodać punkty kształtu:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Tu znajdziesz kod źródłowy klasy VectorDataProvider i powiązanych klas:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
