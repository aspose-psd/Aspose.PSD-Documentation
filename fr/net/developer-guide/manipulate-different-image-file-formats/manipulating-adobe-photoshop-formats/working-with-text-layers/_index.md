---
title: Travailler avec les calques de texte
type: docs
weight: 170
url: /fr/travailler-avec-les-calques-de-texte/
---

## **Ajouter un calque de texte**
Aspose.PSD pour .NET vous permet d'ajouter un calque de texte dans un fichier PSD. Les étapes pour ajouter un calque de texte dans un fichier PSD sont aussi simples que ci-dessous :

- Chargez un fichier PSD en tant qu'image en utilisant la méthode d'usine [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) exposée par la [classe Image](https://reference.aspose.com/psd/net/aspose.psd/image)
- Appelez la méthode [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) qui accepte du texte et une instance de la classe [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)
- Enregistrez les résultats

Le code suivant montre comment ajouter un calque de texte dans un fichier PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}


## **Définir la position du calque de texte**
Aspose.PSD pour .NET vous permet de définir la position d'un calque de texte dans un fichier PSD. Les étapes pour définir la position du calque de texte dans un fichier PSD sont aussi simples que ci-dessous :

- Chargez un fichier PSD en tant qu'image en utilisant la méthode d'usine **Load** exposée par la classe Image
- Appelez la méthode AddTextLayer en spécifiant les positions de gauche et de haut du calque de texte
- Enregistrez les résultats

Le code suivant montre comment définir la position du calque de texte dans un fichier PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}


## **Obtenir les propriétés de texte d'un calque de texte**
En utilisant Aspose.PSD pour .NET, vous pouvez obtenir et mettre à jour les propriétés de texte de différentes parties de texte disponibles dans le calque de texte PSD. Cet article démontre comment obtenir des paragraphes, des styles et des propriétés de texte du calque de texte et les mettre à jour.

Le code ci-dessous montre comment accomplir cette exigence.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


Voici un autre exemple qui démontre comment un développeur peut obtenir le formatage de texte de différentes portions de texte à partir de [TextLayer](https://reference.aspose.com/net/psd/aspose.psd/fileformats/psd/layers/textlayer) en utilisant [Aspose.PSD pour .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}


## **Mettre à jour le calque de texte dans un fichier PSD**
Aspose.PSD pour .NET vous permet de manipuler le texte dans le calque de texte d'un fichier PSD. Veuillez utiliser la classe Aspose.PSD.FileFormats.Psd.Layers.TextLayer pour mettre à jour le texte dans le calque PSD. Le code suivant charge un fichier PSD, accède au calque de texte, met à jour le texte et enregistre le fichier PSD sous un nouveau nom en utilisant la méthode [**UpdateText**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer/methods/updatetext/index) de [Aspose.PSD.FileFormats.Psd.Layers.TextLayer](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/layers/textlayer).


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}


## **Prise en charge des calques de texte en temps d'exécution**
Cet article montre comment ajouter des calques de texte en temps d'exécution pour les images PSD. Le code ci-dessous a été fourni.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
