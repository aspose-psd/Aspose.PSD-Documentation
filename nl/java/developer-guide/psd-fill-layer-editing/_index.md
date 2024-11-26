---
title: PSD Vul laag bijwerken met Java
weight: 100
type: docs
description: Voorbeelden van het gebruik van alle soorten aanpassingslagen, inclusief Kleurvulling, Gradiëntvulling en Patroonvulling
keywords: [vul laag, Kleurvulling, Gradiëntvulling, Patroonvulling, psd api, java, voorbeeldcode]
url: nl/java/psd-fill-layer-editing/
---

## **Overzicht**

Het maken van een reguliere laag omvat het gebruik van de createRegularLayer-functie, die parameters vereist voor het definiëren van de positie en grootte van de laag. Deze functie maakt een nieuwe laag, stelt de grenzen in en vult deze met een gespecificeerde kleur.

Voor een kleurvullingslaag gebruikt u de FillLayer.createInstance-methode met de FillType.Color-parameter. Zodra de vul laag is aangemaakt, kunt u de vulinstellingen benaderen via de fill_settings-eigenschap en de gewenste kleur instellen met behulp van de color-eigenschap van de ColorFillSettings-klasse. In deze context wordt de kleur ingesteld op Color.getCoral(). Daarnaast wordt de clipping-eigenschap van de vul laag ingesteld op 1, waardoor deze fungeert als een afknipmasker.

Gradiëntvullagen worden op een vergelijkbare manier aangemaakt met behulp van de FillLayer.createInstance-methode, maar met de FillType.Gradient-parameter. Net als bij kleurvullagen benadert u de vulinstellingen via fill_settings en stelt u de gradiëntkleurpunten en transparantiepunten in. In dit voorbeeld worden de gradiëntkleurpunten gedefinieerd met de GradientColorPoint-klasse en de transparantiepunten met de GradientTransparencyPoint-klasse. De clipping-eigenschap van de vul laag wordt ook ingesteld op 1.

Patroonvullagen worden gemaakt met behulp van FillLayer.createInstance met de FillType.Pattern-parameter. Opnieuw benadert u de vulinstellingen via fill_settings en stelt u de patroongegevens en andere eigenschappen in. In deze code worden de patroongegevens gedefinieerd met behulp van de PatternFillSettings-klasse, en wordt de clipping-eigenschap ingesteld op 1.

Zodra de vul lagen zijn aangemaakt, voegt u ze toe aan het PSD-image met behulp van de addLayer-methode, waarbij u de weergavenaam en andere eigenschappen voor elke vul laag specificieert.

Tenslotte, sla het PSD-image en het bijbehorende PNG-image op met de verstrekte code. De PNG-opties zijn geconfigureerd om ware kleur met alfa te gebruiken voor transparantie.

Raadpleeg het volledige voorbeeld voor meer details.

## **Voorbeeld**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentatie-Java-Aspose-psd-Fill-Layer-Bewerken.java" >}}
