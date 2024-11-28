---
title: Utilisation de la couche d'ajustement pour l'amélioration de PSD
weight: 100
type: docs
description: Exemples d'utilisation des calques d'ajustement via Aspose.PSD pour C#
keywords: [calque d'ajustement, amélioration de photo, ajustement de courbes, amélioration de niveaux, inversion, filtre photo, API psd, C#, csharp, exemple de code]
url: fr/couche-d-ajustement-amelioration/
---

## Aperçu

Dans cet article, nous explorerons l'édition des calques d'ajustement dans Aspose.PSD pour C#. Les calques d'ajustement sont une fonctionnalité puissante dans l'édition d'images qui vous permettent d'apporter des modifications non destructives à vos images. Aspose.PSD fournit un ensemble complet de classes de calques d'ajustement que vous pouvez utiliser pour modifier divers aspects de vos images.

Pour illustrer l'édition des calques d'ajustement, nous utiliserons un extrait de code d'exemple à la fin de la page qui charge une image PSD et applique différentes modifications à ses calques.

Dans l'extrait de code ci-dessous, nous commençons par charger l'image PSD en utilisant la méthode `PsdImage.Load()`. Nous configurons ensuite les options pour enregistrer les fichiers PNG de sortie. La classe `PngOptions` nous permet de spécifier le type de couleur pour l'image de sortie.

Ensuite, nous parcourons chaque calque de l'image PSD et vérifions son type en utilisant la méthode `IsAssignable()`. Si le calque est d'un type spécifique, nous le convertissons en ce type en utilisant la méthode `Cast()` et appliquons l'ajustement souhaité. Par exemple, nous ajustons la luminosité et le contraste d'une `BrightnessContrastLayer`, modifions les niveaux d'une `LevelsLayer`, ajoutons un point de courbe à une `CurvesLayer`, etc.

Vous pouvez ajouter du code supplémentaire pour appliquer d'autres ajustements à leurs calques respectifs. Aspose.PSD fournit une large gamme de classes de calques d'ajustement, telles que [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), et plus encore.

Enfin, nous enregistrons l'image modifiée en utilisant la méthode `Save()` de la classe `PsdImage`.

Ce code fournit un aperçu de base de la façon d'éditer les calques d'ajustement dans Aspose.PSD pour C#. Vous pouvez personnaliser les ajustements selon vos besoins et explorer les différentes options disponibles dans la documentation de l'API.

## Exemple

Voici un exemple de code démontrant comment utiliser les calques d'ajustement avec Aspose.PSD pour C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

Pour des informations plus détaillées et des exemples, veuillez visiter la [documentation Aspose.PSD pour C#](https://docs.aspose.com/psd/net/).
