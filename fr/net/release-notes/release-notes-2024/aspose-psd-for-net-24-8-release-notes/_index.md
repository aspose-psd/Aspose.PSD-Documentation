---
title: Aspose.PSD pour .NET 24.8 - Notes de version
type: docs
weight: 50
url: /fr/net/aspose-psd-pour-net-24-8-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD pour .NET 24.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                          | **Catégorie** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-2091 | [Format AI] Ajout de la gestion des groupes XObject                                                 | Amélioration  |
| PSDNET-1754 | Amélioration des capacités de transformation de déformation en ajoutant les WarpSettings pour TextLayer et SmartObjectLayer | Fonctionnalité      |
| PSDNET-1836 | [Format AI] Gérer les calques dans les opérateurs des flux de contenu                                | Fonctionnalité      |
| PSDNET-2015 | Le résultat du rendu du fichier AI est très différent de celui des résultats d'Illustrator               | Problème          |
| PSDNET-2093 | Le lien de l'objet intelligent ne s'applique pas à tous les objets intelligents dans le fichier PSD                                  | Problème          |

## **Changements dans l'API publique**
# **APIs ajoutées:**

- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.WarpSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.WarpSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.OSTypeStructure[],Aspose.PSD.Rectangle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Rotate
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Value
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.Bounds
- P:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpSettings.MeshPoints
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Horizontal
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpRotates.Vertical
- T:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.None
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Custom
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arc
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcUpper
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.ArcLower
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Arch
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Bulge
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Flag
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Fish
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Rise
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Wave
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Twist
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Squeeze
- F:Aspose.PSD.FileFormats.Psd.Layers.Warp.WarpStyles.Inflate

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-1754. Améliorer les capacités de transformation de déformation en ajoutant WarpSettings pour TextLayer et SmartObjectLayer**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "smart_without_warp.psd");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

string[] outputImageFile = new string[4];
string[] outputPsdFile = new string[4];

for (int caseIndex = 0; caseIndex < outputImageFile.Length; caseIndex++)
{
    outputImageFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".png");
    outputPsdFile[caseIndex] = Path.Combine(outputFolder, "export_" + caseIndex + ".psd");

    using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
    {
        foreach (Layer layer in img.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                var smartLayer = (SmartObjectLayer)layer;
                smartLayer.WarpSettings = GetWarpSettingsByIndex(smartLayer.WarpSettings, caseIndex);
            }

            if (layer is TextLayer)
            {
                var textLayer = (TextLayer)layer;

                if (caseIndex != 3)
                {
                    textLayer.WarpSettings = GetWarpSettingsByIndex(textLayer.WarpSettings, caseIndex);
                }
            }
        }

        img.Save(outputPsdFile[caseIndex], new PsdOptions());
    }

    using (PsdImage img = (PsdImage)Image.Load(outputPsdFile[caseIndex], opt))
    {
        img.Save(outputImageFile[caseIndex],
            new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
    }
}

WarpSettings GetWarpSettingsByIndex(WarpSettings warpParams, int caseIndex)
{
    switch (caseIndex)
    {
        case 0:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 20;
            break;
        case 1:
            warpParams.Style = WarpStyles.Rise;
            warpParams.Rotate = WarpRotates.Vertical;
            warpParams.Value = 10;
            break;
        case 2:
            warpParams.Style = WarpStyles.Flag;
            warpParams.Rotate = WarpRotates.Horizontal;
            warpParams.Value = 30;
            break;
        case 3:
            warpParams.Style = WarpStyles.Custom;
            warpParams.MeshPoints[2].Y += 70;
            break;
    }

    return warpParams;
}
{{< /highlight >}}

**PSDNET-1836. [Format AI] Gérer les calques dans les opérateurs des flux de contenu**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Layers-NoPen.ai");
string outputFile = Path.Combine(outputFolder, "Layers-NoPen.output.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}

//// Les courbes du calque nommé "Pen" doivent être masquées
{{< /highlight >}}

**PSDNET-2015. Le rendu du fichier AI est très différent de celui des résultats d'Illustrator**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "4.ai");
string outputFilePath = Path.Combine(outputFolder, "4.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2093. Le lien d'objet intelligent ne s'applique pas à tous les objets intelligents dans le fichier PSD**

{{< highlight csharp >}}
string[] files = { "simple_test", "w22" };
string changeFile = Path.Combine(baseFolder, "image(19).png");

string[] sourceFile = new string[files.Length];
string[] outputFiles = new string[files.Length];

for (int i = 0; i < files.Length; i++)
{
    sourceFile[i] = Path.Combine(baseFolder, files[i] + ".psd");
    outputFiles[i] = Path.Combine(outputFolder, files[i] + "_output.psd");

    using (var image = (PsdImage)Image.Load(sourceFile[i]))
    {
        foreach (Layer layer in image.Layers)
        {
            if (layer is SmartObjectLayer)
            {
                SmartObjectLayer smart = (SmartObjectLayer)layer;

                // Pour le deuxième calque intelligent, il y avait une erreur ici
                smart.ReplaceContents(changeFile);
            }
        }

        image.Save(outputFiles[i]);
    }
}
{{< /highlight >}}
