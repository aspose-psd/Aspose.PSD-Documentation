---
title: Het gebruik van Aanpassingslaag voor PSD-verbeteringen
weight: 100
type: docs
description: Voorbeelden van het gebruik van aanpassingslagen via Aspose.PSD voor Python
keywords: [aanpassingslaag, foto verbeteren, curve aanpassing, niveaus verbeteren, omkeren, foto filter,  psd api, python, codevoorbeeld]
url: nl/python-net/aanpassingslaag-verbetering/
---

## **Overzicht**

In dit artikel zullen we de bewerking van aanpassingslagen in Aspose.PSD voor Python verkennen. Aanpassingslagen zijn een krachtige functie in beeldbewerking waarmee je niet-destructieve wijzigingen kunt aanbrengen aan je afbeeldingen. Aspose.PSD biedt een uitgebreide reeks klassen voor aanpassingslagen die je kunt gebruiken om verschillende aspecten van je afbeeldingen te wijzigen.

Om de bewerking van aanpassingslagen te demonstreren, zullen we een voorbeeldcodefragment aan het einde van de pagina gebruiken dat een PSD-afbeelding laadt en verschillende aanpassingen toepast op de lagen.

In het onderstaande codefragment beginnen we met het laden van de PSD-afbeelding met behulp van de methode PsdImage.load(). Vervolgens stellen we de opties in voor het opslaan van de uitvoer PNG-bestanden. De klasse PngOptions stelt ons in staat om het kleurtype voor de uitvoerafbeelding te specificeren.

Vervolgens doorlopen we elke laag in de PSD-afbeelding en controleren we het type ervan met behulp van de methode is_assignable(). Als de laag van een specifiek type is, passen we het toe op dat type met behulp van de methode cast() en passen de gewenste aanpassing toe. Bijvoorbeeld, we passen de helderheid en het contrast aan van een BrightnessContrastLayer, wijzigen de niveaus van een LevelsLayer, voegen een curvepunt toe aan een CurvesLayer, enzovoort.

Je kunt aanvullende code toevoegen om andere aanpassingen toe te passen op hun respectievelijke lagen. Aspose.PSD biedt een breed scala aan klassen voor aanpassingslagen, zoals [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), en meer.

Tot slot slaan we de gewijzigde afbeelding op met behulp van de methode save() van de klasse PsdImage.

Deze code biedt een basisoverzicht van hoe je aanpassingslagen kunt bewerken in Aspose.PSD voor Python. Je kunt de aanpassingen aanpassen aan je behoeften en de verschillende opties verkennen die beschikbaar zijn in de API-documentatie.

Controleer het volledige voorbeeld.

## **Voorbeeld**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentatie-Python-Aspose-aanpassingslaag-verbetering.py" >}}
