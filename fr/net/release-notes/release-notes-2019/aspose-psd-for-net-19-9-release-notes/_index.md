---
title: Aspose.PSD pour .NET 19.9 - Notes de version
type: docs
weight: 40
url: /fr/net/aspose-psd-pour-net-19-9-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 19.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

| **Clé** | **Résumé** | **Catégorie** |
| :- | :- | :- |
| PSDNET-160 | Nom de calque incorrect extrait | Fonctionnalité |
| PSDNET-175 | Obtention des propriétés de texte d'une partie différente de texte à l'intérieur de PSD TextLayer | Fonctionnalité |
| PSDNET-190 | Prise en charge de l'ajout d'un groupe de calques | Fonctionnalité |
| PSDNET-192 | Prise en charge de la propriété d'échelle pour le calque de remplissage de dégradé | Fonctionnalité |
| PSDNET-162 | Ajustement de la luminosité | Amélioration |
| PSDNET-174 | IndexOutOfRangeException lors de l'enregistrement de l'image PSD en tant que JPEG | Bogue |
| PSDNET-180 | La mise à jour du texte du calque de texte lance une exception | Bogue |
| PSDNET-182 | Enregistrement de l'image PSD après une opération RotateFlip produit un fichier corrompu qui ne peut pas être ouvert | Bogue |

## **Changements d'API publics**

