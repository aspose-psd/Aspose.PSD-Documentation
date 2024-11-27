---
title: Notes de publication d'Aspose.PSD pour .NET 20.10
type: docs
weight: 30
url: /fr/net/aspose-psd-pour-net-20-10-notes-de-release/
---

{{% alert color="primary" %}} 

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-565|Exception lors de l'enregistrement du fichier PSD spécifique avec des calques de texte|Bogue|
|PSDNET-680|Les polices sont perdues après plusieurs allers-retours avec Aspose.PSD|Bogue|
|PSDNET-704|Rendu de la couche d'objet intelligent|Fonctionnalité|
|PSDNET-707|Prise en charge des transformations non destructives de l'objet intelligent|Fonctionnalité|
|PSDNET-711|Le calque de texte est décalé après l'enregistrement sans aucun changement|Bogue|
|PSDNET-720|Aspose.PSD 20.8: Exception de conversion de Psd en Tiff|Bogue|

## **Modifications de l'API publique**
# **APIs ajoutées :**
- Aucune
# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-565. Exception lors de l'enregistrement du fichier PSD spécifique avec des calques de texte**
{{< highlight csharp >}}
            string nomFichierSource = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string fichierSortie = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
            {
                image.Save(fichierSortie, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. Les polices sont perdues après plusieurs allers-retours avec Aspose.PSD**
{{< highlight csharp >}}
            string sourceFichier = "TwoFonts.psd";

            string sortiePsd1 = "sortie1.psd";
            string sortiePsd2 = "sortie2.psd";
            string sortiePng1 = "sortie1.png";
            string sortiePng2 = "sortie2.png";

            void SontEgaux(int attendu, int réel)
            {
                if (attendu != réel)
                {
                    throw new Exception("Les valeurs ne sont pas égales.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFichier))
            {
                var calqueTexte = (TextLayer)psdImage.Layers[1];

                SontEgaux(1, calqueTexte.TextData.Items[0].Style.FontIndex);
                SontEgaux(0, calqueTexte.TextData.Items[1].Style.FontIndex);

                calqueTexte.TextData.UpdateLayerData();

                SontEgaux(1, calqueTexte.TextData.Items[0].Style.FontIndex);
                SontEgaux(0, calqueTexte.TextData.Items[1].Style.FontIndex);

                psdImage.Save(sortiePsd1, new PsdOptions(psdImage));
                psdImage.Save(sortiePng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(sortiePsd1))
            {
                var calqueTexte = (TextLayer)psdImage.Layers[1];

                SontEgaux(1, calqueTexte.TextData.Items[0].Style.FontIndex);
                SontEgaux(0, calqueTexte.TextData.Items[1].Style.FontIndex);

                calqueTexte.TextData.UpdateLayerData();

                SontEgaux(1, calqueTexte.TextData.Items[0].Style.FontIndex);
                SontEgaux(0, calqueTexte.TextData.Items[1].Style.FontIndex);

                psdImage.Save(sortiePsd2, new PsdOptions(psdImage));
                psdImage.Save(sortiePng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Rendu de la couche d'objet intelligent**
{{< highlight csharp >}}
            // Cet exemple montre comment remplacer le contenu de la couche d'objet intelligent Adobe® Photoshop® et son rendu correct.
            string répertoireDonnées = "PSDNET704_1\\";
            string cheminFichier = répertoireDonnées + "new_panama-papers-4-trans4.psd";
            string cheminSortiePng = répertoireDonnées + "new_panama-papers-4-trans4_replaced.png";
            string cheminSortiePsd = répertoireDonnées + "new_panama-papers-4-trans4_replaced.psd";
            string cheminNouveauContenu = répertoireDonnées + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
            {
                var calqueObjetIntelligent = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                calqueObjetIntelligent.ReplaceContents(cheminNouveauContenu);
                image.Save(cheminSortiePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(cheminSortiePsd, new PsdOptions(image));
            }

            // Cet exemple montre comment mettre à jour le cache d'image des calques d'objet intelligent Adobe® Photoshop® et leur rendu correct.
            cheminFichier = répertoireDonnées + "LayeredSmartObjects8bit2.psd";
            cheminSortiePng = répertoireDonnées + "LayeredSmartObjects8bit2_updated.png";
            cheminSortiePsd = répertoireDonnées + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(cheminSortiePng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(cheminSortiePsd, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. Prise en charge des transformations non destructives de l'objet intelligent**
{{< highlight csharp >}}
            string répertoireDonnées = "PSDNET707_1\\";
            string répertoireSortie = répertoireDonnées;

            // Ces exemples montrent des transformations non destructives du fichier PSD avec SmartObjectLayer.
            // Nous pouvons redimensionner, faire pivoter, incliner, déformer, transformer en perspective ou déformer un calque sans
            // perdre les données ou la qualité de l'image d'origine car les transformations n'affectent pas les données d'origine.

            // Cet exemple montre comment redimensionner l'image Adobe® Photoshop® avec des calques d'objet intelligent :
            ExempleRedimensionImageObjetIntelligent("new_panama-papers-8-trans4-linked");
            ExempleRedimensionImageObjetIntelligent("picture-frame-4-linked3");
            ExempleRedimensionImageObjetIntelligent("gorilla");

            // Cet exemple montre comment redimensionner le fichier PSD avec des calques d'objet intelligent.
            void ExempleRedimensionImageObjetIntelligent(string nomFichier)
            {
                const int échelle = 4;
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + "Resize_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + "Resize_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    int nouvelleLargeur = image.Width * échelle;
                    int nouvelleHauteur = image.Height * échelle;
                    image.Resize(nouvelleLargeur, nouvelleHauteur);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Cet exemple montre comment redimensionner la couche d'objet intelligent Adobe® Photoshop®.
            ExempleRedimensionCoucheObjetIntelligent("new_panama-papers-8-trans4-linked");
            ExempleRedimensionCoucheObjetIntelligent("gorilla");

            // Cet exemple montre comment redimensionner une couche d'objet intelligent dans le fichier PSD.
            void ExempleRedimensionCoucheObjetIntelligent(string nomFichier)
            {
                const double échelle = 3.5;
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + "ResizeLast_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + "ResizeLast_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    var calqueObjetIntelligent = image.Layers[image.Layers.Length - 1];
                    int nouvelleLargeur = (int)(calqueObjetIntelligent.Width * échelle);
                    int nouvelleHauteur = (int)(calqueObjetIntelligent.Height * échelle);
                    calqueObjetIntelligent.Resize(nouvelleLargeur, nouvelleHauteur);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
                }
            }

            // Cet exemple montre comment recadrer la couche d'objet intelligent Adobe® Photoshop®.
            ExempleRecadrageCoucheObjetIntelligent("new_panama-papers-8-trans4-linked");
            ExempleRecadrageCoucheObjetIntelligent("gorilla");

            // Cet exemple montre comment recadrer une couche d'objet intelligent dans le fichier PSD.
            void ExempleRecadrageCoucheObjetIntelligent(string nomFichier)
            {
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + "CropLast_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + "CropLast_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    var calqueObjetIntelligent = image.Layers[image.Layers.Length - 1];
                    calqueObjetIntelligent.Crop(25, 15, 30, 10);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Cet exemple montre comment recadrer la couche d'objet intelligent Adobe® Photoshop®:
            ExempleRecadrageImageObjetIntelligent("new_panama-papers-8-trans4-linked");
            ExempleRecadrageImageObjetIntelligent("gorilla");

            // Cet exemple montre comment recadrer le fichier PSD avec des calques d'objet intelligent.
            void ExempleRecadrageImageObjetIntelligent(string nomFichier)
            {
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + "Crop_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + "Crop_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    image.Crop(25, 10, 30, 5);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Cet exemple montre comment faire pivoter et retourner l'image Adobe® Photoshop® avec des calques d'objet intelligent :
            ExempleRotationRetournementImageObjetIntelligent("gorilla", RotateFlipType.Rotate90FlipNone);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            ExempleRotationRetournementImageObjetIntelligent("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Cet exemple montre comment faire pivoter et retourner le fichier PSD avec des calques d'objet intelligent.
            void ExempleRotationRetournementImageObjetIntelligent(string nomFichier, RotateFlipType typeRotationRetournement)
            {
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + typeRotationRetournement + "_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + typeRotationRetournement + "_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    image.RotateFlip(typeRotationRetournement);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Cet exemple montre comment faire pivoter et retourner la couche d'objet intelligent Adobe® Photoshop®.
            ExempleRotationRetournementCoucheObjetIntelligent("gorilla", RotateFlipType.Rotate90FlipNone);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            ExempleRotationRetournementCoucheObjetIntelligent("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Cet exemple montre comment faire pivoter et retourner une couche d'objet intelligent dans le fichier PSD.
            void ExempleRotationRetournementCoucheObjetIntelligent(string nomFichier, RotateFlipType typeRotationRetournement)
            {
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = répertoireSortie + typeRotationRetournement + "Last_" + nomFichier + ".psd";
                string cheminSortiePng = répertoireSortie + typeRotationRetournement + "Last_" + nomFichier + ".png";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    var calqueObjetIntelligent = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    calqueObjetIntelligent.RotateFlip(typeRotationRetournement);
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminSortiePng, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Cet exemple montre comment faire pivoter la couche d'objet intelligent Adobe® Photoshop® par n'importe quel angle :
            const string FormatAngle = "+#;-#;+0";
            ExempleRotationCoucheObjetIntelligent("gorilla", 45, false);
            ExempleRotationCoucheObjetIntelligent("gorilla", 45, true);
            ExempleRotationCoucheObjetIntelligent("r3-embedded-transform2", -30, true);
            ExempleRotationCoucheObjetIntelligent("r3-embedded-transform2", -30, false);
            ExempleRotationCoucheObjetIntelligent("new_panama-papers-8-trans4-linked", 190, false);
            ExempleRotationCoucheObjetIntelligent("new_panama-papers-8-trans4-linked", 190, true);

            // Cet exemple montre comment faire pivoter une couche d'objet intelligent dans le fichier PSD par n'importe quel angle.
            void ExempleRotationCoucheObjetIntelligent(string nomFichier, float angle, bool redimensionProportionnellement)
            {
                string préfixe = "RotateLast" +  angle.ToString(FormatAngle) + (redimensionProportionnellement ? "ResizeProportionally" : "") + "_";
                string cheminFichier = répertoireDonnées + nomFichier + ".psd";
                string cheminSortie = ré