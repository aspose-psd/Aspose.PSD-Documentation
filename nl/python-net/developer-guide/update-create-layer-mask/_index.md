---
title: Werken met maskers in Aspose.PSD voor Python
weight: 100
type: docs
description: Voorbeelden van hoe te werken met Clipping, Raster en Vector Maskers binnen PSD-bestand
keywords: [maskers, laagmasker, vectormasker, knipmasker, psd, psd api, python, codevoorbeeld]
url: /nl/python-net/update-create-layer-mask/
---

## **Overzicht**

**Overzicht**
	
	Er zijn 3 soorten maskers in PSD-bestanden:
	1. Knipmaskers
	2. Rastermaskers
	3. Vectormaskers
	
	Dit artikel behandelt alle 3 types.


** Knipmaskers **

Knipmaskers zijn een krachtige functie in grafisch ontwerp en beeldbewerkingssoftware. Ze stellen je in staat om de zichtbaarheid van één laag te controleren op basis van de vorm en inhoud van een andere laag. Met andere woorden, een knipmasker beperkt de zichtbaarheid van een laag tot de vorm van een andere laag eronder.

Om een knipmasker te maken, heb je eerst twee lagen nodig: de basiskleur en de laag die je wilt knippen. De basiskleur bepaalt de vorm of het gebied dat zichtbaar zal zijn, terwijl de laag die je wilt knippen de inhoud bevat die bijgesneden zal worden naar de vorm van de basiskleur.

Wanneer je een knipmasker toepast, is de inhoud van de bijgesneden laag alleen zichtbaar binnen de grenzen van de basiskleur. Eventuele inhoud buiten de grenzen van de basiskleur zal verborgen of bijgesneden worden.

Knipmaskers zijn bijzonder handig wanneer je een effect, zoals een textuur of patroon, wilt toepassen op een specifiek gebied van een afbeelding of kunstwerk. Door een knipmasker te gebruiken, kun je het effect beperken tot het gewenste gebied zonder de rest van de afbeelding te beïnvloeden.

Bekijk het voorbeeld aan het einde van de pagina

** Rastermaskers ** 

Rastermaskers in PSD-bestanden worden gebruikt om de zichtbaarheid van specifieke gebieden binnen een laag te regelen. In tegenstelling tot vectormaskers, die wiskundige vormen gebruiken om de gemaskerde gebieden te definiëren, maken rastermaskers gebruik van op pixel gebaseerde informatie om te bepalen welke delen van een laag zichtbaar of verborgen zijn.

Een rastermasker bestaat uit een grijswaardenafbeelding die op een laag wordt toegepast. De witte gebieden van het masker vertegenwoordigen de zichtbare delen, terwijl de zwarte gebieden de verborgen delen vertegenwoordigen. Grijstinten er tussenin kunnen worden gebruikt om gedeeltelijke transparantie of semi-zichtbare delen te creëren.

Bekijk het voorbeeld aan het einde van de pagina

** Vectormaskers **

Vectormaskers in PSD-bestanden zijn een veelzijdig instrument dat wordt gebruikt om de zichtbaarheid van specifieke gebieden binnen een laag te definiëren op basis van wiskundige vormen. In tegenstelling tot rastermaskers, die op pixel gebaseerde informatie gebruiken, maken vectormaskers gebruik van paden en curven om gladde en schaalbare gemaskerde gebieden te creëren.

Een vectormasker is in feite een pad dat op een laag wordt toegepast. De vorm van het pad bepaalt welke delen van de laag zichtbaar zijn en welke delen verborgen zijn. Door de besturingspunten en curven van het pad te manipuleren, kun je precieze en ingewikkelde gemaskerde gebieden creëren.

Bekijk de [Vectormaskers pagina](psd/nl/net/layer-vector-mask/) voor informatie over hoe de vectormaskers kunnen worden toegevoegd met behulp van bronnen.


## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-psd-update-create-layer-mask.py" >}}
