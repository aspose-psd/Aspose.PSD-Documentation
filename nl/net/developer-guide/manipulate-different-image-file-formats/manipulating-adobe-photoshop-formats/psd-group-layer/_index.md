---
title: Voorbeeld van het gebruik van groepslagen in Aspose.PSD voor C#
weight: 100
type: docs
description: Gebruik van Groep Laag van PSD Bestand via C#
keywords: [laaggroep, groepslaag, laag toevoegen aan groep, psd api, C#, csharp, voorbeeldcode]
url: nl/psd-groepslaag/
---

## Overzicht

Groepslagen in Aspose.PSD voor C# zorgen voor efficiënte organisatie en manipulatie van lagen in een PSD-bestand. Door maplagen te gebruiken, kunt u meerdere lagen groeperen en transformaties of effecten toepassen op de hele groep.

Dit voorbeeld toont het maken van een nieuw PSD-beeld met `PsdImage.Create`. Vervolgens wordt een nieuw `LayerGroup`-object gemaakt met behulp van `AddLayerGroup` van het `PsdImage`-object. De groepslaag is genaamd "Map," ingevoegd op index 0 en zichtbaar gemaakt.

Vervolgens worden twee `Layer`-objecten gemaakt met hun `DisplayName`-eigenschappen ingesteld. Deze lagen worden aan de groepslaag toegevoegd met behulp van `AddLayer`.

Lagen binnen de groep kunnen worden benaderd via de `Layers`-eigenschap van het `LayerGroup`-object. Het voorbeeld controleert dat de weergavenamen van de eerste en tweede lagen in de groep "Laag 1" en "Laag 2" zijn.

Na het aanpassen van de groepslagen wordt het bijgewerkte PSD-beeld opgeslagen met de `Save`-methode van het `PsdImage`-object.

Dit basisvoorbeeld introduceert het werken met groepslagen met Aspose.PSD voor C#. De bibliotheek biedt geavanceerde functies voor manipulatie en transformatie van lagen in PSD-bestanden. Raadpleeg de Aspose.PSD voor C# documentatie voor meer gedetailleerde voorbeelden en functies.

Hier is een voorbeeldcode die het gebruiken van groepslagen demonstreert in Aspose.PSD voor C#:

## Voorbeeld

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ExportLayerGroupToImage-ExportLayerGroupToImage.cs" >}}

Voor meer gedetailleerde informatie en voorbeelden, bezoek alstublieft de [Aspose.PSD voor C# documentatie](https://docs.aspose.com/psd/net/).
