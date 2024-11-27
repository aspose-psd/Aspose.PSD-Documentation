---
title: Aspose.PSD pour .NET 19.8 - Notes de version
type: docs
weight: 50
url: /fr/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}} 

Cette page contient les notes de version pour Aspose.PSD pour .NET 19.8

{{% /alert %}} 

|**Clé**|**Résumé**|**Catégorie**|
| :- | :- | :- |
|PSDNET-184|Charger des fichiers d'image JPEG, PNG et autres dans PsdImage à partir du flux|Fonctionnalité|
|PSDNET-134|Implémenter le rendu du calque de remplissage : Dégradé|Fonctionnalité|
|PSDNET-166|La sauvegarde des PSD en PDF ne permet pas de sélectionner du texte|Fonctionnalité|
|PSDNET-158|Prise en charge de la sauvegarde de PSB en PDF|Fonctionnalité|
|PSDNET-189|Utilisation élevée de la mémoire lors du chargement de PSD en mode Lecture seule|Amélioration|
|PSDNET-171|Après la création d'un nouveau calque de texte, le fichier PSD devient illisible pour PS|Bogue|
|PSDNET-156|Exception lors du chargement de PSD|Bogue|

## **Changements d'API Publique**
# **APIs ajoutées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **APIs supprimées :**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Exemples d'utilisation:**

**PSDNET-184. Charger des fichiers d'image JPEG, PNG et autres dans PsdImage à partir du flux**

{{< highlight java >}}

    // Charger des fichiers d'image JPEG, PNG et autres dans PsdImage à partir du flux

    string outputFilePath = "PsdResult.psd";

    var filesList = new string[]

    {

        "PsdExample.psd",

        "BmpExample.bmp",

        "GifExample.gif",

        "Jpeg2000Example.jpf",

        "JpegExample.jpg",

        "PngExample.png",

        "TiffExample.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Implémenter le rendu du calque de remplissage : Dégradé**

{{< highlight java >}}

             // Implémenter le rendu du calque de remplissage : Dégradé

            string fileName = "FillLayerGradient.psd";

            GradientType[] gradientTypes = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(fileName))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradientTypes)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(fileName + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. La sauvegarde des PSD en PDF ne permet pas de sélectionner du texte**

{{< highlight java >}}

  // La sauvegarde des PSD en PDF ne permet pas de sélectionner du texte

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Après la création d'un nouveau calque de texte, le fichier PSD devient illisible pour PS**

{{< highlight java >}}

 // Après la création d'un nouveau calque de texte sur le serveur de compilation, le fichier PSD devient illisible pour PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}

**PSDNET-156. Exception lors du chargement de PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Utilisation élevée de la mémoire lors du chargement de PSD en mode Lecture seule**

{{< highlight java >}}

 // Utilisation élevée de la mémoire lors du chargement de PSD en mode Lecture seule

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // La consommation de mémoire doit être inférieure à 100 Mo pour ces exemples

            if (memoryUsed > 100)

            {

                throw new Exception("La consommation de mémoire est trop importante");

            }

{{< /highlight >}}

**PSDNET-158. Prise en charge de la sauvegarde de PSB en PDF**

{{< highlight java >}}

 // Prise en charge de la sauvegarde de PSB en PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
