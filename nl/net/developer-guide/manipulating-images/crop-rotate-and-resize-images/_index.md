---
title: Afbeeldingen bijsnijden, roteren en formaat wijzigen
type: docs
weight: 40
url: /nl/net/afbeeldingen-bijsnijden-rotaten-formaat-wijzigen/
---

## **Afbeeldingen bijsnijden**
Bij het bijsnijden van afbeeldingen gaat het meestal om het verwijderen van de buitenste delen van een afbeelding om de compositie te verbeteren. Bijsnijden kan ook worden gebruikt om een deel van een afbeelding uit te knippen om de focus te vergroten op een specifiek gebied. De Aspose.PSD API ondersteunt twee verschillende benaderingen voor het bijsnijden van afbeeldingen: via verschuivingen en rechthoek.
### **Bijsnijden via verschuivingen**
De klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) biedt een overbelaste versie van de Crop-methode die 4 gehele getallen accepteert die respectievelijk links, rechts, boven en onder aanduiden. Op basis van deze vier waarden verplaatst de Crop-methode de afbeeldingsgrenzen naar het midden van de afbeelding en verwijdert het buitenste gedeelte. Het onderstaande codefragment toont hoe je een afbeelding kunt bijsnijden via verschuivingen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-BijsnijdenViaVerschuivingen-BijsnijdenViaVerschuivingen.cs" >}}
### **Bijsnijden via rechthoek**
De klasse [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) biedt een andere overbelaste versie van de Crop-methode die een instantie van de Rectangle-klasse accepteert. Je kunt elk deel van een afbeelding uitknippen door de gewenste grenzen aan het Rectangle-object te geven. Het onderstaande codefragment toont hoe je een afbeelding kunt bijsnijden via een rechthoek.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-BijsnijdenViaRechthoek-BijsnijdenViaRechthoek.cs" >}}
## **Roteren en spiegelen van een afbeelding**
Aspose.PSD voor .NET is een gebruiksvriendelijke bibliotheek omdat het eenvoudige methoden biedt om complexe handelingen uit te voeren. Bijvoorbeeld, Aspose.PSD voor .NET heeft de RotateFlip-methode verstrekt voor de basisklasse Image als een toepassing behoefte heeft aan het roteren van een afbeelding. Ongeacht het beeldformaat kan de bibliotheek specifieke roteer- en spiegelprocedures uitvoeren.
### **Een afbeelding roteren**
De Image.RotateFlip-methode kan worden gebruikt om de afbeelding met 90/180/270 graden te roteren en de afbeelding horizontaal of verticaal te spiegelen. De Image.RotateFlip-methode accepteert een parameter van het type RotateFlipType dat het type rotatie en spiegeling specificeert die op de afbeelding moeten worden toegepast. De stappen om te roteren en spiegelen zijn zo eenvoudig als hieronder,

1. Laad een afbeelding in met behulp van de fabrieksmethode Load blootgesteld door de klasse Image.
1. Roep de Image.RotateFlip-methode aan terwijl je het juiste RotateFlipType specificieert.
1. Sla de resultaten op.

Het volgende codevoorbeeld toont hoe je de RotateFlip-eigenschap van een Image en de RotateFlipType-enumeratie kunt instellen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-RoterenVanEenAfbeelding-RoterenVanEenAfbeelding.cs" >}}
## **Een afbeelding roteren op een specifieke hoek**
Aspose.PSD voor .NET API ontsluit de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-methode om zijn gebruikers te helpen die een afbeelding op een specifieke hoek willen roteren. In tegenstelling tot de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip-methode, accepteert de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-methode drie parameters:

1. Rotatiehoek: Een parameter van het type float dat de rotatiehoek aangeeft waarmee de afbeelding moet worden geroteerd. Een positieve waarde roteert de afbeelding met de klok mee; een negatieve waarde voert een tegen-de-klok-in rotatie uit.
1. Proportioneel schalen: Een parameter van het type boolean specificeert of de afmetingen van de afbeelding moeten worden gewijzigd volgens de geprojecteerde hoekpunten van de geroteerde rechthoek. Als deze op false is ingesteld, blijven de afmetingen van de afbeelding ongewijzigd en worden alleen de interne afbeeldingsinhoud geroteerd.
1. Achtergrondkleur: Een parameter van het type Color geeft de kleur aan die moet worden ingevuld in de achtergrond van de geroteerde afbeelding.

