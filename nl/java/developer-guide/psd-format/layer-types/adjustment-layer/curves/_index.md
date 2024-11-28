---
title: Curves Aanpassingslaag
type: docs
weight: 30
url: /nl/java/layer-types/adjustment-layer/curves/
---

# Werken met de Curves aanpassingslaag in Photoshop met Java

Het doel van dit artikel is het demonstreren van de mogelijkheden van de Aspose.PSD bibliotheek voor Java bij het **werken met Curves aanpassingslagen** in Adobe® Photoshop®-documenten. De bibliotheek is volledig autonoom en werkt daarom zonder dat de Photoshop fotobewerker geïnstalleerd hoeft te zijn. De [volledige lijst met functies](https://docs.aspose.com/psd/java/features/) is te vinden in onze kennisbank. Laten we nu teruggaan naar Curves.

## API-overzicht

De Curves tool kan worden gerepresenteerd als een diagonale lijn (curve) op een grafiek met hooglichten in de rechterbovenhoek en schaduwen in de rechterbenedenhoek.

De bibliotheek biedt een API om met de curve te werken, namelijk, de [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer) klasse. Echter heeft deze klasse **twee compleet verschillende benaderingen** om met de curve te werken. Daarom kan het op elk moment in een van de twee modi worden bewerkt:

- Continu (de curve wordt gerepresenteerd als een pad met punten op de buigingsplaatsen)
- Discreet (de curve wordt gerepresenteerd als een stippellijn)

Dus, de bibliotheek heeft twee manieren om de curve aan te passen met behulp van respectievelijk de [continu manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) en [discrete manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager). Vervolgens zullen we uitleggen hoe elk van hen te gebruiken aan de hand van een specifiek voorbeeld.

## Kleur en toon aanpassen met behulp van de Curves Continu Manager

De [Curves Continu Manager](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) **configureert buigingspunten van een continue curve** voor het composietkanaal (RGB) evenals voor elk afzonderlijk kleurkanaal. Ter demonstratie zullen enkele Curves-aanpassingen (a) worden toegepast op een verduisterde afbeelding van een orkest (b) om een opgehelderde afbeelding met warmere kleuren te verkrijgen (c):

![Curves Aanpassingslaag Figuur 1](curves-psd-adjustment-layer-figure-1.png)

Aangezien er twee managers zijn, is het noodzakelijk om er expliciet een te selecteren (in dit geval de continu manager), voordat deze wordt verkregen. Vervolgens kunnen we direct buigpunten toevoegen op bepaalde coördinaten voor gewenste kleurkanalen (composiet RGB, respectievelijk rood en blauw) om de vorm van de curve opnieuw te creëren:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

De oorsprong van de coördinaten is in de linkeronderhoek. De maximale coördinatiewaarde van een punt is beperkt tot het gegevenstype (byte) en is gelijk aan 255 (127 voor het ondertekende type).

Er zijn ook nog een paar [andere methoden](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) die je kunt gebruiken.

## Toon aanpassen met behulp van de Curves Discreet Manager

De Curves Discrete Manager maakt ook het positioneren van curvepunten mogelijk (eigenlijk het veranderen van kleur en toon), maar het verschil is dat ze dit op een andere manier doen. Ten eerste bestaat de **curve uit punten** of stippen (geen continue lijn). Ten tweede **plaatst deze manager nergens een punt** op de grafiek. In plaats daarvan **verplaatst deze het punt omhoog of omlaag** met een waardebereik tussen 255 en 0 respectievelijk. Standaard nemen waarden van curvepunten incrementeel toe om een curve te vormen die onder een hoek van 45 graden staat.

Dus, met dat in gedachten, is het gemakkelijk om de "Negatieve (RBG)" Photoshop-instelling opnieuw te creëren (a) en deze toe te passen op een grijswaardebeeld van een vallei (b) om uiteindelijk een negatieve representatie van de vallei te verkrijgen (c).

![Curves Aanpassingslaag Figuur 2](curves-psd-adjustment-layer-figure-2.png) Allereerst, vergeet niet om de overeenkomstige manager te selecteren om deze te kunnen gebruiken en stel vervolgens waarden van punt van de curve in aflopende volgorde in, te beginnen vanaf 255 naar beneden naar 0 voor elk curvepunt (totaal 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

De manager biedt ook nog een paar [andere methoden](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) voor het beheren van de curve.

## Conclusie

In dit artikel hebben we geleerd hoe we kunnen werken met Curves aanpassingslagen in Photoshop-documenten met behulp van Aspose.PSD voor Java op twee volledig verschillende manieren (continue en discrete managers).
