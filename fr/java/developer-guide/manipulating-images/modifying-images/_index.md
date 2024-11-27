---
title: Modification d'Images
type: docs
weight: 50
url: /fr/java/modification-images/
---

## **Dithering pour les Images Raster**
La dithering est une technique permettant de créer l'illusion de nouvelles couleurs et nuances en variant le motif de points qui composent réellement une image. C'est le moyen le plus courant de réduire la gamme de couleurs des images à 256 (ou moins) couleurs. Aspose.PSD fournit le support de dithering pour la classe RasterImage en introduisant la méthode Dither qui accepte deux paramètres. Le premier est de type DitheringMethod à appliquer avec deux options possibles : FloydSteinbergDithering et ThresholdDithering. Le deuxième paramètre de la méthode Dither est le BitCount en entier. BitCount définit la taille d'échantillonnage pour le résultat de dithering. La valeur par défaut est 1 qui représente le noir et blanc, tandis que les valeurs autorisées sont 1, 4, 8 générant des palettes avec respectivement 2, 4 et 256 couleurs.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.java" >}}
## **Ajustement de la Luminosité, du Contraste et du Gamma**
Les ajustements de couleur dans les images numériques sont l'une des fonctionnalités principales que la plupart des bibliothèques de traitement d'images offrent. Les ajustements de couleur peuvent être catégorisés comme suit.

1. La luminosité se réfère à la clarté ou l'obscurité de la couleur. Augmenter la luminosité d'une image éclaire toutes les couleurs tandis que diminuer la luminosité assombrit toutes les couleurs.
1. Le contraste concerne le rendu des objets ou détails dans une image plus évidents. Augmenter le contraste d'une image augmente la différence entre les zones claires et sombres de sorte que les zones claires deviennent plus claires et les zones sombres plus sombres. Diminuer le contraste fera que les zones plus claires et plus sombres restent approximativement les mêmes mais l'image globale devient plus homogène.
1. Le gamma optimise le contraste et la luminosité de l'éclairage indirect qui illumine un objet dans l'image.
### **Ajuster la Luminosité**
Aspose.PSD pour Java API fournit la méthode AdjustBrightness pour la classe RasterImage qui peut être utilisée pour ajuster la luminosité de l'image en passant une valeur entière en tant que paramètre. La valeur de paramètre la plus élevée désigne une image plus lumineuse. Voici l'image d'origine et l'image résultante pour comparaison.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.java" >}}
### **Ajuster le Contraste**
La méthode AdjustContrast exposée par la classe RasterImage peut être utilisée pour ajuster le contraste d'une image en passant une valeur flottante en tant que paramètre.

La valeur de paramètre la plus élevée désigne un contraste plus élevé dans l'image donnée. Voici l'image d'origine et l'image résultante pour comparaison.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.java" >}}
### **Ajuster le Gamma**
La méthode AdjustGamma exposée par la classe RasterImage a deux versions. Une des surcharges accepte une valeur flottante et effectue la correction Gamma pour les coefficients des canaux rouge, bleu et vert. Tandis que l'autre surcharge accepte trois paramètres flottants représentant chaque coefficient de couleur séparément. L'exemple de code suivant montre comment ajuster le Gamma sur une image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.java" >}}
## **Flouter une Image**
Cet article démontre l'utilisation d'Aspose.PSD pour Java pour réaliser un effet de flou sur une image. Les APIs d'Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD pour Java a exposé la classe GaussianBlurFilterOptions pour créer un effet de flou à la volée. La classe GaussianBlurFilterOptions nécessite des valeurs de rayon et sigma pour créer un effet de flou sur une image. Les étapes pour réaliser le flou sont aussi simples que ci-dessous :

1. Charger une image en utilisant la méthode factory Load exposée par la classe Image.
1. Convertir l'image en RasterImage.
1. Créer une instance de la classe GaussianBlurFilterOptions avec le constructeur par défaut ou fournir les valeurs de rayon et sigma dans le constructeur.
1. Appeler la méthode RasterImage.Filter en spécifiant le rectangle comme limites de l'image et l'instance de la classe GaussianBlurFilterOptions.
1. Sauvegarder les résultats.

L'exemple de code suivant montre comment créer un effet de flou sur une image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-BlurAnImage-BlurAnImage.java" >}}
## **Vérifier la Transparence de l'Image**
Cet article démontre l'utilisation d'Aspose.PSD pour Java pour vérifier la transparence de l'image. Les étapes pour vérifier la transparence de l'image sont aussi simples que ci-dessous :

1. Charger une image en utilisant la méthode factory Load exposée par la classe Image.
1. Vérifier l'opacité de l'image. Si l'opacité est zéro, l'image est transparente.
1. L'exemple de code suivant montre comment vérifier si l'image est transparente ou non.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.java" >}}
## **Implémenter un Compresseur GIF avec Perte**
En utilisant Aspose.PSD pour Java, les développeurs peuvent définir la différence de pixels. La compression du GIF est basée sur un "dictionnaire" de chaînes de pixels observées. L'encodeur normal recherche dans le dictionnaire la chaîne de pixels la plus longue qui correspond exactement aux pixels de l'image. L'encodeur avec perte choisit la chaîne de pixels la plus longue qui est "assez similaire" aux pixels de l'image. Ci-dessous se trouve une démonstration du code de ladite fonctionnalité.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.java" >}}
## **Implémenter le Rééchantillonnage Bicubique**
Le rééchantillonnage signifie que vous modifiez les dimensions de pixel d'une image. Lorsque vous rééchantillonnez, vous éliminez des pixels et supprimez donc des informations et des détails de votre image. Lorsque vous agrandissez, vous ajoutez des pixels. Photoshop ajoute ces pixels en utilisant l'interpolation. Cet article démontre comment vous pouvez effectuer le rééchantillonnage bicubique en utilisant Aspose.PSD pour Java.

Ci-dessous se trouve une démonstration du code de ladite fonctionnalité.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.java" >}}
## **Inverser la Couche d'Ajustement**
Cet article démontre comment vous pouvez réaliser la **couche d'ajustement d'inversion** en utilisant Aspose.PSD pour Java.  Une couche d'ajustement est un type particulier de couche utilisé principalement pour la correction des couleurs. Plutôt que d'avoir un contenu propre, elles ajustent les informations sur les calques en dessous d'elles. La couche d'ajustement d'inversion crée un effet photo négatif en inversant les couleurs d'une image.

Ci-dessous se trouve une démonstration du code de ladite fonctionnalité.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-InvertAdjustmentLayer-InvertAdjustmentLayer.java" >}}

