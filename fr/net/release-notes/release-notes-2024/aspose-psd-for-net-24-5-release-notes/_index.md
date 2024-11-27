---
title: Aspose.PSD pour .NET 24.5 - Notes de version
type: docs
weight: 80
url: /fr/net/aspose-psd-for-net-24-5-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 24.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                           | **Catégorie** |
|:------------|:--------------------------------------------------------------------------------------|:-------------|
| PSDNET-1897 | [Format AI] Ajouter le support de la gestion des fichiers AI avec en-tête EPSF         | Fonctionnalité      |
| PSDNET-1755 | La semi-transparence est traitée de manière erronée sur l'aperçu du fichier psd        | Problème      |
| PSDNET-1942 | Rendu partiellement incorrect de la calque de forme                                     | Problème      |
| PSDNET-1957 | Exception lors de la sauvegarde des fichiers PSD avec une taille supérieure à 200 Mo et de grandes dimensions | Problème      |
| PSDNET-1998 | Exception d'échec de sauvegarde d'image lors de la sauvegarde au format PDF après la mise à jour de 23.7 à 24.3 | Problème      |
| PSDNET-2033 | Corriger le problème dans la méthode GetFontInfoRecords pour les polices chinoises       | Problème      |

## **Changements dans l'API publique**
# **APIs ajoutées:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-1755. La semi-transparence est traitée de manière erronée sur l'aperçu du fichier psd**

{{< highlight csharp >}}
// La semi-transparence est traitée de manière erronée sur l'aperçu du fichier psd.
// BackgroundContents assigné à Blanc. Les zones transparentes doivent avoir une couleur blanche.

string fichierSource = Path.Combine(baseFolder, "frog_nosymb.psd");
string fichierSortie = Path.Combine(outputFolder, "frog_nosymb_backgroundcontents_output.psd");

using (PsdImage imagePsd = (PsdImage)Image.Load(fichierSource))
{
    RawColor couleurFond = new RawColor(PixelDataFormat.Rgb32Bpp);
    int valeurArgb = 255 << 24 | 255 << 16 | 255 << 8 | 255;
    couleurFond.SetAsInt(valeurArgb); // Blanc

    PsdOptions optionsPsd = new PsdOptions(imagePsd)
    {
        ColorMode = ColorModes.Rgb,
        CompressionMethod = CompressionMethod.RLE,
        ChannelsCount = 4,
        BackgroundContents = couleurFond,
    };

    imagePsd.Save(fichierSortie, optionsPsd);
}
{{< /highlight >}}

**PSDNET-1897. [Format AI] Ajouter le support de gestion des fichiers AI avec en-tête EPSF**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "example.ai");
string cheminFichierSortie = Path.Combine(outputFolder, "example.png");

void AssertAreEqual(object attendu, object reel)
{
    if (!object.Equals(attendu, reel))
    {
        throw new Exception("Les objets ne sont pas égaux.");
    }
}

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    AssertAreEqual(image.Layers.Length, 2);
    AssertAreEqual(image.Layers[0].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[0].ColorIndex, -1);
    AssertAreEqual(image.Layers[1].HasMultiLayerMasks, false);
    AssertAreEqual(image.Layers[1].ColorIndex, -1);

    image.Save(cheminFichierSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1942. Rendu partiellement incorrect de la calque de forme**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "ShapeLayerTest.psd");
string fichierSortie = Path.Combine(outputFolder, "ShapeLayerTest_output.psd");
const int RatioImgToPsd = 256 * 65535;

using (var im = (PsdImage)Image.Load(fichierSource))
{
    ShapeLayer calqueForme = (ShapeLayer)im.Layers[2];
    IPath chemin = calqueForme.Path;
    IPathShape[] formesChemin = chemin.GetItems();
    List<BezierKnotRecord> listeNoeuds = new List<BezierKnotRecord>();
    foreach (IPathShape formeChemin in formesChemin)
    {
        BezierKnotRecord[] noeuds = formeChemin.GetItems();
        listeNoeuds.AddRange(noeuds);
    }

    // Changer les propriétés du calque
    var nouvelleForme = new PathShape();

    BezierKnotRecord[] noeudsBezier = new BezierKnotRecord[]
    {
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(100, 100),
                    calqueForme.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    calqueForme.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 100),
                    calqueForme.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(50, 490),
                    calqueForme.Container.Size),
                PointFToResourcePoint(
                    new PointF(100, 490),
                    calqueForme.Container.Size), // Point d'ancrage
                PointFToResourcePoint(
                    new PointF(150, 490),
                    calqueForme.Container.Size),
            },
        },
        new BezierKnotRecord()
        {
            IsLinked = true,
            Points = new Point[3]
            {
                PointFToResourcePoint(
                    new PointF(490, 150),
                    calqueForme.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 50),
                    calqueForme.Container.Size),
                PointFToResourcePoint(
                    new PointF(490, 20),
                    calqueForme.Container.Size),
            },
        },
    };

    nouvelleForme.SetItems(noeudsBezier);

    List<IPathShape> nouvellesFormes = new List<IPathShape>(formesChemin);
    nouvellesFormes.Add(nouvelleForme);

    IPathShape[] formeCheminNouveau = nouvellesFormes.ToArray();
    chemin.SetItems(formeCheminNouveau);

    calqueForme.Update();

    im.Save(fichierSortie, new PsdOptions());
}

