---
title: Aspose.PSD pour .NET 24.2 - Notes de publication
type: docs
weight: 110
url: /fr/net/aspose-psd-for-net-24-2-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                  | **Catégorie** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503 | Gérer la propriété Angle pour PatternFillSettings                            |   Fonctionnalité   |
| PSDNET-1719 | Prise en charge de l'échelle verticale et horizontale pour TextLayer        |     Fonctionnalité     |
| PSDNET-1783 | [Format AI] Implémentez le rendu correct de l'arrière-plan dans le format AI basé sur PDF |     Fonctionnalité     |
| PSDNET-1611 | Modifier le mécanisme de distorsion dans la déformation                     |     Amélioration     |
| PSDNET-1802 | Accélérer la déformation                                                   |     Amélioration     |
| PSDNET-995  | Exception "Échec du chargement de l'image." lors de l'ouverture du document   |     Erreur     |
| PSDNET-1491 | Correction de l'enregistrement des fichiers psd ayant un motif de contour   |     Erreur     |
| PSDNET-1642 | Le style de texte est incorrect dans un objet intelligent lorsque nous utilisons ReplaceContents    |     Erreur     |
| PSDNET-1884 | [Format AI] Corriger le rendu Cubic Bezier dans le fichier AI               |     Erreur     |

## **Changements de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDNET-1503. Gérer la propriété Angle pour PatternFillSettings**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "PatternFillLayerWide_0.psd");
string fichierSortie = Path.Combine(dossierSortie, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(fichierSortie, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(fichierSortie, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Prise en charge de l'échelle verticale et horizontale pour TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(dossierBase, "1719_src.psd");
string output = Path.Combine(dossierSortie, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [Format AI] Implémentez le rendu correct de l'arrière-plan dans le format AI basé sur PDF**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "pineapples.ai");
string cheminSortie = Path.Combine(dossierSortie, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    image.Save(cheminSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Exception "Échec du chargement de l'image." lors de l'ouverture du document**

{{< highlight csharp >}}
string fichierSource1 = Path.Combine(dossierBase, "PRODUCT.ai");
string fichierSortie1 = Path.Combine(dossierSortie, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(fichierSource1))
{
    image.Save(fichierSortie1, new PngOptions());
}

string fichierSource2 = Path.Combine(dossierBase, "Dolota.ai");
string fichierSortie2 = Path.Combine(dossierSortie, "Dolota.png");

using (AiImage image = (AiImage)Image.Load(fichierSource2))
{
    image.Save(fichierSortie2, new PngOptions());
}

string fichierSource3 = Path.Combine(dossierBase, "ARS_novelty_2108_out_01(1).ai");
string fichierSortie3 = Path.Combine(dossierSortie, "ARS_novelty_2108_out_01(1).png");

using (AiImage image = (AiImage)Image.Load(fichierSource3))
{
    image.Save(fichierSortie3, new PngOptions());
}

string fichierSource4 = Path.Combine(dossierBase, "bit_gear.ai");
string fichierSortie4 = Path.Combine(dossierSortie, "bit_gear.png");

using (AiImage image = (AiImage)Image.Load(fichierSource4))
{
    image.Save(fichierSortie4, new PngOptions());
}

string fichierSource5 = Path.Combine(dossierBase, "test.ai");
string fichierSortie5 = Path.Combine(dossierSortie, "test.png");

using (AiImage image = (AiImage)Image.Load(fichierSource5))
{
    image.Save(fichierSortie5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. Correction de l'enregistrement des fichiers psd ayant un motif de contour**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "StrokeShapePattern.psd");
string fichierSortie = Path.Combine(dossierSortie, "StrokeShapePattern_output.psd");

Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] newPattern = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
};

using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    PattResource pattResource;
    foreach (var globalLayerResource in image.GlobalLayerResources)
    {
        if (globalLayerResource is PattResource)
        {
            pattResource = (PattResource)globalLayerResource;
            PattResourceData patternItem = pattResource.Patterns[0]; // Données du motif interne de contour

            patternItem.PatternId = guid.ToString();
            patternItem.Name = newPatternName;
            patternItem.SetPattern(newPattern, newPatternBounds);

            break;
        }
    }

    strokeInternalFillSettings.PatternName = newPatternName;
    strokeInternalFillSettings.PatternId = guid.ToString() + "\0";

    shapeLayer.Update();

    image.Save(fichierSortie);
}

// Vérifier les données modifiées.
using (PsdImage image = (PsdImage)Image.Load(fichierSortie))
{
    ShapeLayer shapeLayer = (ShapeLayer)image.Layers[1];
    PatternFillSettings strokeInternalFillSettings = (PatternFillSettings)shapeLayer.Fill;

    Assert.AreEqual(guid.ToString().ToUpper(), strokeInternalFillSettings.PatternId);
    Assert.AreEqual(newPatternName, strokeInternalFillSettings.PatternName + "\0");
}
{{< /highlight >}}

**PSDNET-1642. Le style de texte est incorrect dans un objet intelligent lorsque nous utilisons ReplaceContents**

{{< highlight csharp >}}
string fichierEntrée = Path.Combine(dossierBase, "source.psd");
string sortie2 = Path.Combine(dossierSortie, "output.png");

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;

using (PsdImage psdImage = (PsdImage)Image.Load(fichierEntrée, psdLoadOptions))
{
    SmartObjectLayer smartObject = (SmartObjectLayer)psdImage.Layers[1];

    using (PsdImage smartObjectImage = (PsdImage)smartObject.LoadContents(psdLoadOptions))
    {
        smartObject.ReplaceContents(smartObjectImage);
    }

    psdImage.Save(sortie2, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1884. [Format AI] Corriger le rendu Cubic Bezier dans le fichier AI**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "Typography.ai");
string cheminSortie = Path.Combine(dossierSortie, "Typography.png");

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    image.Save(cheminSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1611. Modifier le mécanisme de distorsion dans la déformation**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "crow_grid.psd");
string fichierSortie = Path.Combine(dossierSortie, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(fichierSource, opt))
{
    img.Save(fichierSortie, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1802. Accélérer la déformation**

{{< highlight csharp >}}
string fichierSource = Path.Combine(dossierBase, "output.psd");
string fichierSortie = Path.Combine(dossierSortie, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

var sw = new Stopwatch();
sw.Start();

using (PsdImage img = (PsdImage)Image.Load(fichierSource, opt))
{
    img.Save(fichierSortie, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}

sw.Stop();

// ancienne valeur = 193300
// Nouvelle valeur =  55500
int tempsEnSec = (int)sw.Elapsed.TotalMilliseconds;
if (tempsEnSec > 100000)
{
    throw new Exception("Le temps de traitement est trop long");
}
{{< /highlight >}}
