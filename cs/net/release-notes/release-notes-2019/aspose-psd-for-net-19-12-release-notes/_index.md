---
title: Aspose.PSD pro .NET 19.12 - Poznámky k vydání
type: docs
weight: 10
url: /cs/net/aspose-psd-pro-net-19-12-poznamky-k-vydani/
---

{{% alert color="primary" %}}

Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Klíč**|**Souhrn**|**Kategorie**|
| :- | :- | :- |
|PSDNET-11|[Podpora vrstvy odkazů](/psd/cs/net/prace-s-vrstvami/#prace-s-vrstvami-podporavrstvyodkazu)|Funkce|
|PSDNET-131|[Podpora zdroje SoCo](/psd/cs/net/podpora-zdroje-socoresource/)|Funkce|
|PSDNET-115|Při aktualizaci textové vrstvy s řetězcem se přidávají závěrečné zlomy do existujících závorek|Chyba|
|PSDNET-157|Uložení PSB jako PNG zamrzává|Chyba|
|PSDNET-250|Výjimka při načítání souboru PSD s CMYK bez vrstev s kompresí RLE|Chyba|
|PSDNET-161|Výjimka při aktualizaci textových vrstev|Chyba|
|PSDNET-222|Změna velikosti některých souborů PSD s maskami vrstev funguje nesprávně|Chyba|
|PSDNET-244|Uložení PSD se současným Globalization.CultureInfo.CurrentCulture vede k výjimkám při načítání|Chyba|

## **Změny ve veřejném API**
# **Přidaná API:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Odstraněná API:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Příklady použití:**
**PSDNET-11. Podpora vrstvy odkazů**

{{< highlight java >}}

       using (var psd = (PsdImage)Image.Load("example.psd"))

<|ipynb_marker|> Output

{

            Layer[] layers = psd.Layers;

            // spojit všechny vrstvy do jedné skupiny odkazů

            short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

            // získat id pro jednu vrstvu

            short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

            if (layersLinkGroupId != linkGroupId)

            {

                throw new Exception("layersLinkGroupId a linkGroupId nejsou shodné.");

            }

            // získat všechny propojené vrstvy podle id skupiny odkazů.

            Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

            // odpojit každou vrstvu ze skupiny

            foreach (var linkedLayer in linkedLayers)

            {

                psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

            }

            // získat NULL pro id skupiny odkazů, která neobsahuje žádné vrstvy ve skupině.

            linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

            if (linkedLayers != null)

            {

                throw new Exception("Pole linkedLayers není NULL.");

            }

            psd.Save("psdnet11_output.psd");

        }

{{< /highlight >}}

**PSDNET-131. Podpora zdroje SoCoResource**

{{< highlight java >}}

      // Podpora zdroje SoCoResource

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

**PSDNET-115. Přidání zlomků na existující zlomky, pokud je textová vrstva aktualizována řetězcem**

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

                throw new InvalidDataException("Aktualizovaný text je neplatný");

            }

        }

{{< /highlight >}}

**PSDNET-157. Uložení PSB jako PNG zamrzává**

{{< highlight java >}}

       // Uložení PSB jako PNG

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}



` `**PSDNET-250. Výjimka při načítání CMYK souboru PSD bez vrstvy s kompresí RLE**

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

` `**PSDNET-161. Výjimka při aktualizaci textových vrstev**

{{< highlight java >}}

      // Načtení souboru PSD jako obrázku a přetypování na PsdImage

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



**PSDNET-222. Změna velikosti některých souborů PSD s maskami vrstev funguje nesprávně**

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



**PSDNET-244. Uložení PSD se současným Globalization.CultureInfo.CurrentCulture vede k výjimkám při načítání**

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

            // Načtení souboru PSD jako obrázku a přetypování na PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            // Načtení souboru PSD jako obrázku a přetypování na PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}