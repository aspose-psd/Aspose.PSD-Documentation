---
title: Modification d'images
type: docs
weight: 50
url: /fr/net/modifier-les-images/
---

## **Dithering pour les images raster**
Le dithering est une technique de création de l'illusion de nouvelles couleurs et nuances en variant le motif de points qui créent réellement une image. C'est le moyen le plus courant de réduire la gamme de couleurs des images à 256 (ou moins) couleurs. Aspose.PSD fournit la prise en charge du dithering pour la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) en introduisant la méthode Dither qui accepte deux paramètres. Le premier est de type DitheringMethod à appliquer avec deux options possibles : FloydSteinbergDithering et ThresholdDithering. Le deuxième paramètre de la méthode [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) est le BitCount en entier. BitCount définit la taille d'échantillonnage pour le résultat du dithering. La valeur par défaut est 1, ce qui représente le noir et blanc, tandis que les valeurs autorisées sont 1, 4, 8 générant des palettes avec respectivement 2, 4 et 256 couleurs.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-DitheringpourImagesRaster-DitheringpourImagesRaster.cs" >}}

## **Ajustement de la luminosité, du contraste et du gamma**
Les ajustements de couleur dans les images numériques sont l'une des fonctionnalités principales que la plupart des bibliothèques de traitement d'images fournissent. Les ajustements de couleur peuvent être catégorisés comme suit.

1. La luminosité fait référence à la clarté ou à l'obscurité d'une couleur. Augmenter la luminosité d'une image éclaire toutes les couleurs tandis que diminuer la luminosité assombrit toutes les couleurs.
1. Le contraste renvoie à rendre les objets ou les détails dans une image plus évidents. Augmenter le contraste d'une image augmente la différence entre les zones claires et sombres de sorte que les zones claires deviennent plus claires et les zones sombres deviennent plus sombres. Diminuer le contraste fera que les zones plus claires et plus sombres resteront approximativement les mêmes mais l'image globale deviendra plus homogène.
1. Le gamma optimise le contraste et la luminosité de l'éclairage indirect qui éclaire un objet dans l'image.

### **Ajustement de la luminosité**
Aspose.PSD pour l'API .NET fournit la méthode [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) pour la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) qui peut être utilisée pour ajuster la luminosité de l'image en passant une valeur entière en tant que paramètre. La valeur de paramètre la plus élevée correspond à une image plus lumineuse. Voici l'image d'origine et l'image résultante pour comparaison.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-AjustementLuminosite-AjustementLuminosite.cs" >}}

### **Ajustement du contraste**
La méthode [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) exposée par la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) peut être utilisée pour ajuster le contraste d'une image en passant une valeur flottante en tant que paramètre.

La valeur de paramètre la plus élevée indique un contraste plus élevé dans l'image donnée. Voici l'image d'origine et l'image résultante pour comparaison.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-AjustementContraste-AjustementContraste.cs" >}}

### **Ajustement de Gamma**
La méthode [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) exposée par la classe [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) a deux versions. L'une des surcharges accepte une valeur flottante et effectue la correction Gamma pour les coefficients des canaux rouge, bleu et vert. Alors que l'autre surcharge accepte trois valeurs flottantes représentant chaque coefficient de couleur séparément. L'exemple de code suivant montre comment AdjustGamma sur une image.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-AjustementGamma-AjustementGamma.cs" >}}

## **Flouter une image**
Cet article démontre l'utilisation d'Aspose.PSD pour .NET pour appliquer l'effet de flou sur une image. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD pour .NET a exposé la classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) pour créer un effet de flou à la volée. La classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) nécessite des valeurs de rayon et de sigma pour créer un effet de flou sur une image. Les étapes pour effectuer le redimensionnement sont aussi simples que ci-dessous :

1. Charger une image en utilisant la méthode d'usine Load exposée par la classe Image.
1. Convertir l'image en [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. Créer une instance de la classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) avec le constructeur par défaut ou fournir des valeurs de rayon et de sigma dans le constructeur.
1. Appeler la méthode Filter de [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) tout en spécifiant le rectangle comme limites de l'image et une instance de la classe [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions).
1. Enregistrer les résultats.

L'exemple de code suivant montre comment créer un effet de flou sur une image.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-FlouterUneImage-FlouterUneImage.cs" >}}

## **Vérifier la transparence de l'image**
Cet article démontre l'utilisation d'Aspose.PSD pour .NET pour vérifier la transparence de l'image. Les étapes pour vérifier la transparence de l'image sont aussi simples que ci-dessous :

1. Charger une image en utilisant la méthode d'usine [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) exposée par la classe [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. Vérifier l'opacité de l'image. Si l'opacité est nulle, l'image est transparente.
1. L'exemple de code suivant montre comment vérifier si l'image est transparente ou non.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-VerifierLaTransparenceImage-VerifierLaTransparenceImage.cs" >}}

## **Implémenter le Compresseur GIF Lossy**
En utilisant Aspose.PSD pour .NET, les développeurs peuvent définir une différence de pixel. La compression du GIF est basée sur un "dictionnaire" de chaînes de pixels vus. L'encodeur normal recherche dans le dictionnaire la chaîne la plus longue de pixels qui correspondent exactement aux pixels de l'image. L'encodeur lossy choisit la chaîne la plus longue de pixels qui est "suffisamment similaire" aux pixels de l'image. Ci-dessous se trouve la démonstration du code de ladite fonctionnalité.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-ImplementerCompresseurGIFLossy-ImplementerCompresseurGIFLossy.cs" >}}

## **Implémenter le rééchantillonnage bicubique**
Le rééchantillonnage signifie que vous modifiez les dimensions en pixels d'une image. Lorsque vous sous-échantillonnez, vous éliminez des pixels et supprimez donc des informations et des détails de votre image. Lorsque vous sur-échantillonnez, vous ajoutez des pixels. Photoshop ajoute ces pixels en utilisant l'interpolation. Cet article montre comment vous pouvez effectuer le rééchantillonnage bicubique en utilisant Aspose.PSD pour .NET.

Ci-dessous se trouve la démonstration du code de ladite fonctionnalité.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-ImplanterResamplageBicubique-ImplanterResamplageBicubique.cs" >}}

## **Couche d'ajustement de l'équilibre des couleurs**
Cet article démontre l'utilisation d'Aspose.PSD pour .NET pour réaliser la **couche d'ajustement de l'équilibre des couleurs** sur une image. La couche d'ajustement de l'équilibre des couleurs vous donne la possibilité d'apporter des ajustements à la coloration de vos images. Elle présente les trois canaux de couleur et leurs couleurs complémentaires et vous permet d'ajuster l'équilibre de ces paires pour changer l'apparence d'une photo.

Ci-dessous se trouve la démonstration du code de ladite fonctionnalité.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-AjustementÉquilibreCouleur-CoucheAjustementÉquilibreCouleur.cs" >}}

## **Couche d'ajustement d'inversion**
Cet article démontre comment vous pouvez effectuer la **couche d'ajustement d'inversion** en utilisant Aspose.PSD pour .NET. Une couche d'ajustement est un type spécial de couche utilisé principalement pour la correction des couleurs. Plutôt que d'avoir un contenu propre, elles ajustent les informations sur les calques en dessous d'elles. La couche d'ajustement d'inversion crée un effet négatif de photo en inversant les couleurs d'une image.

Ci-dessous se trouve la démonstration du code de ladite fonctionnalité.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-DessinEtMiseEnFormeImages-CoucheAjustementInversion-CoucheAjustementInversion.cs" >}}
