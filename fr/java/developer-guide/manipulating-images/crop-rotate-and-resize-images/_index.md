---
title: Rogner, Faire Pivoter et Redimensionner les Images
type: docs
weight: 40
url: /fr/java/crop-rotate-and-resize-images/
---

## **Rogner les Images**
Le rognage d'image se réfère généralement à la suppression des parties extérieures d'une image pour améliorer le cadrage. Le rognage peut également être utilisé pour découper une partie de l'image afin de mettre en valeur une zone particulière. L'API Aspose.PSD prend en charge deux approches différentes pour le rognage des images : par décalages et par rectangle.
### **Rognage par Décalages**
La classe RasterImage fournit une version surchargée de la méthode Crop qui accepte 4 valeurs entières indiquant Gauche, Droite, Haut et Bas. À partir de ces quatre valeurs, la méthode Crop déplace les limites de l'image vers le centre de l'image tout en supprimant la partie extérieure. Le code ci-dessous montre comment rogner une image par décalages.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.java" >}}
 
### **Rognage par Rectangle**
La classe RasterImage fournit une autre version surchargée de la méthode Crop qui accepte une instance de la classe Rectangle. Vous pouvez découper n'importe quelle partie d'une image en fournissant les limites souhaitées à l'objet Rectangle. Le code ci-dessous montre comment rogner une image par Rectangle.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.java" >}}

## **Rotation et Retournement d'Image**
Aspose.PSD pour Java est une bibliothèque facile à utiliser car elle propose des méthodes simples pour effectuer des opérations complexes. Par exemple, Aspose.PSD pour Java a fourni la méthode RotateFlip pour sa classe de base Image si une application nécessite de faire pivoter une image. Indépendamment du format de l'image, la bibliothèque peut effectuer une rotation et un retournement spécifiques sur celle-ci.
### **Rotation d'une Image**
La méthode Image.RotateFlip peut être utilisée pour faire pivoter l'image de 90/180/270 degrés et la retourner horizontalement ou verticalement. La méthode Image.RotateFlip accepte un paramètre de type RotateFlipType qui spécifie le type de rotation et de retournement à appliquer à l'image. Les étapes pour effectuer une rotation et un retournement sont aussi simples que ci-dessous,

1. Charger l'image en utilisant la méthode d'usine Load exposée par la classe Image.
1. Appeler la méthode Image.RotateFlip en spécifiant le RotateFlipType approprié.
1. Enregistrer les résultats.

L'exemple de code suivant montre comment définir la propriété RotateFlip d'une Image et l'énumération RotateFlipType.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.java" >}}

## **Rotation d'une Image sur un Angle Spécifique**
Aspose.PSD pour Java expose la méthode RasterImage.Rotate pour faciliter ses utilisateurs souhaitant faire pivoter une image sur un angle spécifique. Contrairement à la méthode RasterImage.RotateFlip, la méthode RasterImage.Rotate accepte trois paramètres :

1. Angle de rotation : Un paramètre de type float qui spécifie l'angle de rotation auquel l'image doit être pivotée. Une valeur positive fait pivoter l'image dans le sens des aiguilles d'une montre; une valeur négative effectue une rotation dans le sens anti-horaire.
1. Redimensionner de manière proportionnelle : Un paramètre de type booléen qui spécifie si la taille de l'image doit être modifiée en fonction des projections du rectangle pivoté. Si elle est définie sur faux, les dimensions de l'image ne seront pas modifiées et seuls les contenus internes de l'image sont pivotés.
1. Couleur de fond : Un paramètre de type Color spécifie la couleur à remplir à l'arrière-plan de l'image pivotée.

Le code ci-dessous montre comment utiliser la méthode RasterImage.Rotate.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.java" >}}

## **Redimensionner les Images**
Cet article montre comment utiliser Aspose.PSD pour Java pour effectuer une opération de redimensionnement d'image. Les API Aspose.PSD ont exposé des méthodes efficaces et simples à utiliser pour atteindre cet objectif. Aspose.PSD pour Java a exposé la méthode Resize pour la classe Image qui peut être utilisée pour redimensionner des images existantes en cours d'exécution. Il existe deux surcharges de la méthode Resize pour répondre aux besoins de l'application.
### **Redimensionnement Simple**
Les étapes pour effectuer le redimensionnement sont aussi simples que ci-dessous :

1. Charger l'image en utilisant la méthode d'usine Load exposée par la classe Image.
1. Appeler la méthode Image.Resize en spécifiant la nouvelle Hauteur et Largeur.
1. Enregistrer les résultats.

L'exemple de code suivant montre comment redimensionner une image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.java" >}}
### **Redimensionnement avec l'Énumération ResizeType**
L'API Aspose.PSD a exposé une énumération ResizeType qui peut être utilisée avec Image.Resize pour obtenir les résultats souhaités. Le code fourni ci-dessous montre comment utiliser l'énumération ResizeType, tandis que les détails des membres de l'énumération ResizeType peuvent être trouvés en bas de cette page.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.java" >}}


Si vous voulez obtenir un résultat de qualité après l'application du redimensionnement, il est suggéré d'utiliser toujours ResizeType.LanczosResample car il produira des résultats hautement qualitatifs mais peut fonctionner plus lentement que ResizeType.NearestNeighbourResample. D'autre part, l'algorithme ResizeType.NearestNeighbourResample est spécifiquement utilisé pour un redimensionnement rapide tout en compromise sur la qualité de l'image. Cette méthode peut être utile pour la génération de vignettes en temps réel ou des processus similaires où la performance est requise.
## **Redimensionner une Image Proportionnellement**
Vous pouvez redimensionner des images en passant de nouvelles valeurs de hauteur et de largeur en tant que paramètres à la méthode Image.Resize mais dans ce cas, vous devez calculer le rapport d'aspect vous-même. Cela est parce que lorsque la largeur ou la hauteur d'une image est modifiée, l'image est soit mise à l'échelle soit rétrécie pour remplir la nouvelle taille. Si les modifications de la largeur et de la hauteur de l'image ne sont pas proportionnelles, cela peut entraîner un résultat étiré et déformé. Cet article montre comment utiliser l'API Aspose.PSD pour Java pour redimensionner les images en passant soit une nouvelle hauteur soit une nouvelle largeur tout en permettant à l'API de calculer automatiquement la autre valeur proportionnelle.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.java" >}}
### **Énumération ResizeType**
ResizeType détermine le type de redimensionnement à effectuer sur l'image en fonction du filtre sélectionné.

Membres de l'Énumération ResizeType

|**Nom du Membre**|**Valeur**|**Description**|
| :- | :- | :- |
|HautGaucheàHautGauche|0|Le point haut gauche de la nouvelle image coïncidera avec le point haut gauche de l'image originale. Recadrage si nécessaire.|
|HautDroiteàHautDroite|1|Le point haut droit de la nouvelle image coïncidera avec le point haut droit de l'image originale. Recadrage si nécessaire.|
|BasDroiteàBasDroite|2|Le point bas droit de la nouvelle image coïncidera avec le point bas droit de l'image originale. Recadrage si nécessaire.|
|BasGaucheàBasGauche|3|Le point bas gauche de la nouvelle image coïncidera avec le point bas gauche de l'image originale. Recadrage si nécessaire.|
|CentreàCentre|4|Le centre de la nouvelle image coïncidera avec le centre de l'image originale. Recadrage si nécessaire.|
|LanczosResample|5|Reéchantillonnage en utilisant l'algorithme de Lanczos en utilisant un masque 7x7.|
|NearestNeighbourResample|6|Reéchantillonnage en utilisant l'algorithme du plus proche voisin.|

