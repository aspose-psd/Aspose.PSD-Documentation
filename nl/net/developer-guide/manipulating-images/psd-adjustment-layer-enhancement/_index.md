---
title: Het Gebruiken van Aanpassingslaag voor PSD-Verbeteringen
weight: 100
type: docs
description: Voorbeelden van het gebruik van aanpassingslagen via Aspose.PSD voor C#
keywords: [aanpassingslaag, foto verbeteren, curves aanpassingen, levels verbetering, omkeren, foto filter, psd api, C#, csharp, codevoorbeeld]
url: nl/adjustment-layer-enhancement/
---

## Overzicht

In dit artikel zullen we het bewerken van aanpassingslagen in Aspose.PSD voor C# verkennen. Aanpassingslagen zijn een krachtige functie in de beeldbewerking waarmee u niet-destructieve wijzigingen kunt aanbrengen in uw afbeeldingen. Aspose.PSD biedt een uitgebreide set van klassen voor aanpassingslagen die u kunt gebruiken om verschillende aspecten van uw afbeeldingen te wijzigen.

Om het bewerken van aanpassingslagen te demonstreren, zullen we een voorbeeldcodefragment aan het einde van de pagina gebruiken dat een PSD-afbeelding laadt en verschillende aanpassingen toepast op de lagen ervan.

In het onderstaande codefragment beginnen we met het laden van de PSD-afbeelding met behulp van de `PsdImage.Load()` methode. Vervolgens stellen we de opties in voor het opslaan van de uitvoer-PNG-bestanden. De `PngOptions` klasse stelt ons in staat om het kleurtype voor de uitvoerafbeelding op te geven.

Vervolgens itereren we door elke laag in de PSD-afbeelding en controleren we het type ervan met behulp van de `IsAssignable()` methode. Als de laag van een specifiek type is, gieten we deze om naar dat type met behulp van de `Cast()` methode en passen we de gewenste aanpassing toe. Zo passen we bijvoorbeeld de helderheid en het contrast aan van een `BrightnessContrastLayer`, wijzigen we de niveaus van een `LevelsLayer`, voegen we een curvepunt toe aan een `CurvesLayer`, enzovoort.

U kunt extra code toevoegen om andere aanpassingen toe te passen op hun respectievelijke lagen. Aspose.PSD biedt een breed scala aan klassen voor aanpassingslagen, zoals [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), en meer.

Tot slot slaan we de gewijzigde afbeelding op met behulp van de `Save()` methode van de `PsdImage` klasse.

Deze code biedt een basisoverzicht van hoe u aanpassingslagen kunt bewerken in Aspose.PSD voor C#. U kunt de aanpassingen aanpassen aan uw vereisten en de verschillende opties in de API-documentatie verkennen.

## Voorbeeld

Hier is een codevoorbeeld dat demonstreert hoe u aanpassingslagen kunt gebruiken met behulp van Aspose.PSD voor C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Voor meer gedetailleerde informatie en voorbeelden, bezoek alstublieft de [Aspose.PSD voor C# documentatie](https://docs.aspose.com/psd/net/).
