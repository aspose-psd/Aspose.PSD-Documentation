---
title: Werken met maskers in Aspose.PSD voor С#
weight: 100
type: docs
description: Voorbeelden van hoe te werken met Knippen, Raster en Vector Maskers in een PSD-bestand
keywords: [maskers, laagmasker, vector masker, knipmasker, psd, psd api, C#, csharp, codevoorbeeld]
url: nl/net/update-create-layer-mask/
---

## Overzicht

Er zijn drie soorten maskers in PSD-bestanden:
1. Knipmaskers
2. Rastermaskers
3. Vectormaskers

Dit artikel behandelt alle drie de soorten.

### Knipmaskers

Knipmaskers zijn een krachtige functie in grafisch ontwerp en beeldbewerkingssoftware waarmee je de zichtbaarheid van één laag kunt controleren op basis van de vorm en inhoud van een andere laag. Een knipmasker beperkt essentieel de zichtbaarheid van een laag tot de vorm die wordt gedefinieerd door een andere laag eronder.

Om een knipmasker te maken, heb je twee lagen nodig: de basillaag en de kniplaag. De basillaag definieert de vorm of het gebied dat zichtbaar zal zijn, terwijl de kniplaag de inhoud bevat die beperkt zal worden tot de vorm van de basillaag.

Bij het toepassen van een knipmasker is de inhoud van de kniplaag alleen zichtbaar binnen de grenzen van de basillaag. Elke inhoud buiten de grenzen van de basillaag wordt verborgen of bijgesneden.

Knipmaskers zijn bijzonder handig voor het toepassen van effecten, zoals texturen of patronen, op specifieke gebieden van een afbeelding of kunstwerk. Door een knipmasker te gebruiken, kun je ervoor zorgen dat het effect beperkt blijft tot het gewenste gebied zonder de rest van de afbeelding te beïnvloeden.

### Rastermaskers

Rastermaskers in PSD-bestanden zijn essentieel voor het controleren van de zichtbaarheid van specifieke gebieden binnen een laag. In tegenstelling tot vectormaskers, die wiskundige vormen gebruiken om gemaskerde gebieden te definiëren, gebruiken rastermaskers op pixelinformatie gebaseerde informatie om te bepalen welke delen van een laag zichtbaar of verborgen zijn.

Een rastermasker bestaat uit een grijswaardenafbeelding toegepast op een laag. De witte gebieden van het masker vertegenwoordigen de zichtbare delen, terwijl de zwarte gebieden de verborgen delen vertegenwoordigen. Grijstinten daartussen creëren gedeeltelijke transparantie of semi-zichtbare gebieden.

Met rastermaskers kun je ingewikkelde maskeringseffecten bereiken, waardoor je nauwkeurige controle hebt over de zichtbaarheid van lagen op basis van details op pixelniveau. Deze functie is bijzonder nuttig voor taken die gedetailleerde bewerking en blending binnen een afbeelding vereisen.

### Vectormaskers

Vectormaskers in PSD-bestanden zijn een veelzijdige tool om de zichtbaarheid van specifieke gebieden binnen een laag te definiëren op basis van wiskundige vormen. In tegenstelling tot rastermaskers, die op pixelinformatie zijn gebaseerd, gebruiken vectormaskers paden en krommen om gladde en schaalbare gemaskerde gebieden te creëren.

Een vectormasker is essentieel een pad toegepast op een laag. De vorm van het pad bepaalt welke delen van de laag zichtbaar zijn en welke verborgen zijn. Door de besturingspunten en krommen van het pad te manipuleren, kun je nauwkeurige en ingewikkelde gemaskerde gebieden creëren.

Vectormaskers zijn bijzonder handig voor het creëren van schone, schaalbare maskers die gemakkelijk kunnen worden aangepast zonder verlies van kwaliteit. Deze functie is ideaal voor taken die hoge precisie en flexibiliteit vereisen bij het definiëren van zichtbare gebieden binnen een laag.

Voor meer informatie over het toevoegen van vectormaskers, bezoek de [Vectormaskers pagina](psd/nl/nl/layer-vector-mask/).

## Voorbeeld
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WerkenMetMaskers-WerkenMetMaskers.cs" >}}

Voor meer gedetailleerde informatie en voorbeelden, bezoek alstublieft de [Aspose.PSD voor C# documentatie](https://docs.aspose.com/psd/nl/).
