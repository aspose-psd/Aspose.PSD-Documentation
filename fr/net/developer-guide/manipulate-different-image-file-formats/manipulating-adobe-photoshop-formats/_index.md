---
title: Manipulation des formats Adobe Photoshop
type: docs
weight: 20
url: /fr/net/manipulation-des-formats-adobe-photoshop/
---

## **Fusionner des calques PSD avec d'autres calques**

## **Exporter une image en PSD**
PSD, document PhotoShop, est le format de fichier par défaut utilisé par Adobe Photoshop pour travailler avec des images. Aspose.PSD vous permet de charger, modifier et enregistrer des fichiers en PSD afin qu'ils puissent être ouverts et édités dans Photoshop. Cet article montre comment enregistrer un fichier en PSD avec Aspose.PSD, et il discute également de certains des paramètres qui peuvent être utilisés lors de l'enregistrement dans ce format. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) est une classe spécialisée dans l'espace de noms [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) utilisée pour exporter des images en PSD. Pour exporter en PSD, créez une instance de la classe Image, soit chargée à partir d'un fichier image existant (miniatures par exemple) soit créée à partir de zéro. Cet article explique comment. Dans les exemples ci-dessous, une image est créée à partir de zéro. Une fois qu'elle est créée et que les données de pixels sont remplies, enregistrez l'image en utilisant la méthode de sauvegarde de la classe Image, et fournissez un objet PsdOptions en tant que deuxième argument. Plusieurs des propriétés de la classe PsdOptions peuvent être définies pour une conversion avancée. Certaines des propriétés sont ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) et Version. Aspose.PSD prend en charge les méthodes de compression suivantes à travers l'énumération CompressionMethod :

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

Les modes de couleur suivants sont pris en charge à travers l'énumération [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes) :

- ColorModes.Bitmap
- ColorModes.Nuances de gris
- ColorModes.RGB

Des ressources supplémentaires peuvent être ajoutées, telles que des ressources miniatures pour les versions PSD v4.0, v5.0 et supérieures, ou des ressources de grille et de guide pour les versions PSD v4.0 et supérieures. Le code ci-dessous crée un fichier Image à partir de zéro, remplit les pixels et l'enregistre en PSD avec une compression RLE et un mode de couleur en nuances de gris. Le code ci-dessous montre comment exporter une image en PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **Importation d'image sur un calque PSD**
Cet article démontre l'utilisation d'Aspose.PSD pour ajouter ou importer une image sur un calque PSD. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé la méthode [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) de la classe Layer pour ajouter/importer une image dans un fichier PSD. La méthode DrawImage a besoin des valeurs d'emplacement et d'image pour ajouter/importer une image dans un fichier PSD. Les étapes pour importer une image sur un calque PSD sont aussi simples que ci-dessous :

- Charger un fichier PSD en tant qu'image en utilisant la méthode d'usine Load exposée par la classe Image.
- Créer une instance de la classe Layer à partir du flux avec un fichier Png, Jpeg, Tiff, Gif, Bmp, Psd ou J2k
- Ajouter un calque au PSD en utilisant la méthode AddLayer
- Enregistrer les résultats.


Le code ci-dessous montre comment importer l'image sur un calque PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **Remplacement de couleur dans les calques PSD**
Cet article démontre l'utilisation d'Aspose.PSD pour ajouter ou importer une image sur un calque PSD. Les API Aspose.PSD ont exposé des méthodes efficaces et faciles à utiliser pour atteindre cet objectif. Aspose.PSD a exposé la méthode DrawImage de la classe Layer pour ajouter/importer une image dans un fichier PSD. La méthode DrawImage a besoin des valeurs d'emplacement et d'image pour ajouter/importer une image dans un fichier PSD. Les étapes pour importer une image sur un calque PSD sont aussi simples que ci-dessous :

