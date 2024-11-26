---
title: Aanpassingslaag Helderheid Contrast
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/brightness-contrast/
---

# Werken met de Photoshop Helderheid/Contrast aanpassingslaag in Java

In dit artikel passen we een Helderheid/Contrast aanpassing toe op een Adobe® Photoshop® document met behulp van de Aspose.PSD voor Java® bibliotheek. Daarnaast zullen we meer te weten komen over de bibliotheekfuncties die verband houden met dit soort aanpassingslaag op de lange termijn.

Maar eerst een beetje theorie.

De Helderheid/Contrast aanpassingslaag verandert de helderheid en het contrast van de afbeelding. Maar wacht even, wat betekent dat eigenlijk? Het verhogen van de helderheid maakt de kleurwaarde lichter tot wit en het verlagen van de helderheid maakt de kleurwaarde donkerder tot zwart. Het verhogen van het contrast zal op zijn beurt het verschil tussen lichte en donkere kleuren vergroten en het verlagen van het contrast zal dat verschil respectievelijk verkleinen; dit betekent dat lichte kleuren lichter worden en donkere kleuren donkerder worden.

## De ondersteunde kleurmodus

De bibliotheek maakt het mogelijk om Helderheid/Contrast aanpassingslagen toe te voegen aan afbeeldingen in RGB, CMYK of Lab kleurmodus.

## Het huidige en oude gedrag

De huidige bibliotheekimplementatie (v20.6 op het moment van schrijven) maakt gebruik van het standaard Photoshop-algoritme dat het volledige toonbereik van de schaduwen tot de hooglichten behoudt, maar het ondersteunt nog niet het oude gedrag. Dit betekent dat de bibliotheek Helderheid/Contrast aanpassingslagen ondersteunt in documenten die zijn gemaakt in de nieuwste versies van Photoshop (CS4 en hoger). U kunt echter [verouderde implementatie van de Helderheid/Contrast aanpassingslaag aanvragen](https://forum.aspose.com/c/psd) op ons forum als u dat nodig heeft.

## Helderheid en contrast aanpassen

Laten we nu beschrijven hoe de high-level API van de Helderheid/Contrast aanpassingslaag werkt (vooruitkijkend, de API is eenvoudig). De PsdImage-klasse bevat een fabrieksmethode (addBrightnessContrastAdjustmentLayer) om de BrightnessContrastLayer-klasse te instantiëren die de toegangspoort is voor helderheid en contrast aanpassing. De BrightnessContrastLayer-klasse bevat slechts een paar getters en setters voor toegang tot de helderheid en contrast eigenschappen en om hun waarden te wijzigen.

![|Voorbeeld van Helderheid/Contrast Aanpassingslaag in PSD](brightness-contrast-psd-adjustment-layer-figure-1.png)

Laten we dus een afbeelding van een hond (b) nemen, bijvoorbeeld, om de helderheid1 en contrast2 aan te passen (a), met alleen de fabrieksmethode met overeenkomstige argumenten, om uiteindelijk een afbeelding (c) te krijgen die er levendiger uitziet:

BrightnessContrastLayer brightnessContrastLayer = psdImage.addBrightnessContrastAdjustmentLayer(15, 27);

Opmerkingen:

1. De waarde van de helderheid moet liggen tussen -150 en 150.
2. De waarde van het contrast moet liggen tussen -50 en 100.

Raadpleeg de documentatie van [BrightnessContrastLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BrightnessContrastLayer) voor meer informatie.

## Conclusie

In dit artikel hebben we een snel overzicht gekregen van de Helderheid/Contrast aanpassingslaag en geleerd hoe we de helderheid en contrast van de afbeelding kunnen aanpassen met behulp van de fabrieksmethode.

Raadpleeg onze serie [artikelen over aanpassingslaag-API's](/nl/psd/java/layer-types/adjustment-layer/) van Aspose.PSD voor Java om meer te leren.
