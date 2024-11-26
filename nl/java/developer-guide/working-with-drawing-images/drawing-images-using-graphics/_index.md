---
title: Tekenen van afbeeldingen met Graphics
type: docs
weight: 20
url: /nl/java/drawing-images-using-graphics/
---

## **Tekenen van afbeeldingen met Graphics**


Met de Aspose.PSD-bibliotheek kunt u eenvoudige vormen tekenen zoals lijnen, rechthoeken en cirkels, maar ook complexe vormen zoals veelhoeken, curves, bogen en Bezier-vormen. De Aspose.PSD-bibliotheek maakt dergelijke vormen met behulp van de Graphics-klasse die zich bevindt in de Aspose.PSD-namespace. Graphics-objecten zijn verantwoordelijk voor het uitvoeren van verschillende tekenoperaties op een afbeelding, waardoor het oppervlak van de afbeelding verandert. De Graphics-klasse maakt gebruik van verschillende hulpobjecten om de vormen te verbeteren:

- Pennen, om lijnen te trekken, vormen te omlijnen of andere geometrische voorstellingen te renderen.
- Penselen, om te definiëren hoe gebieden worden ingekleurd.
- Lettertypen, om de vorm van tekens van tekst te definiëren.
### **Teken met de Graphics-klasse**
Hieronder vindt u een codevoorbeeld dat het gebruik van de Graphics-klasse demonstreert. De voorbeeldbroncode is opgesplitst in verschillende delen om het eenvoudig en gemakkelijk te volgen te houden. Stap voor stap tonen de voorbeelden hoe u:

1. Een afbeelding maakt.
1. Een Graphics-object maakt en initialiseert.
1. Het oppervlak leegmaakt.
1. Een ellips tekent.
1. Een gevulde veelhoek tekent en de afbeelding opslaat.
### **Programmeermonsters**
#### **Een afbeelding maken**
Begin met het maken van een afbeelding met een van de methoden die worden beschreven in Bestanden maken.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **Maak en initialiseer een Graphics-object**
Maak vervolgens een Graphics-object aan door het Image-object door te gegeven aan de constructor.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **Maak het oppervlak leeg**
Maak het Graphics-oppervlak leeg door de Clear-methode van de Graphics-klasse aan te roepen en geef een kleur door als parameter. Deze methode vult het Graphics-oppervlak met de opgegeven kleur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **Teken een ellips**
U zult merken dat de Graphics-klasse meerdere methoden heeft blootgesteld om vormen te tekenen en in te vullen. U vindt de volledige lijst met methoden in de Aspose.PSD voor Java API Reference. Er zijn verschillende overloadversies van de DrawEllipse-methode blootgesteld door de Graphics-klasse. Al deze methoden accepteren een Pen-object als eerste argument. De latere parameters dienen om het begrenzingskader rond de ellips te definiëren. Gebruik voor dit voorbeeld de versie die een Rectangle-object accepteert als tweede parameter om een ellips te tekenen met het Pen-object in de gewenste kleur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **Teken een gevulde veelhoek**
Teken vervolgens een veelhoek met gebruik van de LinearGradientBrush en een array van punten. De Graphics-klasse heeft verschillende overloadversies van de FillPolygon-methode blootgesteld. Al deze methoden accepteren een Brush-object als eerste argument, waarin de kenmerken van de vulling worden gedefinieerd. Het tweede argument is een array van punten. Let erop dat elk twee opeenvolgende punten in het array een zijde van de veelhoek specificeren.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **Afbeeldingen tekenen met Graphics: Volledige broncode**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}



Alle klassen die IDisposable implementeren en toegang hebben tot niet-beheerde resources, worden geïnstantieerd in een Using-verklaring om ervoor te zorgen dat ze correct worden verwijderd.
