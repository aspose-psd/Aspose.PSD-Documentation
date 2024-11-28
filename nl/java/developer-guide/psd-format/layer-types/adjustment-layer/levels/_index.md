---
title: Aanpassingslaag zwart en wit
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/levels/
---

## Werken met de aanpassingslaag Niveaus in Java

In dit artikel zullen we leren hoe we het toonbereik en de kleurbalans van een foto in [PSD-bestandsindeling](/psd/nl/java/psd-format/) programmeerbaar kunnen aanpassen in Java. We gebruiken niet de Adobe® Photoshop® fotobewerker zelf. In plaats daarvan gebruiken we de bibliotheek Aspose.PSD voor Java die zelfstandig werkt om het Photoshop-document te manipuleren.

Hoewel Aspose.PSD voor Java meer dan voldoende [tools ondersteunt om de foto te bewerken](/psd/nl/java/manipulating-images/) zoals wij willen, laten we toch **werken met de API voor aanpassingslaag Niveaus** omdat dit een van de eenvoudigste en snelste manieren is om het werk te doen.

## API-overzicht

De huidige implementatie (20.6 op het moment van schrijven) van de API voor aanpassing van de Niveaus **ondersteunt alle basisfuncties van Photoshop Niveaus** , namelijk het aanpassen van de invoer- en uitvoerniveaus voor het samengestelde kanaal (RGB) evenals voor elk primaire kleurkanaal (rood, groen en blauw).

De API van de aanpassingslaag Niveaus is eenvoudig. De klasse [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) is het startpunt voor de aanpassing van de Niveaus. Het bevat een paar methoden om toegang te krijgen tot kleurkanalen: getMasterChannel en getChannel(int). Beide methoden retourneren [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) dat overeenkomstige eigenschappen heeft voor manipulatie van invoer- en uitvoerniveaus. Het verschil is dat getMasterChannel dient om het samengestelde kleurkanaal (RGB) aan te passen, terwijl getChannel toegang geeft tot een specifiek kleurkanaal (rood, groen of blauw) op basis van zijn index.

## Compatibiliteit met kleurmodi

Het is de moeite waard toe te voegen dat de aanpassingslaag Niveaus **compatibel is met de overgrote meerderheid van de kleurmodi** volgens Photoshop Niveaus. Daarom is het mogelijk om Niveaus aan te passen voor afbeeldingen in Grijswaarden (grijs kanaal), RGB (RGB, rood, groen en blauw kanalen), CMYK (CMYK, cyaan, magenta, geel en zwart kanalen), Duotonen (monotone kanaal) en LAB (helderheid, a en b kanalen) kleurmodi.

## Toonbereik aanpassen

Eenvoudig gezegd, de tooncorrectie wordt toegepast op een afbeelding om de schaduwen en de highlights opnieuw toe te wijzen voor een betere verdeling van de middentonen. Over het algemeen **maakt dit de afbeelding er contrastrijker uit** , indien correct uitgevoerd. Laten we bijvoorbeeld een foto van een hond nemen (b) en het toonbereik aanpassen (a - de schermafbeelding komt uit het venster Photoshop Niveaus voor duidelijkheid) om de foto er contrastrijker uit te laten zien (c).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Niveaus Laag Figuur 1](levels-adjustment-figure-1.png)|

Om **het algehele toonbereik aan te passen** van een afbeelding, moeten de invoerniveaus van het hoofdkanaal worden ingesteld:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

Het is nodig om in gedachten te houden dat de invoerniveaus tussen 0 en 253 moeten liggen voor schaduwen, tussen 9,99 en 0,01 voor middentonen en tussen 2 en 255 voor highlights. Het bereik van uitvoerniveaus moet tussen 0 en 255 liggen.

Meer voorbeelden nodig? Je kunt ze vinden op [Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) en in de [kennisbank](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## Conclusie

Samenvattend heeft Aspose.PSD voor Java een handige en eenvoudige API voor het aanpassen van het toonbereik en de kleurbalans van een afbeelding die compatibel is met bijna alle kleurmodi. De API van de aanpassingslaag Niveaus van de bibliotheek lijkt op Photoshop Niveaus, daarom is het gemakkelijk om aan de slag te gaan, zelfs als je nog nooit eerder met de bibliotheek hebt gewerkt.
