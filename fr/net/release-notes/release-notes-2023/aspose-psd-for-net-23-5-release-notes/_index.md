---
title: Aspose.PSD pour .NET 23.5 - Notes de publication
type: docs
weight: 80
url: /fr/net/aspose-psd-pour-net-23-5-notes-de-publication/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 23.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}


| **Clé**     | **Résumé**                                                                | **Catégorie** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-343  | Prise en charge du filtre : Aiguiser -> Aiguiser                            | Fonction     |
| PSDNET-1179 | Enregistrement du fichier PSD (RGB/8 bits ou RGB/16 bits) sans calques en 32 bits | Fonction     |
| PSDNET-1408 | Implémenter la gestion des objets de tracé des ressources vsms ou vmsk pour ShapeLayer | Fonction     |
| PSDNET-1508 | Ajouter l'influence des points de grille les uns sur les autres           | Fonction     |


## **Changements de l'API publique**
# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LrXxResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.IsDisabled
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.PathOperations
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.#ctor(Aspose.PSD.FileFormats.Core.VectorPaths.LengthRecord,Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.IsClosed
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ShapeIndex
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.SetItems(Aspose.PSD.FileFormats.Core.VectorPaths.BezierKnotRecord[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PathShape.ToVectorPathRecords
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsFillStartsWithAllPixels
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.IsInverted
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.GetItems
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.SetItems(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IPathShape[])
- T:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.DescriptorStructure)
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterId
- F:Aspose.PSD.FileFormats.Psd.Layers.SmartFilters.SharpenSmartFilter.FilterType


# **APIs supprimées :**
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorPathRecordFactory.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr16Resource.Save(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.#ctor(System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Layers
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Signature
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lr32Resource.Save(Aspose.PSD.StreamContainer,System.Int32)


## **Exemples d'utilisation :**

**PSDNET-343. Prise en charge du filtre : Aiguiser -> Aiguiser**

{{< highlight csharp >}}
string fichierSource = "aiguiser_source.psd";
string psdSortie = "aiguiser_sortie.psd";
string pngSortie = "aiguiser_sortie.png";

void AssertAreEqual(object attendu, object reel)
{
    if (!object.Equals(attendu, reel))
    {
        throw new Exception("Les objets ne sont pas égaux.");
    }
}

using (var image = (PsdImage)Image.Load(fichierSource))
{
    SmartObjectLayer calqueObjetIntelligent = (SmartObjectLayer)image.Layers[1];

    // modifier les filtres intelligents
    SharpenSmartFilter aiguiser = (SharpenSmartFilter)calqueObjetIntelligent.SmartFilters.Filters[0];

    // vérifier les valeurs du filtre
    AssertAreEqual(BlendMode.Normal, aiguiser.BlendMode);
    AssertAreEqual(100d, aiguiser.Opacity);
    AssertAreEqual(true, aiguiser.IsEnabled);

    // mettre à jour les valeurs du filtre
    aiguiser.BlendMode = BlendMode.Divide;
    aiguiser.Opacity = 75;
    aiguiser.IsEnabled = false;

    // ajouter de nouveaux éléments de filtre
    var filtres = new List<SmartFilter>(calqueObjetIntelligent.SmartFilters.Filters);
    filtres.Add(new SharpenSmartFilter());
    calqueObjetIntelligent.SmartFilters.Filters = filtres.ToArray();

    // appliquer les modifications
    calqueObjetIntelligent.SmartFilters.UpdateResourceValues();
    calqueObjetIntelligent.UpdateModifiedContent();

    image.Save(psdSortie);
    image.Save(pngSortie, new PngOptions());
}
{{< /highlight >}}


**PSDNET-1179. Enregistrement du fichier PSD (RGB/8 bits ou RGB/16 bits) sans calques en 32 bits**

{{< highlight csharp >}}
string fichierEntree = "input_8bit_rle.psd";
string fichierPsdSortie = "output_32bit.psd";
string fichierImageSortie32 = "output_de_32bit.png";

using (PsdImage imageSrc = (PsdImage)Image.Load(fichierEntree))
{
    PsdOptions optionsTotales = new PsdOptions() { ChannelBitsCount = 32, ColorMode = ColorModes.Rgb };
    imageSrc.Save(fichierPsdSortie, optionsTotales);

    using (var image32 = Image.Load(fichierPsdSortie))
    {
        image32.Save(fichierImageSortie32, new PngOptions() { ColorType = PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
    }
}
{{< /highlight >}}


**PSDNET-1408. Implémenter la gestion des objets de tracé des ressources vsms ou vmsk pour ShapeLayer**

{{< highlight csharp >}}
string fichierSrc = "ShapeLayerTest.psd";
string fichierSortie = "ShapeLayerTest-out.psd";

using (PsdImage image = (PsdImage)Image.Load(fichierSrc, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer calqueForme = image.Layers[1];
    VectorPathDataResource ressourceDonneesChemin = (VectorPathDataResource)calqueForme.Resources[1];

    bool estRempliCommenceAvecTousLesPixels;
    List<IPathShape> formes = ObtenirFormesDeLaRessource(ressourceDonneesChemin, out estRempliCommenceAvecTousLesPixels);

    // Supprimer une forme
    formes.RemoveAt(1);

    // Enregistrer les données modifiées dans la ressource
    List<VectorPathRecord> chemin = new List<VectorPathRecord>();
    chemin.Add(new PathFillRuleRecord(null));
    chemin.Add(new InitialFillRuleRecord(estRempliCommenceAvecTousLesPixels));

    for (ushort i = 0; i < formes.Count; i++)
    {
        PathShape forme = (PathShape)formes[i];
        forme.ShapeIndex = i;
        chemin.AddRange(forme.ToVectorPathRecords());
    }

    ressourceDonneesChemin.Paths = chemin.ToArray();

    image.Save(fichierSortie);
}

// Vérifier les valeurs modifiées dans le fichier enregistré
using (PsdImage image = (PsdImage)Image.Load(fichierSortie, new PsdLoadOptions { LoadEffectsResource = true }))
{
    Layer calqueForme = image.Layers[1];
    VectorPathDataResource ressourceDonneesChemin = (VectorPathDataResource)calqueForme.Resources[1];

    bool estRempliCommenceAvecTousLesPixels;
    List<IPathShape> formes = ObtenirFormesDeLaRessource(ressourceDonneesChemin, out estRempliCommenceAvecTousLesPixels);

    // Le fichier enregistré devrait avoir 1 forme
    AssertAreEqual(1, formes.Count);
}

void AssertAreEqual(object attendu, object reel, string message = null)
{
    if (!object.Equals(attendu, reel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}

List<IPathShape> ObtenirFormesDeLaRessource(VectorPathDataResource ressourceDonneesChemin, out bool estRempliCommenceAvecTousLesPixels)
{
    List<IPathShape> formes = new List<IPathShape>();
    LengthRecord enregistrementLongueur = null;
    estRempliCommenceAvecTousLesPixels = false;
    List<BezierKnotRecord> enregistrementsNoeudBezier = new List<BezierKnotRecord>();

    foreach (var enregistrementChemin in ressourceDonneesChemin.Paths)
    {
        if (enregistrementChemin is LengthRecord)
        {
            if (enregistrementsNoeudBezier.Count > 0)
            {
                formes.Add(new PathShape(enregistrementLongueur, enregistrementsNoeudBezier.ToArray()));
                enregistrementLongueur = null;
                enregistrementsNoeudBezier.Clear();
            }

            enregistrementLongueur = (LengthRecord)enregistrementChemin;
        }
        else if (enregistrementChemin is BezierKnotRecord)
        {
            enregistrementsNoeudBezier.Add((BezierKnotRecord)enregistrementChemin);
        }
        else if (enregistrementChemin is InitialFillRuleRecord)
        {
            InitialFillRuleRecord enregistrementRegleRemplissageInitial = (InitialFillRuleRecord)enregistrementChemin;
            estRempliCommenceAvecTousLesPixels = enregistrementRegleRemplissageInitial.IsFillStartsWithAllPixels;
        }
    }

    if (enregistrementsNoeudBezier.Count > 0)
    {
        formes.Add(new PathShape(enregistrementLongueur, enregistrementsNoeudBezier.ToArray()));
        enregistrementLongueur = null;
        enregistrementsNoeudBezier.Clear();
    }

    return formes;
}
{{< /highlight >}}


**PSDNET-1508. Ajouter l'influence des points de grille les uns sur les autres**

{{< highlight csharp >}}
string fichierSource = "Bottom_Right.psd";
string fichierSortie = "sortie.png";

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions { AllowWarpRepaint = true }))
{
    image.Save(fichierSortie, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha});
}
{{< /highlight >}}