- Charger un fichier PSD en tant qu'image en utilisant la méthode d'usine Load exposée par la classe Image.
- Créer une instance de la classe Layer et assigner le calque d'image PSD à celle-ci.
- Charger l'image qui doit être ajoutée ou en créer une à partir de zéro.
- Appeler la méthode Layer.DrawImage en spécifiant l'emplacement et l'instance d'image.
- Enregistrer les résultats.


Le code ci-dessous montre comment importer une image sur un calque PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **Création de miniatures à partir de fichiers PSD**
Le PSD est le format de document natif de l'application Photoshop d'Adobe. Adobe Photoshop (version 5.0 et ultérieure) stocke des informations de vignette pour l'affichage prévisualisé dans un bloc de ressources d'image qui se compose d'un en-tête initial de 28 octets, suivi d'une vignette JFIF en ordre RVB (rouge, vert, bleu). L'API Aspose.PSD fournit un mécanisme facile à utiliser pour accéder aux ressources du fichier PSD. Ces ressources comprennent également la ressource de vignette qui peut à son tour être récupérée et enregistrée sur disque selon les besoins de l'application. Le code ci-dessous montre comment créer des miniatures à partir de fichiers PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **Création de fichiers PSD indexés**
Aspose.PSD pour .NET API peut créer des fichiers PSD indexés à partir de zéro. Cet article démontre l'utilisation des classes PsdOptions et [PsdImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage) pour créer un PSD indexé tout en dessinant quelques formes sur le canevas nouvellement créé. Les étapes simples suivantes sont nécessaires pour créer un fichier PSD indexé.

- Créez une instance de PsdOptions et définissez sa source.
- Définissez la propriété ColorMode de PsdOptions sur ColorModes.Indexed.
- Créez une nouvelle palette de couleurs à partir de l'espace RGB et définissez-la comme propriété Palette de PsdOptions.
- Définissez la propriété CompressionMethod sur l'algorithme de compression requis.
- Créez une nouvelle image PSD en appelant la méthode PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create).
- Dessinez des graphiques ou effectuez d'autres opérations selon les besoins.
- Appelez la méthode PsdImage.Save pour valider toutes les modifications.

Le code ci-dessous montre comment créer des fichiers PSD indexés.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **Exportation du calque PSD en image matricielle**
Aspose.PSD pour .NET vous permet d'exporter des calques dans un fichier PSD en images matricielles. Veuillez utiliser la méthode [Aspose.PSD.FileFormats.Psd.Layers.Layer.Save](https://reference.aspose.com/psd/net/aspose.psd/image/methods/save/index) pour exporter le calque vers l'image. Le code d'exemple suivant charge un fichier PSD et exporte chacun de ses calques dans une image PNG en utilisant Aspose.PSD.FileFormats.Psd.Layers.Layer.Save. Une fois que tous les calques sont exportés en images PNG, vous pouvez les ouvrir à l'aide de votre visionneuse d'images préférée. Le code ci-dessous montre comment exporter un calque PSD en une image matricielle.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportPSDLayerToRasterImage-ExportPSDLayerToRasterImage.cs" >}}
## **Mettre à jour le calque de texte dans un fichier PSD**
Aspose.PSD pour .NET vous permet de manipuler le texte dans le calque de texte d'un fichier PSD. Veuillez utiliser la classe [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/textlayer) pour mettre à jour le texte dans le calque PSD. Le code d'exemple suivant charge un fichier PSD, accède au calque de texte, met à jour le texte et enregistre le fichier PSD avec un nouveau nom en utilisant la méthode [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/textlayer/methods/updatetext/index).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **Détection d'un PSD aplatit**
Aspose.PSD pour .NET vous permet de détecter si un fichier PSD donné est aplatit ou non. La propriété IsFlatten a été introduite dans la classe Aspose.PSD.FileFormats.Psd.PsdImage pour atteindre cette fonctionnalité. Le code d'exemple suivant charge un fichier PSD et accède à la propriété [IsFlatten](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/psdimage/properties/is