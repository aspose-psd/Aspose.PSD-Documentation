---
title: Couche d'ajustement Inverser
type: docs
weight: 30
url: /fr/java/layer-types/adjustment-layer/invert/
---

# Travailler avec la couche d'ajustement Inverser de Photoshop en Java

Dans cet article, nous allons montrer comment transformer une image dans un document Photoshop en une image négative de manière programmatique en Java. À cet effet, nous utiliserons la bibliothèque de manipulation de format de fichier PSD appelée Aspose.PSD pour Java.

L'API d'inversion des couleurs permet d'**ajouter un effet négatif à une image**. Vous avez peut-être déjà vu comment [inverser les couleurs d'une image en utilisant une couche d'ajustement Courbes](/psd/fr/java/layer-types/adjustment-layer/curves/). Cependant, aujourd'hui nous allons considérer une manière plus rapide et plus facile de réaliser cette tâche avec la couche d'ajustement Inverser.

## Aperçu de l'API

**L'API de la couche d'ajustement Inverser** se compose de la classe de la couche elle-même qui est [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). Cette classe ne possède pas de membres publics propres, car elle hérite de tous les membres publics de la classe parente ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). Ce fait simplifie son utilisation car tout ce que vous avez à faire est de l'ajouter à un fichier PSD et l'image devient négative.

## Inverser les couleurs de l'image

Ainsi, même si cela semble évident, permettez-nous de démontrer pour plus de clarté comment **appliquer la couche d'ajustement Inverser à l'image** d'un astronaute (a) pour créer l'effet négatif pour cette image (b).

![Exemple de couche d'ajustement Inverser Avant et Après](invert-adjustment-layer-figure-1.png)

Pour **inverser les couleurs de l'image**, ajoutez simplement une couche d'ajustement Inverser dans PSD :

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

C'est tout ! Il n'y a pas de propriétés spécifiques à configurer pour ce type de couche d'ajustement.

## Conclusion

Dans cet article, nous avons appris à propos de l'API de la couche d'ajustement Inverser d'Aspose.PSD pour Java. C'est un outil simple pour obtenir des images négatives car l'API de cette couche d'ajustement ne déclare aucun membre public.
