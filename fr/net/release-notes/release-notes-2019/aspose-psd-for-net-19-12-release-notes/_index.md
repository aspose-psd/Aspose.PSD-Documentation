---
title: Notes de version Aspose.PSD pour .NET 19.12
type: docs
weight: 10
url: /fr/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD pour .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-11|[Support de la couche liée](/psd/fr/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Fonctionnalité|
|PSDNET-131|[Support de SoCoResource](/psd/fr/net/support-of-socoresource/)|Fonctionnalité|
|PSDNET-115|Des sauts de ligne sont ajoutés aux sauts de ligne existants si un calque de texte est mis à jour avec une chaîne|Bogue|
|PSDNET-157|Blocage lors de l'enregistrement d'un PSB en PNG|Bogue|
|PSDNET-250|Exception lors du chargement d'un fichier PSD CMJN sans calques avec compression RLE|Bogue|
|PSDNET-161|Exception lors de la mise à jour des calques de texte|Bogue|
|PSDNET-222|Le redimensionnement de certains fichiers PSD avec des masques de calque fonctionne de manière incorrecte|Bogue|
|PSDNET-244|L'enregistrement d'un PSD avec certaines Globalization.CultureInfo.CurrentCulture entraîne des exceptions lors du chargement|Bogue|

## **Changements de l'API publique**
# **APIs ajoutées :**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **APIs supprimées :**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Exemples d'utilisation :**
**PSDNET-11. Support de la couche liée**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("exemple.psd"))

            {

                Layer[] calques = psd.Layers;

                // lier tous les calques dans un groupe lié

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(calques);

                // obtenir l'ID pour un calque

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(calques[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("les identifiants de calque et de groupe lié ne sont pas égaux.");

                }

                // obtenir tous les calques liés par l'ID de groupe lié.

                Layer[] calquesLies = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // délier chaque calque du groupe

                foreach (var calqueLie in calquesLies)

                {

                    psd.LinkedLayersManager.UnlinkLayer(calqueLie);

                }

                // récupérer NULL pour un ID de groupe lié qui n'a pas de calques dans le groupe.

                calquesLies = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (calquesLies != null)

                {

                    throw new Exception("Le champ calquesLies n'est pas NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Support de SoCoResource**

{{< highlight java >}}

      // Support de SoCoResource

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var calque in im.Layers)

        {

            if (calque is FillLayer)

            {

                var fillLayer = (FillLayer)calque;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. Des sauts de ligne sont ajoutés aux sauts de ligne existants si un calque de texte est mis à jour avec une chaîne**

{{< highlight java >}}

           const string NouveauTexte = "abcdef\rzxcvbn";

        string cheminSource = "FichierTestPourCaractèresAsiatiques.psd");

        string cheminSortie = "resultat.psd";

        using (var image = (PsdImage)Image.Load(cheminSource))

        {

            var calque = (TextLayer)image.Layers[0];

            var optionsImage = new PsdOptions(image);

            calque.UpdateText(NouveauTexte);

            image.Save(cheminSortie, optionsImage);

        }

        using (var imageCreee = (PsdImage)Image.Load(cheminSortie))

        {

            var calqueCree = (TextLayer)imageCreee.Layers[0];

            if (NouveauTexte != calqueCree.Text)

            {

                throw new InvalidDataException("Le texte mis à jour est invalide");

            }

        }

{{< /highlight >}}

**PSDNET-157. Blocage lors de l'enregistrement d'un PSB en PNG**

{{< highlight java >}}

       // Enregistrer un PSB en tant que PNG 

    string nomFichierSource = "exemple.psb";

    string nomFichierSortie = "exemple.png";

    using (PsdImage image = (PsdImage)Image.Load(nomFichierSource))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(nomFichierSortie, options);

    }

{{< /highlight >}}



` `**PSDNET-250. Exception lors du chargement d'un fichier PSD CMJN sans calque avec compression RLE**

{{< highlight java >}}

     void ChargerDonnéesBrutesDepuisPsd()

        {

            string cheminSource = "CMJNAvecAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(cheminSource))

            {

                var paramètresDonnéesBrutes = image.RawDataSettings;

                RawDataTester chargeur = new RawDataTester();

                image.LoadRawData(image.Bounds, paramètresDonnéesBrutes, chargeur);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end)

            {

            }

            public void Process(Rectangle rectangle, byte[] pixels, Point start, Point end, LoadOptions loadOptions)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Exception lors de la mise à jour des calques de texte**

{{< highlight java >}}

      // Charger un fichier PSD en tant qu'image et le convertir en PsdImage

    using (PsdImage imagePSD = (PsdImage)Image.Load("exemple.psd"))

    {

        foreach (var calque in imagePSD.Layers)

        {

            if (calque is TextLayer)

            {

                TextLayer calqueTexte = calque as TextLayer;

                calqueTexte.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        imagePSD.Save("MettreÀJourCalqueTexteDansFichierPSD_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. Le redimensionnement de certains fichiers PSD avec des masques de calque fonctionne de manière incorrecte**

{{< highlight java >}}

     int échelle = 2;

        string[] noms = {

                             "UnRégulierEtUnAjustementAvecVecteurEtMasqueDeCalque",

                             "CalqueDeNiveauxAvecMasqueDeCalqueRgb",

                             "CalqueDeNiveauxAvecMasqueDeCalqueCmyk",

                             "CalqueDajustementBalanceDesCouleurs"

                         };

        for (int i = 0; i < noms.Length; i++)

        {

            string cheminFichierSource = noms[i] + ".psd";

            string cheminFichierSortie = "sortie_" + cheminFichierSource;

            string cheminPngSortie = "sortie_" + noms[i] + ".png";

            var optionsChargementPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(cheminFichierSource, optionsChargementPsd))

            {

                image.Resize(image.Width * échelle, image.Height * échelle);

                image.Save(cheminFichierSortie, new PsdOptions());

                image.Save(cheminPngSortie, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. L'enregistrement d'un PSD avec certaines Globalization.CultureInfo.CurrentCulture entraîne des exceptions lors du chargement**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string nomFichierSource = string.Format("exemple-{0}.psd", i);

            var optionsChargementPsd = new PsdLoadOptions() { LoadEffectsResource = true };

            var optionsEnregistrementPsd = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string nomFichierSortie = "résultat-" + nomFichierSource;

            // Charger un fichier PSD en tant qu'image et le convertir en PsdImage

            using (PsdImage image = (PsdImage)Image.Load(nomFichierSource, optionsChargementPsd))

            {

                image.Resize(160, 120);

                image.Save(nomFichierSortie, optionsEnregistrementPsd);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // Charger un fichier PSD en tant qu'image et le convertir en PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(nomFichierSource, optionsChargementPsd))

            {

                image2.Resize(160, 120);

                image2.Save(nomFichierSortie, optionsEnregistrementPsd);

            }

        }

{{< /highlight >}}