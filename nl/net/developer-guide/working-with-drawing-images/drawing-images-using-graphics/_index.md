---
title: Het tekenen van afbeeldingen met behulp van Graphics
type: docs
weight: 20
url: /nl/net/het-tekenen-van-afbeeldingen-met-behulp-van-graphics/
---

## **Het tekenen van afbeeldingen met behulp van Graphics**
Met de Aspose.PSD-bibliotheek kun je eenvoudige vormen tekenen zoals lijnen, rechthoeken en cirkels, evenals complexe vormen zoals veelhoeken, curves, bogen en Bezier-vormen. De Aspose.PSD-bibliotheek maakt dergelijke vormen met behulp van de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-klasse die zich bevindt in de Aspose.PSD-namespace. Graphics-objecten zijn verantwoordelijk voor het uitvoeren van verschillende tekenoperaties op een afbeelding, waardoor het oppervlak van de afbeelding verandert. De [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-klasse maakt gebruik van diverse hulpobjecten om de vormen te verbeteren:

·          Pennen, om lijnen te tekenen, vormen te omlijnen of andere meetkundige representaties weer te geven.

·          Penselen, om te definiëren hoe gebieden worden ingekleurd.

·          Lettertypes, om de vorm van tekens van tekst te definiëren.
### **Teken met de Graphics-klasse**
Hieronder staat een codevoorbeeld dat het gebruik van de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-klasse demonstreert. De voorbeeldbroncode is opgesplitst in verschillende delen om het eenvoudig en gemakkelijk te volgen te houden. Stap voor stap tonen de voorbeelden hoe je:

1. Een afbeelding maakt.
1. Een Graphics-object maakt en initialiseert.
1. Het oppervlak wist.
1. Een ellips tekent.
1. Een opgevulde veelhoek tekent en de afbeelding opslaat.
### **Programmeervoorbeelden**
#### **Een Afbeelding Maken**
Begin met het maken van een afbeelding met behulp van een van de methoden die worden beschreven in Het maken van bestanden.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Maak en Initialiseer een Graphics-Object**
Maak vervolgens een Graphics-object en initialiseer het door het Image-object door te gegeven aan de constructor.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **Wis het Oppervlak**
Wis het Graphics-oppervlak door de Clear-methode van de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-klasse aan te roepen en een kleur mee te geven als parameter. Deze methode vult het Graphics-oppervlak met de meegegeven kleur.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **Teken een Ellips**
Je zult opmerken dat de [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)-klasse veel methoden heeft blootgesteld om vormen te tekenen en in te vullen. Je vindt de volledige lijst van methoden in de Aspose.PSD voor .NET API Referentie. Er zijn verschillende overload-versies van de DrawEllipse-methode blootgesteld door de Graphics-klasse. Al deze methoden accepteren een Pen-object als eerste argument. De latere parameters worden meegegeven om het begrenzingskader rond de ellips te definiëren. Voor dit voorbeeld, gebruik de versie die een Rectangle-object als tweede parameter accepteert om een ellips te tekenen met het Pen-object in de gewenste kleur.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **Teken een Opgevulde Veelhoek**
Teken vervolgens een veelhoek met behulp van de LinearGradientBrush en een reeks punten. De Graphics-klasse heeft verschillende overload-versies van de FillPolygon()-methode blootgesteld. Al deze accepteren een Brush-object als eerste argument, waarbij de kenmerken van de vulling worden gedefinieerd. Het tweede argument is een reeks punten. Let op dat elke twee opeenvolgende punten in de reeks een zijde van de veelhoek specificeren.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **Het tekenen van afbeeldingen met behulp van Graphics : Complete Bron**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

Alle klassen die IDisposable implementeren en toegang hebben tot onbeheerde resources worden geïnstantieerd in een Using-statement om ervoor te zorgen dat ze correct worden afgesloten.
