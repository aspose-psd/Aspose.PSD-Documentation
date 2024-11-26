---
title: Slimme Filter Manipulatie in Aspose.PSD voor C#
weight: 100
type: docs
description: Voorbeelden van hoe Slimme Filters te gebruiken in een PSD-bestand
keywords: [slimme filter, ruis toevoegen, gauss vervagen, verscherpen, filter, psd filter, psd api, C#, csharp, codevoorbeeld]
url: nl/smart-filters/
---

## Overzicht

Er zijn drie manieren om slimme filters toe te passen in Aspose.PSD voor C#.

### Direct Filter Toepassen

Dit voorbeeld laat zien hoe je direct slimme filters kunt toepassen in Aspose.PSD voor C#.

Geef eerst het bron-PSD-bestand, het uitvoerbestand voor de originele afbeelding en het uitvoerbestand voor de bijgewerkte afbeelding op.

Laad vervolgens de PSD-afbeelding met behulp van de `Image.Load`-methode en typeer het als een `PsdImage`-object.

Sla de originele afbeelding op met de `Save`-methode met de opgegeven uitvoernaam.

Maak een `SharpenSmartFilter`-object aan dat het toe te passen slimme filter vertegenwoordigt.

Haal de reguliere laag op uit de PSD-afbeelding met behulp van `psdImage.Layers[1]`.

Pas de `sharpenFilter` drie keer toe op de reguliere laag in een lus.

Sla tot slot de bijgewerkte afbeelding op met de `Save`-methode met de opgegeven uitvoernaam.

Deze code laat zien hoe je direct slimme filters kunt toepassen in Aspose.PSD voor C#. Door de juiste filterobjecten te gebruiken en deze toe te passen op de gewenste lagen, kun je de gewenste effecten op je afbeeldingen bereiken.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulatie van Slimme Filters in Slimme Objecten

Dit voorbeeld laat zien hoe je slimme filters kunt manipuleren binnen slimme objecten.

Geef eerst het bron-PSD-bestand, het uitvoerbestand voor de originele afbeelding en het uitvoerbestand voor de bijgewerkte afbeelding op.

Laad de PSD-afbeelding met behulp van de `Image.Load`-methode en typeer het als een `PsdImage`-object.

Sla de originele afbeelding op met de `Save`-methode met de opgegeven uitvoernaam.

Typeer de tweede laag van de PSD-afbeelding als een `SmartObjectLaag`-object.

Bewerk de slimme filters. Dit voorbeeld laat zien hoe je werkt met `GaussianBlurSmartFilter` en `AddNoiseSmartFilter`.

Voor `GaussianBlurSmartFilter`, werk de filterwaarden bij, waaronder straal, mengmodus, dekking en ingeschakelde status.

Voor `AddNoiseSmartFilter`, stel de ruisverdeling in op `NoiseDistribution.UNIFORM`.

Voeg nieuwe filteritems toe aan de slimme objectlaag: nog een `GaussianBlurSmartFilter` en `AddNoiseSmartFilter`.

Pas de wijzigingen toe met behulp van de `UpdateResourceValues`-methode.

Pas de filters direct toe op de laag en op de masker van de laag met respectievelijk de `Apply`- en `ApplyToMask`-methoden.

Sla de bijgewerkte afbeelding op met de `Save`-methode met de opgegeven uitvoernaam.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Toepassen van Slimme Filters op Laag Masker

Slimme filters zijn een krachtige tool voor beeldbewerking waarmee gebruikers verschillende filters en effecten kunnen toepassen. Een interessante techniek is deze toe te passen op maskers, waarmee je nauwkeurig de gebieden kunt beheren die door het filter worden beïnvloed.

Een masker is een grijswaardebeeld dat de transparantie van bepaalde afbeeldingsgebieden bepaalt, met selectieve toepassing van filters, aanpassingen of effecten.

Bij het toepassen van slimme filters op maskers worden de filters alleen toegepast op de door het masker gespecificeerde gebieden. Deze precieze controle maakt manipulatie van de intensiteit en omvang van het filter mogelijk.

Voor meer gedetailleerde informatie en voorbeelden, raadpleeg de [Aspose.PSD for C# documentatie](https://docs.aspose.com/psd/net/).
