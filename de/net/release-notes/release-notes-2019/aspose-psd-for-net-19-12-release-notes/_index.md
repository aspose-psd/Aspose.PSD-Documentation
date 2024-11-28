---
title: Aspose.PSD für .NET 19.12 - Versionshinweise
type: docs
weight: 10
url: /de/net/aspose-psd-fuer-net-19-12-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Schlüssel**|**Zusammenfassung**|**Kategorie**|
| :- | :- | :- |
|PSDNET-11|[Unterstützung von Linked Layer](/psd/de/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Funktion|
|PSDNET-131|[Unterstützung von SoCoResource](/psd/de/net/support-of-socoresource/)|Funktion|
|PSDNET-115|Zeilenumbrüche werden den vorhandenen Zeilenumbrüchen hinzugefügt, wenn ein TextLayer mit einem String aktualisiert wird|Fehler|
|PSDNET-157|Einfrieren beim Speichern von PSB als PNG|Fehler|
|PSDNET-250|Ausnahme beim Laden einer CMYK-PSD-Datei ohne Ebenen mit RLE-Komprimierung|Fehler|
|PSDNET-161|Ausnahme beim Aktualisieren von Textebenen|Fehler|
|PSDNET-222|Skalierung einiger PSD-Dateien mit Ebenenmasken funktioniert falsch|Fehler|
|PSDNET-244|Das Speichern einer PSD mit Globalization.CultureInfo.CurrentCulture führt zu Ausnahmen beim Laden|Fehler|

## **Änderungen an der öffentlichen API**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Entfernte APIs:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Anwendungsbeispiele:**
**PSDNET-11. Unterstützung von Linked Layer**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("example.psd"))

            {

                Layer[] layers = psd.Layers;

                // alle Ebenen in einer Linked-Gruppe verlinken

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // ID für eine Ebene abrufen

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId und linkGroupId sind nicht gleich.");

                }

                // alle verknüpften Ebenen anhand der Verknüpfungsgruppen-ID abrufen.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // jede Ebene aus der Gruppe trennen

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // für eine Verknüpfungsgruppen-ID, die keine Ebenen in der Gruppe hat, NULL abrufen

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("Das Feld linkedLayers ist nicht NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}


**PSDNET-131. Unterstützung von SoCoResource**

{{< highlight java >}}

      // Unterstützung von SoCoResource

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


**PSDNET-115. Zeilenumbrüche werden den vorhandenen Zeilenumbrüchen hinzugefügt, wenn ein TextLayer mit einem String aktualisiert wird**

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

                throw new InvalidDataException("Aktualisierter Text ist ungültig");

            }

        }

{{< /highlight >}}


**PSDNET-157. Einfrieren beim Speichern von PSB als PNG**

{{< highlight java >}}

       // Speichern von PSB als PNG

    string sourceFileName = "sample.psb";

    string outFileName = "sample.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}


` ` **PSDNET-250. Ausnahme beim Laden einer CMYK-PSD-Datei ohne Ebene mit RLE-Komprimierung**

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


` ` **PSDNET-161. Ausnahme beim Aktualisieren von Textebenen**

{{< highlight java >}}

      // Laden einer PSD-Datei als Bild und Casten in PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("example.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("Test aktualisieren", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("UpdateTextLayerInPSDFile_out.psd");

    }

{{< /highlight >}}


**PSDNET-222. Skalierung einiger PSD-Dateien mit Ebenenmasken funktioniert falsch**

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


**PSDNET-244. Das Speichern einer PSD mit Globalization.CultureInfo.CurrentCulture führt zu Ausnahmen beim Laden**

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

            // Laden einer PSD-Datei als Bild und Casten in PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentUICulture = culture;

            // Laden einer PSD-Datei als Bild und Casten in PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}
