---
title: Notes de version Aspose.PSD pour .NET 21.8
type: docs
weight: 50
url: /fr/net/aspose-psd-pour-net-21-8-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-698|Prise en charge des méthodes de compression ZipWithPrediction|Fonctionnalité|
|PSDNET-663|L'espacement du texte est incorrect dans le PSD généré|Bogue|
|PSDNET-685|Exception lors de l'enregistrement du PSD|Bogue|
|PSDNET-927|Distance incorrecte entre les lignes et les symboles dans Aspose.PSD lorsque nous l'utilisons sans licence|Bogue|

## **Changements apportés à l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDNET-663. L'espacement du texte est incorrect dans le PSD généré**

{{< highlight csharp >}}
            string nomFichierSource = "source.psd";
            string nomFichierSortie = "sortie.png";

            using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
            {
                image.Save(nomFichierSortie, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. Exception lors de l'enregistrement du PSD**

{{< highlight csharp >}}
            string nomFichierSource = "Fichier.psd";
            string nomFichierSortie = "Fichier2.psd";

            using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
            {
                var couche1 = (TextLayer)image.Layers[1];
                couche1.TextData.UpdateLayerData();

                image.Save(nomFichierSortie);
            }
{{< /highlight >}}

**PSDNET-698. Prise en charge des méthodes de compression ZipWithPrediction**

{{< highlight csharp >}}
            string cheminFichierEntree = "zipTest698.psd";

            string sortiePng = "sortie.png";
            string sortieBrut = "out_Raw.psd";
            string sortieZip = "out_Zip.psd";

            using (Image image = Image.Load(cheminFichierEntree))
            {
                image.Save(sortiePng, new PngOptions());

                image.Save(sortieBrut, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                image.Save(sortieZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Distance incorrecte entre les lignes et les symboles dans Aspose.PSD lorsque nous l'utilisons sans licence**

{{< highlight csharp >}}
            bool[] etatsLicence = new bool[] {false, true };
            for (int i = 0; i < etatsLicence.Length; i++)
            {
                bool testLicence = etatsLicence[i];
                if (testLicence)
                {
                    License licence = new License();
                    licence.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string fichierSource = "psdnetTest927.psd";
                string fichierSortie = "out_" + testLicence.ToString() + "_psdnetTest927.png";

                using (var image = (PsdImage)Image.Load(fichierSource))
                {
                    image.Save(fichierSortie, new PngOptions());
                }
            }
{{< /highlight >}}
