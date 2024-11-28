---
title: Ondersteuning van Vullagen
type: docs
weight: 50
url: /nl/java/ondersteuning-van-vullagen/
---


## **Ondersteuning van Vullagen Met Kleur Vulling**
Dit artikel demonstreert hoe u een PSD-laag met kleur kunt vullen. Gebruik de Aspose.PSD.FileFormats.Psd.Layers.FillLayer om kleur toe te voegen aan een PSD-laag. De volgende codefragmenten laden een PSD-bestand, openen de FillLayer-klasse en stellen de kleur in met behulp van de FillLayer.FillSettings-eigenschap.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-BestandenWijzigenEnConverterenAfbeeldingen-PSD-KleurVullingsLaag-KleurVullingsLaag.java" >}}
## **Ondersteuning van Vullagen Met Gradiënt Vulling**
Dit artikel demonstreert het gebruik van een gradiëntvulling om een PSD-laag te vullen. Aspose.PSD API's hebben efficiënte en gemakkelijk te gebruiken methoden blootgelegd om dit doel te bereiken. Aspose.PSD heeft de klassen GradientColorPoint en GradientTransparencyPoint blootgesteld om een gradiënteffect aan een laag toe te voegen.

` `De stappen om een PSD-laag met een gradiëntvulling te vullen zijn zo eenvoudig als hieronder:

- Laad een PSD-bestand als afbeelding met behulp van de factory-methode Load blootgesteld door de Image-klasse.
- Stel instellingen eigenschappen in van het FillLayer object.
- Maak een lijst van ColorPoints met vereiste kleuren en positie van de kleur.
- Maak een lijst van transparencyPoints met vereiste dekking en positie van het transparantiepunt.
- Roep de FillLayer.Update methode aan.
- Sla de resultaten op.



Het volgende codefragment toont u hoe u een gradiëntvulling toevoegt om een PSD-laag te vullen.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-BestandenWijzigenEnConverterenAfbeeldingen-PSD-GradiëntVullingsLaag-GradiëntVullingsLaag.java" >}}


## **Slageffect Met Kleurvulling**
Dit artikel demonstreert hoe u een slageffect met kleurvulling kunt weergeven. Het slageffect wordt gebruikt om slagen en randen aan lagen en vormen toe te voegen. Het kan worden gebruikt om lijnen in een egale kleur te maken, kleurrijke gradiënten, evenals patroonranden.

De stappen om een slageffect met kleurvulling weer te geven zijn zo eenvoudig als hieronder:

- Stel de eigenschap **LoadEffectsResource** in.
- Laad een PSD-bestand als afbeelding met behulp van de factory-methode Load blootgesteld door de Image-klasse en definieer **PsdLoadOptions**.
- Stel instellingen eigenschappen in van **ColorFillSetting.**
- Sla de resultaten op.

Het volgende codefragment toont u hoe u een slageffect met kleurvulling kunt weergeven.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Voorbeelden-src-main-java-com-aspose-psd-voorbeelden-BestandenWijzigenEnConverterenAfbeeldingen-PSD-SlageffectMetKleurvulling-SlageffectMetKleurvulling.java" >}}


