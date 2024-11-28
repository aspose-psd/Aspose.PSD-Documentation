---
title: Création, ouverture et enregistrement des fichiers PSD
type: docs
weight: 10
url: /fr/creating-opening-and-saving-psd-files/
---

## **Exporter une image au format PSD**
PSD, document PhotoShop, est le format de fichier par défaut utilisé par Adobe PhotoShop pour travailler avec des images. Aspose.PSD vous permet de charger, éditer et enregistrer des fichiers au format PSD afin qu'ils puissent être ouverts et édités dans PhotoShop. Cet article montre comment enregistrer un fichier au format PSD avec Aspose.PSD, et discute également de certains des paramètres qui peuvent être utilisés lors de l'enregistrement dans ce format. PsdOptions est une classe spécialisée dans l'espace de noms ImageOptions utilisée pour exporter des images au format PSD. Pour exporter au format PSD, créez une instance de la classe Image, soit chargée à partir d'un fichier image existant (miniatures par exemple), soit créée à partir de zéro. Cet article explique comment faire. Dans les exemples ci-dessous, une image est créée à partir de zéro. Une fois qu'elle est créée et que les données de pixels sont remplies, enregistrez l'image en utilisant la méthode Save de la classe Image, et fournissez un objet PsdOptions comme deuxième argument. Plusieurs des propriétés de la classe PsdOptions peuvent être définies pour une conversion avancée. Certaines des propriétés sont ColorMode, CompressionMethod et Version. Aspose.PSD prend en charge les méthodes de compression suivantes à travers l'énumération CompressionMethod :

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Les modes de couleurs suivants sont pris en charge à travers l'énumération ColorModes :

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB



Des ressources supplémentaires peuvent être ajoutées, telles que des ressources de vignettes pour les PSD v4.0, v5.0 et supérieurs, ou des ressources de grille et de guide pour les PSD v4.0 et supérieurs. Le code ci-dessous crée un fichier BMP à partir de zéro, remplit les pixels et l'enregistre en PSD avec une compression RLE et un mode couleur en niveaux de gris. Le code suivant vous montre comment exporter une image au format PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.java" >}}
## **Importer une image dans une couche PSD**
Cet article démontre l'utilisation de Aspose.PSD pour ajouter ou importer une image dans une couche PSD. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé la méthode DrawImage de la classe Layer pour ajouter/importer une image dans un fichier PSD. La méthode DrawImage a besoin des valeurs de localisation et d'image pour ajouter/importer une image dans un fichier PSD. Les étapes pour importer une image dans une couche PSD sont aussi simples que ci-dessous :

- Chargez un fichier PSD en tant qu'image en utilisant la méthode factory Load exposée par la classe Image.
- Créez une instance de la classe Layer et attribuez-lui la couche d'image PSD.
- Chargez l'image qui doit être ajoutée ou créez-en une à partir de zéro.
- Appelez la méthode Layer.DrawImage en spécifiant la localisation et l'instance d'image.
- Enregistrez les résultats.



Le code suivant vous montre comment importer une image dans une couche PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ImportImageToPSDLayer-ImportImageToPSDLayer.java" >}}


## **Création de vignettes à partir de fichiers PSD**
PSD est le format de document natif de l'application Photoshop d'Adobe. Adobe Photoshop (version 5.0 et ultérieure) stocke des informations de vignette pour l'affichage en prévisualisation dans un bloc de ressources d'image qui se compose d'un en-tête initial de 28 octets, suivi d'une vignette JFIF dans l'ordre RVB (rouge, vert, bleu). L'API Aspose.PSD fournit un mécanisme facile à utiliser pour accéder aux ressources du fichier PSD. Ces ressources incluent également la ressource de vignette qui peut à son tour être récupérée et enregistrée sur le disque selon les besoins de l'application. Le code suivant vous montre comment créer des vignettes à partir de fichiers PSD.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.java" >}}


## **Création de fichiers PSD indexés**
Aspose.PSD pour l'API Java peut créer des fichiers PSD indexés à partir de zéro. Cet article démontre l'utilisation des classes PsdOptions et PsdImage pour créer un PSD indexé tout en dessinant des formes sur le canevas nouvellement créé. Les étapes simples suivantes sont nécessaires pour créer un fichier PSD indexé.

- Créez une instance de PsdOptions et définissez sa source.
- Définissez la propriété ColorMode de PsdOptions sur ColorModes.Indexed.
- Créez une nouvelle palette de couleurs à partir de l'espace RGB et définissez-la comme propriété Palette de PsdOptions.
- Définissez la propriété CompressionMethod sur l'algorithme de compression requis.
- Créez une nouvelle image PSD en appelant la méthode PsdImage.Create.
- Dessinez des graphiques ou effectuez d'autres opérations selon les besoins.
- Appelez la méthode PsdImage.Save pour valider tous les changements.



Le code suivant vous montre comment créer des fichiers PSD indexés.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.java" >}}
## **Exporter une couche PSD en image matricielle**
Aspose.PSD pour Java vous permet d'exporter des couches dans un fichier PSD en images matricielles. Veuillez utiliser la méthode Aspose.PSD.FileFormats.Psd.Layers.Layer.Save pour exporter la couche en image. Le code d'exemple suivant charge un fichier PSD et exporte chacune de ses couches en une image PNG en utilisant Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Une fois que toutes les couches sont exportées en images PNG, vous pouvez les ouvrir avec votre visualiseur d'images préféré. Le code suivant vous montre comment exporter une couche PSD en image matricielle.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.java" >}}
