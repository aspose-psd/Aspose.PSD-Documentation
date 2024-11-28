---
title: Notes de publication d'Aspose.PSD pour .NET 21.5
type: docs
weight: 80
url: /fr/net/aspose-psd-for-net-21-5-release-notes/
---

{{% alert color="primary" %}}

Cette page contient les notes de publication pour [Aspose.PSD pour .NET 21.5](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Clé** | **Résumé** | **Catégorie** |
| :- | :- | :- |
|PSDNET-758|Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels|Fonctionnalité|
|PSDNET-862|Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels lorsque seul un calque est redimensionné|Fonctionnalité|
|PSDNET-578|Chaîne de texte tronquée|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**

**PSDNET-578. Chaîne de texte tronquée**

{{< highlight csharp >}}
            string fichierSrc = "grinched-regular-font.psd";
            string sortie = "output_grinched-regular-font.psd.png";

            // Définir le chemin des polices
            System.Collections.Generic.List<string> polices = new System.Collections.Generic.List<string>();
            polices.AddRange(FontSettings.GetDefaultFontsFolders());
            polices.Add(@"Fonts\");
            FontSettings.SetFontsFolders(polices.ToArray(), true);

            using (PsdImage image = (PsdImage)Image.Load(fichierSrc))
            {
                image.Save(sortie, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-758. Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels**

{{< highlight csharp >}}
            string nomFichierSource = "vectorShapes.psd";
            string nomFichierSortie = "out_vectorShapes.psd";
            string dossierDonnées = "PSDNET758_1";
            string cheminSource = Path.Combine(dossierDonnées, nomFichierSource);
            string cheminSortie = Path.Combine(dossierDonnées, nomFichierSortie);
            using (var imagePsd = (PsdImage)Image.Load(cheminSource))
            {
                foreach (var calque in imagePsd.Layers)
                {
                    calque.Resize(calque.Width * 5 / 4, calque.Height / 2);
                }

                imagePsd.Save(cheminSortie);
                imagePsd.Save(Path.ChangeExtension(cheminSortie, ".png"), new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
            }
{{< /highlight >}}

**PSDNET-862. Prise en charge du redimensionnement des calques de forme avec des chemins vectoriels lorsque seul un calque est redimensionné**

{{< highlight csharp >}}
            // Cet exemple montre comment redimensionner les calques avec une ressource de Vogk et de chemin vectoriel dans l'image PSD
            float scaleX = 0.45f;
            float scaleY = 1.60f;
            string dossierDonnées = "PSDNET862_1";
            string nomFichierSource = Path.Combine(dossierDonnées, "vectorShapes.psd");
            using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))
            {
                for (int indiceCalque = 1; indiceCalque < image.Layers.Length; indiceCalque++, scaleX += 0.25f, scaleY -= 0.25f)
                {
                    var calque = image.Layers[indiceCalque];
                    var nouvelleLargeur = (int)Math.Round(calque.Width * scaleX);
                    var nouvelleHauteur = (int)Math.Round(calque.Height * scaleY);
                    calque.Resize(nouvelleLargeur, nouvelleHauteur);

                    Thread.CurrentThread.CurrentCulture = CultureInfo.CreateSpecificCulture("en-GB");
                    string nomSortie = string.Format("resized_{0}_{1}_{2}", indiceCalque, scaleX, scaleY);
                    string cheminSortie = Path.Combine(dossierDonnées, nomSortie + ".psd");
                    string cheminPngSortie = Path.Combine(dossierDonnées, nomSortie + ".png");
                    image.Save(cheminSortie, new PsdOptions(image));
                    image.Save(cheminPngSortie, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
