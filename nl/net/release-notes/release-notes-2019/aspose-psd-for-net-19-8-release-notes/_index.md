---
title: Aspose.PSD voor .NET 19.8 - Release-opmerkingen
type: docs
weight: 50
url: /nl/net/aspose-psd-voor-net-19-8-release-opmerkingen/
---

{{% alert color="primary" %}} 

Deze pagina bevat release-opmerkingen voor Aspose.PSD voor .NET 19.8

{{% /alert %}} 

|**Sleutel**|**Samenvatting**|**Categorie**|
| :- | :- | :- |
|PSDNET-184|Laad JPEG, PNG en andere afbeeldingsbestanden naar PsdImage vanuit een stream|Functie|
|PSDNET-134|Implementeer het renderen van Fill Layer: Gradient|Functie|
|PSDNET-166|Opslaan van PSD naar PDF biedt geen selecteerbare tekst|Functie|
|PSDNET-158|Ondersteuning voor opslaan van PSB als PDF|Functie|
|PSDNET-189|Hoge geheugengebruik bij het laden van PSD met alleen-lezen modus|Verbetering|
|PSDNET-171|Na het aanmaken van een nieuwe TextLayer werd het PSD-bestand onleesbaar voor PS|Fout|
|PSDNET-156|Uitzondering bij het laden van PSD|Fout|

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Verwijderde API's:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Gebruik voorbeelden:**
**PSDNET-184. laad JPEG, PNG en andere afbeeldingsbestanden naar PsdImage vanuit een stream**

{{< highlight java >}}

    // laad JPEG, PNG en andere afbeeldingsbestanden naar PsdImage vanuit een stream

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

**PSDNET-134. Implementeer het renderen van Fill Layer: Gradient**

{{< highlight java >}}

             // Implementeer het renderen van Fill Layer: Gradient

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

**PSDNET-166. Opslaan van PSD naar PDF biedt geen selecteerbare tekst**

{{< highlight java >}}

  // Opslaan van PSD naar PDF biedt geen selecteerbare tekst

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Na het aanmaken van een nieuwe TextLayer werd het PSD-bestand onleesbaar voor PS**

{{< highlight java >}}

 // Na het aanmaken van een nieuwe TextLayer op de Build Server werd het PSD-bestand onleesbaar voor PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Enkele tekst", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Uitzondering bij het laden van PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Hoog geheugengebruik bij het laden van PSD met alleen-lezen modus**

{{< highlight java >}}

 // Hoog geheugengebruik van Aspose.PSD bij het laden van PSD met alleen-lezen modus

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Geheugengebruik moet minder dan 100 MB zijn voor deze voorbeelden

            if (memoryUsed > 100)

            {

                throw new Exception("Gebruik van geheugen is te groot");

            }

{{< /highlight >}}

**PSDNET-158. Ondersteuning voor opslaan van PSB als PDF**

{{< highlight java >}}

 // Ondersteuning voor opslaan van PSB als PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