# **APIs ajoutées:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.AddLayerGroup(System.String,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.IText
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Items
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.Text
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortion
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.AddPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.InsertPortion(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.RemovePortion(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.UpdateLayerData
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Justification
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.FirstLineIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.StartIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EndIndent
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceBefore
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.SpaceAfter
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoHyphenate
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.HyphenatedWordSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PreHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.PostHyphen
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.ConsecutiveHyphens
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Zone
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.WordSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LetterSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.GlyphSpacing
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.LeadingType
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Hanging
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Burasagari
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.KinsokuOrder
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.EveryLineComposer
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Text
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Style
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextPortion.Paragraph
- T:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontSize
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoLeading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Leading
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Tracking
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Kerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FillColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StrokeColor
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HindiNumbers
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Apply(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IsEqual(Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle)
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TextData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IGradientFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GdFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientFillSettings.Scale

# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**

**PSDNET-160. Nom de calque incorrect extrait**

Pour afficher correctement le nom du calque, utilisez la propriété **DisplayName**. Un setter est désormais ajouté pour cette propriété et la propriété peut être modifiée. Lorsque Photoshop enregistre le nom du calque en utilisant la propriété Nom, les caractères coréens sont stockés comme byte 63'?' en ASCII. Utilisez la propriété **DisplayName** car la propriété Nom ne prend pas en charge les caractères coréens.

{{< highlight java >}}
             // apporter des modifications dans les noms de calques et enregistrer
            using (var image = (PsdImage)Image.Load("calques avec noms.psd"))
            {
                for (int i = 0; i < image.Layers.Length; i++)
                {
                    var calque = image.Layers[i];
                    // définir une nouvelle valeur dans la propriété DisplayName
                    calque.DisplayName += "_modifié";
                }
                image.Save("sortie.psd");
            }
{{< /highlight >}}

**PSDNET-175. Obtention des propriétés de texte d'une partie différente de texte à l'intérieur de PSD TextLayer**

{{< highlight java >}}
            const double Tolérance = 0,0001;
            var cheminFichier = "ParagraphesTroisCouleurs.psd";
            var cheminSortie = "ParagraphesTroisCouleurs_sortie.psd";
            using (var im = (PsdImage)Image.Load(cheminFichier))
            {
                for (int i = 0; i < im.Layers.Length; i++)
                {
                    var calque = im.Layers[i] as TextLayer;
                    if (calque != null)
                    {
                        var portions = calque.TextData.Items;
                        if (portions.Length != 4)
                        {
                            throw new Exception();
                        }
                        // Vérification du texte de chaque portion
                        if (portions[0].Text != "Ancien " ||
                            portions[1].Text != "couleur" ||
                            portions[2].Text != " texte\r" ||
                            portions[3].Text != "Deuxième paragraphe\r")
                        {
                            throw new Exception();
                        }
                        // Vérification des données de paragraphe
                        // Les paragraphes ont une justification différente
                        if (
                            portions[0].Paragraph.Justification != 0 ||
                            portions[1].Paragraph.Justification != 0 ||
                            portions[2].Paragraph.Justification != 0 ||
                            portions[3].Paragraph.Justification != 2)
                        {
                            throw new Exception();
                        }
                        // Toutes les autres propriétés du premier et du deuxième paragraphe sont égales
                        for (int j = 0; j < portions.Length; j++)
                        {
                            var paragraphe = portions[j].Paragraph;
                            if (Math.Abs(paragraphe.AutoLeading - 1,2) > Tolérance ||
                                paragraphe.AutoHyphenate != false ||
                                paragraphe.Burasagari != false ||
                                paragraphe.ConsecutiveHyphens != 8 ||
                                Math.Abs(paragraphe.StartIndent) > Tolérance ||
                                Math.Abs(paragraphe.EndIndent) > Tolérance ||
                                paragraphe.EveryLineComposer != false ||
                                Math.Abs(paragraphe.FirstLineIndent) > Tolérance ||
                                paragraphe.GlyphSpacing.Length != 3 ||
                                Math.Abs(paragraphe.GlyphSpacing[0] - 1) > Tolérance ||
                                Math.Abs(paragraphe.GlyphSpacing[1] - 1) > Tolérance ||
                                Math.Abs(paragraphe.GlyphSpacing[2] - 1) > Tolérance ||
                                paragraphe.Hanging != false ||
                                paragraphe.HyphenatedWordSize != 6 ||
                                paragraphe.KinsokuOrder != 0 ||
                                paragraphe.LetterSpacing.Length != 3 ||
                                Math.Abs(paragraphe.LetterSpacing[0]) > Tolérance ||
                                Math.Abs(paragraphe.LetterSpacing[1]) > Tolérance ||
                                Math.Abs(paragraphe.LetterSpacing[2]) > Tolérance ||
                                paragraphe.LeadingType != LeadingMode.Auto ||
                                paragraphe.PreHyphen != 2 ||
                                paragraphe.PostHyphen != 2 ||
                                Math.Abs(paragraphe.SpaceBefore) > Tolérance ||
                                Math.Abs(paragraphe.SpaceAfter) > Tolérance ||
                                paragraphe.WordSpacing.Length != 3 ||
                                Math.Abs(paragraphe.WordSpacing[0] - 0,8) > Tolérance ||
                                Math.Abs(paragraphe.WordSpacing[1] - 1,0) > Tolérance ||
                                Math.Abs(paragraphe.WordSpacing[2] - 1,33) > Tolérance ||
                                Math.Abs(paragraphe.Zone - 36,0) > Tolérance)
                            {
                                throw new Exception();
                            }
                        }
                        // Vérification des données de style
                        // Les styles ont des couleurs et des tailles de police différentes
                        if (Math.Abs(portions[0].Style.FontSize - 12) > Tolérance ||
                            Math.Abs(portions[1].Style.FontSize - 12) > Tolérance ||
                            Math.Abs(portions[2].Style.FontSize - 12) > Tolérance ||
                            Math.Abs(portions[3].Style.FontSize - 10) > Tolérance)
                        {
                            throw new Exception();
                        }
                        if (portions[0].Style.FillColor != Color.FromArgb(255, 145, 0, 0) ||
                            portions[1].Style.FillColor != Color.FromArgb(255, 201, 128, 2) ||
                            portions[2].Style.FillColor != Color.FromArgb(255, 18, 143, 4) ||
                            portions[3].Style.FillColor != Color.FromArgb(255, 145, 42, 100))
                        {
                            throw new Exception();
                        }
                        for (int j = 0; j < portions.Length; j++)
                        {
                            var style = portions[j].Style;
                            if (style.AutoLeading != false ||
                                style.HindiNumbers != false ||
                                style.Kerning != 0 ||
                                style.Leading != 0 ||
                                style.StrokeColor != Color.FromArgb(255, 175, 90, 163) ||
                                style.Tracking != 50)
                            {
                                throw new Exception();
                            }
                        }
                        // Exemple de modification de texte
                        portions[0].Text = "Bonjour ";
                        portions[1].Text = "le Monde";
                        // Exemple de suppression de portions de texte
                        calque.TextData.RemovePortion(3);
                        calque.TextData.RemovePortion(2);
                        // Exemple d'ajout d'une nouvelle portion de texte
                        var portionCréée = calque.TextData.ProducePortion();
                        portionCréée.Text = "!!!\r";
                        calque.TextData.AddPortion(portionCréée);
                        portions = calque.TextData.Items;
                        // Exemple de modification de paragraphe et de style pour les portions
                        // Définir une justification correcte
                        portions[0].Paragraph.Justification = 1;
                        portions[1].Paragraph.Justification = 1;
                        portions[2].Paragraph.Justification = 1;
                        // Différentes couleurs pour chaque style. Elles seront modifiées, mais le rendu n'est pas entièrement pris en charge
                        portions[0].Style.FillColor = Color.Aquamarine;
                        portions[1].Style.FillColor = Color.Violet;
                        portions[2].Style.FillColor = Color.LightBlue;
                        // Différente police. Elle sera modifiée, mais le rendu n'est pas entièrement pris en charge
                        portions[0].Style.FontSize = 6;
                        portions[1].Style.FontSize = 8;
                        portions[2].Style.FontSize = 10;
                        calque.TextData.UpdateLayerData();
                        im.Save(cheminSortie, new PsdOptions(im));
                        break;
                    }
                }
            }
{{< /highlight >}}

**PSDNET-190. Prise en charge de l'ajout d'un groupe de calques**

{{< highlight java >}}
             // -Groupe 1
            // --Calque 1
            // --Groupe 2
            // ---Calque 2
            // ---Calque 3
            // --Calque 4
            string dossierDonnées = "test_psdnet190.psd";
            var optionsCréation = new PsdOptions();
            optionsCréation.Source = new FileCreateSource(dossierDonnées, false);
            optionsCréation.Palette = new PsdColorPalette(new Color[] { Color.Green });
            using (var imagePSD = (PsdImage)Image.Create(optionsCréation, 500, 500))
            {
                LayerGroup groupe1 = imagePSD.AddLayerGroup("Groupe 1", 0, true);
                Layer calque1 = new Layer(imagePSD);
                calque1.Name = "Calque 1";
                groupe1.AddLayer(calque1);
                LayerGroup groupe2 = groupe1.AddLayerGroup("Groupe 2", 1);
                Layer calque2 = new Layer(imagePSD);
                calque2.Name = "Calque 2";
                groupe2.AddLayer(calque2);
                Layer calque3 = new Layer(imagePSD);
                calque3.Name = "Calque 3";
                groupe2.AddLayer(calque3);
                Layer calque4 = new Layer(imagePSD);
                calque4.Name = "Calque 4";
                groupe1.AddLayer(calque4);
                imagePSD.Save();
            }
{{< /highlight >}}

**PSDNET-192. Prise en charge de la propriété d'échelle pour le calque de remplissage de dégradé**

{{< highlight java >}}
            using (var image = (PsdImage)Image.Load("RemplissageCalqueDégradé.psd"))
            {
                // obtention d'un calque de remplissage
                FillLayer calqueRemplissage = null;
                foreach (var calque in image.Layers)
                {
                    calqueRemplissage = calque as FillLayer;
                    if (calqueRemplissage != null)
                    {
                        break;
                    }
                }
                var paramètres = calqueRemplissage.FillSettings as IGradientFillSettings;
                // mise à jour de la valeur d'échelle
                paramètres.Scale = 200;
                calqueRemplissage.Update(); // Met à jour les données de pixels
                image.Save("imageMiseAEchelle.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}



**PSDNET-174. IndexOutOfRangeException lors de l'enregistrement de l'image PSD en tant que JPEG**

{{< highlight java >}}
         using (var image = Aspose.PSD.Image.Load("ExemplePSD.psd"))
        {
            image.Save("exempleJPG.jpg", new JpegOptions());
        }
{{< /highlight >}}

**PSDNET-180. La mise à jour du texte du calque de texte lance une exception**

{{< highlight java >}}

           // La mise à jour du texte du calque de texte lance une exception

            string cheminFichier = "FlipVertical.psd";

            string cheminSortie =