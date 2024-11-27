---
title: Travailler avec des masques dans Aspose.PSD pour C#
weight: 100
type: docs
description: Exemples de comment travailler avec les masques de découpe, de trame et vectoriels dans un fichier PSD
keywords: [masques, masque de calque, masque vectoriel, masque de découpe, psd, api psd, C#, csharp, exemple de code]
url: fr/net/update-create-layer-mask/
---

## Aperçu

Il y a trois types de masques dans les fichiers PSD :
1. Masques de découpe
2. Masques de trame
3. Masques vectoriels

Cet article couvre les trois types.

### Masques de découpe

Les masques de découpe sont une fonctionnalité puissante dans les logiciels de conception graphique et d'édition d'images qui vous permettent de contrôler la visibilité d'une couche en fonction de la forme et du contenu d'une autre couche. Essentiellement, un masque de découpe restreint la visibilité d'une couche à la forme définie par une autre couche en dessous.

Pour créer un masque de découpe, vous avez besoin de deux couches : la couche de base et la couche de découpe. La couche de base définit la forme ou la zone qui sera visible, tandis que la couche de découpe contient le contenu qui sera confiné à la forme de la couche de base.

Lorsque vous appliquez un masque de découpe, le contenu de la couche de découpe est uniquement visible à l'intérieur des limites de la couche de base. Tout contenu à l'extérieur des limites de la couche de base est caché ou découpé.

Les masques de découpe sont particulièrement utiles pour appliquer des effets, tels que des textures ou des motifs, à des zones spécifiques d'une image ou d'une œuvre d'art. En utilisant un masque de découpe, vous pouvez vous assurer que l'effet est confiné à la zone souhaitée sans affecter le reste de l'image.

### Masques de trame

Les masques de trame dans les fichiers PSD sont essentiels pour contrôler la visibilité de zones spécifiques au sein d'une couche. Contrairement aux masques vectoriels, qui utilisent des formes mathématiques pour définir des zones masquées, les masques de trame utilisent des informations basées sur les pixels pour déterminer quelles parties d'une couche sont visibles ou cachées.

Un masque de trame est constitué d'une image en niveaux de gris appliquée à une couche. Les zones blanches du masque représentent les parties visibles, tandis que les zones noires représentent les parties cachées. Les nuances de gris intermédiaires créent une transparence partielle ou des zones semi-visibles.

En utilisant des masques de trame, vous pouvez obtenir des effets de masquage complexes, permettant un contrôle précis de la visibilité de la couche en fonction des détails au niveau des pixels. Cette fonctionnalité est particulièrement utile pour les tâches nécessitant des ajustements détaillés et des mélanges au sein d'une image.

### Masques vectoriels

Les masques vectoriels dans les fichiers PSD sont un outil polyvalent utilisé pour définir la visibilité de zones spécifiques au sein d'une couche en fonction de formes mathématiques. Contrairement aux masques de trame, qui utilisent des informations basées sur les pixels, les masques vectoriels utilisent des chemins et des courbes pour créer des zones masquées lisses et évolutives.

Un masque vectoriel est essentiellement un chemin appliqué à une couche. La forme du chemin détermine quelles parties de la couche sont visibles et lesquelles sont cachées. En manipulant les points de contrôle et les courbes du chemin, vous pouvez créer des zones masquées précises et complexes.

Les masques vectoriels sont particulièrement utiles pour créer des masques propres et évolutifs qui peuvent être facilement ajustés sans perte de qualité. Cette fonctionnalité est idéale pour les tâches nécessitant une grande précision et une flexibilité dans la définition de zones visibles au sein d'une couche.

Pour plus d'informations sur l'ajout de masques vectoriels, veuillez visiter la page des [Masques Vectoriels](psd/fr/fr/layer-vector-mask/).

## Exemple
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "WorkingWithMasks-WorkingWithMasks.cs" >}}

Pour plus d'informations détaillées et d'exemples, veuillez consulter la [documentation Aspose.PSD pour C#](https://docs.aspose.com/psd/net/).