using (var im = (PsdImage)Image.Load(fichierSortie))
{
    ShapeLayer calqueForme = (ShapeLayer)im.Layers[2];
    IPath chemin = calqueForme.Path;
    IPathShape[] formesChemin = chemin.GetItems();
    List<BezierKnotRecord> listeNoeuds = new List<BezierKnotRecord>();
    foreach (IPathShape formeChemin in formesChemin)
    {
        BezierKnotRecord[] noeuds = formeChemin.GetItems();
        listeNoeuds.AddRange(noeuds);
    }

    AssertAreEqual(3, formesChemin.Length);
    AssertAreEqual(42, calqueForme.Left);
    AssertAreEqual(14, calqueForme.Top);
    AssertAreEqual(1600, calqueForme.Bounds.Width);
    AssertAreEqual(1086, calqueForme.Bounds.Height);
}

Point PointFToResourcePoint(PointF point, Size tailleImage)
{
    return new Point(
        (int)Math.Round(point.Y * (RatioImgToPsd / tailleImage.Height)),
        (int)Math.Round(point.X * (RatioImgToPsd / tailleImage.Width)));
}

void AssertAreEqual(object attendu, object reel, string message = null)
{
    if (!object.Equals(attendu, reel))
    {
        throw new Exception(message ?? "Les objets ne sont pas égaux.");
    }
}
{{< /highlight >}}

**PSDNET-1957. Exception lors de la sauvegarde des fichiers PSD avec une taille supérieure à 200 Mo et de grandes dimensions**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "bigfile.psd");
string fichierSortie = Path.Combine(outputFolder, "output_raw.psd");

PsdLoadOptions optionsChargement = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var imagePsd = (PsdImage)Image.Load(fichierSource, optionsChargement))
{
    // Il ne devrait y avoir aucune erreur ici
    imagePsd.Save(fichierSortie, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}
{{< /highlight >}}

**PSDNET-1998. Exception d'échec de sauvegarde d'image lors de la sauvegarde au format PDF après la mise à jour de 23.7 à 24.3**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "CVFlor.psd");
string fichierSortie = Path.Combine(outputFolder, "_export.pdf");

using (var imagePsd = (PsdImage)Image.Load(fichierSource))
{
    PdfOptions optionsSauvegarde = new PdfOptions();
    optionsSauvegarde.PdfCoreOptions = new PdfCoreOptions();

    imagePsd.Save(fichierSortie, optionsSauvegarde);
}
{{< /highlight >}}

**PSDNET-2033. Corriger le problème dans la méthode GetFontInfoRecords pour les polices chinoises**

{{< highlight csharp >}}
var dossierPolice = Path.Combine(baseFolder, "Font");
string fichierSource = Path.Combine(baseFolder, "bd-worlds-best-pink.psd");

PsdLoadOptions optionsChargementPsd = new PsdLoadOptions();
optionsChargementPsd.LoadEffectsResource = true;
optionsChargementPsd.AllowWarpRepaint = true;
try
{
    FontSettings.SetFontsFolders(new string[] { dossierPolice }, true);
    FontSettings.UpdateFonts();

    using (PsdImage image = (PsdImage)PsdImage.Load(fichierSource, optionsChargementPsd))
    {
        foreach (var calque in image.Layers)
        {
            var calqueTexte = calque as TextLayer;

            if (calqueTexte != null)
            {
                if (calqueTexte.Text == "best")
                {
                    // Sans cette correction, il y aura une exception en raison de la police chinoise.
                    calqueTexte.UpdateText("SUСCESS");
                }
            }
        }
    }
}
finally
{
    FontSettings.Reset();
    FontSettings.UpdateFonts();
}
{{< /highlight >}}
