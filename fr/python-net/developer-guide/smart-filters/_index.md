---
title: Manipulation intelligente des filtres dans Aspose.PSD pour Python
weight: 100
type: docs
description: Exemples de l'utilisation des filtres intelligents dans les fichiers PSD
keywords: [filtre intelligent, ajouter du bruit, flou gaussien, renforcer, filtre, filtre psd, api psd, python, exemple de code]
url: fr/python-net/filtres-intelligents/
---

## **Vue d'ensemble**

Il existe 3 façons d'appliquer des filtres intelligents dans Aspose.PSD pour Python.

## **Application directe du filtre**
Dans cet exemple de code, nous pouvons voir comment appliquer directement des filtres intelligents dans Aspose.PSD pour Python.

Tout d'abord, le code spécifie le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

Ensuite, le code charge l'image PSD en utilisant la méthode Image.load() et la caste en un objet PsdImage.

L'image originale est ensuite enregistrée en utilisant la méthode save(), avec le nom de fichier de sortie spécifié.

Un objet SharpenSmartFilter est créé, qui représente le filtre intelligent à appliquer.

Ensuite, le code récupère la couche régulière de l'image PSD en utilisant im.layers[1].

Une boucle est ensuite utilisée pour appliquer le filtre de renforcement à la couche régulière trois fois.

Enfin, l'image mise à jour est enregistrée en utilisant la méthode save() et le nom du fichier de sortie spécifié.

Ce code démontre comment appliquer directement des filtres intelligents dans Aspose.PSD pour Python. En utilisant les objets de filtre appropriés et en les appliquant aux couches désirées, vous pouvez obtenir les effets souhaités sur vos images.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-direct-apply.py" >}}

## **Manipulation des filtres intelligents dans les objets intelligents**

Tout d'abord, le code spécifie le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

L'image PSD est chargée en utilisant la méthode Image.load(), puis caste en un objet PsdImage.

L'image originale est enregistrée en utilisant la méthode save(), avec le nom de fichier de sortie spécifié.

Ensuite, le code caste la deuxième couche de l'image PSD en un objet SmartObjectLayer, représentant la couche d'objet intelligent.

Le code passe ensuite à l'édition des filtres intelligents. Dans cet exemple, il montre comment travailler avec deux types de filtres intelligents : GaussianBlurSmartFilter et AddNoiseSmartFilter.

Pour GaussianBlurSmartFilter, le code met à jour les valeurs du filtre, y compris le rayon, le mode de fusion, l'opacité, et s'il est activé ou non.

Pour AddNoiseSmartFilter, le code définit la distribution de bruit sur NoiseDistribution.UNIFORM.

Ensuite, le code ajoute deux nouveaux éléments de filtre à la couche d'objet intelligent : un autre GaussianBlurSmartFilter et un AddNoiseSmartFilter.

Après avoir ajouté les nouveaux filtres, le code applique les modifications en utilisant la méthode update_resource_values().

Enfin, le code montre comment appliquer directement les filtres à la couche et au masque de la couche en utilisant respectivement les méthodes apply() et apply_to_mask().

L'image mise à jour est ensuite enregistrée en utilisant la méthode save() et le nom de fichier de sortie spécifié.

En suivant cet exemple de code, vous pouvez apprendre comment travailler avec des filtres intelligents dans Aspose.PSD pour Python. La bibliothèque fournit une large gamme de filtres intelligents, chacun avec son propre ensemble de propriétés et de méthodes qui peuvent être personnalisées pour obtenir les effets désirés sur vos images.

{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-smart-filter-features.py" >}}

## **Application des filtres intelligents au masque de couche**

Application des filtres intelligents aux masques : une puissante technique de retouche d'image

Les filtres intelligents sont une fonctionnalité populaire dans les logiciels de retouche d'image qui permettent aux utilisateurs d'appliquer divers filtres et effets à leurs images. Une technique intéressante qui peut être réalisée en utilisant des filtres intelligents est de les appliquer aux masques. Dans cet article, nous allons explorer comment appliquer des filtres intelligents aux masques et discuter de leur utilisation dans le monde de la retouche d'image.

Qu'est-ce qu'un masque ? Avant d'appliquer des filtres intelligents aux masques, comprenons d'abord ce qu'est un masque. En retouche d'image, un masque est une image en niveaux de gris qui détermine la transparence de certaines zones d'une image. Un masque peut être utilisé pour appliquer sélectivement des filtres, des ajustements ou des effets à des parties spécifiques d'une image, tout en laissant les autres zones inchangées.

Application des filtres intelligents aux masques : Lors de l'application des filtres intelligents aux masques, les filtres ne sont appliqués qu'aux zones spécifiées par le masque. Cela permet un contrôle précis sur quelles parties de l'image sont affectées par le filtre. En manipulant le masque, vous pouvez déterminer l'intensité et l'étendue de l'effet du filtre.

Veuillez consulter l'exemple précédent et la méthode : [Référence de l'API Appliquer un filtre intelligent au masque](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.smartfilters/smartfilter/#apply_to_mask_layer_with_mask_2)
