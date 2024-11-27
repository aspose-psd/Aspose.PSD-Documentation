---
title: Notes de version Aspose.PSD pour .NET 19.4
type: docs
weight: 90
url: /fr/net/aspose-psd-pour-dotnet-19-4-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour Aspose.PSD pour .NET 19.4

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-87|Fonctionnalité pour charger des fichiers d'images JPEG/PNG/etc dans PsdImage sans chargement direct (ce qui n'est pas pris en charge dans Aspose.PSD)|Fonctionnalité|
|PSDNET-120|Prise en charge du mode couleur RGB avec 16 bits/canal (64 bits par couleur)|Fonctionnalité|
|PSDNET-108|Prise en charge des masques vectoriels de calque et de la rotation personnalisée des calques de texte|Fonctionnalité|
|PSDNET-99|Tous les caractères asiatiques ne sont pas rendus correctement|Bogue|
|PSDNET-116|Les symboles \r\n sont interprétés comme un double saut de ligne, ce qui est incorrect|Bogue|
|PSDNET-117|Si TextLayer est mis à jour avec une chaîne contenant des sauts de ligne, le fichier PSD devient illisible|Bogue|
|PSDNET-118|Si TextLayer est mis à jour avec une chaîne contenant des symboles de tabulation, le traitement échoue avec une exception|Bogue|

## **Changements d'API publique**
# **APIs ajoutées:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
# **APIs supprimées:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
...
...

## **Exemples d'utilisation:**
**PSDNET-87. Fonctionnalité pour charger des fichiers d'images JPEG/PNG/etc dans PsdImage sans chargement direct (ce qui n'est pas pris en charge dans Aspose.PSD)**

{{< highlight java >}}

 string filePath = "PsdExample.psd";

string outputFilePath = "PsdResult.psd";

using(var image = new PsdImage(200, 200)) {

 using(var im = Image.Load(filePath)) {

  Layer layer = null;

  try {

   layer = new Layer((RasterImage) im);

   image.AddLayer(layer);

  } catch (Exception e) {

   if (layer != null) {

    layer.Dispose();

   }

   throw;

  }

 }

 image.Save(outputFilePath);

}  

{{< /highlight >}}
...
...