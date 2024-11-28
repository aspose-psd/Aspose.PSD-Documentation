---
title: Aspose.PSD pour .NET 23.11 - Notes de version
type: docs
weight: 20
url: /fr/net/aspose-psd-pour-net-23-11-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                            | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412  | Support de LMskResource                                                                                | Fonctionnalité |
| PSDNET-1669 | [Format AI] Ajout de la capacité de rendre un fichier AI basé sur PDF avec Aspose.PSD                   | Fonctionnalité |
| PSDNET-1702 | [Format AI] Ajout de la prise en charge de l'opérateur PostScript "cm"                                   | Fonctionnalité |
| PSDNET-1752 | Ajout de nouveaux types de déformations : Wave, Shell Up, Shell Down                                     | Fonctionnalité |
| PSDNET-1797 | Ajout de la prise en charge de la déformation verticale                                                 | Fonctionnalité |
| PSDNET-1756 | System.ArgumentNullException : 'La valeur ne peut pas être nulle. (Paramètre 'key')' lors de l'appel de TextLayer.GetFonts() | Anomalie |


## **Changements de l'API publique**
# **APIs ajoutées:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale


# **APIs supprimées:**
- Aucune


## **Exemples d'utilisation:**
**PSDNET-412. Support de LMskResource**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierDeBase, "fichierSource.psd");
string outputPsd = Path.Combine(dossierSortie, "fichierSource_sortie.psd");

void AssertAreEqual(object attendu, object actuel)
{
    if (!object.Equals(attendu, actuel))
    {
        throw new Exception("Les objets ne sont pas égaux.");
    }
}

// Chargement de l'image 16 bits.
using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    // Recherche de LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in image.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Vérification des propriétés de LmskResource.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Modification des propriétés de LmskResource.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Enregistrer l'image.
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1669. [Format AI] Ajouter la capacité de rendre un fichier AI basé sur PDF avec Aspose.PSD**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierDeBase, "ai_un.ai");
string outputPng = Path.Combine(dossierSortie, "ai_un_sortie.png");

// Chargement de l'image AI basée sur PDF.
using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    // Enregistrer l'image AI en tant qu'image PNG.
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [Format AI] Ajouter la prise en charge de l'opérateur PostScript "cm"**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierDeBase, "ai_deux.ai");
string outputPng = Path.Combine(dossierSortie, "ai_deux_sortie.png");

// Chargement de l'image AI.
using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    // Enregistrer l'image AI en tant qu'image PNG.
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Ajouter de nouveaux types de déformations : Wave, Shell Up, Shell Down**

{{< highlight csharp >}}
var optionsChargement = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var optionsEnregistrement = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string fichierPoisson = Path.Combine(dossierDeBase, "1752_deformation_poisson.psd");
string fichierLevée = Path.Combine(dossierDeBase, "1752_deformation_levee.psd");
string fichierVague = Path.Combine(dossierDeBase, "1752_deformation_vague.psd");

string fichierSortiePoisson = Path.Combine(dossierSortie, "1752_sortie_poisson.png");
string fichierSortieLevée = Path.Combine(dossierSortie, "1752_sortie_levee.png");
string fichierSortieVague = Path.Combine(dossierSortie, "1752_sortie_vague.png");

using (var imagePoisson = (PsdImage)Image.Load(fichierPoisson, optionsChargement))
{
    imagePoisson.Save(fichierSortiePoisson, optionsEnregistrement);
}

using (var imageLevée = (PsdImage)Image.Load(fichierLevée, optionsChargement))
{
    imageLevée.Save(fichierSortieLevée, optionsEnregistrement);
}

using (var imageVague = (PsdImage)Image.Load(fichierVague, optionsChargement))
{
    imageVague.Save(fichierSortieVague, optionsEnregistrement);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException : 'La valeur ne peut pas être nulle. (Paramètre 'key')' lors de l'appel de TextLayer.GetFonts()**

{{< highlight csharp >}}
string src = Path.Combine(dossierDeBase, "SimpleText.psd");

FontSettings.RemoveFontCacheFile();

using (var psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Ajouter la prise en charge de la déformation verticale**

{{< highlight csharp >}}
var optionsChargement = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var optionsEnregistrement = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string fichierArcInférieur = Path.Combine(dossierDeBase, "1797_deformation_arc_inferieur_v.psd");
string fichierArcSupérieur = Path.Combine(dossierDeBase, "1797_deformation_arc_superieur_v.psd");
string fichierArche = Path.Combine(dossierDeBase, "1797_deformation_arche_v.psd");
string fichierBosse = Path.Combine(dossierDeBase, "1797_deformation_bosse_v.psd");
string fichierDrapeau = Path.Combine(dossierDeBase, "1797_deformation_drapeau_v.psd");
string fichierPoisson = Path.Combine(dossierDeBase, "1797_deformation_poisson_v.psd");
string fichierLevée = Path.Combine(dossierDeBase, "1797_sortie_levee_v.psd");
string fichierVague = Path.Combine(dossierDeBase, "1797_sortie_vague_v.psd");

string fichierSortieArcInférieur = Path.Combine(dossierSortie, "1797_deformation_arc_inférieur_v.png");
string fichierSortieArcSupérieur = Path.Combine(dossierSortie, "1797_deformation_arc_superieur_v.png");
string fichierSortieArche = Path.Combine(dossierSortie, "1797_deformation_arche_v.png");
string fichierSortieBosse = Path.Combine(dossierSortie, "1797_deformation_bosse_v.png");
string fichierSortieDrapeau = Path.Combine(dossierSortie, "1797_deformation_drapeau_v.png");
string fichierSortiePoisson = Path.Combine(dossierSortie, "1797_sortie_poisson_v.png");
string fichierSortieLevée = Path.Combine(dossierSortie, "1797_sortie_levee_v.png");
string fichierSortieVague = Path.Combine(dossierSortie, "1797_sortie_vague_v.png");

using (var psdImage = (PsdImage)Image.Load(fichierArcInférieur, optionsChargement)) { psdImage.Save(fichierSortieArcInférieur, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierArcSupérieur, optionsChargement)) { psdImage.Save(fichierSortieArcSupérieur, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierArche, optionsChargement)) { psdImage.Save(fichierSortieArche, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierBosse, optionsChargement)) { psdImage.Save(fichierSortieBosse, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierDrapeau, optionsChargement)) { psdImage.Save(fichierSortieDrapeau, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierPoisson, optionsChargement)) { psdImage.Save(fichierSortiePoisson, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierLevée, optionsChargement)) { psdImage.Save(fichierSortieLevée, optionsEnregistrement); }
using (var psdImage = (PsdImage)Image.Load(fichierVague, optionsChargement)) { psdImage.Save(fichierSortieVague, optionsEnregistrement); }
{{< /highlight >}}
