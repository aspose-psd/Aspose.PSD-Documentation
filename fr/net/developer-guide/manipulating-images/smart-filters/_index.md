---
title: Manipulation du Filtre Intelligent dans Aspose.PSD pour С#
weight: 100
type: docs
description: Exemples d'utilisation des Filtres Intelligents dans le Fichier PSD
keywords: [filtre intelligent, ajouter du bruit, flou gaussien, aiguiser, filtre, filtre psd, api psd, C#, csharp, exemple de code]
url: fr/net/smart-filters/
---

## Aperçu

Il existe trois façons d'appliquer des filtres intelligents dans Aspose.PSD pour C#.

### Application Directe du Filtre

Cet exemple montre comment appliquer directement des filtres intelligents dans Aspose.PSD pour C#.

Tout d'abord, spécifiez le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

Ensuite, chargez l'image PSD en utilisant la méthode `Image.Load` et convertissez-la en objet `PsdImage`.

Enregistrez l'image originale en utilisant la méthode `Save` avec le nom de fichier de sortie spécifié.

Créez un objet `SharpenSmartFilter`, représentant le filtre intelligent à appliquer.

Récupérez la couche régulière de l'image PSD en utilisant `psdImage.Layers[1]`.

Appliquez le `sharpenFilter` à la couche régulière trois fois dans une boucle.

Enfin, enregistrez l'image mise à jour en utilisant la méthode `Save` avec le nom de fichier de sortie spécifié.

Ce code montre comment appliquer directement des filtres intelligents dans Aspose.PSD pour C#. En utilisant les objets de filtre appropriés et en les appliquant aux calques désirés, vous pouvez atteindre les effets souhaités sur vos images.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "DirectlyApplySmartFilter-DirectlyApplySmartFilter.cs" >}}

### Manipulation des Filtres Intelligents dans les Objets Intelligents

Cet exemple montre comment manipuler des filtres intelligents dans des objets intelligents.

Tout d'abord, spécifiez le fichier PSD source, le fichier de sortie pour l'image originale et le fichier de sortie pour l'image mise à jour.

Chargez l'image PSD en utilisant la méthode `Image.Load` et convertissez-la en objet `PsdImage`.

Enregistrez l'image originale en utilisant la méthode `Save` avec le nom de fichier de sortie spécifié.

Convertissez la deuxième couche de l'image PSD en un objet `SmartObjectLayer`.

Modifiez les filtres intelligents. Cet exemple montre comment travailler avec `GaussianBlurSmartFilter` et `AddNoiseSmartFilter`.

Pour `GaussianBlurSmartFilter`, mettez à jour les valeurs du filtre, y compris le rayon, le mode de fusion, l'opacité et l'état activé.

Pour `AddNoiseSmartFilter`, définissez la distribution du bruit sur `NoiseDistribution.UNIFORM`.

Ajoutez de nouveaux éléments de filtre à la couche d'objet intelligent : un autre `GaussianBlurSmartFilter` et `AddNoiseSmartFilter`.

Appliquez les modifications en utilisant la méthode `UpdateResourceValues`.

Appliquez les filtres directement sur la couche et sur le masque de la couche en utilisant respectivement les méthodes `Apply` et `ApplyToMask`.

Enregistrez l'image mise à jour en utilisant la méthode `Save` avec le nom de fichier de sortie spécifié.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "ManipulatingSmartFiltersInSmartObjects-ManipulatingSmartFiltersInSmartObjects.cs" >}}

### Application de Filtres Intelligents au Masque de Calque

Les filtres intelligents sont un outil puissant d'édition d'image qui permet aux utilisateurs d'appliquer divers filtres et effets. Une technique intéressante est de les appliquer aux masques, ce qui permet de contrôler précisément les zones affectées par le filtre.

Un masque est une image en niveaux de gris déterminant la transparence de certaines zones de l'image, appliquant sélectivement des filtres, des ajustements ou des effets.

Lors de l'application de filtres intelligents aux masques, les filtres ne s'appliquent qu'aux zones spécifiées par le masque. Ce contrôle précis permet de manipuler l'intensité et l'étendue du filtre.

Pour des informations plus détaillées et des exemples, consultez la [documentation Aspose.PSD pour C#](https://docs.aspose.com/psd/net/).

