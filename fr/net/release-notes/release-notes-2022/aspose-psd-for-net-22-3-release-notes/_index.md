---
title: Aspose.PSD pour .NET 22.3 - Notes de version
type: docs
weight: 100
url: /fr/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version de [Aspose.PSD pour .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé** | **Résumé** | **Catégorie** |
| :- | :- | :- |
|PSDNET-210|Ajouter la propriété IsOpen pour le groupe de calques|Fonctionnalité|
|PSDNET-643|L'image PSD avec des masques de calque raster ignore les masques lors de l'enregistrement en image PSD 16 bits|Bogue|
|PSDNET-899|Le mode de fusion Dissoudre ne s'applique pas au dossier avec un masque|Bogue|
|PSDNET-1047|Un fichier spécifique ne peut pas être ouvert par Photoshop après l'enregistrement dans Aspose.PSD 21.11|Bogue|
|PSDNET-1068|Rendu incorrect du calque avec le mode de fusion Linear Dodge (Ajouter)|Bogue|
|PSDNET-1069|La couche de remplissage de motif lance une exception lors de la mise à jour après le chargement|Bogue|


## **Changements de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **APIs supprimées :**
- Aucune


## **Exemples d'utilisation :**

**PSDNET-210.Ajouter la propriété IsOpen pour le groupe de calques**

{{< highlight csharp >}}
// Exemple de lecture et d'écriture de la propriété IsOpen à l'exécution.
string nomFichierSource = "LayerGroupOpenClose.psd";
string nomFichierSortie = "Sortie" + nomFichierSource;

using (var image = (PsdImage)Image.Load(nomFichierSource))
{
    foreach (var calque in image.Layers)
    {
        if (calque is LayerGroup && calque.Name == "Group 1")
        {
            bool estOuvertGroup1 = ((LayerGroup)calque).IsOpen;
            ((LayerGroup)calque).IsOpen = !estOuvertGroup1;
        }

        if (calque is LayerGroup && calque.Name == "Group 2")
        {
            bool estOuvertGroup2 = ((LayerGroup)calque).IsOpen;           
            ((LayerGroup)calque).IsOpen = !estOuvertGroup2;
        }
    }

    image.Save(nomFichierSortie);
}
{{< /highlight >}}

**PSDNET-643. L'image PSD avec des masques de calque raster ignore les masques lors de l'enregistrement en image PSD 16 bits**

{{< highlight csharp >}}
            string cheminFichierSource = "UneReguliereEtUneReguliereAvecMasque.psd";
            string cheminFichierSortie = "sortie_UneReguliereEtUneReguliereAvecMasque.psd";

            using (PsdImage image = (PsdImage)Image.Load(cheminFichierSource))
            {
                image.Save(cheminFichierSortie, new PsdOptions(image)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Le mode de fusion Dissoudre ne s'applique pas au dossier avec un masque**

{{< highlight csharp >}}
            string fichierSource = "psdnet899.psd";
            string pngSortie = "sortie_psdnet899.png";

            using (PsdImage image = (PsdImage) Image.Load(fichierSource))
            {
                image.Save(pngSortie, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Un fichier spécifique ne peut pas être ouvert par Photoshop après l'enregistrement dans Aspose.PSD 21.11**

{{< highlight csharp >}}
            string fichierSource = "psdnet1047.psd";
            string psdSortie = "sortie_psdnet1047.psd";

            using (PsdImage image = (PsdImage) Image.Load(fichierSource))
            {
                image.Save(psdSortie);
            }

            // Besoin d'ouvrir manuellement le PSD de sortie par Photoshop.

            using (PsdImage image = (PsdImage) Image.Load(psdSortie))
            {
                // aucune exception.
            }
{{< /highlight >}}

**PSDNET-1068. Rendu incorrect du calque avec le mode de fusion Linear Dodge (Ajouter)**

{{< highlight csharp >}}
            string fichierSource = "casse.psd";
            string pngSortie = "sortie_casse.psd.png";

            using (var psdImage = (PsdImage) Image.Load(fichierSource))
            {
                psdImage.Save(pngSortie, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. La couche de remplissage de motif lance une exception lors de la mise à jour après le chargement**

{{< highlight csharp >}}
            string fichierSource = "TousLesTypesLayerPsd.psd";

            using (var image = (PsdImage) Image.Load(fichierSource))
            {
                var coucheRemplissage = (FillLayer)image.Layers[9];
                coucheRemplissage.Update();
            }
{{< /highlight >}}
