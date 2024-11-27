---
title: Aspose.PSD pour .NET 24.6 - Notes de version
type: docs
weight: 70
url: /fr/net/aspose-psd-pour-net-24-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 24.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                         | **Catégorie** |
|:------------|:------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Implémenter le support de la couche de carte de dégradé                                                                               | Fonctionnalité      |
| PSDNET-1670 | [Format AI] Ajouter le support de la métadonnée XPacket au format AI                                                                               | Fonctionnalité      |
| PSDNET-1831 | Implémenter les types de torsion Inflate, Squeeze et Twist                                                                               | Fonctionnalité      |
| PSDNET-1653 | Les modes Rvb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux dans le fichier avec des calques de planche d'art                                                                               | Problème      |
| PSDNET-1775 | La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique                                                                               | Problème      |
| PSDNET-2052 | L'image étendue sur la toile est rognée après l'enregistrement. Les données sont perdues mais l'aperçu est correct                                                                               | Problème      |

## **Changements d'API publique**
# **APIs ajoutées:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-1450. Implémenter le support de la couche de carte de dégradé**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "gradient_map_src.psd");
string fichierSortie = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(fichierSource))
{
    // Ajouter une couche d'ajustement de carte de dégradé.
    GradientMapLayer couche = im.AddGradientMapAdjustmentLayer();
    couche.GradientSettings.Reverse = true;

    im.Save(fichierSortie);
}

// Vérifier les changements enregistrés
using (PsdImage im = (PsdImage)Image.Load(fichierSortie))
{
    GradientMapLayer coucheCarteDeGradient = im.Layers[1] as GradientMapLayer;
    GradientFillSettings réglagesGradient = (GradientFillSettings)coucheCarteDeGradient.GradientSettings;

    AssertAreEqual(0.0, réglagesGradient.Angle);
    AssertAreEqual((short)4096, réglagesGradient.Interpolation);
    AssertAreEqual(true, réglagesGradient.Reverse);
    AssertAreEqual(false, réglagesGradient.AlignWithLayer);
    AssertAreEqual(false, réglagesGradient.Dither);
    AssertAreEqual(GradientType.Linear, réglagesGradient.GradientType);
    AssertAreEqual(100, réglagesGradient.Scale);
    AssertAreEqual(0.0, réglagesGradient.HorizontalOffset);
    AssertAreEqual(0.0, réglagesGradient.VerticalOffset);
    AssertAreEqual("Personnalisé", réglagesGradient.GradientName);
}

void AssertAreEqual(object attendu, object réel, string message = null)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [Format AI] Ajouter le support de la métadonnée XPacket au format AI**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object attendu, object réel)
{
    if (!object.Equals(attendu, réel))
    {
        throw new Exception("Les objets ne sont pas égaux.");
    }
}

void AssertIsNotNull(object objetTest)
{
    if (objetTest == null)
    {
        throw new Exception("Les objets de test sont nuls.");
    }
}

string cléOutilCréation = ":OutilCréation";
string cléNPages = "xmpTPg:NPages";
string cléUnité = "stDim:unit";
string cléHauteur = "stDim:h";
string cléLargeur = "stDim:w";

string outilCréationAttendu = "Adobe Illustrator CC 22.1 (Windows)";
string nPagesAttendu = "1";
string unitéAttendue = "Pixels";
double hauteurAttendue = 768;
double largeurAttendue = 1366;

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    // Les métadonnées Xmp ont été ajoutées.
    var métadonnéesXmp = image.XmpData;

    AssertIsNotNull(métadonnéesXmp);

    // Maintenant, nous pouvons accéder aux paquets Xmp des fichiers AI.
    var packageBasique = métadonnéesXmp.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var package = métadonnéesXmp.Packages[4];

    // Et nous avons accès au contenu de ces paquets.
    var outilCréation = packageBasique[cléOutilCréation].ToString();
    var nPages = package[cléNPages];
    var unité = package[cléUnité];
    var hauteur = double.Parse(package[cléHauteur].ToString(), CultureInfo.InvariantCulture);
    var largeur = double.Parse(package[cléLargeur].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(outilCréation, outilCréationAttendu);
    AssertAreEqual(nPages, nPagesAttendu);
    AssertAreEqual(unité, unitéAttendue);
    AssertAreEqual(hauteur, hauteurAttendue);
    AssertAreEqual(largeur, largeurAttendue);
}
{{< /highlight >}}

**PSDNET-1831. Implémenter les types de torsion Inflate, Squeeze et Twist**

{{< highlight csharp >}}
string[] fichiers = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string préfixe in fichiers)
{
    string fichierSource = Path.Combine(baseFolder, préfixe + ".psd");
    string fichierSortie = Path.Combine(outputFolder, préfixe + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(fichierSortie, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Les modes Rvb et Lab ne peuvent pas contenir moins de 3 canaux et plus de 4 canaux dans le fichier avec des calques de planche d'art**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "Rgb5Channels.psb");
string fichierSortie = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(fichierSource))
{
    // Il ne devrait pas y avoir d'exception ici
    image.Save(fichierSortie);
}
{{< /highlight >}}

**PSDNET-1775. La zone de traitement supérieure doit être positive. (Paramètre 'areaToProcess') lors du traitement d'un fichier spécifique**

{{< highlight csharp >}}
string fichierSource = @"BANNERS_2_Intel-Gamer_psak.psd";
string fichierSortie = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions optionsChargement = new PsdLoadOptions();
optionsChargement.LoadEffectsResource = true;
optionsChargement.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(fichierSource, optionsChargement))
{
    image.Save(fichierSortie);
    // Il ne devrait pas y avoir d'exception
}
{{< /highlight >}}

**PSDNET-2052. L'image étendue sur la toile est rognée après l'enregistrement. Les données sont perdues mais l'aperçu est correct**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "bigfile.psd");

string fichierSortie = Path.Combine(outputFolder, "bigfile_output.psd");
string imageSortie = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions optionsChargement = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(fichierSource, optionsChargement))
{
    // Il ne devrait pas y avoir d'erreur ici
    psdImage.Save(fichierSortie, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(fichierSortie, optionsChargement))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Il ne devrait pas y avoir d'erreur ici
    psdImage.Save(imageSortie, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
