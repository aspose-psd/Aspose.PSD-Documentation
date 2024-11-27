---
title: Application des filtres médian et de Wiener
type: docs
weight: 10
url: /fr/application-des-filtres-median-et-de-wiener/
---

## **Application des filtres médian et de Wiener**
Le filtre médian est une technique de filtrage numérique non linéaire, souvent utilisée pour supprimer le bruit. Une telle réduction du bruit est une étape de prétraitement typique pour améliorer les résultats du traitement ultérieur. Le filtre de Wiener est le filtre linéaire stationnaire optimal en terme d'erreur quadratique moyenne (EQM) pour les images dégradées par du bruit additif et du flou. En utilisant l'API Aspose.PSD pour les développeurs Java, il est possible d'appliquer un filtre médian pour débruiter l'image et d'appliquer un filtre gaussien de Wiener sur les images. Cet article démontre comment les filtres médian et gaussien de Wiener peuvent être appliqués aux images.
### **Application du filtre médian**
Aspose.PSD fournit la classe MedianFilterOptions pour appliquer un filtre sur une RasterImage. L'extrait de code fourni ci-dessous démontre comment appliquer un filtre médian à une image matricielle.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **Application du filtre gaussien de Wiener**
Aspose.PSD fournit la classe GaussWienerFilterOptions pour appliquer un filtre sur une RasterImage. L'extrait de code fourni ci-dessous démontre comment appliquer un filtre gaussien de Wiener à une image matricielle.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **Application du filtre gaussien de Wiener pour une image en couleurs**
Aspose.PSD fournit des GaussWienerFilterOptions également pour les images en couleurs. L'extrait de code fourni ci-dessous démontre comment appliquer un filtre gaussien de Wiener à une image en couleurs.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **Application du filtre de Wiener en mouvement**
Aspose.PSD fournit la classe MotionWienerFilterOptions pour appliquer un filtre sur une RasterImage. L'extrait de code fourni ci-dessous démontre comment appliquer un filtre de Wiener en mouvement à une image matricielle.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **Appliquer un filtre de correction sur une image**
Cet article démontre l'utilisation d'Aspose.PSD pour Java pour effectuer des filtres de correction sur une image. Les API Aspose.PSD exposent des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD pour Java a exposé les classes BilateralSmoothingFilterOptions et SharpenFilterOptions pour la filtration. La classe BilateralSmoothingFilterOptions nécessite un entier en tant que taille. Les étapes pour effectuer un redimensionnement sont aussi simples que ci-dessous :
1. Charger une image en utilisant la méthode factory Load exposée par la classe Image.
1. Convertir l'image en RasterImage.
1. Créer des instances des classes BilateralSmoothingFilterOptions et SharpenFilterOptions.
1. Appeler la méthode RasterImage.Filter en spécifiant le rectangle comme limites de l'image et une instance de la classe BilateralSmoothingFilterOptions.
1. Appeler la méthode RasterImage.Filter en spécifiant le rectangle comme limites de l'image et une instance de la classe SharpenFilterOptions.
1. Ajuster le contraste.
1. Régler la luminosité.
1. Sauvegarder les résultats.

L'extrait de code suivant montre comment appliquer un filtre de correction.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **Utiliser l'algorithme de seuillage de Bradley**
Le seuillage d'image est utilisé dans les applications graphiques. L'objectif du seuillage d'une image est de classer les pixels en "sombres" ou "clairs". L'API Aspose.PSD vous permet d'utiliser le seuillage de Bradley lors de la conversion d'images. L'extrait de code suivant vous montre comment définir la valeur de seuil et ensuite invoquer l'algorithme de seuillage de Bradley.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
