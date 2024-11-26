---
title: Werken met maskers in Aspose.PSD voor Java
weight: 100
type: docs
description: Voorbeelden van hoe je kunt werken met Clipping, Raster en Vector Maskers in een PSD-bestand
keywords: [maskers, laagmasker, vectormasker, knipmasker, psd, psd api, java, codesample]
url: /nl/java/update-create-layer-mask/
---

## **Overzicht**

**Overzicht**
	
	Er zijn 3 soorten maskers in PSD-bestanden:
	1. Knipmaskers
	2. Rastermaskers
	3. Vectormaskers
	
	Dit artikel behandelt alle 3 typen.

**Knipmaskers**

Knipmaskers zijn een krachtige functie in grafisch ontwerp en beeldbewerkingssoftware, vooral in Java. Ze maken nauwkeurige controle mogelijk over de zichtbaarheid van één laag op basis van de vorm en de inhoud van een andere laag. Een knipmasker beperkt in wezen de zichtbaarheid van een laag tot de vorm van een andere laag eronder.

Om een knipmasker in Java toe te passen, heb je eerst twee lagen nodig: de basellaag en de laag die je wilt knippen. De basellaag definieert de vorm of het gebied dat zichtbaar blijft, terwijl de laag die moet worden geknipt de inhoud bevat die zich aan de vorm van de basellaag zal aanpassen.

Wanneer een knipmasker in Java wordt toegepast, is de inhoud van de geknipte laag alleen zichtbaar binnen de grenzen van de basellaag. Elke inhoud buiten deze grenzen zal verborgen of afgeknipt worden.

Knipmaskers zijn vooral waardevol bij het toepassen van effecten, zoals texturen of patronen, op specifieke delen van een afbeelding of kunstwerk. Door een knipmasker te gebruiken, kun je het effect beperken tot het gewenste gebied zonder de rest van de afbeelding te beïnvloeden.

Raadpleeg het voorbeeld aan het einde van de pagina voor verduidelijking.

**Rastermaskers** 

Rastermaskers in Java-bestanden worden gebruikt om de zichtbaarheid van specifieke gebieden binnen een laag te beheren. In tegenstelling tot vectormaskers, die wiskundige vormen gebruiken om gemaskerde gebieden te definiëren, vertrouwen rastermaskers op op pixelinformatie gebaseerde gegevens om zichtbare of verborgen regio's te bepalen.

Een rastermasker bestaat uit een grijswaardenafbeelding die op een laag wordt toegepast. Witte gebieden van het masker duiden op zichtbaarheid, terwijl zwarte gebieden verborgen delen vertegenwoordigen. Grijstinten daartussen kunnen gedeeltelijke transparantie of semi-zichtbare gebieden creëren.

Raadpleeg het voorbeeld aan het einde van de pagina voor een beter begrip.

**Vectormaskers**

Vectormaskers in Java-bestanden zijn veelzijdige tools die worden gebruikt om de zichtbaarheid van specifieke gebieden binnen een laag te beschrijven op basis van wiskundige vormen. In tegenstelling tot rastermaskers, die afhankelijk zijn van op pixels gebaseerde gegevens, maken vectormaskers gebruik van paden en curven om gladde en schaalbare gemaskerde gebieden te creëren.

Een vectormasker bestaat in feite uit een pad dat op een laag wordt toegepast. De vorm van dit pad bepaalt welke delen van de laag zichtbaar zijn en welke verborgen zijn. Door de besturingspunten en curven van het pad te manipuleren, kunnen nauwkeurige en ingewikkelde gemaskerde gebieden worden gecreëerd.

Raadpleeg de [Vectormaskers pagina](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) voor informatie over het toevoegen van vectormaskers met behulp van bronnen.

## **Voorbeeld**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-update-create-layer-mask.java" >}}
