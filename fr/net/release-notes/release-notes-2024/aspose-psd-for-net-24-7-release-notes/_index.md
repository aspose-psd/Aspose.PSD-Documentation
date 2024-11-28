---
title: Aspose.PSD pour .NET 24.7 - Notes de version
type: docs
weight: 60
url: /fr/net/aspose-psd-pour-net-24-7-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Exception "Échec du chargement de l'image" lors de l'ouverture du document AI                   | Bug      |
| PSDNET-2022 | Texte rendu incorrectement dans les fichiers PDF de sortie                                       | Bug      |
| PSDNET-2061 | Résoudre l'exception ImageSaveException : Échec de l'exportation de l'image pour le fichier donné sur Linux | Bug      |
| PSDNET-2080 | Résoudre le chargement des polices lors de l'utilisation de Aspose.Drawing                        | Bug      |
| PSDNET-2085 | Une 'opération arithmétique a donné lieu à un débordement' lors de la création d'une couche d'objet intelligent en utilisant un grand JPEG | Bug      |
| PSDNET-2100 | Le fichier AI ne peut pas être converti en fichier JPG                                           | Bug      |

## **Changements d'API publics**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-1029. Exception "Échec du chargement de l'image" lors de l'ouverture du document AI**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string fichierSortie = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    image.Save(fichierSortie, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Texte rendu incorrectement dans les fichiers PDF de sortie**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Résoudre l'exception ImageSaveException : Échec de l'exportation de l'image pour le fichier donné sur Linux**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string fichierSortie = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var optionsSauvegarde = new JpegOptions() { Quality = 70 };
    psdImage.Save(fichierSortie, optionsSauvegarde);
}
{{< /highlight >}}

**PSDNET-2080. Résoudre le chargement des polices lors de l'utilisation de Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Avant la mise à jour. Nombre de polices installées : " + installedFonts.Families.Length);
    Console.WriteLine("- Plateforme : " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Actualiser le cache des polices en essayant d'obtenir le nom de police Adobe pour 'Arial' : "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Après la mise à jour. Nombre de polices installées : " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. Une 'opération arithmétique a donné lieu à un débordement' lors de la création d'une couche d'objet intelligent en utilisant un grand JPEG**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Couche de test";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Le fichier AI ne peut pas être converti en fichier JPG**

{{< highlight csharp >}}
string fichierSource = Path.Combine(baseFolder, "aaa.ai");
string fichierSortie = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(fichierSource))
{
    image.Save(fichierSortie, new PngOptions());
}
{{< /highlight >}}
