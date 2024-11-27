---
title: Manipulation des images PNG
type: docs
weight: 30
url: /fr/java/manipulation-images-png/
---

## **Spécification de la transparence pour les images PNG**
L'un des avantages de sauvegarder des images au format PNG est que le PNG peut avoir un arrière-plan transparent. Aspose.PSD pour Java fournit la fonctionnalité pour spécifier la transparence pour les classes PngImage & RasterImage comme démontré dans la section ci-dessous. L'API Aspose.PSD pour Java peut être utilisée pour définir n'importe quelle couleur comme transparente lors de la création de nouvelles images PNG ou de la conversion d'images existantes au format PNG. À cette fin, l'API Aspose.PSD pour Java a exposé la propriété TransparentColor et l'énumération PngColorType qui peuvent être définies pour spécifier n'importe quelle couleur à rendre transparente dans l'image PNG. Le snippet de code fourni ci-dessous démontre comment convertir une image PSD existante en image PNG en utilisant le constructeur surchargé PngImage et en spécifiant la couleur désirée comme transparente.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.java" >}}
## **Définition de la résolution des images PNG**
Aspose.PSD pour Java expose la classe ResolutionSetting qui peut être utilisée pour définir la résolution pour tous les formats d'image, y compris PNG. Cet article démontre l'utilisation de l'API Aspose.PSD pour Java pour définir les paramètres de résolution horizontale et verticale pour le format d'image PNG. Le snippet de code ci-dessous charge une image PSD existante et la convertit au format PNG en changeant également la résolution.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.java" >}}
## **Compression des fichiers PNG**
Le format Portable Network Graphic (PNG) est un format de compression sans perte pour transmettre un bitmap sur des réseaux. Lorsque vous enregistrez une image en tant que fichier PNG dans n'importe quel programme, il se peut que l'on vous demande de choisir un niveau de compression dans une plage de 0 à n'importe quel niveau maximal. Ce réglage compresse en fait la taille du fichier et ne diminue pas la qualité de l'image. Cet article décrit comment les API Aspose.PSD vous permettent de contrôler la taille des fichiers PNG. Les API Aspose.PSD peuvent être utilisées pour définir les niveaux de compression pour le format de fichier PNG en utilisant la classe PngOptions qui a une propriété CompressionLevel de type int. Cette propriété accepte une valeur de 0 à 9 où 9 est la compression maximale. Le snippet de code fourni ci-dessous démontre comment définir les niveaux de compression en utilisant Aspose.PSD pour l'API Java.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.java" >}}
## **Spécification de la profondeur de bits pour les images PNG**
La profondeur de bits en imagerie est le nombre de bits utilisés pour indiquer la couleur d'un seul pixel dans une image bitmap. Comme tous les autres formats bitmap, la profondeur de couleur des PNG est également représentée en bits tels que 1-bit (2 couleurs), 2-bit (4 couleurs), 4-bit (16 couleurs) et 8-bit (256 couleurs). L'API Aspose.PSD pour Java peut être utilisée pour définir la profondeur de bits pour les images PNG en utilisant la propriété BitDepth exposée par la classe PngOptions. Actuellement, la propriété BitDepth peut être définie à 1, 2, 4 ou 8 bits pour les types de couleur en niveaux de gris et indexés. Pour tous les autres types de couleur, seuls 8 bits sont pris en charge. Le snippet de code fourni ci-dessous démontre comment définir la profondeur de bits pour une image PNG.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.java" >}}
## **Application de méthodes de filtre sur les images PNG**
Aspose.PSD pour Java expose l'énumération PngFilterType qui peut être utilisée pour définir le type de filtre pour une image PNG. Le snippet de code ci-dessous démontre comment appliquer un filtre sur un fichier PSD existant pour une image PNG en utilisant PngFilterType.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.java" >}}
## **Changement de la couleur d'arrière-plan d'une image PNG transparente**
Les images au format PNG peuvent avoir un arrière-plan transparent. Aspose.PSD pour Java fournit la fonctionnalité de changer la couleur d'arrière-plan d'une image PNG qui a un arrière-plan transparent. L'API Aspose.PSD pour Java peut être utilisée pour définir/changer la couleur d'une image PNG transparente. Le snippet de code fourni ci-dessous démontre comment définir/changer la couleur d'arrière-plan d'une image PNG transparente.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.java" >}}
