---
title: Calque d'ajustement du filtre photo
type: docs
weight: 30
url: /fr/java/layer-types/adjustment-layer/photo-filter/
---

# Travailler avec le calque d'ajustement du filtre photo de Photoshop en Java

Aujourd'hui, nous verrons comment appliquer un calque d'ajustement de filtre photo à un document Photoshop existant en utilisant Aspose.PSD pour Java qui est la bibliothèque permettant de manipuler le format de fichier PSD.

**L'API du calque d'ajustement du filtre photo** modifie l'équilibre des couleurs de l'image en utilisant un traitement par teinte. L'image résultante ressemblera à celle obtenue après utilisation d'un filtre d'appareil photo réel. Notez que l'API du calque d'ajustement du filtre photo de la bibliothèque diffère légèrement de celle de Photoshop car il n'y a pas encore de filtres prédéfinis. Cependant, elle est similaire à tous les autres égards. Cela signifie que vous pouvez définir une couleur pour la teinte et en modifier l'intensité (densité) ainsi que utiliser l'option Conserver la luminosité.

## Aperçu de l'API

L'API du calque d'ajustement du filtre photo est assez simple à utiliser. Il existe la classe principale [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer) qui sert de point d'entrée à ce calque d'ajustement et contient uniquement trois propriétés publiques, à savoir, couleur, densité et conserver la luminosité grâce auxquelles l'ajustement se produit.

## Ajuster l'équilibre des couleurs

Comme il n'y a pas grand-chose à dire, considérons **un exemple d'ajustement de l'équilibre des couleurs** en utilisant le filtre photo immédiatement. Nous allons ajouter un filtre de réchauffement (a) manuellement à l'image d'une sculpture de cerf (b) pour obtenir une image aux tons chauds (c) qui est plus agréable à regarder.

![Exemple de calque d'ajustement du filtre photo](photo-filter-adjustment-layer-figure-1.png)

Tout d'abord, notez que [la méthode de fabrique](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addPhotoFilterLayer-com.aspose.psd.Color-) diffère des autres méthodes pour [d'autres calques d'ajustement](https://docs.aspose.com/display/psdjava/PSD+Adjustment+Layers) car il n'y a pas de méthode par défaut (sans arguments). Par conséquent, pour ajouter un calque d'ajustement du filtre photo dans un document Photoshop chargé, un seul argument est requis, qui est la [couleur](https://reference.aspose.com/psd/java/com.aspose.psd/Color). Ainsi, pour recréer l'effet du filtre de réchauffement, passez simplement le orange comme argument à la méthode de fabrique, puis définissez la densité en utilisant les setters correspondants :

    PhotoFilterLayer photoFilterLayer = psdImage.addPhotoFilterLayer(Color._fromArgb_(236, 138, 0));
    photoFilterLayer.setDensity(25);

Il convient d'ajouter que la propriété Densité a une valeur par défaut qui est de 100 ainsi que vrai est la valeur par défaut pour la propriété Conserver la luminosité (c'est la raison pour laquelle nous n'activons pas explicitement cette option).

## Conclusion

Dans cet article, nous avons examiné l'utilisation de l'API du calque d'ajustement du filtre photo d'Aspose.PSD pour Java. Cet outil est simple à utiliser et permet d'ajouter une teinte à une image avec une densité variable. C'est un moyen rapide d'ajuster l'équilibre des couleurs de toute l'image.
