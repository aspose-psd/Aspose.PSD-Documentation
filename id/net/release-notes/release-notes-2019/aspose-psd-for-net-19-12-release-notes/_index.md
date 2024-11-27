---
title: Catatan Rilis Aspose.PSD untuk .NET 19.12 
type: docs
weight: 10
url: /id/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-11|[Dukungan untuk Layer Terhubung](/psd/id/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Fitur|
|PSDNET-131|[Dukungan untuk SoCoResource](/psd/id/net/support-of-socoresource/)|Fitur|
|PSDNET-115|LineBreaks ditambahkan ke LineBreaks yang ada jika TextLayer diperbarui dengan string|Bug|
|PSDNET-157|Menyimpan PSB sebagai PNG membeku|Bug|
|PSDNET-250|Exception saat memuat file PSD CMYK tanpa layer dengan kompresi RLE|Bug|
|PSDNET-161|Exception saat memperbarui layer teks|Bug|
|PSDNET-222|Mengubah skala beberapa file PSD dengan layer mask bekerja tidak benar|Bug|
|PSDNET-244|Menyimpan PSD dengan beberapa Globalization.CultureInfo.CurrentCulture menyebabkan pengecualian saat memuat|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **API Dihapus:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Contoh Penggunaan:**
**PSDNET-11. Dukungan untuk Layer Terhubung**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("contoh.psd"))

            {

                Layer[] layers = psd.Layers;

                // menghubungkan semua layer dalam satu grup terhubung

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // mendapatkan id untuk satu layer

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId dan linkGroupId tidak sama.");

                }

                // mendapatkan semua layer yang terhubung berdasarkan id grup terhubung.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // membatalkan penghubungan setiap layer dari grup

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // mengembalikan NULL untuk id grup yang tidak memiliki layer dalam grup.

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("Bidang linkedLayers tidak NULL.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. Dukungan untuk SoCoResource**

{{< highlight java >}}

      // Dukungan untuk SoCoResource

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

**PSDNET-115. LineBreaks ditambahkan ke LineBreaks yang ada jika TextLayer diperbarui dengan string**

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

                throw new InvalidDataException("Teks yang diperbarui tidak valid");

            }

        }

{{< /highlight >}}

**PSDNET-157. Menyimpan PSB sebagai PNG membeku**

{{< highlight java >}}

       // Menyimpan PSB sebagai PNG 

    string sourceFileName = "contoh.psb";

    string outFileName = "contoh.png";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        PngOptions options = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        image.Save(outFileName, options);

    }

{{< /highlight >}}



` `**PSDNET-250. Exception saat memuat file PSD CMYK tanpa layer dengan kompresi RLE**

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



` `**PSDNET-161. Exception saat memperbarui layer teks**

{{< highlight java >}}

      // Memuat file PSD sebagai gambar dan mengonversinya ke PsdImage

    using (PsdImage psdImage = (PsdImage)Image.Load("contoh.psd"))

    {

        foreach (var layer in psdImage.Layers)

        {

            if (layer is TextLayer)

            {

                TextLayer textLayer = layer as TextLayer;

                textLayer.UpdateText("tes pembaruan", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdImage.Save("PerbaruiTextLayerDalamFilePSD_keluaran.psd");

    }

{{< /highlight >}}



**PSDNET-222. Mengubah skala beberapa file PSD dengan layer mask bekerja tidak benar**

{{< highlight java >}}

     int scale = 2;

        string[] names = {

                             "SatuRegulerDanSatuPenyesuaianDenganVektorDanLayerMask",

                             "LayerLevelDenganLayerMaskRgb",

                             "LayerLevelDenganLayerMaskCmyk",

                             "LayerPenyesuaianKeseimbanganWarna"

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



**PSDNET-244. Menyimpan PSD dengan beberapa Globalization.CultureInfo.CurrentCulture menyebabkan pengecualian saat memuat**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string sourceFileName = string.Format("contoh-{0}.psd", i);

            var psdLoadOptions = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdSaveOptions = new PsdOptions();

            var culture = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentThread.CurrentUICulture = culture;

            string outputFileName = "keluaran-" + sourceFileName;

            // Memuat file PSD sebagai gambar dan mengonversinya ke PsdImage

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image.Resize(160, 120);

                image.Save(outputFileName, psdSaveOptions);

            }

            culture = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = culture;

            System.Threading.Thread.CurrentUICulture = culture;

            // Memuat file PSD sebagai gambar dan mengonversinya ke PsdImage

            using (PsdImage image2 = (PsdImage)Image.Load(sourceFileName, psdLoadOptions))

            {

                image2.Resize(160, 120);

                image2.Save(outputFileName, psdSaveOptions);

            }

        }

{{< /highlight >}}