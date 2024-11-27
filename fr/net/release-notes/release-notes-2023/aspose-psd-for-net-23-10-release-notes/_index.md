---
title: Aspose.PSD pour .NET 23.10 - Notes de publication
type: docs
weight: 30
url: /fr/net/aspose-psd-pour-net-23-10-notes-de-publication/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication de [Aspose.PSD pour .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                | **Catégorie** |
|:------------|:------------------------------------------------------------------------|:--------|
| PSDNET-692 | Support de la direction du texte vertical | Fonctionnalité |
| PSDNET-1402 | Utiliser les paramètres de contour à partir de la ressource vstk dans le rendu de contour de forme | Fonctionnalité |
| PSDNET-1607 | Implémenter le rendu de la zone interne des formes de contour | Fonctionnalité |
| PSDNET-1644 | Ne pas redessiner un calque de forme s'il n'a pas été modifié | Fonctionnalité |
| PSDNET-1696 | [Format AI] Ajouter la prise en charge de la lecture de l'en-tête des fichiers AI basés sur PDF | Fonctionnalité |
| PSDNET-1560 | Diverses manières de définir la résolution d'un fichier Psd ne fonctionnent pas | Bug |
| PSDNET-1728 | FontSettings.SetFontsFolders ne fonctionne pas ou Aspose.PSD utilise une police incorrecte | Bug |
| PSDNET-1739 | Régression. Correction de l'exception de référence nulle soulevée lors de l'enregistrement de l'image Psd lorsqu'un calque de forme est présent | Bug |


## **Changements de l'API publique**

# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **APIs supprimées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Exemples d'utilisation :**

**PSDNET-692. Support de la direction du texte vertical**

{{< highlight csharp >}}
string fichierSource = "692_lt1.psd";
string fichierSortie = "692_output.png";
string dossierPolices = "692_Fonts";

var dossiersPolices = new List<string>(FontSettings.GetFontsFolders());
dossiersPolices.Add(dossierPolices);
FontSettings.SetFontsFolders(dossiersPolices.ToArray(), true);

using (PsdImage imagePsd = (PsdImage)Image.Load(fichierSource))
{
    imagePsd.Save(fichierSortie, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}