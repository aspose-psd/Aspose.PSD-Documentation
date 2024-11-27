---
title: Manipulation intelligente des filtres dans Aspose.PSD pour Java
weight: 100
type: docs
description: Exemples d'utilisation des filtres intelligents dans les fichiers PSD
keywords: [filtre intelligent, ajouter du bruit, flou gaussien, netteté, filtre, filtre psd, api psd, java, exemple de code]
url: fr/java/filtres-intelligents/
---

## **Aperçu**

Il existe 3 méthodes pour appliquer des filtres intelligents dans Aspose.PSD pour Java.

## ** Application directe des filtres **
Cet exemple de code montre comment appliquer directement des filtres intelligents dans Aspose.PSD pour Java.

Initialement, le code définit le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

Ensuite, le code charge l'image PSD en utilisant la méthode Image.load() et la convertit en un objet PsdImage.

L'image originale est sauvegardée en utilisant la méthode save(), en spécifiant le nom du fichier de sortie.

Un objet SharpenSmartFilter est instancié pour représenter le filtre intelligent souhaité.

Ensuite, le code extrait la couche régulière de l'image PSD en utilisant psdImage.getLayers()[1].

Une boucle est utilisée pour appliquer le filtre d'affûtage à la couche régulière trois fois.

Enfin, l'image mise à jour est sauvegardée en utilisant la méthode save() avec le nom du fichier de sortie fourni.

Ce code illustre l'application directe des filtres intelligents dans Aspose.PSD pour Java. En utilisant des objets de filtre appropriés et en les appliquant aux calques désirés, des effets souhaités peuvent être obtenus sur les images.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-direct-apply.java" >}}

## ** Manipulation des filtres intelligents dans les objets intelligents **

Cet extrait de code explique comment manipuler les filtres intelligents au sein des objets intelligents dans Aspose.PSD pour Java.

Initialement, le code définit le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

L'image PSD est chargée en utilisant la méthode Image.load() puis convertie en un objet PsdImage.

L'image originale est sauvegardée en utilisant la méthode save(), en spécifiant le nom du fichier de sortie.

Ensuite, le code convertit la deuxième couche de l'image PSD en un objet SmartObjectLayer, représentant la couche d'objet intelligent.

Par la suite, le code montre comment éditer les filtres intelligents, présentant deux types : GaussianBlurSmartFilter et AddNoiseSmartFilter.

Pour GaussianBlurSmartFilter, le code met à jour les valeurs du filtre telles que le rayon, le mode de fusion, l'opacité et l'état d'activation.

Pour AddNoiseSmartFilter, le code définit la distribution de bruit sur NoiseDistribution.Uniform.

Ensuite, le code ajoute deux nouveaux éléments de filtre à la couche d'objet intelligent : un autre GaussianBlurSmartFilter et un AddNoiseSmartFilter.

Après l'ajout de nouveaux filtres, le code applique les modifications en utilisant la méthode updateResourceValues().

Enfin, le code montre comment appliquer directement des filtres à la couche et à son masque en utilisant les méthodes apply() et applyToMask() respectivement.

L'image mise à jour est ensuite sauvegardée en utilisant la méthode save() avec le nom du fichier de sortie fourni.

En suivant cet exemple de code, vous pouvez comprendre comment manipuler les filtres intelligents au sein des objets intelligents dans Aspose.PSD pour Java. La bibliothèque offre une large gamme de filtres intelligents, chacun avec son propre ensemble de propriétés et de méthodes qui peuvent être personnalisées pour obtenir les effets souhaités sur les images.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-smart-filter-features.java" >}}

## ** Application des filtres intelligents au masque de calque **

Application des filtres intelligents aux masques : une technique de retouche d'image puissante

Les filtres intelligents, fréquents dans les logiciels de retouche d'image, permettent aux utilisateurs d'appliquer divers filtres et effets à leurs images. Une technique intrigante permise par les filtres intelligents est leur application aux masques. Cet article explore l'application des filtres intelligents aux masques et discute de leur utilité dans le domaine de la retouche d'image.

Comprendre les masques : Avant de plonger dans l'application des filtres intelligents aux masques, il est crucial de comprendre le concept d'un masque. En retouche d'image, un masque est une image en niveaux de gris dictant la transparence de zones spécifiques à l'intérieur d'une image. Les masques permettent une application sélective de filtres, d'ajustements ou d'effets à des parties particulières d'une image tout en laissant les autres intactes.

Application des filtres intelligents aux masques : Lorsque des filtres intelligents sont appliqués aux masques, ils n'affectent que les zones spécifiées par le masque, offrant un contrôle précis sur l'impact du filtre. En manipulant le masque, les utilisateurs peuvent moduler l'intensité et l'étendue de l'effet du filtre.

Veuillez vous référer à l'exemple précédent et à la méthode : [Référence de l'API - Application du filtre intelligent au masque](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
