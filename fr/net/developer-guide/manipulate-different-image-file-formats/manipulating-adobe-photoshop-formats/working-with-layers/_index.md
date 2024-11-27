---
title: Travailler avec les calques
type: docs
weight: 150
url: /fr/net/travailler-avec-les-calques/
---

## **Créer un groupe de calques**
Un groupe de calques est composé d'un ou de plusieurs calques et il aide à organiser des calques similaires ou liés. En utilisant Aspose.PSD pour .NET, vous pouvez créer un groupe de calques. À cet effet, une nouvelle méthode [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) a été ajoutée dans la classe PsdImage pour ajouter le groupe de calques.

Les étapes pour créer des groupes de calques sont aussi simples que ci-dessous :

- Créez une instance d'une image en utilisant la classe PsdImage avec une largeur, une hauteur et des options d'image spécifiées.
- Créez un [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/layergroup) avec le nom de groupe et l'index spécifiés.
- Créez une instance de la classe Layer et attribuez-lui l'image PSD.
- Ajoutez le calque créé au groupe de calques en utilisant la méthode AddLayer exposée par la classe LayerGroup.
- Enregistrez les résultats.

Le code suivant vous montre comment créer un groupe de calques.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **Renommer un calque**
Vous pouvez utiliser un nom que vous souhaitez, mais la pratique typique est d'utiliser une description générale de l'objet ou de l'élément qui se trouve sur ce calque. Cet article montre comment vous pouvez changer le nom d'un calque en utilisant Aspose.PSD pour .NET. À cet effet, une nouvelle propriété [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/displayname) a été ajoutée dans la classe Layer pour afficher correctement un nom de calque. Il a été observé que lorsque Photoshop enregistre un nom de calque en utilisant la propriété [**Name**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/name), alors les caractères coréens sont stockés en tant que byte 63'?' en ASCII. Donc, si vous voulez afficher correctement un nom de calque, utilisez la propriété **DisplayName** car la propriété **Name** ne prend pas en charge les caractères coréens.

L'exemple de code suivant montre comment vous pouvez renommer un calque.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}

## **Prise en charge des calques liés**
La liaison des calques est similaire au regroupement des calques. Si vous liez deux calques ou plus, cela vous permettra de faire des changements spécifiques à ces calques liés. Par exemple, si vous appliquez des transformations à un calque, elles seront appliquées à tous les autres calques liés. Cet article montre comment obtenir et délier des calques liés en utilisant [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
