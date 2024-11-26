---
title: Exposure Aanpassingslaag
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/exposure/
---

# Werken met Photoshop Exposure aanpassingslaag in Java

In dit artikel gaan we een Exposure aanpassingslaag toevoegen aan het Adobe® Photoshop®-document met behulp van Aspose.PSD voor Java - een bibliotheek voor het manipuleren van PSD-bestandsindelingen. De bibliotheek werkt zonder de geïnstalleerde Photoshop-editor omdat het eigen beeldverwerkingsalgoritmen gebruikt. We hebben ook enkele details geleerd die verband houden met de belichtingsaanpassings-API van de bibliotheek.

## API-overzicht

De Exposure aanpassingslaag wordt geconfigureerd via de [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer) klasse die de volgende eigenschappen bevat om met de belichtingsaanpassing te werken:

- Het bepaalt hoeveel licht de foto heeft door de hele histogram relatief tot de zwarten samen te drukken of uit te rekken. Het heeft hoofdzakelijk invloed op de hooglichten.
- In tegenstelling tot belichting-offset heeft hoofdzakelijk invloed op de schaduwen.
- Gammacorrectie. Het corrigeert de lichtsterkte van de afbeelding.

## Correcte belichting

Het corrigeren van de belichting en gerelateerde eigenschappen is zo eenvoudig als het wijzigen van een paar eigenschappen van de klasse. Laten we enkele belichtingsaanpassingen (a) toepassen op een onderbelichte foto van een bibliotheek (b) om deze waarneembaar te maken voor het menselijk oog (c).

![Voorbeeld van Exposure Aanpassingslaag](exposure-adjustment-layer-figure-1.png)

De gehele aanpassing wordt hoofdzakelijk gemaakt met behulp van gammacorrectie. Echter, belichting en offset worden ook een beetje aangepast. Het enige wat je hoeft te doen is de juiste waarden in te stellen voor de eerder genoemde eigenschappen:

    ExposureLayer exposureLayer = psdImage.addExposureAdjustmentLayer();
    exposureLayer.setExposure(-0.03f);
    exposureLayer.setOffset(-0.0005f);
    exposureLayer.setGammaCorrection(1.85f);

Let op dat de belichting in het bereik van -20.0 tot 20.0 moet liggen, de offsetwaarde in het bereik van -0.5 tot 0.5 moet liggen en het bereik van de gammacorrectie tussen 9.99 en 0.01 moet liggen.

Raadpleeg de [API-referentie van de Exposure aanpassingslaag](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ExposureLayer) voor meer details.

## Conclusie

In dit artikel hebben we geleerd hoe we een Exposure aanpassingslaag aan een PSD-bestand kunnen toevoegen om het beeld op te lichten, evenals enkele API-details overwogen.
