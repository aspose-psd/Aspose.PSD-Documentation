---
title: Aspose.PSD pour .NET 22.5 - Notes de publication
type: docs
weight: 80
url: /fr/net/aspose-psd-pour-net-22-5-notes-de-release/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 22.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-952|Ajouter la propriété EffectType à l'interface ILayerEffect|Fonctionnalité|
|PSDNET-1146|Refactorisation de la classe ChannelData|Amélioration|
|PSDNET-657|Faire fonctionner la propriété d'opacité pour DropShadowEffect|Bogue|
|PSDNET-825|Dessin incorrect de la couche d'ajustement à travers la couche transparente dans un cas spécifique|Bogue|
|PSDNET-1168|Améliorer la méthode de Colorize. Coloriser en gris + définir la bonne couleur lorsque la saturation n'est pas à 100|Bogue|
|Article|[Comment exécuter Aspose.PSD dans Docker](https://docs.aspose.com/psd/net/how-to-run-aspose-psd-in-docker/)|Documentation|


## **Changements de l'API publique**
# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor(Aspose.PSD.FileFormats.Psd.CompressionMethod,System.Int32,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ILayerEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.InnerShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.DropShadowEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.EffectType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.OuterGlowEffect.EffectType
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.DropShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.OuterGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.PatternOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.GradientOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.ColorOverlay
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Satin
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerGlow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.InnerShadow
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.Stroke
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.LayerEffectsTypes.BevelEmboss


# **APIs supprimées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.ChannelInformation.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.Equals(System.Object)


## **Exemples d'utilisation :**

**PSDNET-657. Faire fonctionner la propriété d'opacité pour DropShadowEffect**

{{< highlight csharp >}}
string fichierEntree = "fichier_entree.psd";
string imageSortie20 = "image_sortie20.png";
string imageSortie200 = "image_sortie200.png";

using (PsdImage psdImage = (PsdImage)Image.Load(fichierEntree, new LoadOptions()))
{
    Layer coucheTravail = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = coucheTravail.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;

    // Exemple avec Opacité 20
    dropShadowEffect.Opacity = 20;
    psdImage.Save(imageSortie20, new PngOptions());

    // Exemple avec Opacité 200
    dropShadowEffect.Opacity = 200;
    psdImage.Save(imageSortie200, new PngOptions());
}
{{< /highlight >}}

**PSDNET-825. Dessin incorrect de la couche d'ajustement à travers la couche transparente dans un cas spécifique**

{{< highlight csharp >}}
string fichierSource = "entree_825.psd";
string sortiePng = "sortie_psdnet825.png";

using (var psdImage = (PsdImage)Image.Load(fichierSource))
{
    foreach (var element in psdImage.Layers)
    {
        element.IsVisible = false;
    }
    var couche = psdImage.Layers[3];
    psdImage.Layers[1].IsVisible = true;
    psdImage.Layers[3].IsVisible = true;
    psdImage.Layers[4].IsVisible = true;
    psdImage.Layers[7].IsVisible = true;

    var largeur = couche.Width;
    var hauteur = couche.Height;
    var limitesCouche = new Rectangle(couche.Left, couche.Top, largeur, hauteur);
    var limites = new Rectangle(0, 0, largeur, hauteur);
    var image = new PsdImage(limites.Width, limites.Height);

    image.SaveArgb32Pixels(limites, psdImage.LoadArgb32Pixels(limitesCouche));

    image.Save(sortiePng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-952. Ajouter la propriété EffectType à l'interface ILayerEffect**

{{< highlight csharp >}}
string fichierEntree = "fichier_entree.psd";
string sortieSans = "sortieSans.png";
string sortieAvec = "sortieAvec.png";

using (PsdImage psdImage = (PsdImage)Image.Load(fichierEntree, new LoadOptions()))
{
    psdImage.Save(sortieSans, new PngOptions());

    Layer coucheTravail = psdImage.Layers[1];

    DropShadowEffect dropShadowEffect = coucheTravail.BlendingOptions.AddDropShadow();
    dropShadowEffect.Distance = 0;
    dropShadowEffect.Size = 8;
    dropShadowEffect.Opacity = 20;

    foreach (ILayerEffect iEffet in coucheTravail.BlendingOptions.Effects)
    {
        if (iEffet.EffectType == LayerEffectsTypes.DropShadow)
        {
            // il a été attrapé
            psdImage.Save(sortieAvec, new PngOptions());
        }
    }
}
{{< /highlight >}}

**PSDNET-1168. Améliorer la méthode Colorize. Coloriser en gris + définir la bonne couleur lorsque la saturation n'est pas à 100**

{{< highlight csharp >}}
string fichierSrc = "Colorize.psd";            
string sortieSimple = "sortie_simple.png";
string sortieColorize = "sortie_colorize.png";

using (var psdImage = (PsdImage)Image.Load(fichierSrc))
{
    // Image sans propriété Colorize
    psdImage.Save(sortieSimple, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
    
    // Définir la propriété Colorize
    foreach (Layer couche in psdImage.Layers)
    {
        if (couche is HueSaturationLayer)
        {
            HueSaturationLayer coucheTeinteSaturation = (HueSaturationLayer)couche;
            coucheTeinteSaturation.Colorize = true;
            break;
        }
    }
    
    // Image avec propriété Colorize
    psdImage.Save(sortieColorize, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
