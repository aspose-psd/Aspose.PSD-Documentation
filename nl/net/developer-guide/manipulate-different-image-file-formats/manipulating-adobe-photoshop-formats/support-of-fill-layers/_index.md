---
title: Ondersteuning van Vullagen
type: docs
weight: 90
url: /nl/ondersteuning-vullagen/
---

## **Vullagen Met Patroonvulling**
Dit artikel toont hoe u de [PSD ](https://wiki.fileformat.com/image/psd/)laag kunt vullen met de Patroonvulling. Een Patroon is een afbeelding, kleur, schaduw of lijn die wordt gebruikt om een gebied van een afbeelding te vullen. Gebruik de Aspose.PSD.FileFormats.Psd.Layers.FillLayer om een Patroon toe te voegen aan de PSD-laag. De volgende codefragmenten laden een PSD-bestand, openen de [Filllayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)klasse en stellen het Patroon in met behulp van de [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings) eigenschappen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}


Hier is nog een voorbeeld dat laat zien hoe [Aspose.PSD](https://products.aspose.com/psd/net) het patroon rendert door gebruik te maken van [FillLayer ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer)en [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings)[ ](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Vullagen Met Verloopvulling**
Dit artikel demonstreert het gebruik van Verloopvulling om de PSD-laag te vullen. Aspose.PSD-API's hebben efficiënte en eenvoudig te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) en [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) klassen blootgelegd om een Verloopeffect toe te voegen aan een laag.

De stappen om de [PSD ](https://wiki.fileformat.com/image/psd/)laag te vullen met Verloopvulling zijn eenvoudig, zoals hieronder:

- Laad een PSD-bestand als afbeelding met behulp van de fabrieksmethode [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) aangeboden door de [Image](https://reference.aspose.com/net/psd/aspose.psd/image) klasse.
- Stel de instellingseigenschappen in van het [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) object.
- Maak een lijst van [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) met de vereiste kleuren en posities van kleur.
- Maak een lijst van transparantiepunten met de benodigde dekking en positie van het transparantiepunt.
- Roep de [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update) methode aan.
- Sla de resultaten op.



Het volgende codefragment toont hoe u Verloopvulling kunt toevoegen om de PSD-laag te vullen.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**Hier is nog een voorbeeld dat gebruik maakt van de [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** eigenschap om de PSD-laag te vullen met Verloopvulling. Aspose.PSD ondersteunt de volgende verloopsoorten via de GradientType enumeratie:

- **GradientType.Linear:**       In een lineair verloop verloopt de kle
