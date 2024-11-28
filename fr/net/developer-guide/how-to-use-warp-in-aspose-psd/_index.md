---
title: Comment utiliser Warp dans Aspose.PSD
type: docs
weight: 40
url: /fr/net/comment-utiliser-warp-dans-aspose-psd/
---

## **Partie 1 – Rendu d'un fichier PSD avec l'effet Warp**

Photoshop enregistre l'image rendue après l'application de l'effet Warp. Notre bibliothèque peut reproduire ou re-rendre l'image avec l'effet Warp. Pour activer cette fonctionnalité, définissez simplement le drapeau AllowWarpRepaint dans les paramètres lors de l'ouverture du fichier PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-1.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 1](warp1.png)

En plus de rendre l'effet Warp pour les SmartLayers, notre bibliothèque prend également en charge Warp pour les TextLayers. Le code d'implémentation reste identique, la seule différence étant dans le nom de fichier.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-2.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 2](warp2.png)

**! Note :** Actuellement, notre bibliothèque prend en charge le rendu à la fois du Warp personnalisé (où les utilisateurs manipulent les points du maillage) et de tous les types de Warps standards.
* - Actuellement, notre bibliothèque prend en charge le Warp personnalisé avec le maillage standard, et nous travaillons activement à étendre notre prise en charge pour inclure tous les types de maillages dans un proche avenir.


## **Partie 2 – Modification de l'effet Warp**

Notre bibliothèque vous permet non seulement de rendre, mais aussi de modifier (ajouter) l'effet Warp.
Ces modifications sont facilitées par les fonctionnalités de la classe **WarpParams**.

| **Fonctionnalité** | **Description**                                                         |
|:-------------------|:-------------------------------------------------------------------------|
| Limites            | Renvoie les limites de l'image déformée.                                 |
| PointsMaillage     | Un tableau de points, chaque point représentant un sommet du maillage de déformation. |
| Valeur             | La valeur de l'effet Warp pour les effets de déformation non personnalisés. |
| RotationWarp       | Une énumération définissant la direction des effets de déformation non personnalisés. |
| StylesWarp         | Une énumération définissant le type d'effet de déformation. |

L'exemple de code ci-dessous montre comment déterminer le type d'effet Warp pour une Smart Layer et ajuster le type et l'intensité de la distorsion pour l'effet.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-3.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 3](warp3.png)

## **Partie 3 – Ajout de l'effet Warp**

L'exemple de code ci-dessous montre comment ajouter un effet Warp standard à une Smart Layer.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-4.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 4](warp4.png)

L'exemple de code ci-dessous montre comment ajouter un effet Warp personnalisé à une Smart Layer.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-5.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 5](warp5.png)

L'exemple de code ci-dessous montre comment ajouter un effet Warp à un Text Layer.
**! Note :** Selon les normes de Photoshop, l'effet Warp pour les Text Layers est généralement limité au type standard. Cependant, notre bibliothèque prend en charge l'utilisation de deux types d'effets Warp. Veuillez noter que de tels fichiers peuvent ne pas être entièrement compatibles avec Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendu-5.cs" >}}

Résultat :
![Résultat Warp Aspose.PSD pour .NET 6](warp6.png)

Nous améliorons et élargissons continuellement les capacités de notre effet Warp, en mettant l'accent sur l'amélioration de sa vitesse, de sa qualité, et de sa fonctionnalité prise en charge. Restez informés avec nos sorties mensuelles pour les derniers développements.
Votre équipe Aspose.PSD
