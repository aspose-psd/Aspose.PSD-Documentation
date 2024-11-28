---
title: Laag Vector Masker
type: docs
weight: 10
url: /nl/laag-vector-masker/
---

## **Overzicht van het laag vector masker**
Een vector masker is een resolutie-onafhankelijk pad dat de inhoud van de laag uitsnijdt. Vector maskers zijn meestal nauwkeuriger dan die gemaakt met op pixels gebaseerde tools. U kunt vector maskers maken met de pen- of vormgereedschappen.

Aspose.PSD ondersteunt het renderen en toepassen van vector maskers. U kunt vector maskers bewerken door het bewerken van Vector Paths.
## **Vectorpad in Aspose.PSD**
Toegang tot vectorpaden in Aspose.PSD wordt geboden via [VsmsResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) en [VmskResouce](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) bronnen die kindklassen zijn van [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Hoe een vectorpad bewerken?**
### **Structuur van vectorpad**
De basisstructuur om paden te manipuleren is [VectorPathRecord.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord) Maar voor uw gemak wordt de volgende oplossing voorgesteld.

Voor eenvoudige bewerking van vectorpaden kunt u de [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) klasse gebruiken, die methoden bevat voor gemakkelijke bewerking van vectorgegevens in resources afgeleid van VectorPathDataResource.

Begin met het maken van een object van het type VectorPath.

Voor gemak kunt u de statische methode [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) gebruiken, die een vectorresource in de invoerlaag zal vinden en op basis daarvan een VectorPath-object zal maken.



Na alle bewerkingen kunt u het VectorPath-object met wijzigingen terug toepassen op de laag met behulp van de statische methode [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Het VectorPath-type bevat een lijst van [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) elementen en beschrijft een volledig vectorbeeld dat kan bestaan uit één of meer vormen.

![todo:image_alt_text](layer-vector-mask_1.png)

Elke PathShape is een vectorfiguur die bestaat uit een aparte set Bezier-knopen (punt).

Knopen zijn objecten van het type [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) die essentieel zijn voor het opbouwen van de figuur.

![todo:image_alt_text](layer-vector-mask_2.png)

Het volgende codevoorbeeld toont hoe toegang te krijgen tot een figuur en punten.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Hoe een vorm maken?**
Om een vorm te bewerken, moet u een bestaande ophalen uit de [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) lijst, of een nieuwe vorm toevoegen door een [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) instantie te maken en deze toe te voegen aan de [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) lijst.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Hoe knopen (punten) toevoegen?**
U kunt de punten van een vorm manipuleren als elementen van een reguliere lijst met behulp van de PathShape.Points eigenschap, bijvoorbeeld, u kunt vormpunten toevoegen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}



BezierKnot bevat een ankerpunt en twee bedieningspunten.

![todo:image_alt_text](layer-vector-mask_3.png)

Als anker- en bedieningspunten dezelfde waarden hebben, zal die knoop een scherpe hoek hebben.

Om de positie van het ankerpunt samen met de bedieningspunten te wijzigen (vergelijkbaar met wat er gebeurt in Photoshop), heeft de BezierKnot een Shift methode.

Het volgende codevoorbeeld laat zien hoe een volledige Bezier-knoop verticaal omhoog te verplaatsen volgens de Y-coördinaat:

U kunt de punten van een vorm manipuleren als elementen van een reguliere lijst met behulp van de PathShape.Points eigenschap, bijvoorbeeld, u kunt vormpunten toevoegen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}


## **Eigenschappen van PathShape**
Het bewerken van PathShape is niet beperkt tot het bewerken van knopen, dit type heeft ook andere eigenschappen.
### **PathOperations (Boolean-operaties)**
De [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) eigenschap is een zogenaamde booleanbewerking, waarbij de waarde verandert hoe meerdere vormen worden gemengd.

Er zijn de volgende mogelijke waarden:

- 0 = Uitsluiten van overlappende vormen (XOR-operatie).
- 1 = Combineren van vormen (OF-operatie).
- 2 = Aftrekken van voorste vorm (NIET-operatie).
- 3 = Intersectie van vormgebieden (EN-operatie).

![todo:image_alt_text](layer-vector-mask_4.png)
### **IsClosed Eigenschap**
Ook kunnen we met behulp van de PathShape.IsClosed eigenschap bepalen of de eerste en laatste knoop van een vorm met elkaar zijn verbonden.

|**Gesloten vorm**|**Open vorm**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **FillColor Eigenschap**
Geen enkele figuur kan zijn eigen kleur hebben, dus u kunt de kleur van het hele vectorpad veranderen met de VectorPath.FillColor eigenschap.

U kunt de punten van een vorm manipuleren als elementen van een reguliere lijst met behulp van de PathShape.Points eigenschap, bijvoorbeeld, u kunt vormpunten toevoegen:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}


## **Hier vindt u de broncode van VectorDataProvider en gerelateerde klassen:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
