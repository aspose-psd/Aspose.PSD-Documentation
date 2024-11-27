---
title: Utilisation de la couche d'ajustement pour les améliorations PSD
weight: 100
type: docs
description: Exemples d'utilisation de la couche d'ajustement via Aspose.PSD pour Java
keywords: [couche d'ajustement, amélioration de photo, ajustement de courbes, amélioration de niveaux, inverser, filtre photo,  api psd, java, exemple de code]
url: fr/java/ajustement-de-la-couche-damelioration/
---

## **Aperçu**

Cet article explore l'édition des couches d'ajustement dans Aspose.PSD pour Java. Les couches d'ajustement sont une fonctionnalité puissante dans l'édition d'images qui vous permettent de faire des modifications non destructives sur vos images. Aspose.PSD fournit un ensemble complet de classes de couches d'ajustement que vous pouvez utiliser pour modifier divers aspects de vos images.

Pour démontrer l'édition des couches d'ajustement, nous fournirons un extrait de code d'exemple à la fin de la page qui charge une image PSD et applique différentes ajustements à ses couches.

Dans l'extrait de code suivant, nous commençons par charger l'image PSD en utilisant la méthode PsdImage.load(). Ensuite, nous configurons les options pour sauvegarder les fichiers PNG de sortie. La classe PngOptions nous permet de spécifier le type de couleur pour l'image de sortie.

Ensuite, nous itérons à travers chaque couche de l'image PSD et vérifions son type en utilisant la méthode isAssignable(). Si la couche est d'un type spécifique, nous la castons à ce type en utilisant la méthode cast() et appliquons l'ajustement souhaité. Par exemple, nous ajustons la luminosité et le contraste d'une BrightnessContrastLayer, modifions les niveaux d'une LevelsLayer, ajoutons un point de courbe à une CurvesLayer, et ainsi de suite.

Vous pouvez ajouter du code supplémentaire pour appliquer d'autres ajustements à leurs couches respectives. Aspose.PSD fournit une large gamme de classes de couches d'ajustement, telles que [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), et plus encore.

Enfin, nous sauvegardons l'image modifiée en utilisant la méthode save() de la classe PsdImage.

Cela fournit un aperçu de base de la façon d'éditer les couches d'ajustement dans Aspose.PSD pour Java. Vous pouvez personnaliser les ajustements selon vos besoins et explorer les différentes options disponibles dans la documentation de l'API.

Veuillez consulter l'exemple complet ci-dessous.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
