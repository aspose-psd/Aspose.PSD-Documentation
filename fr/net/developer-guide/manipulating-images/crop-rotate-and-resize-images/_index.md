---
title: Rogner, Faire pivoter et Redimensionner les images
type: docs
weight: 40
url: /fr/net/crop-rotate-and-resize-images/
---

## **Rogner les images**
Le rognage d'image fait généralement référence à la suppression des parties extérieures d'une image pour améliorer le cadrage. Le rognage peut également être utilisé pour découper une partie de l'image afin de mettre davantage l'accent sur une zone particulière. L'API Aspose.PSD prend en charge deux approches différentes pour le rognage d'images : par décalages et par rectangle.
### **Rogner par décalages**
La classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) propose une version surchargée de la méthode Crop qui accepte 4 valeurs entières dénotant Gauche, Droite, Haut et Bas. Sur la base de ces quatre valeurs, la méthode Crop déplace les limites de l'image vers le centre de l'image en éliminant la partie extérieure. L'extrait de code ci-dessous montre comment rogner une image par décalages.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **Rogner par rectangle**
La classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) propose une autre version surchargée de la méthode Crop qui accepte une instance de la classe Rectangle. Vous pouvez découper n'importe quelle portion d'une image en fournissant les limites désirées à l'objet Rectangle. L'extrait de code ci-dessous montre comment rogner une image par Rectangle.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **Rotation et Retournement d'une image**
Aspose.PSD pour .NET est une bibliothèque facile à utiliser car elle propose des méthodes simples pour effectuer des opérations complexes. Par exemple, Aspose.PSD pour .NET a fourni la méthode RotateFlip pour sa classe de base Image si une application nécessite la rotation d'une image. Indépendamment du format de l'image, la bibliothèque peut effectuer une procédure spécifique de Rotation & Retournement.
### **Rotation d'une image**
La méthode Image.RotateFlip peut être utilisée pour faire pivoter l'image de 90/180/270 degrés et retourner l'image horizontalement ou verticalement. La méthode Image.RotateFlip accepte un paramètre de type RotateFlipType qui spécifie le type de rotation et de retournement à appliquer à l'image. Les étapes pour effectuer la rotation & le retournement sont aussi simples que ci-dessous,

1. Charger l'image en utilisant la méthode factory Load exposée par la classe Image.
1. Appeler la méthode Image.RotateFlip en spécifiant le RotateFlipType approprié.
1. Sauvegarder les résultats.

L'exemple de code suivant montre comment définir la propriété RotateFlip d'une Image et l'énumération RotateFlipType.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **Rotation d'une image selon un angle spécifique**
Aspose.PSD pour .NET API expose la méthode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate pour faciliter ses utilisateurs qui souhaitent faire pivoter une image selon un angle spécifique. Contrairement à la méthode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip, la méthode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate accepte trois paramètres :

1. Angle de rotation : Un paramètre de type float qui spécifie l'angle de rotation auquel l'image doit être tournée. Une valeur positive fait tourner l'image dans le sens des aiguilles d'une montre ; une valeur négative effectue une rotation dans le sens antihoraire.
1. Redimensionnement proportionnel : Un paramètre de type booléen spécifie si la taille de l'image doit être modifiée en fonction des projections du rectangle tourné. Si défini sur false, les dimensions de l'image ne seront pas modifiées et seuls les contenus internes de l'image seront tournés.
1. Couleur d'arrière-plan : Un paramètre de type Color qui spécifie la couleur à remplir à l'arrière-plan de l'image tournée.

L'extrait de code ci-dessous montre l'utilisation de la méthode [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **Redimensionner les images**
Cet article démontre l'utilisation d'Aspose.PSD pour .NET pour effectuer l'opération de redimensionnement sur une image. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD pour .NET a exposé la méthode Resize pour la classe Image qui peut être utilisée pour redimensionner des images existantes sur le pouce. Il existe deux surcharges de la méthode Resize pour répondre aux besoins de l'application.
### **Redimensionnement simple**
Les étapes pour effectuer le redimensionnement sont aussi simples que ci-dessous :

1. Charger l'image en utilisant la méthode factory Load exposée par la classe Image.
1. Appeler la méthode Image.Resize en spécifiant la nouvelle Hauteur & Largeur.
1. Sauvegarder les résultats.

L'exemple de code suivant montre comment redimensionner une image.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **Redimensionner avec l'énumération ResizeType**
Aspose.PSD API a exposé l'énumération ResizeType qui peut être utilisée avec Image.Resize pour obtenir des résultats souhaités. L'extrait de code fourni ci-dessous montre l'utilisation de l'énumération ResizeType, alors que les détails des membres de l'énumération ResizeType se trouvent en bas de cette page.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}
Si vous souhaitez obtenir un résultat de qualité après l'application du redimensionnement, il est recommandé d'utiliser toujours ResizeType.LanczosResample car cela produira des résultats hautement qualitatifs mais pourrait fonctionner plus lentement que ResizeType.NearestNeighbourResample. D'autre part, l'algorithme ResizeType.NearestNeighbourResample est spécifiquement utilisé pour le redimensionnement rapide en compromettant la qualité de l'image. Cette méthode peut être utile pour la génération de miniatures en temps réel ou des processus similaires où la performance est requise.
## **Redimensionner une image de manière proportionnelle**
Vous pouvez redimensionner des images en passant de nouvelles valeurs de hauteur & largeur en paramètres à la méthode Image.Resize mais dans ce cas, vous devez calculer le rapport d'aspect vous-même. Cela est nécessaire car quand la largeur ou la hauteur d'une image est modifiée, l'image est soit mise à l'échelle soit rétrécie pour remplir la nouvelle taille. Si les changements de la largeur et de la hauteur d'une image ne sont pas proportionnels, cela peut conduire à un résultat étiré et déformé. Cet article démontre l'utilisation d'Aspose.PSD pour .NET API pour redimensionner des images en passant soit une nouvelle hauteur soit une nouvelle largeur tout en permettant à l'API de calculer automatiquement la valeur proportionnelle de l'autre.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **Énumération ResizeType**
ResizeType détermine le type de redimensionnement à effectuer sur l'image en fonction du filtre sélectionné.

Membres de l'**Énumération [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)**

|**Nom du Membre**|**Valeur**|**Description**|
| :- | :- | :- |
|LeftTopToLeftTop|0|Le point en haut à gauche de la nouvelle image coïncidera avec le point en haut à gauche de l'image d'origine. Un rognage se produira si nécessaire.|
|RightTopToRightTop|1|Le point en haut à droite de la nouvelle image coïncidera avec le point en haut à droite de l'image d'origine. Un rognage se produira si nécessaire.|
|RightBottomToRightBottom|2|Le point en bas à droite de la nouvelle image coïncidera avec le point en bas à droite de l'image d'origine. Un rognage se produira si nécessaire.|
|LeftBottomToLeftBottom|3|Le point en bas à gauche de la nouvelle image coïncidera avec le point en bas à gauche de l'image d'origine. Un rognage se produira si nécessaire.|
|CenterToCenter|4|Le centre de la nouvelle image coïncidera avec le centre de l'image d'origine. Un rognage se produira si nécessaire.|
|LanczosResample|5|Rééchantillonner en utilisant l'algorithme de Lanczos en utilisant un masque 7x7.|
|NearestNeighbourResample|6|Réeschantillonner en utilisant un algorithme du voisin le plus proche.|
