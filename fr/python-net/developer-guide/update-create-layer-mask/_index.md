---
title: Travailler avec les masques dans Aspose.PSD pour Python
weight: 100
type: docs
description: Exemples de comment travailler avec les masques de détourage, de trame et de vecteur dans un fichier PSD
keywords: [masques, masque de calque, masque de vecteur, masque de détourage, psd, api psd, python, exemple de code]
url: fr/python-net/update-create-layer-mask/
---

## **Aperçu**

**Aperçu**
	
	Il y a 3 types de masques dans les fichiers PSD :
	1. Masques de détourage
	2. Masques de trame
	3. Masques de vecteur
	
	Cet article couvre les 3 types.

**Masques de détourage**

Les masques de détourage sont une fonctionnalité puissante dans les logiciels de conception graphique et de retouche d'image. Ils vous permettent de contrôler la visibilité d'une couche en fonction de la forme et du contenu d'une autre couche. En d'autres termes, un masque de détourage restreint la visibilité d'une couche à la forme d'une autre couche en dessous.

Pour créer un masque de détourage, vous avez d'abord besoin de deux calques : le calque de base et le calque que vous souhaitez détourer. Le calque de base définit la forme ou la zone qui sera visible, tandis que le calque à détourer contient le contenu qui sera détouré à la forme du calque de base.

Lorsque vous appliquez un masque de détourage, le contenu du calque détouré est uniquement visible à l'intérieur des limites du calque de base. Tout contenu à l'extérieur des limites du calque de base sera caché ou détouré.

Les masques de détourage sont particulièrement utiles lorsque vous souhaitez appliquer un effet, tel qu'une texture ou un motif, à une zone spécifique d'une image ou d'une œuvre d'art. En utilisant un masque de détourage, vous pouvez limiter l'effet à la zone souhaitée sans affecter le reste de l'image.

Veuillez consulter l'exemple à la fin de la page

**Masques de trame**

Les masques de trame dans les fichiers PSD sont utilisés pour contrôler la visibilité de zones spécifiques à l'intérieur d'une couche. Contrairement aux masques de vecteur, qui utilisent des formes mathématiques pour définir les zones masquées, les masques de trame utilisent des informations basées sur les pixels pour déterminer quelles parties d'une couche sont visibles ou cachées.

Un masque de trame se compose d'une image en niveaux de gris qui est appliquée à une couche. Les zones blanches du masque représentent les parties visibles, tandis que les zones noires représentent les parties cachées. Les nuances de gris entre les deux peuvent être utilisées pour créer une transparence partielle ou des zones semi-visibles.

Veuillez consulter l'exemple à la fin de la page

**Masques de vecteur**

Les masques de vecteur dans les fichiers PSD sont un outil polyvalent utilisé pour définir la visibilité de zones spécifiques à l'intérieur d'une couche en fonction de formes mathématiques. Contrairement aux masques de trame, qui utilisent des informations basées sur les pixels, les masques de vecteur utilisent des chemins et des courbes pour créer des zones masquées lisses et évolutives.

Un masque de vecteur est essentiellement un chemin appliqué à une couche. La forme du chemin détermine quelles parties de la couche sont visibles et quelles parties sont cachées. En manipulant les points de contrôle et les courbes du chemin, vous pouvez créer des zones masquées précises et complexes.

Veuillez consulter la [page des Masques de vecteur](fr/psd/net/layer-vector-mask/) pour obtenir des informations sur la façon dont les masques de vecteur peuvent être ajoutés en utilisant des ressources.


## **Exemple**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-psd-update-create-layer-mask.py" >}}
