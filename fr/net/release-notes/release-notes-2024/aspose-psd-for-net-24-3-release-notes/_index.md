---
title: Aspose.PSD pour .NET 24.3 - Notes de publication
type: docs
weight: 100
url: /fr/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé**     | **Résumé**                                                          | **Catégorie** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI Format] Réduire le temps de chargement des grandes images AI multipages         |     Amélioration     |
| PSDNET-1905 | Le fichier PSD, après la conversion de 8 bits en 16 bits, est devenu illisible |     Bug     |
| PSDNET-1906 | Le fichier PSD, après la conversion de 8 bits en 32 bits, est devenu illisible |     Bug     |
| PSDNET-1921 | [AI Format] Corriger l'affichage de la Courbe courte dans le fichier AI                 |     Bug     |

## **Changements de l'API publique**
# **APIs ajoutées:**
- Aucune

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-1905. Le fichier PSD, après la conversion de 8 bits en 16 bits, est devenu illisible**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // est bon
    }
    else
    {
        throw new Exception("Mauvaise ressource globale, la première ressource devrait être Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. Le fichier PSD, après la conversion de 8 bits en 32 bits, est devenu illisible**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // est bon
    }
    else
    {
        throw new Exception("Mauvaise ressource globale, la première ressource devrait être Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI Format] Corriger l'affichage de la Courbe courte dans le fichier AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
