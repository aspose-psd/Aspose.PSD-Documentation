---
title: Travailler avec des masques dans Aspose.PSD pour Java
weight: 100
type: docs
description: Exemples de comment travailler avec les masques de recadrage, raster et vectoriels dans un fichier PSD
keywords: [masques, masque de calque, masque vectoriel, masque de recadrage, psd, api psd, java, exemple de code]
url: /fr/java/update-create-layer-mask/
---

## **Aperçu**

**Aperçu**

Il existe 3 types de masques dans les fichiers PSD:
1. Masques de recadrage
2. Masques raster
3. Masques vectoriels

Cet article couvre les 3 types.

**Masques de recadrage**

Les masques de recadrage sont une fonctionnalité robuste dans les logiciels de conception graphique et de retouche d'image, notamment en Java. Ils permettent un contrôle précis sur la visibilité d'une couche en fonction de la forme et du contenu d'une autre couche. Fondamentalement, un masque de recadrage restreint la visibilité d'une couche à la forme d'une autre couche en dessous.

Pour implémenter un masque de recadrage en Java, vous aurez d'abord besoin de deux couches : la couche de base et la couche que vous allez recadrer. La couche de base définit la forme ou la zone qui restera visible, tandis que la couche à recadrer contient le contenu qui doit se conformer à la forme de la couche de base.

Lorsqu'un masque de recadrage est appliqué en Java, le contenu de la couche recadrée est seulement visible à l'intérieur des limites de la couche de base. Tout contenu en dehors de ces limites sera caché ou recadré.

Les masques de recadrage se révèlent particulièrement précieux lors de l'application d'effets, tels que des textures ou des motifs, à des zones spécifiques d'une image ou d'une œuvre d'art. En utilisant un masque de recadrage, vous pouvez confiner l'effet à la zone souhaitée sans affecter le reste de l'image.

Veuillez vous référer à l'exemple à la fin de la page pour plus de clarté.

**Masques raster**

Dans les fichiers Java, les masques raster sont utilisés pour gérer la visibilité de zones spécifiques au sein d'une couche. Contrairement aux masques vectoriels, qui utilisent des formes mathématiques pour définir des zones masquées, les masques raster se basent sur des informations pixel par pixel pour déterminer les régions visibles ou cachées.

Un masque raster comprend une image en niveaux de gris appliquée à une couche. Les zones blanches du masque indiquent la visibilité, tandis que les zones noires représentent les parties cachées. Les nuances de gris entre les deux peuvent créer des régions de transparence partielle ou semi-visibles.

Veuillez vous référer à l'exemple à la fin de la page pour une meilleure compréhension.

**Masques vectoriels**

Dans les fichiers Java, les masques vectoriels sont des outils polyvalents utilisés pour délimiter la visibilité de zones spécifiques au sein d'une couche en fonction de formes mathématiques. Contrairement aux masques raster, qui dépendent de données pixel par pixel, les masques vectoriels utilisent des chemins et des courbes pour créer des zones masquées lisses et scalables.

Un masque vectoriel consiste essentiellement en un chemin appliqué à une couche. La forme de ce chemin détermine quelles parties de la couche sont visibles et lesquelles sont cachées. En manipulant les points de contrôle et les courbes du chemin, des zones masquées précises et complexes peuvent être créées.

Veuillez vous référer à la [page des Masques Vectoriels](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/layermaskdatashort/) pour des informations sur l'ajout de masques vectoriels en utilisant des ressources.

## **Exemple**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-update-create-layer-mask.java" >}}
