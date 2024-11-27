---
title: Aspose.PSD pour .NET 21.1 - Notes de version
type: docs
weight: 120
url: /fr/net/aspose-psd-pour-dotnet-21-1-notes-de-version/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 21.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-766|Aspose.PSD 20.10: Exception lors de la tentative de conversion d'un fichier Psd particulier en png|Bogue|
|PSDNET-792|Exception lors de l'enregistrement de PSD avec un objet intelligent en PNG|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées :**
- Aucune

# **APIs supprimées :**
- Aucune

## **Exemples d'utilisation :**
**PSDNET-766. Aspose.PSD 20.10: Exception lors de la tentative de conversion d'un fichier Psd particulier en png**
{{< highlight csharp >}}
            const string dossierDeBase = "PSDNET766_1\\";
            const string dossierDeSortie = dossierDeBase + "output\\";
            string cheminFichierSource = dossierDeBase + "school-admission-flyer-template-05052019.psd";
            string cheminFichierSortie = dossierDeSortie + "chool-admission-flyer-template-05052019_output.psd";
            string cheminFichierPngSortie = Path.ChangeExtension(cheminFichierSortie, ".png");
            OptionsDeChargementPsd options = new OptionsDeChargementPsd();
            using (ImagePsd image = (ImagePsd)Image.Load(cheminFichierSource, options))
            {
                image.Save(cheminFichierSortie, new OptionsDePsd(image));
                image.Save(cheminFichierPngSortie, new OptionsPng() { TypeCouleur = TypeCouleurPng.VraieCouleurAvecAlpha });
            }
{{< /highlight >}}

**PSDNET-792. Exception lors de l'enregistrement de PSD avec un objet intelligent en PNG**
{{< highlight csharp >}}
            const string dossierDeBase = "PSDNET792_1\\";
            const string dossierDeSortie = dossierDeBase + "output\\";
            string cheminFichierSource = dossierDeBase + "1.psd";
            string cheminFichierSortie = dossierDeSortie + "1_output.psd";
            string cheminFichierPngSortie = Path.ChangeExtension(cheminFichierSortie, ".png");
            OptionsDeChargementPsd options = new OptionsDeChargementPsd() { ChargerRessourcesEffets = true };
            using (ImagePsd image = (ImagePsd)Image.Load(cheminFichierSource, options))
            {
                var longueur = image.Couches.Longueur;
                for (int i = 0; i < longueur; i++)
                {
                    // Recherche de l'objet intelligent
                    var intelligent = image.Couches[i] as CoucheObjetIntelligent;
                    if (intelligent != null && intelligent.Nom == "__D__")
                    {
                        // Nous chargeons la couche d'objet intelligent à partir du flux mémoire,
                        // Mais nous pouvons utiliser intelligent.ExporterContenu(quelqueChemin) pour exporter l'objet intelligent vers un fichier
                        using (var flux = new MemoryStream(intelligent.Contenu))
                        {
                            flux.Position = 0;
                            using (var imageDansIntelligent = (ImagePsd)Image.Load(flux))
                            {
                                for (int j = 0; j < imageDansIntelligent.Couches.Longueur; j++)
                                {
                                    // Recherche de la couche de texte
                                    var coucheTexte = imageDansIntelligent.Couches[j] as CoucheTexte;
                                    if (coucheTexte != null)
                                    {
                                        // Nous pouvons utiliser simplement ActualiserTexte, mais de cette façon, cela nous donne la possibilité de modifier le texte par parties
                                        // Créer des couches de texte multilignes et d'autres fonctionnalités de style de texte et de paragraphe
                                        // Veuillez faire attention. Si le contenu de l'objet intelligent n'est pas PSD, vous ne pouvez pas utiliser cette méthode de modification de texte
                                        // Dans ce cas, vous devriez utiliser Graphic API : https://docs.aspose.com/psd/net/drawing-images-using-graphics/
                                        var donneesTexte = coucheTexte.DonneesTexte;
                                        donneesTexte.Elements[0].Texte = "Meilleur";

                                        // Vous devez modifier la taille du texte si vous souhaitez que l'image soit belle.
                                        donneesTexte.Elements[0].Style.TaillePolice = 170;
                                    }
                                }

                                // Il est préférable d'utiliser RemplacerContenu. Il va automatiquement réafficher l'objet intelligent
                                intelligent.RemplacerContenu(imageDansIntelligent);
                            }
                        }
                    }
                }

                // De cette manière, nous enregistrons le fichier PSD modifié
                image.Save(cheminFichierSortie, new OptionsDePsd(image));
                image.Save(cheminFichierPngSortie, new OptionsPng() { TypeCouleur = TypeCouleurPng.VraieCouleurAvecAlpha });
            }
{{< /highlight >}}
