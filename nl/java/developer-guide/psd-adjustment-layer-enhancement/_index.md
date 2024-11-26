---
title: Het Gebruik van Aanpassingslaag voor PSD-Verbeteringen
weight: 100
type: docs
description: Voorbeelden van het gebruik van aanpassingslaag via Aspose.PSD voor Java
keywords: [aanpassingslaag, foto verbeteren, curve aanpassing, niveaus verbetering, omkeren, foto filter,  psd api, java, voorbeeldcode]
url: nl/java/adjustment-layer-enhancement/
---

## **Overzicht**

Dit artikel verkent het bewerken van aanpassingslagen in Aspose.PSD voor Java. Aanpassingslagen zijn een krachtige functie in beeldbewerking waarmee u niet-destructieve wijzigingen kunt aanbrengen in uw afbeeldingen. Aspose.PSD biedt een uitgebreide set aanpassingslaagklassen die u kunt gebruiken om verschillende aspecten van uw afbeeldingen te wijzigen.

Om het bewerken van aanpassingslagen te demonstreren, zullen we een voorbeeldcodefragment aan het einde van de pagina verstrekken dat een PSD-afbeelding laadt en verschillende aanpassingen toepast op de lagen.

In het volgende codefragment beginnen we met het laden van de PSD-afbeelding met behulp van de methode PsdImage.load(). Vervolgens stellen we de opties in voor het opslaan van de uitvoer-PNG-bestanden. De klasse PngOptions stelt ons in staat het kleurtype voor de uitvoerafbeelding te specificeren.

Vervolgens itereren we door elke laag in de PSD-afbeelding en controleren we het type met de methode isAssignable(). Als de laag van een specifiek type is, casten we deze naar dat type met behulp van de methode cast() en passen we de gewenste aanpassing toe. Bijvoorbeeld, we passen de helderheid en het contrast aan van een BrightnessContrastLayer, wijzigen de niveaus van een LevelsLayer, voegen een curve-punt toe aan een CurvesLayer, enzovoort.

U kunt extra code toevoegen om andere aanpassingen toe te passen op hun respectievelijke lagen. Aspose.PSD biedt een breed scala aan aanpassingslaagklassen, zoals [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), en meer.

Tenslotte slaan we de aangepaste afbeelding op met behulp van de methode save() van de klasse PsdImage.

Dit geeft een basisoverzicht van hoe u aanpassingslagen kunt bewerken in Aspose.PSD voor Java. U kunt de aanpassingen aanpassen aan uw vereisten en de verschillende opties verkennen die beschikbaar zijn in de API-documentatie.

Bekijk hieronder het volledige voorbeeld.

## **Voorbeeld**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
