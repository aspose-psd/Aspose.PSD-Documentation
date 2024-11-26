---
title: Afbeeldingen Bijsnijden, Draaien en Formaat wijzigen
type: docs
weight: 40
url: /nl/java/afbeeldingen-bijsnijden-draaien-en-formaat-wijzigen/
---

## **Afbeeldingen Bijsnijden**
Het bijsnijden van afbeeldingen verwijst meestal naar het verwijderen van de buitenste delen van een afbeelding om het kader te verbeteren. Bijsnijden kan ook worden gebruikt om een deel van een afbeelding uit te snijden om de focus op een specifiek gebied te vergroten. De Aspose.PSD API ondersteunt twee verschillende benaderingen voor het bijsnijden van afbeeldingen: met verschuivingen en rechthoek.
### **Bijsnijden met Verschuivingen**
De klasse RasterImage biedt een overbelaste versie van de Crop-methode die 4 integerwaarden accepteert die Links, Rechts, Boven en Onder aangeven. Op basis van deze vier waarden verplaatst de Crop-methode de afbeeldingsgrenzen naar het midden van de afbeelding terwijl het buitenste gedeelte wordt verwijderd. Het onderstaande codefragment toont hoe je een afbeelding bijsnijdt met verschuivingen.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
### **Bijsnijden met een Rechthoek**
De klasse RasterImage biedt een andere overbelaste versie van de Crop-methode die een instantie van de Rectangle-klasse accepteert. Je kunt elk deel van een afbeelding uitsnijden door de gewenste grenzen aan het Rectangle-object te geven. Het onderstaande codefragment toont hoe je een afbeelding bijsnijdt met een rechthoek.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}
## **Afbeelding Draaien en Omdraaien**
Aspose.PSD voor Java is een eenvoudig te gebruiken bibliotheek omdat het eenvoudige methoden biedt om complexe bewerkingen uit te voeren. Zo heeft Aspose.PSD voor Java bijvoorbeeld de RotateFlip-methode geleverd voor zijn basisklasse Image als een toepassing een afbeelding moet roteren. Ongeacht het afbeeldingsformaat kan de bibliotheek specifieke rotatie- en omdraaibewerkingen uitvoeren.
### **Een Afbeelding Roteren**
De Image.RotateFlip-methode kan worden gebruikt om de afbeelding met 90/180/270 graden te roteren en de afbeelding horizontaal of verticaal om te draaien. De Image.RotateFlip-methode accepteert een parameter van het type RotateFlipType die het type rotatie en omdraaien specificeert dat op de afbeelding moet worden toegepast. De stappen om te roteren en om te draaien zijn net zo eenvoudig als hieronder:

1. Laad een afbeelding in met de fabrieksmethode Load blootgesteld door de klasse Image.
1. Roep de Image.RotateFlip-methode aan terwijl je het juiste RotateFlipType specificeert.
1. Sla de resultaten op.

Het onderstaande codevoorbeeld toont hoe je de RotateFlip-eigenschap van een Image en de RotateFlipType-enumeratie instelt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}
## **Afbeelding Draaien op een Specifieke Hoek**
Aspose.PSD voor Java API maakt gebruik van de RasterImage.Rotate-methode om gebruikers de mogelijkheid te bieden om een afbeelding op een specifieke hoek te draaien. In tegenstelling tot de RasterImage.RotateFlip-methode accepteert de RasterImage.Rotate-methode drie parameters:

1. Rotatiehoek: een parameter van het type float die de rotatiehoek aangeeft waarmee de afbeelding moet worden gedraaid. Een positieve waarde roteert de afbeelding met de klok mee; een negatieve waarde voert een tegen de klok in rotatie uit.
1. Proportioneel herschalen: een parameter van het type Boolean dat aangeeft of de afmetingen van de afbeelding moeten worden gewijzigd op basis van de geprojecteerde hoeken van de geroteerde rechthoek. Als dit op false is ingesteld, blijven de afmetingen van de afbeelding ongewijzigd en wordt alleen de interne inhoud van de afbeelding geroteerd.
1. Achtergrondkleur: een parameter van het type Color die de kleur aangeeft die moet worden ingevuld in de achtergrond van de geroteerde afbeelding.

