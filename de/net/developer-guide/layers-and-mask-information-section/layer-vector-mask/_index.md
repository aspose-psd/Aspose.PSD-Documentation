---
title: Vektor-Masken in Schichten
type: docs
weight: 10
url: /de/net/vektor-masken-in-schichten/
---

## **Übersicht über Vektor-Masken in Schichten**
Eine Vektor-Maske ist ein auflösungsunabhängiger Pfad, der den Inhalt der Schicht ausschneidet. Vektor-Masken sind in der Regel genauer als solche, die mit pixelbasierten Werkzeugen erstellt wurden. Sie erstellen Vektor-Masken mit den Stift- oder Formwerkzeugen.

Aspose.PSD unterstützt das Rendern und Anwenden von Vektor-Masken. Sie können Vektor-Masken bearbeiten, indem Sie Vektor-Pfade bearbeiten.

## **Vektorpfad in Aspose.PSD**
Der Zugriff auf Vektorpfade in Aspose.PSD erfolgt über [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) und [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) Ressourcen, die Kindklassen von [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource) sind.

![todo:image_alt_text](layer-vector-mask_0.png)

## **Wie bearbeitet man einen Vektorpfad?**
### **Vektorpfad-Struktur**
Die Basisklasse zur Manipulation von Pfaden ist [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord). Aber für Ihre Bequemlichkeit wird die folgende Lösung vorgeschlagen.

Für eine einfache Bearbeitung von Vektorpfaden sollten Sie die [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) Klasse verwenden, die Methoden für die komfortable Bearbeitung von Vektordaten in Ressourcen enthält, die von VectorPathDataResource abgeleitet sind.

Beginnen Sie mit der Erstellung eines Objekts des Typs VectorPath.

Zur Vereinfachung können Sie die statische Methode  [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs)verwenden. Diese Methode findet eine Vektorressource in der Eingabeschicht und erstellt ein VectorPath-Objekt darauf basierend.



Nach allen Bearbeitungen können Sie das VectorPath-Objekt mit den Änderungen zurück zur Schicht anwenden, indem Sie die statische Methode [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) verwenden.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Der VectorPath-Typ enthält eine Liste von [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs)-Elementen und beschreibt ein gesamtes Vektorbild, das aus einer oder mehreren Formen bestehen kann.

![todo:image_alt_text](layer-vector-mask_1.png)



Jede PathShape ist eine Vektorgestalt, die aus einem separaten Satz von Bezier-Knoten (Punkt) besteht.

Knoten sind Objekte des Typs [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), die im Wesentlichen die Punkte sind, aus denen die Figur aufgebaut wird.

![todo:image_alt_text](layer-vector-mask_2.png)

Im folgenden Codebeispiel wird gezeigt, wie auf eine Figur und Punkte zugegriffen wird.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Wie erstellt man eine Form?**
Um eine Form zu bearbeiten, müssen Sie eine vorhandene aus der [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs)-Liste abrufen oder eine neue Form hinzufügen, indem Sie eine Instanz von [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) erstellen und sie der [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs)-Liste hinzufügen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3" >}}
### **Wie fügt man Knoten (Punkte) hinzu?**
Man kann die Punkte der Form als Elemente einer regulären Liste mit Hilfe der PathShape.Points-Eigenschaft bearbeiten. Zum Beispiel können Sie Formpunkte hinzufügen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4" >}}



BezierKnot enthält Ankerpunkt und zwei Steuerpunkte.

![todo:image_alt_text](layer-vector-mask_3.png)

Wenn Anker- und Steuerpunkte dieselben Werte haben, wird dieser Knoten einen spitzen Winkel haben.

Um die Position des Ankerpunkts zusammen mit den Steuerpunkten zu ändern (ähnlich wie es in Photoshop geschieht), hat der BezierKnot eine Shift-Methode.

Das folgende Codebeispiel zeigt das Verschieben des gesamten Bezierknotens vertikal nach oben um die Y-Koordinate:

Man kann die Punkte der Form als Elemente einer regulären Liste mit  der PathShape.Points-Eigenschaft bearbeiten. Zum Beispiel können Sie Formpunkte hinzufügen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5" >}}


## **PathShape-Eigenschaften**
Die Bearbeitung von PathShape ist nicht auf das Bearbeiten von Knoten beschränkt, dieser Typ hat auch andere Eigenschaften.
### **Pfadoperationen (Boolesche Operationen)**
Die [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations)-Eigenschaft ist eine sogenannte boolesche Operation, deren Wertänderung definiert, wie mehrere Formen vermischt werden.

Es gibt die folgenden möglichen Werte:

- 0 = ExcludeOverlappingShapes (XOR-Operation).
- 1 = CombineShapes (OR-Operation).
- 2 = SubtractFrontShape (NOT-Operation).
- 3 = IntersectShapeAreas (AND-Operation).

![todo:image_alt_text](layer-vector-mask_4.png)
### **IsClosed-Eigenschaft**
Durch Verwendung der PathShape.IsClosed-Eigenschaft können wir feststellen, ob der erste und der letzte Knoten einer Form verbunden sind.

|**Geschlossene Form**|**Geöffnete Form**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **FillColor-Eigenschaft**
Keine Figur kann ihre eigene Farbe haben, so können Sie die Farbe des gesamten Vektorpfads mit der VectorPath.FillColor-Eigenschaft ändern.

Die Punkte der Form können als Elemente einer regulären Liste mit Hilfe der PathShape.Points-Eigenschaft bearbeitet werden. Zum Beispiel können Sie Formpunkte hinzufügen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6" >}}


## **Hier finden Sie den Quellcode von VectorDataProvider und verwandten Klassen:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
