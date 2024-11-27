---
title: Notes de version Aspose.PSD for .NET 20.11
type: docs
weight: 20
url: /fr/net/aspose-psd-for-net-20-11-release-notes/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour [Aspose.PSD for .NET 20.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-713|Aspose.PSD ne peut pas convertir les PSD en d'autres modes de couleur/Profondeur de bits sans les enregistrer en tant que fichiers|Fonctionnalité|
|PSDNET-754|Ajouter la capacité de copier un calque d'objet intelligent dans l'image PSD|Fonctionnalité|
|PSDNET-267|Exception lors du chargement et de l'enregistrement du fichier PSD avec Effets de calque|Bogue|
|PSDNET-579|La méthode "Image.LoadRawData" génère une exception NullPointer|Bogue|
|PSDNET-741|ImageLoadException est lancée lors de la tentative d'ouverture du fichier|Bogue|
|PSDNET-744|Aspose.PSD 20.10: Impossible de charger Psd|Bogue|

## **Modifications de l'API publique**
# **APIs ajoutées:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.Convert(Aspose.PSD.ImageOptions.PsdOptions)
- F:Aspose.PSD.FileFormats.Psd.ResourceBlock.ResouceBlockMeSaSignature
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.NewSmartObjectViaCopy
- M:Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer.DuplicateLayer
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.NewSmartObjectViaCopy(Aspose.PSD.FileFormats.Psd.Layers.SmartObjects.SmartObjectLayer)
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(System.Int32[])
- M:Aspose.PSD.FileFormats.Psd.SmartObjectProvider.ConvertToSmartObject(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
# **APIs supprimées:**
- Aucune

## **Exemples d'utilisation:**
**PSDNET-267. Exception lors du chargement et de l'enregistrement du fichier PSD avec Effets de calque**
{{< highlight csharp >}}
            string dataDir = "PSDNET267_1\\";
            string inputFilePath = dataDir + "LayerEffectsTest.psd";
            string outputFilePath = dataDir + "LayerEffectsTestOutput.psd";
            using (var image = (PsdImage)Image.Load(inputFilePath, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFilePath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-579. La méthode "Image.LoadRawData" génère une exception NullPointer**
{{< highlight csharp >}}
            string dataDir = "PSDNET579_1\\";
            string srcFile = dataDir + "CmykWithAlpha_raw.psd";
            using (RasterImage image = (RasterImage)Image.Load(srcFile))
            {
                Rectangle rect = image.Bounds;
                RawDataRetriever rawDataRetriever = new RawDataRetriever(rect, image.RawDataSettings);
                image.LoadRawData(rect, image.RawDataSettings, rawDataRetriever);
                rawDataRetriever.GetData();
            }

    class RawDataRetriever : Aspose.PSD.IPartialRawDataLoader
    {
        private readonly byte[] rawData;
        private int rawDataIndex;

        public RawDataRetriever(Rectangle rectangle, RawDataSettings rawDataSettings)
        {
            int totalSize = rawDataSettings.LineSize * rectangle.Height;
            if (totalSize == 0)
            {
                totalSize = rectangle.Width * rectangle.Height * 5;
            }

            this.rawData = new byte[totalSize];
        }

        public byte[] GetData()
        {
            return this.rawData;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end)
        {
            Array.Copy(data, 0, this.rawData, this.rawDataIndex, data.Length);
            this.rawDataIndex += data.Length;
        }

        public void Process(Rectangle rectangle, byte[] data, Point start, Point end, LoadOptions loadOptions)
        {
            throw new NotImplementedException();
        }
    }
{{< /highlight >}}
**PSDNET-713. Aspose.PSD ne peut pas convertir les PSD en d'autres modes de couleur/Profondeur de bits sans les enregistrer en tant que fichiers**
{{< highlight csharp >}}
            string dataDir = "PSDNET713_1\\";
            string outputDir = dataDir + "output\\";

            // Ces exemples démontrent la conversion du format d'image PSD en d'autres modes de couleur/Profondeur de bits.
            ConversionImage(ColorModes.Echelle_de_Gris, 16, 2);
            ConversionImage(ColorModes.Echelle_de_Gris, 8, 2);
            ConversionImage(ColorModes.Echelle_de_Gris, 8, 1);
            ConversionImage(ColorModes.Rvb, 8, 4);
            ConversionImage(ColorModes.Rvb, 16, 4);
            ConversionImage(ColorModes.CMYK, 8, 5);
            ConversionImage(ColorModes.CMYK, 16, 5);

            void ConversionImage(ColorModes modeCouleur, short compteurBitsCanal, short nombreCanaux)
            {
                var compression = compteurBitsCanal > 8 ? CompressionMethod.Raw : CompressionMethod.RLE;
                EnregistrerEnPsdPuisChargerEtEnregistrerEnPng(
                    "ExempleDeMiseEnSurbrillanceCouleurDeFeuille",
                    modeCouleur,
                    compteurBitsCanal,
                    nombreCanaux,
                    compression,
                    1);
                EnregistrerEnPsdPuisChargerEtEnregistrerEnPng(
                    "ExempleDOpaciteDeRemplissage",
                    modeCouleur,
                    compteurBitsCanal,
                    nombreCanaux,
                    compression,
                    2);
                EnregistrerEnPsdPuisChargerEtEnregistrerEnPng(
                    "MasqueDeDecoupeRegulier",
                    modeCouleur,
                    compteurBitsCanal,
                    nombreCanaux,
                    compression,
                    3);
            }

            // Enregistre en PSD puis charge le fichier enregistré et enregistre en PNG.
            void EnregistrerEnPsdPuisChargerEtEnregistrerEnPng(
                string fichier,
                ColorModes modeCouleur,
                short compteurBitsCanal,
                short nombreCanaux,
                CompressionMethod compression,
                int numeroCalque)
            {
                string srcFile = dataDir + fichier + ".psd";
                string postfix = modeCouleur.ToString() + compteurBitsCanal + "bits" + nombreCanaux + "canaux" +
                                 compression;
                string fileName = fichier + "_" + postfix + ".psd";
                string exportPath = outputDir + fileName;
                PsdOptions psdOptions = new PsdOptions()
                {
                    ColorMode = modeCouleur,
                    CompteurBitsCanal = compteurBitsCanal,
                    NombreCanaux = nombreCanaux,
                    MethodeCompression = compression
                };
                using (var image = (PsdImage)Image.Load(srcFile))
                {
                    image.Convert(psdOptions);

                    RasterCachedImage raster = image.Layers.Length > 0 && numeroCalque >= 0
                        ? (RasterCachedImage)image.Layers[numeroCalque]
                        : image;
                    Aspose.PSD.Graphics graphics = new Graphics(raster);
                    int largeur = raster.Width;
                    int hauteur = raster.Height;
                    Rectangle rect = new Rectangle(
                        largeur / 3,
                        hauteur / 3,
                        largeur - (2 * (largeur / 3)) - 1,
                        hauteur - (2 * (hauteur / 3)) - 1);
                    graphics.DrawRectangle(new Aspose.PSD.Pen(Color.GrisFonce, 1), rect);

                    image.Save(exportPath);
                }

                string pngExportPath = Path.ChangeExtension(exportPath, "png");
                using (PsdImage image = (PsdImage)Image.Load(exportPath))
                {
                    image.Save(pngExportPath, new PngOptions() { TypeCouleur = PngColorType.VraiesCouleursAvecAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-741. ImageLoadException est lancée lors de la tentative d'ouverture du fichier**
{{< highlight csharp >}}
            string dataDir = "PSDNET741_1\\";
            string inputFile = dataDir + "input.psd";
            string outputFile = dataDir + "output.psd";

            using (var psdImage = (PsdImage)Image.Load(inputFile))
            {
                psdImage.Save(outputFile, new PsdOptions(psdImage));
            }

            using (var psdImage2 = (PsdImage)Image.Load(outputFile))
            {
                // Aucune exception ici...
            }
{{< /highlight >}}
**PSDNET-744. Aspose.PSD 20.10: Impossible de charger Psd**
{{< highlight csharp >}}         
            void SontEgaux(object attendu, object reel)
            {
                if (!object.Equals(attendu, reel))
                {
                    throw new Exception("Les valeurs ne sont pas égales.");
                }
            }

            string srcFile = "GST-CHALLAN(2)1..psd";
            string output = "output.psd";

            using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
            {
                SontEgaux(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[23].Signature);
                SontEgaux(ResourceBlock.ResouceBlockMeSaSignature, psdImage.ImageResources[24].Signature);
                psdImage.Save(output);
            }
{{< /highlight >}}
**PSDNET-754. Ajouter la capacité de copier un calque d'objet intelligent dans l'image PSD**
{{< highlight csharp >}}
            string dataDir = "PSDNET754_1\\";
            string outputDir = dataDir + "output\\";

            // Ces exemples montrent comment copier des calques d'objets intelligents dans une image PSD.
            ExempleDeCopieDeCalqueDObjetIntelligent("r-embedded-psd");
            ExempleDeCopieDeCalqueDObjetIntelligent("r-embedded-png");
            ExempleDeCopieDeCalqueDObjetIntelligent("r-embedded-transform");
            ExempleDeCopieDeCalqueDObjetIntelligent("new_panama-papers-8-trans4");

            void ExempleDeCopieDeCalqueDObjetIntelligent(string nomFichier)
            {
                int numeroCalque = 0; // Le numéro du calque à copier
                string cheminFichier = dataDir + nomFichier + ".psd";
                string cheminFichierSortie = outputDir + nomFichier + "_copy_" + numeroCalque;
                string cheminSortiePng = cheminFichierSortie + ".png";
                string cheminSortiePsd = cheminFichierSortie + ".psd";
                using (PsdImage image = (PsdImage)Image.Load(cheminFichier))
                {
                    var calqueObjetIntelligent = (SmartObjectLayer)image.Layers[numeroCalque];
                    var nouveauCalque = calqueObjetIntelligent.NewSmartObjectViaCopy();
                    nouveauCalque.EstVisible = false;
                    AssertIsTrue(object.ReferenceEquals(nouveauCalque, image.Layers[numeroCalque + 1]));
                    AssertIsTrue(object.ReferenceEquals(calqueObjetIntelligent, image.Layers[numeroCalque]));

                    var calqueDuplique = calqueObjetIntelligent.DuplicateLayer();
                    calqueDuplique.NomAffiche = calqueObjetIntelligent.NomAffiche + " image partagée";
                    AssertIsTrue(object.ReferenceEquals(nouveauCalque, image.Layers[numeroCalque + 2]));
                    AssertIsTrue(object.ReferenceEquals(calqueDuplique, image.Layers[numeroCalque + 1]));
                    AssertIsTrue(object.ReferenceEquals(calqueObjetIntelligent, image.Layers[numeroCalque]));

                    using (var imageInterne = (RasterImage)calqueObjetIntelligent.LoadContents(null))
                    {
                        // Inverser l'image d'objet intelligent incorporée (pour une image PSD interne nous inverse uniquement son premier calque)
                        InverserImage(imageInterne);

                        // Remplacer l'image d'objet intelligent incorporée dans le calque PSD
                        calqueObjetIntelligent.RemplacerContents(imageInterne);
                    }

                    // Le calque dupliqué partage son image incorporée avec l'objet intelligent original
                    // et doit être mis à jour explicitement sinon son cache de rendu reste inchangé.
                    // Nous mettons à jour tous les objets intelligents pour nous assurer que le nouveau calque créé par NewSmartObjectViaCopy
                    // ne partage pas l'image incorporée avec les autres.
                    image.SmartObjectProvider.UpdateAllModifiedContent();

                    image.Save(cheminSortiePng, new PngOptions() { TypeCouleur = PngColorType.VraiesCouleursAvecAlpha });
                    image.Save(cheminSortiePsd, new PsdOptions(image));
                }
            }

            // Inverser l'image raster y compris l'image PSD.
            void InverserImage(RasterImage imageInterne)
            {
                var imagePsdInterne = imageInterne as PsdImage;
                if (imagePsdInterne != null)
                {
                    InverserImageRaster(imagePsdInterne.Layers[0]);
                }
                else
                {
                    InverserImageRaster(imageInterne);
                }
            }

            // Inverser l'image raster.
            void InverserImageRaster(RasterImage imageInterne)
            {
                var pixels = imageInterne.LoadArgb32Pixels(imageInterne.Bounds);
                for (int i = 0; i < pixels.Length; i++)
                {
                    var pixel = pixels[i];
                    var alpha = (int)(pixel & 0xff000000);
                    pixels[i] = (~(pixel & 0x00ffffff)) | alpha;
                }

                imageInterne.SaveArgb32Pixels(imageInterne.Bounds, pixels);
            }

            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Attendu vrai"));
                }
            }
{{< /highlight >}}