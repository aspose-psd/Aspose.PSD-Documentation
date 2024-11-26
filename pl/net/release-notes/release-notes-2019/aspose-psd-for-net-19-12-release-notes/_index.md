---
title: Aspose.PSD dla .NET 19.12 - Notatki wydania
type: docs
weight: 10
url: /pl/net/aspose-psd-dla-net-19-12-notatki-wydania/
---

{{% alert color="primary" %}}

Ta strona zawiera notatki wydania dla [Aspose.PSD dla .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klucz**|**Podsumowanie**|**Kategoria**|
| :- | :- | :- |
|PSDNET-11|[Wsparcie dla Warstwy Połączonej](/pl/psd/net/praca-z-warstwami/#workingwithlayers-supportoflinkedlayers)|Funkcja|
|PSDNET-131|[Wsparcie dla SoCoResource](/pl/psd/net/wsparcie-dla-socoresource/)|Funkcja|
|PSDNET-115|Przerwy w liniach są dodawane do istniejących przerw w liniach, jeśli Warstwa Tekstu jest aktualizowana łańcuchem znaków|Błąd|
|PSDNET-157|Zamrażanie podczas zapisywania PSB jako PNG|Błąd|
|PSDNET-250|Wyjątek podczas ładowania pliku PSD CMYK bez warstw z kompresją RLE|Błąd|
|PSDNET-161|Wyjątek podczas aktualizacji warstw tekstowych|Błąd|
|PSDNET-222|Zmiana rozmiaru niektórych plików PSD z maskami warstw działa nieprawidłowo|Błąd|
|PSDNET-244|Zapisywanie PSD z niektórymi Globalization.CultureInfo.CurrentCulture prowadzi do wyjątków podczas ładowania|Błąd|

## **Zmiany w API publicznym**
# **Dodane API:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Usunięte API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Przykłady użycia:**
**PSDNET-11. Wsparcie dla Warstwy Połączonej**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                // połącz wszystkie warstwy w jedną grupę połączoną

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // pobierz identyfikator dla jednej warstwy

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId i linkGroupId nie są równe.");

                }

                // pobierz wszystkie połączone warstwy według identyfikatora grupy łączonej.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // rozłącz każdą warstwę z grupy

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // pobiera NULL dla identyfikatora grupy łączonej, która nie ma warstw w grupie.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("Pole linkedLayers nie jest NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Wsparcie dla SoCoResource**

{{< highlight java >}}

      // Wsparcie dla SoCoResource

    string sourceFileName = "ColorFillLayer.psd";

    string exportPath = "SoCoResource_Edited.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

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

**PSDNET-115. Przerwy w liniach są dodawane do istniejących przerw w liniach, jeśli Warstwa Tekstu jest aktualizowana łańcuchem znaków**

{{< highlight java >}}

           const string NewText = "abcdef\rzxcvbn";

        string sourceFilePath = "TestFileForAsianChars.psd");

        string outputFilePath = "result.psd";

        using (var image = (PsdImage)Image.Load(sourceFilePath))

        {

            var layer = (TextLayer)image.Layers[0];

            var imageOptions = new PsdOptions(image);

            layer.UpdateText(NewText);

            image.Save(outputFilePath, imageOptions);

        }

        using (var createdImage = (PsdImage)Image.Load(outputFilePath))

        {

            var createdLayer = (TextLayer)createdImage.Layers[0];

            if (NewText != createdLayer.Text)

            {

                throw new InvalidDataException("Zaktualizowany tekst jest nieprawidłowy");

            }

        }

{{< /highlight >}}

**PSDNET-157. Zamrażanie podczas zapisywania PSB jako PNG**

{{< highlight java >}}

       // Zapisywanie PSB jako PNG 

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}



` `**PSDNET-250. Wyjątek podczas ładowania pliku PSD CMYK bez warstwy z kompresją RLE**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string sourcePath = "CmykWithAlpha.psd";

            using (RasterImage image = (RasterImage)Image.Load(sourcePath))

            {

                var rawDataSettings = image.RawDataSettings;

                RawDataTester loader = new RawDataTester();

                image.LoadRawData(image.Bounds, rawDataSettings, loader);

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

` `**PSDNET-161. Wyjątek podczas aktualizacji warstw tekstowych**

{{< highlight java >}}

      // Ładowanie pliku PSD jako obrazu i rzutowanie go na PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("test update", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. Zmiana rozmiaru niektórych plików PSD z maskami warstw działa nieprawidłowo**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

                             "LevelsLayerWithLayerMaskRgb",

                             "LevelsLayerWithLayerMaskCmyk",

                             "ColorBalanceAdjustmentLayer"

                         };

        for (int i = 0; i < names.Length; i++)

        {

            string sourceFilePath = names[i] + ".psd";

            string outputFilePath = "output_" + sourceFilePath;

            string outputPngFilePath = "output_" + names[i] + ".png";

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath, psdLoadOptions))

            {

                image.Resize(image.Width * scale, image.Height * scale);

                image.Save(outputFilePath, new PsdOptions());

                image.Save(outputPngFilePath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. Zapisywanie PSD z niektórymi Globalization.CultureInfo.CurrentCulture prowadzi do wyjątków podczas ładowania**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("example-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "output-" + sourceFileName;

            // Ładowanie pliku PSD jako obrazu i rzutowanie go na PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // Ładowanie pliku PSD jako obrazu i rzutowanie go na PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}