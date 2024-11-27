---
title: Utilisation de la couche d'ajustement pour les améliorations PSD
weight: 100
type: docs
description: Exemples d'utilisation de la couche d'ajustement via Aspose.PSD pour Python
keywords: [couche d'ajustement, amélioration de photo, ajustement de courbes, amélioration des niveaux, inversion, filtre photo, api psd, python, exemple de code]
url: fr/python-net/adjustment-layer-enhancement/
---

## **Vue d'ensemble**

Dans cet article, nous explorerons l'édition des couches d'ajustement dans Aspose.PSD pour Python. Les couches d'ajustement sont une fonctionnalité puissante dans l'édition d'images qui vous permettent de faire des modifications non destructives sur vos images. Aspose.PSD fournit un ensemble complet de classes de couche d'ajustement que vous pouvez utiliser pour modifier divers aspects de vos images.

Pour démontrer l'édition des couches d'ajustement, nous utiliserons un extrait de code d'exemple à la fin de la page qui charge une image PSD et applique différentes modifications à ses couches.

Dans l'extrait de code ci-dessous, nous commençons par charger l'image PSD en utilisant la méthode PsdImage.load(). Nous configurons ensuite les options pour enregistrer les fichiers PNG de sortie. La classe PngOptions nous permet de spécifier le type de couleur pour l'image de sortie.

Ensuite, nous itérons à travers chaque couche de l'image PSD et vérifions son type en utilisant la méthode is_assignable(). Si la couche est d'un type spécifique, nous la castons à ce type en utilisant la méthode cast() et appliquons l'ajustement désiré. Par exemple, nous ajustons la luminosité et le contraste d'une BrightnessContrastLayer, modifions les niveaux d'une LevelsLayer, ajoutons un point de courbe à une CurvesLayer, etc.

Vous pouvez ajouter du code supplémentaire pour appliquer d'autres ajustements à leurs couches respectives. Aspose.PSD fournit un large éventail de classes de couche d'ajustement, telles que [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), et plus encore.

Enfin, nous enregistrons l'image modifiée en utilisant la méthode save() de la classe PsdImage.

Ce code fournit un aperçu de base de la manière de modifier les couches d'ajustement dans Aspose.PSD pour Python. Vous pouvez personnaliser les ajustements selon vos besoins et explorer les différentes options disponibles dans la documentation de l'API.

Veuillez consulter l'exemple complet.

## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
