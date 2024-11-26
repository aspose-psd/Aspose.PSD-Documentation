---
title: Omgekeerde Aanpassingslaag
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/invert/
---

# Werken met Photoshop Omgekeerde aanpassingslaag in Java

In dit artikel laten we zien hoe je afbeeldingen in een Photoshop-document programmatisch kunt omzetten naar een negatief met behulp van Java. Hiervoor zullen we de bibliotheek gebruiken voor het manipuleren van PSD-bestandsindeling genaamd Aspose.PSD voor Java.

De kleuromkering API maakt het mogelijk om een **negatief effect aan een afbeelding toe te voegen**. Je hebt misschien al gezien hoe je [de kleuren van een afbeelding omkeert met behulp van de curven aanpassingslaag](/psd/nl/nl/java/layer-types/adjustment-layer/curves/). Vandaag zullen we echter een snellere en eenvoudigere manier overwegen om de klus te klaren met de Omgekeerde aanpassingslaag.

## API-overzicht

**De API van de Omgekeerde aanpassingslaag** bestaat uit de laagsklasse zelf, genaamd [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Deze klasse heeft geen eigen openbare leden, omdat deze alle openbare leden erft van de bovenliggende klasse ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Dit vereenvoudigt het gebruik ervan omdat het enige wat je hoeft te doen is het toevoegen aan een PSD-bestand en de afbeelding wordt negatief.

## Kleuren van afbeelding omkeren

Dus, zelfs als het voor de hand ligt, laten we voor de duidelijkheid zien hoe je een **Omgekeerde aanpassingslaag toepast op de afbeelding** van een astronaut (a) om het negatieve effect voor die afbeelding te creëren (b).

![Voorbeeld van Omgekeerde aanpassingslaag voor en na](invert-adjustment-layer-figure-1.png)

Om de **kleuren van de afbeelding om te keren** voeg je eenvoudig een Omgekeerde aanpassingslaag toe aan de PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

Dat is alles! Er zijn geen specifieke eigenschappen die geconfigureerd moeten worden voor dit type aanpassingslaag.

## Conclusie

In dit artikel hebben we geleerd over de Omgekeerde aanpassingslaag API van Aspose.PSD voor Java. Het is een eenvoudig hulpmiddel om negatieve afbeeldingen te verkrijgen omdat de API van deze aanpassingslaag geen openbare leden declareert.
