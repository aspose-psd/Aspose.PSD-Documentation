---
title: Manipulation des formats Photoshop
type: docs
weight: 10
url: /fr/java/manipulation-des-formats-photoshop/
---

## **Remplacement de couleur dans les couches PSD**
Aspose.PSD for Java vous permet de changer la couleur d'arrière-plan de chaque couche d'un fichier PSD. Veuillez utiliser la classe Aspose.PSD.FileFormats.Psd.Layers.BackgroundColor pour changer la couleur d'arrière-plan de la couche dans la couche PSD. Le code suivant charge un fichier PSD, accède à la couche, met à jour la couleur d'arrière-plan et enregistre le fichier PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.java" >}}
## **Mettre à jour la couche de texte dans un fichier PSD**
Aspose.PSD for Java vous permet de manipuler le texte dans la couche de texte d'un fichier PSD. Veuillez utiliser la classe Aspose.PSD.FileFormats.Psd.Layers.TextLayer pour mettre à jour le texte dans la couche PSD. Le code suivant charge un fichier PSD, accède à la couche de texte, met à jour le texte et enregistre le fichier PSD avec un nouveau nom en utilisant la méthode Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.java" >}}
## **Détection de l'aplatissement PSD**
Aspose.PSD for Java vous permet de détecter si un fichier PSD donné est aplati ou non. La propriété IsFlatten a été introduite dans la classe Aspose.PSD.FileFormats.Psd.PsdImage pour réaliser cette fonctionnalité. Le code suivant charge un fichier PSD et accède à la propriété IsFlatten.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.java" >}}
## **Fusionner des couches PSD**
Cet article montre comment fusionner des couches dans un fichier PSD tout en convertissant un fichier PSD en JPG avec Aspose.PSD. Dans l'exemple ci-dessous, un fichier PSD existant est chargé en passant le chemin du fichier à la méthode statique Load de la classe Image. Une fois chargé, convertissez/castez l'image en PsdImage. Créez une instance de la classe JpegOptions et définissez ses différentes propriétés. Appelez maintenant la méthode Save de l'instance PsdImage. Le code suivant montre comment fusionner des couches PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-MergePSDLayers-MergePSDLayers.java" >}}
## **Prise en charge du niveau de gris avec alpha pour PSD**
Cet article montre comment prendre en charge le niveau de gris avec alpha pour un fichier PSD tout en convertissant un fichier PSD en PNG avec Aspose.PSD. Dans l'exemple ci-dessous, un fichier PSD existant est chargé en passant le chemin du fichier à la méthode statique Load de la classe Image. Une fois chargé, convertissez/castez l'image en PsdImage. Créez une instance de la classe PngOptions et définissez ses différentes propriétés. Définissez la propriété ColorType sur TruecolorWithAlpha. Appelez maintenant la méthode Save de l'instance PngOptions. Le code suivant montre comment convertir en PNG en niveaux de gris avec alpha.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.java" >}}