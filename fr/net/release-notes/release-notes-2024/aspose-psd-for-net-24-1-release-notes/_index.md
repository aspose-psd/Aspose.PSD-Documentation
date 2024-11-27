---
title: Aspose.PSD for .NET 24.1 - Notes de version
type: docs
weight: 120
url: /fr/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**      | **Résumé**                                                                                       | **Catégorie** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Format AI] Ajout d'une gestion de base pour les images AI multipages                               |   Caractéristique   |
| PSDNET-718  | L'effet de texte Warp n'est pas appliqué au texte                                                   |     Problème     |
| PSDNET-1620 | Rendu incorrect du masque dans le fichier spécifique                                               |     Problème     |
| PSDNET-1855 | NullReferenceException dans Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor   |     Problème     |
| PSDNET-1883 | [Format AI] Correction de l'utilisation de la mémoire dans AiExporterUtils                           |     Problème     |



## **Changements de l'API publique**
# **APIs ajoutées:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-718. L'effet de texte Warp n'est pas appliqué au texte**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Rendu incorrect du masque dans le fichier spécifique**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Format AI] Ajout d'une gestion de base pour les images AI multipages**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Charger l'image AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Par défaut, l'ActivePageIndex est 0.
    // Donc si vous enregistrez l'image AI sans modifier cette propriété, la première page sera rendue et enregistrée.
    image.Save(firstPageOutputPng, new PngOptions());

    // Changer l'indice de page active pour la deuxième page.
    image.ActivePageIndex = 1;

    // Enregistrer la deuxième page de l'image AI en tant qu'image PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Changer l'indice de page active pour la troisième page.
    image.ActivePageIndex = 2;

    // Enregistrer la troisième page de l'image AI en tant qu'image PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException dans Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Format AI] Correction de l'utilisation de la mémoire dans AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Charger l'image AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Enregistrer la première page de l'image AI en tant qu'image PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Changer l'indice de page active pour la deuxième page.
    image.ActivePageIndex = 1;

    // Enregistrer la deuxième page de l'image AI en tant qu'image PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Changer l'indice de page active pour la troisième page.
    image.ActivePageIndex = 2;

    // Enregistrer la troisième page de l'image AI en tant qu'image PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("L'utilisation de la mémoire est trop importante. " + memoryUsed + " au lieu de " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