Het onderstaande codefragment toont het gebruik van de RasterImage.Rotate-methode.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}
## **Afbeeldingen Formaat wijzigen**
Dit artikel demonstreert het gebruik van Aspose.PSD voor Java om een formaatwijziging uit te voeren op een afbeelding. Aspose.PSD-API's hebben efficiënte en eenvoudig te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD voor Java heeft de Resize-methode blootgelegd voor de Image-klasse die kan worden gebruikt om bestaande afbeeldingen on-the-fly te herschalen. Er zijn twee overbelastingen van de Resize-methode om te voldoen aan de behoeften van de toepassing.
### **Eenvoudige Formaatwijziging**
De stappen om te herschalen zijn net zo eenvoudig als hieronder:

1. Laad een afbeelding in met de fabrieksmethode Load blootgesteld door de klasse Image.
1. Roep de Image.Resize-methode aan terwijl je de nieuwe Hoogte & Breedte specificeert.
1. Sla de resultaten op.

Het onderstaande codevoorbeeld toont hoe je een afbeelding herschaalt.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Herschalen met ResizeType Enumeratie**
Aspose.PSD API heeft de ResizeType-enumeratie blootgesteld die kan worden gebruikt met Image.Resize om de gewenste resultaten te bereiken. Het onderstaande codefragment laat zien hoe de ResizeType-enumeratie wordt gebruikt, terwijl de details van de ResizeType-enumeratieleden onderaan deze pagina te vinden zijn.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}



Als je kwalitatieve resultaten wilt krijgen na het toepassen van de formaatwijziging, wordt aanbevolen om altijd ResizeType.LanczosResample te gebruiken, omdat dit zeer kwalitatieve resultaten oplevert maar mogelijk langzamer werkt dan ResizeType.NearestNeighbourResample. Aan de andere kant wordt het algoritme ResizeType.NearestNeighbourResample specifiek gebruikt voor snelle herdimensionering met compromis op de beeldkwaliteit. Deze methode kan nuttig zijn voor het genereren van miniaturen in realtime of vergelijkbare processen waar prestatie vereist is.
## **Afbeelding Proportioneel Formaat wijzigen**
Je kunt afbeeldingen herschalen door nieuwe hoogte- en breedtewaarden door te geven als parameters aan de Image.Resize-methode, maar in dat geval moet je zelf de beeldverhouding berekenen. Dit komt doordat wanneer de breedte of hoogte van een afbeelding wordt gewijzigd, de afbeelding wordt geschaald of verkleind om de nieuwe grootte te vullen. Als de wijzigingen aan de breedte en hoogte van een afbeelding niet in verhouding zijn, kan dit leiden tot uitgerekte en vervormde resultaten. Dit artikel demonstreert het gebruik van de Aspose.PSD voor Java API om afbeeldingen te herschalen door nieuwe hoogte of breedte door te geven terwijl de API automatisch de andere proportionele waarde berekent.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **ResizeType Enumeratie**
ResizeType bepaalt het type formaatwijziging dat op de afbeelding moet worden uitgevoerd op basis van het geselecteerde filter.

Leden van ResizeType Enumeratie

|**Lidnaam**|**Waarde**|**Beschrijving**|
| :- | :- | :- |
|LinksBovenNaarLinksBoven|0|Het linkerbovenpunt van de nieuwe afbeelding zal samenvallen met het linkerbovenpunt van de originele afbeelding. Er zal bijsnijden plaatsvinden indien nodig.|
|RechtsBovenNaarRechtsBoven|1|Het rechterbovenpunt van de nieuwe afbeelding zal samenvallen met het rechterbovenpunt van de originele afbeelding. Er zal bijsnijden plaatsvinden indien nodig.|
|RechtsOnderNaarRechtsOnder|2|Het rechteronderpunt van de nieuwe afbeelding zal samenvallen met het rechteronderpunt van de originele afbeelding. Er zal bijsnijden plaatsvinden indien nodig.|
|LinksOnderNaarLinksOnder|3|Het linkerbenedenpunt van de nieuwe afbeelding zal samenvallen met het linkerbenedenpunt van de originele afbeelding. Er zal bijsnijden plaatsvinden indien nodig.|
|MiddenNaarMidden|4|Het midden van de nieuwe afbeelding zal samenvallen met het midden van de originele afbeelding. Er zal bijsnijden plaatsvinden indien nodig.|
|LanczosResample|5|Hersample met Lanczos-algoritme met 7x7 masker.|
|DichtstbijzijndeBuurrelatieHersample|6|Hersample met naburig algoritme.|
