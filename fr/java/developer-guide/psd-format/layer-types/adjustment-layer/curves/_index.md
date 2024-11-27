---
title: Calque d'ajustement de courbes
type: docs
weight: 30
url: /fr/java/types-de-calque/calque-dajustement/courbes/
---

# Travailler avec le calque d'ajustement de courbes Photoshop en Java

L'objectif de cet article est de démontrer les capacités de la bibliothèque Aspose.PSD pour Java lors du **travail avec les calques d'ajustement de courbes** dans les documents Adobe® Photoshop®. La bibliothèque est entièrement autonome. Par conséquent, elle fonctionne sans avoir besoin d'installer l'éditeur de photos Photoshop. La [liste complète des fonctionnalités](https://docs.aspose.com/psd/java/features/) est disponible dans notre base de connaissances. Bon, revenons maintenant aux courbes.

## Présentation de l'API

L'outil Courbes peut être représenté par une ligne diagonale (courbe) sur un graphique avec des points forts dans le coin supérieur droit et des ombres dans le coin inférieur droit.

La bibliothèque fournit une API pour travailler avec la courbe, à savoir, la classe [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). Cependant, cette classe propose **deux approches complètement différentes** pour travailler avec la courbe. Ainsi, il est possible de l'éditer dans l'un des deux modes à la fois :

- Continu (la courbe est représentée comme un chemin avec des points aux endroits de courbure)
- Discret (la courbe est représentée par une ligne en pointillés)

Par conséquent, la bibliothèque propose deux façons de modifier la courbe en utilisant respectivement le [gestionnaire continu](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) et le [gestionnaire discret](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager). Ensuite, nous expliquerons comment utiliser chacun d'eux sur un exemple spécifique.

## Ajuster la couleur et le ton en utilisant le gestionnaire continu des Courbes

Le [Gestionnaire continu des Courbes](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **configure les points de courbure d'une courbe continue** pour le canal composite (RVB) ainsi que pour chaque canal de couleur particulier. À des fins de démonstration, un ajustement des Courbes (a) sera appliqué à une image assombrie d'un orchestre (b) pour obtenir une image éclaircie avec des couleurs plus chaudes (c) :

![Figure 1 du calque d'ajustement de courbes](curves-psd-adjustment-layer-figure-1.png)

Comme il y a deux gestionnaires, il est nécessaire de sélectionner explicitement l'un d'eux (gestionnaire continu dans ce cas), avant de l'obtenir. Ensuite, nous pouvons ajouter directement des points de courbure à certaines coordonnées pour les canaux de couleur souhaités (RVB composite, rouge et bleu respectivement) afin de recréer la forme de la courbe :
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

L'origine des coordonnées se trouve dans le coin inférieur gauche. La valeur de coordonnée maximale d'un point est limitée au type de données (byte) et est égale à 255 (127 pour le type signé).

Il existe également quelques [autres méthodes](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) que vous pouvez utiliser.

## Ajuster le ton en utilisant le gestionnaire discret des Courbes

Le gestionnaire discret des Courbes permet également de positionner des points de courbe (changer la couleur et le ton en réalité), mais la différence est qu'ils le font différemment. Premièrement, la **courbe est composée de points** ou de points (pas d'une ligne solide). Deuxièmement, ce gestionnaire **ne place pas un point n'importe où** sur le graphique. Au lieu de cela, il **déplace le point vers le haut ou vers le bas** dans une plage de valeurs entre 255 et 0 respectivement. Par défaut, les valeurs des points de courbe augmentent de manière incrémentielle pour façonner une courbe qui est à un angle de 45 degrés.

Ainsi, avec cela en tête, il est facile de recréer le préréglage Photoshop "Négatif (RVB)" (a) et de l'appliquer à une image en niveaux de gris d'une vallée (b) pour obtenir à la fin une représentation négative de la vallée (c).

![Curves Adjustment Layer Figure 2](curves-psd-adjustment-layer-figure-2.png) Avant tout, n'oubliez pas de sélectionner le gestionnaire correspondant pour pouvoir l'utiliser, puis définissez les valeurs de point de la courbe en ordre décroissant en commençant par 255 et en descendant à 0 pour chaque point de courbe (255 au total) :

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

Le gestionnaire fournit également quelques [autres méthodes](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) pour gérer la courbe.

## Conclusion

Dans cet article, nous avons appris comment travailler avec les calques d'ajustement de courbes dans les documents Photoshop en utilisant Aspose.PSD pour Java de deux manières complètement différentes (gestionnaires continus et discrets).
