---
title: Modification des masques de calque raster dans un fichier PSD via une API
type: docs
weight: 20
url: /fr/modification-des-masques-de-calque-raster-dans-un-fichier-psd-via-api/
---

## **Aperçu**
**Pour automatiser la modification du format PSD et changer un fichier PSD sans Adobe® Photoshop®, vous pouvez utiliser l'API Aspose.PSD fournie ci-dessous. Il existe des extraits de code C# et .NET qui peuvent vous aider à modifier des fichiers PSD.**

En utilisant les masques de calque et de vecteur PSD, nous pouvons masquer et afficher des pixels de calque sans les supprimer définitivement. Les masques raster sont également appelés masque de calque ou masque utilisateur. L'accès aux masques raster et de vecteur dans Aspose.PSD est fourni via la propriété de calque [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) qui peut être une instance des classes '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' et '[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' qui sont des classes enfant de la classe abstraite 'LayerMaskData'. Si un calque possède à la fois des masques raster et de vecteur, alors une instance de [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull) est fournie. Si un calque possède uniquement un masque raster ou un masque de vecteur, alors une instance de [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort) est fournie. Si la propriété LayerMaskData est nulle, alors le calque n'a aucun masque ou seulement un masque de vecteur désactivé.


|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>Un masque raster et un masque de vecteur désactivé LayerMaskDataShort</p><p>Un masque raster désactivé LayerMaskDataShort</p><p>Un masque raster et un masque de vecteur LayerMaskDataFull</p><p>Un masque raster LayerMaskDataShort</p><p>Un masque de vecteur LayerMaskDataShort</p><p>Un masque de vecteur désactivé null (Mais la ressource de vecteur est présente)</p>|
| :- | :- |
## **Comment obtenir un masque de calque raster dans le fichier PSD ?**
Tout d'abord, nous devons savoir si un calque possède à la fois des masques de vecteur et de calque :

L'exemple de code fourni ci-dessous montre comment obtenir un masque de calque raster

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

Sinon, le type de la propriété de calque LayerMaskData est LayerMaskDataShort. Dans ce cas, vérifions si le calque possède uniquement un masque raster en vérifiant la propriété Flags. Il ne doit pas contenir le drapeau [LayerMaskFlags](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskflags).**UserMaskFromRenderingOtherData**, sinon le masque est une cache de masque de vecteur.

Extrait de code pour obtenir le masque :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

Si vous avez besoin d'**extraire un masque raster** en tant que LayerMaskDataShort (pour de futures manipulations) même lorsque les deux masques sont présents, le LayerMaskDataFull doit être extrait et converti en LayerMaskDataShort. Le code suivant peut être utilisé pour les deux cas :

Extraction d'un masque raster du PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **Comment vérifier si un calque dans le fichier PSD possède un masque raster ?**
Le code C# suivant peut vous aider à vérifier si un calque possèder un masque raster :

Comment savoir si un masque raster est appliqué à un [calque PSD](/psd/fr/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **Comment supprimer / ajouter / mettre à jour un masque de calque raster dans le fichier PSD ?**
Supprimer / ajouter / mettre à jour simplement LayerMaskData n'est pas suffisant pour une sauvegarde correcte car les canaux ne sont pas mis à jour ; bien que cela puisse fournir un rendu correct. Cela ne modifie pas les canaux de masque :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

Nous devrions utiliser la méthode AddLayerMask de calque pour supprimer / ajouter / mettre à jour.

Cela ajoute / met à jour à la fois le masque et les canaux :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

Cela supprime à la fois le masque et les canaux :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **Suppression d'un masque de calque raster dans l'image PSD**
Tout d'abord, nous vérifions si le masque est au format court et s'il ne s'agit pas d'un vecteur, nous pouvons simplement appeler la méthode AddLayerMask avec null pour supprimer le masque raster. Mais s'il est au format complet, nous devons le convertir en un format court laissant ainsi seulement le masque de vecteur. Pour supprimer un masque de calque, ce fragment de code C# .NET peut être utilisé :

Fragment de code sur la suppression du masque de calque du fichier PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **Mise à jour d'un masque de calque raster dans l'image PSD**
C'est simple : si le masque est au format court, nous devons changer ImageData et MaskRectangle si nécessaire, sinon [UserMaskData ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskdata)et [UserMaskRectangle ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull/properties/usermaskrectangle)doivent être changés. Le fragment de code C# .NET suivant peut être utilisé pour mettre à jour un masque de calque :

Mettre à jour le masque de calque PSD avec C#

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

Voici un exemple d'actions possibles qui modifient un masque raster. Celui-ci inverse un masque utilisateur de calque :

Mettre à jour le masque de calque PSD avec C#

{{< gist "aspose-com-gists" "8a4c9ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **Mise à jour d'un masque de vecteur dans le fichier PSD lorsque qu'un masque de calque raster est présent**
Il est supposé que l'utilisateur a déjà modifié une ressource de chemin de vecteur. Ensuite, il peut mettre à jour le masque vectoriel simplement en appelant la méthode de calque [AddLayerMask ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask) :

Mettre à jour le [Masque vectoriel de calque PSD ](/psd/fr/net/layer-vector-mask/)avec C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **Ajout d'un masque de calque raster dans le fichier PSD**
Si un calque n'a pas de masque, nous pouvons ajouter le masque raster donné simplement en appelant la méthode de calque AddLayerMask.

Si le masque n'a pas le drapeau [UserMaskFromRenderingOtherData** ](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags), cela signifie qu'il a déjà un masque raster et nous devons le mettre à jour comme décrit ci-dessus. Sinon, si ce masque est au format court, nous le convertissons en le format complet. Sinon, nous l'utilisons tel quel. Puis mettons à jour UserMaskData, UserMaskRectangle, et d'autres propriétés avec les propriétés de masque données. Le fragment de code C# .NET suivant peut être utilisé pour ajouter (mettre à jour) un masque de calque :

Ajouter un nouveau masque de calque au PSD

{{< gist "aspose-com-gists" "8a9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **Comment vérifier si un masque de calque est activé ?**
Pour connaître l'état d'activation d'un masque de calque, nous pouvons vérifier l'état du drapeau LayerMaskFlags.Disabled dans la propriété Flags pour LayerMaskDataShort ou dans RealFlags pour LayerMaskDataFull. Le fragment de code C# .NET suivant peut être utilisé pour obtenir l'état d'activation d'un masque de calque :

Vérifier si un masque est activé :

{{< gist "aspose-com-gists" "8a4cdcv7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-13.cs" >}}
## **Comment activer ou désactiver un masque de calque raster ?**
Pour activer ou désactiver un masque de calque raster, nous pouvons changer l'état du drapeau LayerMaskFlags.Disabled dans la propriété Flags pour LayerMaskDataShort ou dans RealFlags pour LayerMaskDataFull. Le fragment de code C# .NET suivant peut être utilisé pour changer l'état d'activation d'un masque de calque :

Activer ou désactiver le masque de calque raster :

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-14.cs" >}}
