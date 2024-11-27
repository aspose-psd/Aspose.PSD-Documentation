---
title: Couche PSD
type: docs
weight: 70
url: /fr/net/psd-layer/
---

## **Aperçu**
La couche PSD d'Adobe® Photoshop® est l'un des meilleurs concepts de traitement graphique. Les couches contiennent des informations sur les pixels et peuvent avoir un nombre différent de canaux.

Une des parties les plus importantes de la couche dans le document Photoshop est les ressources de la couche. Vous pouvez obtenir la liste complète des [Ressources de couche](/psd/fr/net/list-of-psd-layer-resources/) prises en charge dans un document PSD depuis notre documentation.

Vous pouvez trouver une interface utilisateur pour manipuler la couche sur la capture d'écran suivante :

![todo:image_alt_text](psd-layer_1.png)

Mais Aspose.PSD se spécialise dans la manipulation programmatique de la couche PSD via [C#](/psd/fr/net/home/) et [Java](https://docs.aspose.com/display/psdjava/Aspose.PSD+for+Java+Home).

Vous trouverez des informations supplémentaires dans cet article : [Manipuler des images](/psd/fr/net/manipulating-images-html/). Toute manipulation peut être effectuée sur l'aperçu PSD et la couche, vous trouverez plus d'informations dans la [Référence de l'API d'image raster Aspose.PSD](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).

## **API de couche PSD disponible**
- Effets de couche
- Propriétés communes des couches
- Métadonnées de couche

## **Exemples de modification de la couche via C#**
### **Ajout d'une nouvelle couche**
Si vous souhaitez ajouter une couche vide à un [fichier PSD](/psd/fr/net/psd-file/) ouvert, vous pouvez utiliser le code suivant.

Ajouter une nouvelle couche au fichier PSD en utilisant l'API

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-AddNewRegularLayerToPSD-AddNewRegularLayerToPSD.cs" >}}

### **Ajout d'une nouvelle couche à partir de fichiers Jpeg, Png, Gif, Ai, Tiff, Bmp**
Des fichiers de tout [format pris en charge](/psd/fr/net/supported-file-formats/) peuvent être ajoutés en tant que nouvelle couche à votre image. Mais vous ne pouvez pas le charger directement.

Vous pouvez utiliser le code ci-dessous pour ajouter une nouvelle couche PSD à partir du fichier de n'importe quel format pris en charge à partir du flux.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}

### **Aplatir toutes les couches ou les groupes de couches**
Cela peut être utile si vous ne voulez pas donner un fichier PSD modifiable à vos utilisateurs. De plus, vous pouvez identifier à travers l'API si le fichier a été aplati.

Aplatir la couche du fichier PSD :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PossibilityToFlattenLayers-PossibilityToFlattenLayers.cs" >}}
