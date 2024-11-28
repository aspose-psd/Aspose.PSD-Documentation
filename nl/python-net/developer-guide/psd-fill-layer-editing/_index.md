---
title: PSD Vul laag bijwerken met behulp van Python
weight: 100
type: docs
description: Voorbeelden van het gebruik van alle soorten aanpassingslagen, waaronder Kleurvulling, Gradiëntvulling en Patroonvulling
keywords: [vul laag, Kleurvulling, Gradiëntvulling, Patroonvulling, psd api, python, voorbeeldcode]
url: nl/python-net/psd-fill-layer-editing/
---

## **Overzicht**

Om een reguliere laag te maken, kunt u de create_regular_layer functie gebruiken die in de code wordt meegeleverd. Deze functie neemt de parameters left, top, width en height om de positie en grootte van de laag te definiëren. Het maakt een nieuwe laag, stelt de grenzen in en vult deze met een opgegeven kleur.

Om een kleurvullingslaag te maken, kunt u de FillLayer.create_instance methode gebruiken met de FillType.COLOR parameter. Nadat u de vul laag hebt gemaakt, kunt u de vulinstellingen ervan benaderen met behulp van de fill_settings eigenschap en de kleur instellen met behulp van de kleur eigenschap van de ColorFillSettings klasse. In de verstrekte code wordt de kleur ingesteld op Color.coral. De clipping eigenschap van de vul laag is ingesteld op 1, waardoor de laag fungeert als een klemmasker.

Om een gradiëntvullingslaag te maken, kunt u de FillLayer.create_instance methode gebruiken met de FillType.GRADIENT parameter. Vergelijkbaar met de kleurvullingslaag kunt u de vulinstellingen benaderen met de fill_settings eigenschap en de gradiëntkleurpunten en transparantiepunten instellen. In de verstrekte code worden de gradiëntkleurpunten gedefinieerd met de GradientColorPoint klasse en de transparantiepunten worden gedefinieerd met de GradientTransparencyPoint klasse. Ook de clipping eigenschap van de vul laag is ingesteld op 1.

Om een patroonvullingslaag te maken, kunt u de FillLayer.create_instance methode gebruiken met de FillType.PATTERN parameter. Opnieuw kunt u de vulinstellingen benaderen met de fill_settings eigenschap en de patroongegevens en andere eigenschappen instellen. In de verstrekte code worden de patroongegevens gedefinieerd met behulp van de PatternFillSettings klasse en de clipping eigenschap is ingesteld op 1.

Nadat u de vul lagen hebt gemaakt, kunt u ze aan de PSD-afbeelding toevoegen met behulp van de add_layer methode. U kunt ook de weergavenaam en andere eigenschappen voor elke vullingslaag specificeren.

Uiteindelijk kunt u de PSD-afbeelding en de overeenkomstige PNG-afbeelding opslaan met behulp van de verstrekte code. De PNG-opties zijn ingesteld om truecolor met alpha voor transparantie te gebruiken.

Controleer het volledige voorbeeld.

## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-psd-fill-laag-bewerking.py" >}}
