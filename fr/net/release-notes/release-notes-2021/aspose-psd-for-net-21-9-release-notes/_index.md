---
title: Notes de publication d'Aspose.PSD pour .NET 21.9
type: docs
weight: 40
url: /fr/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-574|Rendre la compression RLE par défaut pour l'enregistrement PSD afin d'éviter une sortie PSD volumineuse|Fonctionnalité|
|PSDNET-747|Prise en charge des effets de calque de motif de superposition en mode couleur multicanal dans le fichier PSD|Fonctionnalité|
|PSDNET-951|Après la création du nouveau calque, sa propriété de ressources est nulle, ce qui empêche les manipulations (Redimensionner par exemple)|Bogue|
|PSDNET-955|Non prise en charge des méthodes de compression ZipWithPrediction pour 8 bits|Bogue|

## **Changements dans l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDNET-574. Rendre la compression RLE par défaut pour l'enregistrement PSD afin d'éviter une sortie PSD volumineuse**

{{< highlight csharp >}}
            string cheminFichierEntree = "fichier.psd";
            string sortie1 = "sortie_original.psd";
            string sortie2 = "sortie_options_psd.psd";

            using (Image image = Image.Load(cheminFichierEntree))
            {
                image.Save(sortie1);
                image.Save(sortie2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. Prise en charge des effets de calque de motif de superposition en mode couleur multicanal dans le fichier PSD**

{{< highlight csharp >}}
            var nomFichier = "TousLesEffets.psd";
            var fichierSortie = "TousLesEffets_sortie.psd";
            var optionsChargement = new PsdLoadOptions()
            {
                ChargerRessourcesEffets = true
            };

            // Ne devrait pas générer d'exception
            using (var image = Image.Load(nomFichier, optionsChargement))
            {
                // Ne devrait pas générer d'exception
                image.Save(fichierSortie);
            }
{{< /highlight >}}

**PSDNET-951. Après la création du nouveau calque, sa propriété de ressources est nulle, ce qui empêche les manipulations (Redimensionner par exemple)**

{{< highlight csharp >}}
            string fichierPSD = "Calque1.psd";
            string fichierCalque1 = "Calque2.png";
            string fichierCalque2 = "Calque3.png";
            string nomSortieFinal = "sortieFinale.psd";

            void RemplacerCouleur(RasterImage image, Color ancienneCouleur, int différence, Color nouvelleCouleur)
            {
                var pixels = image.LoadArgb32Pixels(image.Bounds);
                var longueur = pixels.Length;

                var ancienR = ancienneCouleur.R;
                var ancienV = ancienneCouleur.G;
                var ancienB = ancienneCouleur.B;
                var nouvelleValeurCouleur = nouvelleCouleur.ToArgb();

                for (int i = 0; i < longueur; i++)
                {
                    // Rouge
                    var r = (byte)((pixels[i] >> 16) & 0xff);
                    // Vert
                    var v = (byte)((pixels[i] >> 8) & 0xff);
                    // Bleu
                    var b = (byte)(pixels[i] & 0xff);

                    int diffRéelle = Math.Abs(r - ancienR) + Math.Abs(v - ancienV) + Math.Abs(b - ancienB);

                    if (diffRéelle <= différence)
                    {
                        pixels[i] = nouvelleValeurCouleur;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pixels);
            }

            Layer Calque2 = null;
            Layer Calque3 = null;
            using (PsdImage image = (PsdImage)Image.Load(fichierPSD))
            {
                #region Ajout du calque 1

                using (var flux = new FileStream(fichierCalque1, FileMode.Open))
                {
                    Calque2 = new Layer(flux);

                    Calque2.Resize(image.Width, image.Height);
                    var largeur = Calque2.Width;
                    var hauteur = Calque2.Height;

                    Calque2.Left = 675;
                    Calque2.Top = 0;

                    Calque2.Right = Calque2.Left + largeur;
                    Calque2.Bottom = Calque2.Top + hauteur;

                    image.AddLayer(Calque2);
                }

                #endregion

                using (var flux = new FileStream(fichierCalque2, FileMode.Open))
                {
                    Calque3 = new Layer(flux);
                    // Remplacement de la couleur blanche par Transparent
                    RemplacerCouleur(Calque3, Color.White, 256, Color.Transparent);
                    Calque2.DrawImage(new Point(0, 0), Calque3);
                }

                image.Save(nomSortieFinal, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. Non prise en charge des méthodes de compression ZipWithPrediction pour 8 bits**

{{< highlight csharp >}}
            string cheminFichierEntree = "zipTest698.psd";
            string sortieZip8 = "sortie_Zip8bit.psd";
            string sortieZip16 = "sortie_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(cheminFichierEntree))
            {
                image.Save(sortieZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(sortieZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
