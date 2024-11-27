---
title: Aspose.PSD pour .NET 23.8 - Notes de version
type: docs
weight: 50
url: /fr/net/aspose-psd-pour-net-23-8-notes-de-version/
---

{{% alert color = "primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                                  | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Ajouter un nouveau type de déformation (Drapeau) | Fonctionnalité |
| PSDNET-1621 | Ajouter de nouveaux types de déformation : arc vers le haut, arc vers le bas, sphère | Fonctionnalité |
| PSDNET-1682 | Implémenter une nouvelle méthode PsdImage.AddPosterizeAdjustmentLayer pour ajouter un nouveau calque Posterize | Fonctionnalité |
| PSDNET-913  | Informations PSD perdues lors de l'ouverture et de la sauvegarde | Problème     |
| PSDNET-1352 | Échec du chargement de l'image | Problème     |
| PSDNET-1553 | Échec du chargement de l'image: Impossible de convertir l'objet de type UnknownStructure en type DescriptorStructure | Problème     |
| PSDNET-1631 | Le fichier modifié dans la bibliothèque tierce corrompt le fichier PSD mais peut être ouvert dans Photoshop | Problème     |


## **Changements d'API publics**
# **APIs ajoutées:**
- M : Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **APIs supprimées:**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-913. Informations PSD perdues lors de l'ouverture et de la sauvegarde**

{{< highlight csharp >}}
string source = "Fichier original.psd";
string outputPsd = "out_Fichier original.psd";
string outputPng = "out_Fichier original.png";

using (var psdImage = (PsdImage)Image.Load(source))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Échec du chargement de l'image**

{{< highlight csharp >}}
string fichierSource1 = "test_text.psd";
string fichierSource2 = "test_smart_object.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(fichierSource1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(fichierSource2))
{
}
{{< /highlight >}}

**PSDNET-1553. Échec du chargement de l'image: Impossible de convertir l'objet de type UnknownStructure en type DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Devrait charger correctement
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Le fichier modifié dans la bibliothèque tierce corrompt le fichier PSD mais peut être ouvert dans Photoshop**

{{< highlight csharp >}}
string fichierSource = "output.psd";
string fichierSortie = "export.png";

using (PsdImage img = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(fichierSortie, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Ajouter un nouveau type de déformation (Drapeau)**

{{< highlight csharp >}}
string fichierSource = "flag_warp.psd";
string fichierSortie = "flag_export.png";

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierSortie, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Ajouter de nouveaux types de déformation : arc vers le haut, arc vers le bas, sphère**

{{< highlight csharp >}}
string fichierArcHaut = "arc_upper_warp.psd";
string fichierArcBas = "arc_lower_warp.psd";
string fichierBosse =  "bulge_warp.psd";

string fichierSortieArcHaut = "ArcUpper_export.png";
string fichierSortieArcBas = "ArcLower_export.png";
string fichierSortieBosse = "Bulge_export.png";

using (var psdImage = (PsdImage)Image.Load(fichierArcHaut, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierSortieArcHaut, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(fichierArcBas, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierSortieArcBas, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(fichierBosse, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(fichierSortieBosse, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implémenter une nouvelle méthode PsdImage.AddPosterizeAdjustmentLayer pour ajouter un nouveau calque Posterize**

{{< highlight csharp >}}
string fichierSource = "zendeya.psd";
string fichierSortie = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(fichierSource))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(fichierSortie);
}

// Vérifier les modifications enregistrées
using (PsdImage image = (PsdImage)Image.Load(
    fichierSortie,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}
