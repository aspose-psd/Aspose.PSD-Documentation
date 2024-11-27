---
title: Prise en charge des calques de remplissage
type: docs
weight: 50
url: /fr/java/support-of-fill-layers/
---


## **Prise en charge des calques de remplissage avec couleur de remplissage**
Cet article démontre comment remplir un calque PSD avec une couleur. Veuillez utiliser la classe Aspose.PSD.FileFormats.Psd.Layers.FillLayer pour ajouter une couleur dans un calque PSD. Les extraits de code suivants chargent un fichier PSD, accèdent à la classe Filllayer et définissent la couleur en utilisant la propriété FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **Prise en charge des calques de remplissage avec dégradé de couleurs**
Cet article démontre l'utilisation du remplissage dégradé pour remplir un calque PSD. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé les classes GradientColorPoint et GradientTransparencyPoint pour ajouter un effet de dégradé à un calque.

` `Les étapes pour remplir un calque PSD avec un dégradé de couleurs sont aussi simples que ci-dessous:

- Charger un fichier PSD en tant qu'image en utilisant la méthode d'usine Load exposée par la classe Image.
- Définir les propriétés des paramètres du calque de remplissage.
- Créer une liste de ColorPoints avec les couleurs requises et la position de la couleur.
- Créer une liste de points de transparence avec l'opacité requise et la position du point de transparence.
- Appeler la méthode FillLayer.Update
- Enregistrer les résultats.

Le code suivant vous montre comment ajouter un remplissage dégradé pour remplir un calque PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **Effet de contour avec remplissage de couleur**
Cet article démontre comment rendre un effet de contour avec un remplissage de couleur. L'effet de contour est utilisé pour ajouter des contours et des bordures aux calques et aux formes. Il peut être utilisé pour créer des lignes de couleur unie, des dégradés colorés, ainsi que des bordures à motifs.

Les étapes pour rendre un effet de contour avec un remplissage de couleur sont aussi simples que ci-dessous:

- Définir la propriété **LoadEffectsResource**.
- Charger un fichier PSD en tant qu'image en utilisant la méthode d'usine Load exposée par la classe Image et définir **PsdLoadOptions**.
- Définir les propriétés des paramètres de **ColorFillSetting.**
- Enregistrer les résultats.

Le code suivant vous montre comment rendre un effet de contour avec un remplissage de couleur.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}




