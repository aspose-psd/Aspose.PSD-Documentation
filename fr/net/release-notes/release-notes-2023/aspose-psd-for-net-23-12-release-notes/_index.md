---
title: Aspose.PSD pour .NET 23.12 - Notes de publication
type: docs
weight: 10
url: /fr/net/aspose-psd-for-net-23-12-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 23.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                               | **Catégorie** |
|:------------|:----------------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1679 | [Format AI] Ajouter le support du rendu d'image matricielle dans la nouvelle version de AI                |   Fonctionnalité   |
| PSDNET-1454 | Gérer le bruit de type Gradient dans GdflResource                                                       |   Fonctionnalité   |
| PSDNET-1827 | Erreur "Référence d'objet non définie à une instance d'un objet." lors de la sauvegarde de la couche de texte après la mise à jour         |     Bug     |
| PSDNET-1776 | Corriger le chargement manuel des polices sur MacOS en utilisant System.Drawing.Common et Aspose.Drawing.                  |     Bug     |
| PSDNET-1536 | AllowWarpRepaint dans les PsdLoadOptions entraîne l'exception                                         |     Bug     |
| PSDNET-1714 | [Format AI] Implémenter le traitement des flux de référence croisée                                     | Amélioration |
| PSDNET-1834 | Le contrôle de licence pour VectorPathDataResource fonctionne de manière incorrecte                     | Amélioration |
| PSDNET-770  | Ouvrir n'importe quel fichier image en tant qu'objet intégré intelligent dans l'image PSD             | Amélioration |
| PSDNET-1864 | Système de licence du plugin Aspose.PSD                                                                    | Amélioration |


## **Changements dans l'API publique**
# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.#ctor(System.IO.Stream)
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.RGB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.HSB
- F:Aspose.PSD.FileFormats.Psd.Layers.Gradient.NoiseColorModel.LAB
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.RndNumberSeed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ShowTransparency
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.UseVectorColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Roughness
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.ColorModel
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MinimumColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.MaximumColor
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.FillType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Color
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Dither
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Reverse
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Angle
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.ColorPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.TransparencyPoints
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.BaseGradientFillSettings.GradientMode
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Interpolation
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.GradientMode
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.#ctor
- T:Aspose.PSD.CustomFontHandler.CustomFontData
- M:Aspose.PSD.Metered.GetProductName
- M:Aspose.PSD.Metered.IsMeteredLicensed
- T:Aspose.PSD.PluginLicenseException
- M:Aspose.PSD.PluginLicenseException.#ctor
- M:Aspose.PSD.Metered.Equals(System.Object)

# **APIs supprimées :**
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- M:Aspose.PSD.Metered.Equals(System.Object)


## **Exemples d'utilisation :**

**PSDNET-1679. [AI Format] Ajouter le support du rendu d'image matricielle dans la nouvelle version de AI**

{{< highlight csharp >}}
            string fichierSource = Path.Combine(dossierBase, "raster.ai");
            string fichierSortie = Path.Combine(dossierSortie, "raster_output.png");

            using (AiImage image = (AiImage)Image.Load(fichierSource))
            {
                image.Save(fichierSortie, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1454. Gérer le bruit de type Gradient dans GdflResource**

{{< highlight csharp >}}
            string fichierSource = "Gradient-Fill.psd";
            string fichierDest = "Gradient-Fill-out.psd";

            using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions()))
            {
                Layer layer = image.Layers[1];

                foreach (LayerResource resource in layer.Resources)
                {
                    GdFlResource gdFlResource = resource as GdFlResource;

                    if (gdFlResource != null)
                    {
                        gdFlResource.Scale = 90;
                        gdFlResource.Angle = 30;
                        gdFlResource.Dither = false;
                        gdFlResource.AlignWithLayer = true;
                        gdFlResource.Reverse = false;

                        break;
                    }
                }

                image.Save(fichierDest, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-1827. Erreur "Référence d'objet non définie à une instance d'un objet." lors de la sauvegarde de la couche de texte après la mise à jour**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "input_1827.psd");
string fichierSortie = Path.Combine(dossierSortie, "out_1827.psd");

using (var psdImage = (PsdImage)Image.Load(fichierSource))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.TextData.UpdateLayerData();
        }
    }

    // Il ne devrait pas y avoir d'erreur ici
    psdImage.Save(fichierSortie);
}
{{< /highlight >}}

**PSDNET-1536. AllowWarpRepaint dans les PsdLoadOptions entraîne l'exception**

{{< highlight csharp >}}
            string fichierSource = @"SizeChart-4 Colors.psd";
            string fichierSortie = @"SizeChart-4 Colors.png";

            using (var psdImage = (PsdImage)Aspose.PSD.Image.Load(fichierSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true })) 
			{ 
				psdImage.Save(fichierSortie + "_original.png", new PngOptions()
				{
					ColorType = PngColorType.TruecolorWithAlpha,
					Progressive = true,
					CompressionLevel = 9
				});
			}
{{< /highlight >}}

**PSDNET-1834. Le contrôle de licence pour VectorPathDataResource fonctionne de manière incorrecte**

{{< highlight csharp >}}
 using (PsdImage im = (PsdImage)Image.Load(DifferentLayerMasks.psd))
 {
     im.Save(complexFiles[i] + "out" + "output.psd");
     im.Save(complexFiles[i] + "out" + "output.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
 }
{{< /highlight >}}

**PSDNET-770. Ouvrir n'importe quel fichier image en tant qu'objet intégré intelligent dans l'image PSD**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "empty.psd");

string fichierAjoutArbre = Path.Combine(dossierBase, "tree.psd");
string fichierAjoutGelee = Path.Combine(dossierBase, "frost.png");

string fichierSortieArbre = Path.Combine(dossierSortie, "tree_export.psd");
string fichierSortieGelee = Path.Combine(dossierSortie, "frost_export.psd");

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(fichierAjoutArbre, FileMode.Open))
    {
        using (SmartObjectLayer smartLayer = new SmartObjectLayer(stream))
        {
            psdImage.AddLayer(smartLayer);

            psdImage.Save(fichierSortieArbre, new PsdOptions());                        
        }
    }
}

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    using (Stream stream = new FileStream(fichierAjoutGelee, FileMode.Open))
    {
        using (SmartObjectLayer smartLayer = new SmartObjectLayer(stream))
        {
            psdImage.AddLayer(smartLayer);

            psdImage.Save(fichierSortieGelee, new PsdOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1864. Système de licence du plugin Aspose.PSD**

{{< highlight csharp >}}            
    var metered = new Metered();
    metered.SetMeteredKey(pluginPublic, pluginPrivate);
			
	// Manipulation spécifique au plugin
{{< /highlight >}}