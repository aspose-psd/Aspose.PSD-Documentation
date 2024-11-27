---
title: Application des Filtres Médian et Wiener
type: docs
weight: 10
url: /fr/application-des-filtres-median-et-wiener/
---

## **Application des Filtres Médian et Wiener**
Le filtre médian est une technique de filtrage numérique non linéaire, souvent utilisée pour supprimer le bruit. Cette réduction de bruit est une étape de prétraitement typique pour améliorer les résultats des traitements ultérieurs. Le filtre de Wiener est le filtre linéaire stationnaire optimal en terme d'erreur quadratique moyenne pour les images dégradées par du bruit additif et du flou. En utilisant Aspose.PSD pour les développeurs API .NET, il est possible d'appliquer un filtre médian pour réduire le bruit de l'image et de mettre en œuvre un filtre de Wiener gaussien sur les images. Cet article montre comment le filtre médian et le filtre de Wiener gaussien peuvent être appliqués aux images.
### **Application du Filtre Médian**
Aspose.PSD fournit la classe [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) pour appliquer un filtre sur une [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). L'extrait de code ci-dessous montre comment appliquer le filtre médian à une image raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Application-des-Filtres-Median-et-Wiener-Application-des-Filtres-Median-et-Wiener.cs" >}}


### **Application du Filtre de Wiener Gaussien**
Aspose.PSD fournit la classe [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) pour appliquer un filtre sur une [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). L'extrait de code ci-dessous montre comment appliquer le filtre de Wiener gaussien à une image raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Application-de-Filtres-Wiener-et-Gauss-Wiener-Application-de-Filtres-Wiener-et-Gauss-Wiener.cs" >}}


### **Application du Filtre de Wiener Gaussien pour une Image Colorée**
Aspose.PSD fournit également [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) pour les images colorées. L'extrait de code ci-dessous montre comment appliquer le filtre de Wiener gaussien à une image en couleur.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Application-de-Filtres-Wiener-et-Gauss-Wiener-pour-Image-Colorée-Application-de-Filtres-Wiener-et-Gauss-Wiener-pour-Image-Colorée.cs" >}}


### **Application du Filtre de Wiener de Mouvement**
Aspose.PSD fournit la classe [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions) pour appliquer un filtre sur une [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage). L'extrait de code ci-dessous montre comment appliquer un filtre de Wiener de mouvement à une image raster.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Application-des-Filtres-Median-et-Wiener-Application-des-Filtres-Median-et-Wiener.cs" >}}


## **Appliquer un Filtre de Correction Sur une Image**
Cet article montre l'utilisation d'Aspose.PSD pour .NET pour effectuer des filtres de correction sur une image. Les APIs d'Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD pour .NET a exposé les classes [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions) et [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions) pour la filtration. La classe BilateralSmoothingFilterOptions nécessite un entier comme taille. Les étapes pour effectuer le redimensionnement sont aussi simples que ci-dessous :

1. Charger une image en utilisant la méthode d'usine Load exposée par la classe Image.
1. Convertir l'image en RasterImage.
1. Créer une instance des classes BilateralSmoothingFilterOptions et SharpenFilterOptions.
1. Appeler la méthode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) en spécifiant le rectangle comme limites de l'image et l'instance de la classe BilateralSmoothingFilterOptions.
1. Appeler la méthode [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) en spécifiant le rectangle comme limites de l'image et l'instance de la classe SharpenFilterOptions.
1. Ajuster le contraste.
1. Définir la luminosité.
1. Sauvegarder les résultats.


## **Utiliser l'algorithme de seuillage de Bradley**
Le seuillage d'image est utilisé dans les applications graphiques. Le but du seuillage d'une image est de classer les pixels comme étant soit "foncés" ou "clair". L'API Aspose.PSD vous permet d'utiliser le seuillage de Bradley lors de la conversion d'images. L'extrait de code suivant montre comment définir la valeur de seuil, puis invoquer l'algorithme de seuillage de Bradley.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Exemples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
