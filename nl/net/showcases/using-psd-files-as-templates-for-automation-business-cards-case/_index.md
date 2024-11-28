---
title: Het gebruik van PSD-bestanden als sjablonen voor automatisering - Geval van visitekaartjes
type: docs
weight: 10
url: /nl/het-gebruik-van-psd-bestanden-als-sjablonen-voor-automatisering-geval-van-visitekaartjes/
---

### **Overzicht**
Dit artikel beschrijft vaak voorkomende gevallen waarbij u enkele lagen in een [PSD-bestand](https://wiki.fileformat.com/image/psd/) programmatisch moet bijwerken, waarbij het PSD/PSB-bestand een bekende sjabloonachtige structuur heeft. Dit kan worden gebruikt om een groot aantal visitekaartjes te maken voor verschillende mensen (geval van visitekaartjes). Of u moet een vertaling van het PSD-bestand maken naar verschillende talen met de vervanging van sommige grafische materialen erin.

Na het lezen van dit artikel weet u hoe u dit kunt doen:

![todo:image_alt_text](het-gebruik-van-psd-bestanden-als-sjablonen-voor-automatisering-geval-van-visitekaartjes_1.png)

## **Eenvoudig geval**
Stel dat u bijvoorbeeld een PSD-sjabloon hebt met de bekende laagnamen. Dus u moet een PSD-laag wijzigen, bijwerken of vervangen via C#. Allereerst moet u het sjabloonbestand openen met Aspose.PSD.

Hoe opent u een PSD-bestand via C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-1.cs" >}}

![todo:image_alt_text](het-gebruik-van-psd-bestanden-als-sjablonen-voor-automatisering-geval-van-visitekaartjes_2.png)

Vervolgens moeten we een laag vinden die we willen vervangen op basis van de naam ervan. Hier is een eenvoudige implementatie voor dit.

Hoe vindt u de laag in het PSD-bestand op basis van de naam ervan?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-2.cs" >}}

Wanneer de laag is gevonden, kunnen we deze op gebruikelijke wijze bijwerken met behulp van [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics):

Hoe tekent u op de PSD-laag Graphics?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-3.cs" >}}

In dit geval tekenen we een nieuw geladen [PNG-afbeelding](https://wiki.fileformat.com/image/png/) op de bestaande PSD-laag, zodat de oude gegevens verloren gaan in het nieuwe bestand.

Maar wat als we ook tekst moeten bijwerken? Het proces zal vergelijkbaar zijn. Zoek de [Tekstlaag](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) op basis van de naam ervan en werk vervolgens programmatisch de Tekstlaag van het Photoshop-bestand bij.

Hoe werkt u de Tekstlaag bij in Photoshop met behulp van C#?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-4.cs" >}}

Aan het einde dienen we onze wijzigingen op te slaan:

Hoe slaat u het gewijzigde PSD-bestand op met [Aspose.PSD](https://products.aspose.com/psd/net)?

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-5.cs" >}}

De resulterende afbeelding:

![todo:image_alt_text](het-gebruik-van-psd-bestanden-als-sjablonen-voor-automatisering-geval-van-visitekaartjes_3.png)

## **Een complex geval met extra functies**
Hierboven hebben we de meest eenvoudige manier getoond om een afbeelding in een laag van een PSD-bestand te vervangen.

Maar Aspose.PSD kan meer complexe extra functies bieden, zoals het toevoegen van een nieuwe laag, het verwijderen van oude lagen en het bijwerken van textlaag met verschillende stijlen in meerregelige tekst.

We kunnen de [Laag](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer) vinden die we willen vervangen, vervolgens vinden we de index ervan in de Lijst met Lagen, verwijderen deze en voegen een nieuwe laag toe nadat we deze hebben aangemaakt vanuit [Jpeg-bestand](https://wiki.fileformat.com/image/jpeg/) op dezelfde plaats.

Maak een nieuwe laag van een bestand en voeg deze toe aan de PSD-afbeelding met behulp van [Aspose.PSD](https://products.aspose.com/psd/net)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-6.cs" >}}

Aan het einde van dit bestand met codefragment corrigeren we de positie van de laag en slaan we het nieuwe Lagen-array op in de Psd-afbeelding.

Hoe kopieert u [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) Laageigenschappen?

{{< gist "aspose-com-gists" "8a4dab2ce866d1642fc8c0ce975175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-7.cs" >}}

En tot slot moeten we tekstlagen bijwerken in de bestaande PSD-afbeelding met behulp van C#. Aspose.PSD ondersteunt het bijwerken van Tekstlaag op basis van [delen](/psd/nl/net/werken-met-tekstlagen/). Elk [tekstdeel](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.text/itextportion) heeft een unieke combinatie van stijl- en alineaeigenschappen.

Hoe kopieert u [PsdImage](https://reference.aspose.com/imaging/net/aspose.imaging.fileformats.psd/psdimage) Laageigenschappen?

{{< gist "aspose-com-gists" "8a4dab2ce866d1642fc8c0ce975175c" "Documentatie-CSharp-Aspose-PsdBestandAlsSjabloon-Snippet-8.cs" >}}

Als resultaat hebben we het PSD-sjabloon gewijzigd via code met een nieuwe laag van Jpeg, Png, J2k, Bmp, Gif of Tiff-bestand en meerregelige tekst met verschillende stijlen in elke regel.

![todo:image_alt_text](het-gebruik-van-psd-bestanden-als-sjablonen-voor-automatisering-geval-van-visitekaartjes_4.png)
