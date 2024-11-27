---
title: Maschera Vettoriale dello Strato
type: docs
weight: 10
url: /it/net/layer-vector-mask/
---

## **Panoramica della Maschera Vettoriale dello Strato**
Una maschera vettoriale è un percorso indipendente dalla risoluzione che ritaglia i contenuti dello strato. Le maschere vettoriali sono di solito più accurate di quelle create con strumenti basati su pixel. È possibile creare maschere vettoriali con gli strumenti penna o forme.

Aspose.PSD supporta il rendering e l'applicazione di maschere vettoriali. È possibile modificare le maschere vettoriali attraverso la modifica dei Percorsi Vettoriali.

## **Percorso vettoriale in Aspose.PSD**
L'accesso ai percorsi vettoriali in Aspose.PSD è fornito tramite le risorse [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) e [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) che sono classi figlie di [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Come modificare un percorso vettoriale?**
### **Struttura del percorso vettoriale**
La struttura di base per manipolare i percorsi è [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) Ma per la tua comodità, viene suggerita la seguente soluzione.

Per modificare facilmente i percorsi vettoriali, dovresti utilizzare la classe [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), che contiene metodi per la comoda modifica dei dati vettoriali nelle risorse derivate da VectorPathDataResource.

Inizia creando un oggetto di tipo VectorPath.

Per comodità, puoi utilizzare il metodo statico [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), troverà una risorsa vettoriale nello strato di input e creerà un oggetto VectorPath basato su di essa.

Dopo tutte le modifiche, è possibile applicare l'oggetto VectorPath con le modifiche indietro allo strato utilizzando il metodo statico [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Il tipo VectorPath contiene un elenco di elementi [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) e descrive un'intera immagine vettoriale che può essere composta da una o più forme.

![todo:image_alt_text](layer-vector-mask_1.png)

Ogni PathShape è una figura vettoriale che è composta da un insieme separato di nodi di Bezier.

I nodi sono oggetti di tipo [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) che rappresentano i punti da cui la figura è costruita.

![todo:image_alt_text](layer-vector-mask_2.png)

Nell'esempio di codice seguente è mostrato come accedere a una figura e ai punti.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}

### **Come creare una forma?**
Per modificare una forma, è necessario prendere una già esistente dall'elenco [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), o aggiungere una nuova forma creando un'istanza [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) e aggiungendola all'elenco [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}

### **Come aggiungere nodi (punti)?**
È possibile manipolare i punti della forma come elementi di un normale elenco usando la proprietà PathShape.Points, ad esempio, è possibile aggiungere punti alla forma:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}


Il BezierKnot contiene un punto di ancoraggio e due punti di controllo.

![todo:image_alt_text](layer-vector-mask_3.png)

Se i punti di ancoraggio e di controllo hanno gli stessi valori, allora quel nodo avrà un angolo acuto.

Per spostare la posizione del punto di ancoraggio insieme ai punti di controllo (similmente a come avviene in Photoshop), il BezierKnot ha un metodo Shift.

Nell'esempio di codice seguente viene illustrato lo spostamento di un intero nodo di Bezier verso l'alto verticalmente per coordinata Y:

È possibile manipolare i punti della forma come elementi di un elenco regolare usando la proprietà PathShape.Points, ad esempio, è possibile aggiungere punti alla forma:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Proprietà di PathShape**
La modifica di PathShape non è limitata alla modifica dei nodi, questo tipo ha anche altre proprietà.
### **PathOperations (Operazioni booleane)**
La proprietà [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) è una cosiddetta operazione booleana, cambiando il valore del quale si definisce come vengono mescolate più forme.

Esistono i seguenti possibili valori:

- 0 = ExcludeOverlappingShapes (operazione XOR).
- 1 = CombineShapes (operazione OR).
- 2 = SubtractFrontShape (operazione NOT).
- 3 = IntersectShapeAreas (operazione AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Proprietà IsClosed**
Inoltre, utilizzando la proprietà PathShape.IsClosed, è possibile determinare se il primo e l'ultimo nodo di una forma sono connessi.

|**Forma chiusa**|**Forma aperta**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **Proprietà FillColor**
Nessuna figura può avere il proprio colore, quindi è possibile cambiare il colore dell'intero percorso vettoriale con la proprietà VectorPath.FillColor.

È possibile manipolare i punti della forma come elementi di un normale elenco usando la proprietà PathShape.Points, ad esempio, è possibile aggiungere punti alla forma:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Qui troverai il codice sorgente di VectorDataProvider e classi correlate:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
