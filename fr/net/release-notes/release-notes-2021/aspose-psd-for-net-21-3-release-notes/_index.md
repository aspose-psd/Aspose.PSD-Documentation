---
title: Notes de version Aspose.PSD pour .NET 21.3
type: docs
weight: 100
url: /fr/net/aspose-psd-for-net-21-3-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de version pour [Aspose.PSD pour .NET 21.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-823|Ajouter la SectionDividerLayer pour améliorer l'expérience avec les groupes de calques|Amélioration|
|PSDNET-694|Lors de la lecture de PattResource, la largeur et la hauteur étaient échangées|Bogue|
|PSDNET-789|Mélange incorrect de plus d'un effet de calque|Bogue|
|PSDNET-805|Ordre et logique de mélange incorrects lorsqu'il y a plus d'un effet de calque|Bogue|
|PSDNET-842|Les propriétés de l'effet de contour ne sont pas enregistrées dans le fichier PSD|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées:**
- T:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer
- M:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.GetRelatedLayerGroup
- P:Aspose.PSD.FileFormats.Psd.Layers.SectionDividerLayer.IsVisibleInGroup

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-694. Lors de la lecture de PattResource, la largeur et la hauteur étaient échangées**

{{< highlight csharp >}}
            string fichierSource = "Untitled-1.psd";
            string fichierSortie = "output.png";

            using (var image = (PsdImage)Image.Load(fichierSource))
            {
                var calqueDeRemp = (FillLayer)image.Layers[1];
                calqueDeRemp.Update(); // invoque le rendu du motif

                image.Save(fichierSortie, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-789. Mélange incorrect de plus d'un effet de calque**

{{< highlight csharp >}}
            string fichierSrc = "source_789.psd";
            string cheminSmartObjectSortie = "output789.png";
            string fichierSortie = "output789.psd";

            using (PsdImage image = (PsdImage)Image.Load(fichierSrc, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var longueur = image.Layers.Length;
                for (int i = 0; i < longueur; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        using (var flux = new MemoryStream(smart.Contents))
                        {
                            flux.Position = 0;
                            using (var imageSmart = (PsdImage)Image.Load(flux))
                            {
                                for (int j = 0; j < imageSmart.Layers.Length; j++)

                                {
                                    // Recherche de calque de texte
                                    var calqueTexte = imageSmart.Layers[j] as TextLayer;
                                    if (calqueTexte != null)
                                    {
                                        var donneesTexte = calqueTexte.TextData;

                                        donneesTexte.Items[0].Text = "Meilleur";
                                        donneesTexte.Items[0].Style.FontSize = 170;
                                    }
                                }

                                smart.ReplaceContents(imageSmart);
                            }
                        }

                        break;
                    }
                }
                // De cette manière, nous enregistrons le fichier PSD modifié
                image.Save(cheminSmartObjectSortie, new PngOptions() { ColorType = PngColorType.VraiesCouleursAvecAlpha });
                image.Save(fichierSortie);
            }
{{< /highlight >}}

**PSDNET-805. Ordre et logique de mélange incorrects lorsqu'il y a plus d'un effet de calque**

{{< highlight csharp >}}
            string fichierSource = "1_200x200.psd";
            string fichierContenu = "Numbers1Best.png";

            string fichierSortiePng = "output.png";
            string fichierSortiePsd = "output.psd";

            using (PsdImage image = (PsdImage)Image.Load(fichierSource, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var longueur = image.Layers.Length;
                for (int i = 0; i < longueur; i++)
                {
                    var smart = image.Layers[i] as SmartObjectLayer;
                    if (smart != null && smart.Name == "__D__")
                    {
                        smart.ReplaceContents(fichierContenu);
                        break;
                    }
                }

                // De cette manière, nous enregistrons le fichier PSD modifié
                image.Save(fichierSortiePng, new PngOptions() { ColorType = PngColorType.VraiesCouleursAvecAlpha });
                image.Save(fichierSortiePsd);
            }
{{< /highlight >}}

**PSDNET-823. Ajouter la SectionDividerLayer pour améliorer l'expérience avec les groupes de calques**

{{< highlight csharp >}}
            // Le code suivant présente les calques SectionDividerLayer et comment obtenir le LayerGroup associé.

            // Hiérarchie des calques
            //    [0]: '</Groupe de calques>' SectionDividerLayer pour le Groupe 1
            //    [1]: 'Calque 1' Calque normal
            //    [2]: '</Groupe de calques>' SectionDividerLayer pour le Groupe 2
            //    [3]: '</Groupe de calques>' SectionDividerLayer pour le Groupe 3
            //    [4]: 'Groupe 3' GroupLayer
            //    [5]: 'Groupe 2' GroupLayer
            //    [6]: 'Groupe 1' GroupLayer

            void AssertAreEqual(object attendu, object reel, string message = null)
            {
                if (!object.Equals(attendu, reel))
                {
                    throw new FormatException(message ?? "Les objets ne sont pas égaux.");
                }
            }

            using (var image = new PsdImage(100, 100))
            {
                // Création de la hiérarchie des calques
                // Ajouter le LayerGroup 'Groupe 1'
                LayerGroup groupe1 = image.AddLayerGroup("Groupe 1", 0, true);
                // Ajouter un calque normal
                Layer calque1 = new Layer();
                calque1.DisplayName = "Calque 1";
                groupe1.AddLayer(calque1);
                // Ajouter le LayerGroup 'Groupe 2'
                LayerGroup groupe2 = groupe1.AddLayerGroup("Groupe 2", 1);
                // Ajouter le LayerGroup 'Groupe 3'
                LayerGroup groupe3 = groupe2.AddLayerGroup("Groupe 3", 0);

                // Obtient les SectionDividerLayer
                SectionDividerLayer diviseur1 = (SectionDividerLayer)image.Layers[0];
                SectionDividerLayer diviseur2 = (SectionDividerLayer)image.Layers[2];
                SectionDividerLayer diviseur3 = (SectionDividerLayer)image.Layers[3];

                // en utilisant la méthode SectionDividerLayer.GetRelatedLayerGroup(), obtenir l'instance LayerGroup associée.
                AssertAreEqual(groupe1.DisplayName, diviseur1.GetRelatedLayerGroup().DisplayName); // le même LayerGroup
                AssertAreEqual(groupe2.DisplayName, diviseur2.GetRelatedLayerGroup().DisplayName); // le même LayerGroup
                AssertAreEqual(groupe3.DisplayName, diviseur3.GetRelatedLayerGroup().DisplayName); // le même LayerGroup

                LayerGroup dossier1 = diviseur1.GetRelatedLayerGroup();
                AssertAreEqual(5, dossier1.Layers.Length); // 'Groupe 1' contient 5 calques
            }
{{< /highlight >}}

**PSDNET-842. Les propriétés de l'effet de contour ne sont pas enregistrées dans le fichier PSD**

{{< highlight csharp >}}
            void AssertAreEqual(object attendu, object reel, string message = null)
            {
                if (!object.Equals(attendu, reel))
                {
                    throw new FormatException(message ?? "Les objets ne sont pas égaux.");
                }
            }

            string fichierSrc = "badStrokeEffect.psd";
            string sortie = "output.psd";

            using (var image = (PsdImage)Image.Load(fichierSrc, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                var calque1 = new Layer();
                image.AddLayer(calque1);
                calque1.BlendingOptions.AddStroke(FillType.Color); // Ne lèvera pas d'exception ArgumentNullException

                StrokeEffect effetContour = image.Layers[1].BlendingOptions.AddStroke(FillType.Color);
                effetContour.Size = 10;
                effetContour.Position = StrokePosition.Outside;
                effetContour.Overprint = true;

                image.Save(sortie);
            }

            // Vérifie les valeurs enregistrées
            using (var image = (PsdImage)Image.Load(sortie, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                StrokeEffect effetContour = (StrokeEffect)image.Layers[1].BlendingOptions.Effects[0];

                AssertAreEqual(10, effetContour.Size);
                AssertAreEqual(StrokePosition.Outside, effetContour.Position);
                AssertAreEqual(true, effetContour.Overprint);
            }
{{< /highlight >}}