Het onderstaande codefragment toont het gebruik van de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate-methode.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-RoterenVanEenAfbeeldingOpEenSpecifiekeHoek-RoterenVanEenAfbeeldingOpEenSpecifiekeHoek.cs" >}}
## **Afbeeldingen formaat wijzigen**
Dit artikel illustreert het gebruik van Aspose.PSD voor .NET om een formaatwijziging uit te voeren op een afbeelding. Aspose.PSD API's hebben efficiënte en eenvoudig te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD voor .NET heeft de Resize-methode blootgesteld voor de Image-klasse die kan worden gebruikt om bestaande afbeeldingen on-the-fly van formaat te wijzigen. Er zijn twee overbelastingen van de Resize-methode om te voldoen aan de behoeften van de toepassing.
### **Eenvoudig formaat wijzigen**
De stappen om een formaatwijziging uit te voeren zijn zo eenvoudig als hieronder:

1. Laad een afbeelding in met behulp van de fabrieksmethode Load blootgesteld door de klasse Image.
1. Roep de Image.Resize-methode aan terwijl je de nieuwe Hoogte & Breedte specificieert.
1. Sla de resultaten op.

Het volgende codevoorbeeld toont hoe je een afbeelding kunt formaat wijzigen.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-EenvoudigFormaatWijzigen-EenvoudigFormaatWijzigen.cs" >}}
### **Formaat wijzigen met ResizeType-enumeratie**
Aspose.PSD API heeft ResizeType-enumeratie blootgelegd die kan worden gebruikt met Image.Resize om gewenste resultaten te behalen. Het onderstaande codefragment toont het gebruik van ResizeType-enumeratie, terwijl de details van de leden van ResizeType-enumeratie te vinden zijn onderaan deze pagina.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-FormaatWijzigenMetResizeTypeEnEnumeratie-FormaatWijzigenMetResizeTypeEnEnumeratie.cs" >}}


Als je kwaliteitsresultaten wilt behalen na het toepassen van de formaataanpassing, dan wordt voorgesteld om altijd ResizeType.LanczosResample te gebruiken, omdat het zeer kwalitatieve resultaten oplevert maar mogelijk langzamer werkt dan ResizeType.NearestNeighbourResample. Aan de andere kant wordt de ResizeType.NearestNeighbourResample algoritme specifiek gebruikt voor snelle formaataanpassing met als compromis de kwaliteit van de afbeelding. Deze methode kan nuttig zijn voor het genereren van miniaturen in real-time of soortgelijke processen waar prestaties vereist zijn.
## **Afbeelding proportioneel formaat wijzigen**
Je kunt afbeeldingen van formaat wijzigen door nieuwe hoogte- en breedtewaarden door te geven als parameters aan de Image.Resize-methode, maar in dat geval moet je zelf de beeldverhouding berekenen. Dit komt omdat wanneer de breedte of hoogte van een afbeelding wordt gewijzigd, wordt de afbeelding geschaald of verkleind om de nieuwe grootte te vullen. Als de wijzigingen in de breedte en hoogte van een afbeelding niet in verhouding zijn, kan dit leiden tot uitgerekte en vervormde resultaten. Dit artikel demonstreert het gebruik van Aspose.PSD voor .NET API om afbeeldingen van formaat te wijzigen door het doorgeven van een nieuwe hoogte of breedte en waarbij de API automatisch de andere evenredige waarde berekent.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Voorbeelden-CSharp-Aspose-TekenenEnOpmaakAfbeeldingen-AfbeeldingProportioneelFormaatWijzigen-AfbeeldingProportioneelFormaatWijzigen.cs" >}}
### **ResizeType-enumeratie**
ResizeType bepaalt het type formaataanpassing dat op de afbeelding moet worden uitgevoerd op basis van het geselecteerde filter.

Leden van [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype) enumeratie

|**Lidnaam**|**Waarde**|**Beschrijving**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Linker bovenhoek van de nieuwe afbeelding zal overeenkomen met de linker bovenhoek van de originele afbeelding. Bijsnijden zal plaatsvinden indien nodig.|
|RightTopToRightTop|1|Rechter bovenhoek van de nieuwe afbeelding zal overeenkomen met de rechter bovenhoek van de originele afbeelding. Bijsnijden zal plaatsvinden indien nodig.|
|RightBottomToRightBottom|2|Rechter onderhoek van de nieuwe afbeelding zal overeenkomen met de rechter onderhoek van de originele afbeelding. Bijsnijden zal plaatsvinden indien nodig.|
|LeftBottomToLeftBottom|3|Linker onderhoek van de nieuwe afbeelding zal overeenkomen met de linker onderhoek van de originele afbeelding. Bijsnijden zal plaatsvinden indien nodig.|
|CenterToCenter|4|Het midden van de nieuwe afbeelding zal overeenkomen met het midden van de originele afbeelding. Bijsnijden zal plaatsvinden indien nodig.|
|LanczosResample|5|Hersampelen met Lanczos-algoritme met een masker van 7x7.|
|NearestNeighbourResample|6|Hersampelen met naburig algoritme.|

