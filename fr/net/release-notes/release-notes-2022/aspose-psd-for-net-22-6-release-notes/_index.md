---
title: Notes de version Aspose.PSD pour .NET 22.6
type: docs
weight: 70
url: /fr/net/aspose-psd-pour-net-22-6-notes-de-version/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-940|Créer une API pour obtenir un hachage unique pour des calques similaires dans différents fichiers|Amélioration|
|PSDNET-678|Rendu incorrect du calque de remplissage avec motif dans le cas où il y a plusieurs motifs et que l'ordre des calques a été modifié|Bogue|
|PSDNET-1125|Exception lors du chargement d'un fichier PSD spécifique avec le mode couleur CMJN|Bogue|


## **Changements d'API publique**
# **APIs ajoutées :**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation:**

**PSDNET-678. Rendu incorrect du calque de remplissage avec motif dans le cas où il y a plusieurs motifs et que l'ordre des calques a été modifié**

{{< highlight csharp >}}
string fichierSource = "mauvaisMotif.psd";
string sortiePng = "sortie_678.png";

using (var imagePsd = (PsdImage)Image.Load(fichierSource))
{
    FillLayer calque1 = (FillLayer)imagePsd.Layers[1];
    FillLayer calque2 = (FillLayer)imagePsd.Layers[2];

    calque1.MettreÀJour();
    calque2.MettreÀJour();

    imagePsd.Save(sortiePng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Créer une API pour obtenir un hachage unique pour des calques similaires dans différents fichiers**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Programme
{
    static void Main()
    {
       //Les scénarios de test sont ici
    }
}
{{< /highlight >}}

**PSDNET-1125. Exception lors du chargement d'un fichier PSD spécifique avec le mode couleur CMJN**

{{< highlight csharp >}}
string fichierSource = "02_canaux-alpha.psd";
string sortiePng = "sortie_1125.png";

using (PsdImage image = (PsdImage)Image.Load(fichierSource))
{
    image.Save(sortiePng, new PngOptions());
}
{{< /highlight >}}