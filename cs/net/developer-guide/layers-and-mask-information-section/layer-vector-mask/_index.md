---
title: Vrstva Vektorová Maskování
type: docs
weight: 10
url: /cs/net/layer-vector-mask/
---

## **Přehled Vektorové Maskování Vrstvy**
Vektorová maska je nezávislá na rozlišení cesty, která ořeže obsah vrstvy. Vektorové masky jsou obvykle přesnější než ty vytvořené s nástroji založenými na pixelech. Vytváříte vektorové masky pomocí nástrojů pero nebo tvary.

Aspose.PSD podporuje vykreslování a použití vektorových masek. Můžete upravovat vektorové masky úpravou Vektorových Cest.
## **Vektorová cesta v Aspose.PSD**
Přístup k vektorovým cestám v Aspose.PSD je poskytován pomocí zdrojů [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) a [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource), které jsou dětskými třídami zdroje [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Jak upravit vektorovou cestu?**
### **Struktura vektorové cesty**
Základní struktura pro manipulaci s cestami je [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord). Pro vaše pohodlí je však navrhováno následující řešení.

Pro snadné úpravy vektorových cest byste měli použít třídu [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), která obsahuje metody pro pohodlnou úpravu vektorových dat v zdrojích odvozených z VectorPathDataResource.

Začněte s vytvořením objektu typu VectorPath.

Pro vaše pohodlí můžete použít statickou metodu [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), ta najde vektorový zdroj ve vstupní vrstvě a vytvoří objekt VectorPath na jeho základě.



Po všech úpravách můžete aplikovat objekt VectorPath s provedenými změnami zpět na vrstvu pomocí statické metody [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Typ VectorPath obsahuje seznam prvků [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) a popisuje celý vektorový obraz, který může obsahovat jeden nebo více tvarů.

![todo:image_alt_text](layer-vector-mask_1.png)



Každý tvar PathShape je vektorová figurka, která se skládá z samostatného souboru uzlů Beziér.

Uzly jsou objekty typu [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), což jsou v podstatě body, ze kterých je figura postavena.

![todo:image_alt_text](layer-vector-mask_2.png)

Následující ukázkový kód ukazuje, jak přistupovat k figuře a bodům.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Jak vytvořit tvar?**
Pro úpravu tvaru musíte získat existující tvar z [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) seznamu nebo přidat nový tvar vytvořením instance [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) a přidáním ho do seznamu [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Jak přidat uzly (body)?**
Body tvaru můžete manipulovat jako prvků běžného seznamu pomocí vlastnosti PathShape.Points, například můžete přidat body tvaru:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}


BezierKnot obsahuje bod Kotvy a dva Řídící body.

![todo:image_alt_text](layer-vector-mask_3.png)

Pokud mají kotva a řídící body stejné hodnoty, pak tento uzel bude mít ostrý úhel.

Chcete-li změnit pozici bodu kotvy spolu s řídícími body (stejně jako se to děje v Photoshopu), má BezierKnot metodu Shift.

Následující ukázkový kód demonstruje posunutí celého beziérova uzlu svisle nahoru podle souřadnice Y:

Body tvaru můžete manipulovat jako prvků běžného seznamu pomocí vlastnosti PathShape.Points, například můžete přidat body tvaru:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Vlastnosti PathShape**
Editace PathShape není omezena pouze na úpravu uzlů, tento typ má také další vlastnosti.
### **Operace Cesty (Booleovské operace)**
Vlastnost [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) je takzvaná booleovská operace, změna hodnoty definuje, jak jsou smíchány různé tvary.

Jsou zde následující možné hodnoty:

- 0 = VyloučitPřekrývajícíSeTvary (operace XOR).
- 1 = KombinovatTvary (operace OR).
- 2 = OdečístPředníTvar (operace NOT).
- 3 = PrůnikPlochTvary (operace AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Vlastnost IsClosed**
Také pomocí vlastnosti PathShape.IsClosed můžeme určit, zda jsou první a poslední uzel tvaru propojeny.

|**Uzavřený tvar**|**Otevřený tvar**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **Vlastnost FillColor**
Žádná figura nemůže mít svou vlastní barvu, takže můžete změnit barvu celého vektorového tvaru pomocí vlastnosti VectorPath.FillColor.

Body tvaru můžete manipulovat jako prvků běžného seznamu pomocí vlastnosti PathShape.Points, například můžete přidat body tvaru:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Zde naleznete zdrojový kód třídy VectorDataProvider a příslušných tříd:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
