---
title: Support des calques de remplissage
type: docs
weight: 90
url: /fr/support-des-calques-de-remplissage/
---

## **Calques de remplissage avec motif de remplissage**
Cet article démontre comment remplir le calque [PSD](https://wiki.fileformat.com/image/psd/) avec le motif de remplissage. Un motif est une image, une couleur, une ombre ou une ligne utilisée pour remplir une zone d'une image. Veuillez utiliser Aspose.PSD.FileFormats.Psd.Layers.FillLayer pour ajouter un motif dans le calque PSD. Les extraits de code suivants chargent un fichier PSD, accèdent à la classe [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) et définissent le motif à l'aide des propriétés [PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}

Voici un autre exemple qui démontre comment [Aspose.PSD](https://products.aspose.com/psd/net) rend le motif en utilisant [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) et [IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **Calques de remplissage avec remplissage dégradé**
Cet article démontre l'utilisation du remplissage dégradé pour remplir le calque PSD. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé les classes [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) et [GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) pour ajouter un effet dégradé à un calque.

Les étapes pour remplir le [calque PSD](https://wiki.fileformat.com/image/psd/) avec un remplissage dégradé sont aussi simples que ci-dessous :

- Charger un fichier PSD en tant qu'image en utilisant la méthode d'usine [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) exposée par la classe [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- Définir les propriétés des paramètres de [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- Créer une liste de [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) avec les couleurs requises et les positions des couleurs.
- Créer une liste de points de transparence avec l'opacité requise et la position du point de transparence.
- Appeler la méthode [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update).
- Enregistrer les résultats.


L'extrait de code suivant vous montre comment ajouter un remplissage dégradé pour remplir un calque PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}

**Voici un autre exemple qui utilise la propriété [**GradientFillSettings.GradientType**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** pour remplir le calque PSD avec un remplissage dégradé. Aspose.PSD prend en charge les types de dégradé suivants via l'énumération GradientType :

- **GradientType.Linear:** Dans un dégradé linéaire, la transition de couleur se fait en ligne droite du ton de départ à la fin.
- **GradientType.Radial:** Dans un dégradé radial, les couleurs se déploient à partir du point de départ selon un motif circulaire.
- **GradientType.Angle:** Dans un dégradé angulaire, le dégradé tourne dans le sens inverse des aiguilles d'une montre autour du point de départ.
- **GradientType.Reflected:** Dans un dégradé réfléchi, la couleur est réfléchie de part et d'autre du point de départ.
- **GradientType.Diamond:** Le dégradé en forme de diamant crée une forme de diamant à partir du point de départ.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **Support de la propriété d'échelle pour le calque de remplissage dégradé**
Cet article démontre comment mettre à l'échelle le calque de remplissage avec un remplissage dégradé en utilisant Aspose.PSD pour .NET. À cette fin, une nouvelle propriété [**Echelle**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) a été ajoutée dans [**IGradientFillSettings**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings). 

Voici la démonstration de code qui montre comment utiliser la propriété **Echelle**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **Calques de remplissage avec remplissage de couleur**
Cet article démontre comment remplir le calque [PSD](https://wiki.fileformat.com/image/psd/) avec une couleur. Veuillez utiliser la classe [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) pour ajouter une couleur dans le calque PSD. L'extrait de code suivant charge un fichier PSD, accède à la classe de calque de remplissage et définit la couleur en utilisant la propriété [FillLayer.FillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/properties/fillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}
