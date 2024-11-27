---
title: Слой Vector Mask
type: docs
weight: 10
url: /bg/net/layer-vector-mask/
---

## **Преглед на слоевия векторен маск**
Векторната маска е път без зависимост от резолюцията, който отрязва съдържанието на слоя. Векторните маски обикновено са по-точни от тези, създадени с инструменти на база на пиксели. Вие създавате векторни маски с помощта на инструментите за писалка или форми.

Aspose.PSD поддържа визуализация и прилагане на векторни маски. Можете да редактирате векторни маски чрез редактиране на векторни пътища.
## **Векторен път в Aspose.PSD**
Достъпът до векторните пътища в Aspose.PSD се осигурява чрез [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) и [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource), които са детски класове на [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Как да редактирате векторен път?**
### **Структура на векторния път**
Основната структура за манипулиране на пътища е [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) Но за ваше удобство се предлага следното решение.

За лесно редактиране на векторни пътища, трябва да използвате класа [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), който съдържа методи за удобно редактиране на векторни данни в ресурси, произтичащи от VectorPathDataResource

Започнете като създадете обект от тип VectorPath.

За ваше удобство можете да използвате статичния метод [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), който ще намери векторен ресурс в подадения слой и ще създаде обект VectorPath върху него.

След всички редакции можете да приложите обекта VectorPath с промените обратно към слоя, използвайки статичния метод [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Типът VectorPath съдържа списък от елементи на [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) и описва цялата векторна изображение, което може да се състои от една или повече форми.

![todo:image_alt_text](layer-vector-mask_1.png)

Всяка форма на пътя е векторна фигура, която се състои от отделен набор от бизие възли (точки).

Възлите са обекти от тип [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), които са основно точките, от които е изградена фигурата.

![todo:image_alt_text](layer-vector-mask_2.png)

Следният примерен код показва как да имате достъп до фигурата и точките.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Как да създадете форма?**
За да редактирате форма, трябва да получите съществуваща от [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) списъка или да добавите нова, като създадете [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) инстанция и я добавите към списъка [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Как да добавите бизии (точки)?**
Можете да манипулиратете точките на формата като елементи на обикновен списък, използвайки свойството PathShape.Points, например, можете да добавите точки на формата:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}



BezierKnot съдържа точката на крепост и две контролни точки.

![todo:image_alt_text](layer-vector-mask_3.png)

Ако точките на крепостта и контролните точки имат същите стойности, този възел ще има остър ъгъл.

За да промените позицията на точката на крепост, заедно с контролните точки (подобно на това, което се случва в Photoshop), в BezierKnot има метод Shift.

Следният примерен код демонстрира движението на целия бизий възел вертикално нагоре по координатата Y:

Можете да манипулиратете точките на формата като елементи на обикновен списък, използвайки свойството PathShape.Points, например, можете да добавите точки на формата:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Свойства на PathShape**
Редактирането на PathShape не се ограничава само до редактиране на възли, този тип също разполага с други свойства.
### **PathOperations (Булеви операции)**
Свойството [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) е така наречена булева операция, чрез промяната на стойността на която се дефинира как се смесват множество форми.

Има следните възможни стойности:

- 0 = ИзключителноПрепокриващиСеФорми (операция XOR).
- 1 = КомбиниранеНаФормите (операция OR).
- 2 = ИзважданеНаПредниятФорма (операция NOT).
- 3 = ПресичанеНаОбластиНаФормата (операция AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Свойство IsClosed (Затворена форма)**
Също така, използвайки свойството PathShape.IsClosed, можем да определим дали първият и последният възел на формата са свързани.

|**Затворена форма**|**Отворена форма**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **FillColor Property**
Нито една фигура не може да има своя собствен цвят, така че можете да промените цвета на целия векторен път с помощта на свойството VectorPath.FillColor.

Можете да манипулиратете точките на формата като елементи на обикновен списък, използвайки свойството PathShape.Points, например, можете да добавите точки на формата:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Тук ще намерите изходния код на VectorDataProvider и свързаните класове:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}