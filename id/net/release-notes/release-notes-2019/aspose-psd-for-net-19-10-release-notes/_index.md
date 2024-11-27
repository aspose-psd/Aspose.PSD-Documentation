---
title: Catatan Rilis Aspose.PSD untuk .NET 19.10
type: dokumen
weight: 30
url: /id/net/aspose-psd-untuk-net-19-10-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk Aspose.PSD untuk .NET 19.10

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-207|[Dukungan untuk Lapisan Penyesuaian Keseimbangan Warna](/psd/id/net/modifying-images/#modifyingimages-colorbalanceadjustmentlayer)|Fitur|
|PSDNET-145|[Dukungan untuk Lapisan Penyesuaian Invert](/psd/id/net/modifying-images/#modifyingimages-invertadjustmentlayer)|Fitur|
|PSDNET-139|[Implementasi Bicubic Resampler](/psd/id/net/modifying-images/#modifyingimages-implementbicubicresampling)|Fitur|
|PSDNET-169|[Menambahkan Dukungan Eksport PSD ke PDF dengan Klipping Masker](/psd/id/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithclippingmask)|Fitur|
|PSDNET-168|[Menambahkan Dukungan Eksport PSD ke PDF dengan Lapisan Penyesuaian](/psd/id/net/convert-psd-to-other-formats/#convertpsdtootherformats-psdtopdfwithadjustmentlayer)|Fitur|
|PSDNET-179|Masalah Mendapatkan Efek Bayangan Terjatuh Lapisan|Peningkatan|
|PSDNET-203|Saat teks diperbarui dengan karakter / maju (forward slash), file tidak dapat dibuka di Photoshop|Bug|
|PSDNET-199|File PSD tidak dapat disimpan saat lapisan teks hanya berisi jeda baris|Bug|
|PSDNET-185|Ukuran Font yang Diekstrak Salah|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.ColorBalanceAdjustmentLayer.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.InvertAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.PreserveLuminosity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.ShadowsYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.MidtonesYellowBlueBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsCyanRedBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsMagentaGreenBalance
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.BlncResource.HighlightsYellowBlueBalance
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.NvrtResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.TransformMatrix
- P:Aspose.PSD.FileFormats.Psd.PsdImage.GlobalAngle
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddColorBalanceAdjustmentLayer
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddInvertAdjustmentLayer
- F:Aspose.PSD.ResizeType.CatmullRom
- F:Aspose.PSD.ResizeType.CubicConvolution
- F:Aspose.PSD.ResizeType.CubicBSpline
- F:Aspose.PSD.ResizeType.Mitchell
- F:Aspose.PSD.ResizeType.SinC
- F:Aspose.PSD.ResizeType.Bell
# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**
**PSDNET-207. Dukungan untuk Lapisan Penyesuaian Keseimbangan Warna**

{{< highlight java >}}

            var filePath = "ColorBalance.psd";

            var outputPath = "ColorBalance_out.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                foreach (var layer in im.Layers)

                {

                    var cbLayer = layer as ColorBalanceAdjustmentLayer;

                    if (cbLayer != null)

                    {

                        cbLayer.ShadowsCyanRedBalance = 30;

                        cbLayer.ShadowsMagentaGreenBalance = -15;

                        cbLayer.ShadowsYellowBlueBalance = 40;

                        cbLayer.MidtonesCyanRedBalance = -90;

                        cbLayer.MidtonesMagentaGreenBalance = -25;

                        cbLayer.MidtonesYellowBlueBalance = 20;

                        cbLayer.HighlightsCyanRedBalance = -30;

                        cbLayer.HighlightsMagentaGreenBalance = 67;

                        cbLayer.HighlightsYellowBlueBalance = -95;

                        cbLayer.PreserveLuminosity = true;

                    }

                }

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-145. Dukungan untuk Lapisan Penyesuaian Invert**

{{< highlight java >}}

            var filePath = "InvertStripes_sebelum.psd";

            var outputPath = "InvertStripes_sesudah.psd";

            using (var im = (PsdImage)Image.Load(filePath))

            {

                im.AddInvertAdjustmentLayer();

                im.Save(outputPath);

            }

{{< /highlight >}}

**PSDNET-139. Implementasi Bicubic Resampler**

{{< highlight java >}}

             string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerCubicConvolutionStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.CubicConvolution);

                image.Save(namaTujuan, new PsdOptions(image));

            }

            string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerCatmullRomStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.CatmullRom);

                image.Save(namaTujuan, new PsdOptions(image));

            }

            string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerMitchellStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.Mitchell);

                image.Save(namaTujuan, new PsdOptions(image));

            }

            string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerCubicBSplineStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.CubicBSpline);

                image.Save(namaTujuan, new PsdOptions(image));

            }

            string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerSinCStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.SinC);

                image.Save(namaTujuan, new PsdOptions(image));

            }

            string fileSumber = "contoh.psd";

            string namaTujuan = "ResamplerBellStripes_sesudah.psd";

            // Memuat gambar yang ada ke dalam instansi kelas PsdImage

            using (PsdImage image = (PsdImage)Image.Load(fileSumber))

            {

                image.Resize(300, 300, ResizeType.Bell);

                image.Save(namaTujuan, new PsdOptions(image));

            }

{{< /highlight >}}

**PSDNET-169. Menambahkan Dukungan Eksport PSD ke PDF dengan Klipping Masker**

{{< highlight java >}}

     using (PsdImage image = (PsdImage)Image.Load("klipping.psd"))

    {

      image.Save("output.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-168. Menambahkan Dukungan Eksport PSD ke PDF dengan Lapisan Penyesuaian**

{{< highlight java >}}

      using (PsdImage image = (PsdImage)Image.Load("contoh.psd"))

    {

      image.Save("dokumen.pdf", new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-203. Saat teks diperbarui dengan karakter / (maju), file tidak dapat dibuka di Photoshop**

{{< highlight java >}}

         var psdImage = (PsdImage)image;

        var layers = psdImage.Layers;

        for (var index = layers.Length - 1; index >= 0; index--)

        {

            var layer = layers[index];

            if (!(layer is TextLayer)) continue;

            var textLayer = (TextLayer)layer;

            textLayer.UpdateText("/");

        }

        var imageOptions = new PsdOptions(psdImage);

        var fileName = Path.GetFileName(filePath);

        var outputFilePath = Path.GetDirectoryName(filePath) + "\\target_" + fileName;

        psdImage.Save(outputFilePath, imageOptions);

{{< /highlight >}}

**PSDNET-199. File PSD tidak dapat disimpan saat lapisan teks hanya berisi jeda baris**

{{< highlight java >}}

 string filePath = "ujicontohJedaBaris2.psd";

string outputPath = "ujicontohJedaBaris2_diubah.psd";

var teksBaru = "\r";

        using (var image = Image.Load(filePath))

        {

            var psdImage = image as PsdImage;

            if (image == null)

            {

                return;

            }

            var layers = psdImage.Layers;

            for (var index = layers.Length - 1; index >= 0; index--)

            {

                var layer = layers[index] as TextLayer;

                if (layer == null)

                {

                    continue;

                }

                layer.UpdateText(teksBaru);

            }

            var imageOptions = new PsdOptions(psdImage);

            psdImage.Save(outputPath, imageOptions);

        }

{{< /highlight >}}

**PSDNET-185. Ukuran Font yang Diekstrak Salah**

{{< highlight java >}}

             // Ukuran Font yang Diekstrak Salah

            string filePath = "直播+电商.psd";

            var toleransi = 0.001;

            using (var image = Image.Load(filePath))

            {

                int indeksLayer = 22;

                // API Lama (Menggunakan ukuran font paragraf pertama)

                PsdImage psdImage = image as PsdImage;

                double[] matriks = ((TextLayer)psdImage.Layers[indeksLayer]).TransformMatrix;

                double ukuranDasarFont = ((TextLayer)psdImage.Layers[indeksLayer]).Font.Size;

                double ukuranFont = matriks[0] * ukuranDasarFont;

                // Memeriksa ukuran font dasar

                if (Math.Abs(100.0 - ukuranDasarFont) > toleransi)

                {

                    throw new Exception("Ukuran font tidak terbaca dengan benar");

                }

                // Memeriksa ukuran font nyata

                if (Math.Abs(88.425 - ukuranFont) > toleransi)

                {

                    throw new Exception("TransformMatrix tidak terbaca dengan benar");

                }

                // API Baru (Satu lapisan teks dapat berisi berbagai ukuran font)

                ITextPortion[] bagian = ((TextLayer)psdImage.Layers[indeksLayer]).TextData.Items;

                ITextStyle gaya = bagian[0].Style;

                double ukuranFontBagian = matriks[0] * gaya.FontSize;

                // Memeriksa ukuran font bagian dasar

                if (Math.Abs(100.0 - gaya.FontSize) > toleransi)

                {

                    throw new Exception("Ukuran font tidak terbaca dengan benar");

                }

                // Memeriksa ukuran font bagian nyata

                if (Math.Abs(88.425 - ukuranFontBagian) > toleransi)

                {

                    throw new Exception("TransformMatrix tidak terbaca dengan benar");

                }

            }

{{< /highlight >}}

**PSDNET-179. Masalah Mendapatkan Efek Bayangan Terjatuh Lapisan**

{{< highlight java >}}

       // Saat properti DropShadowEffect.UseGlobalLight adalah 'true', maka objek DropShadowEffect akan menggunakan nilai sudut dari properti PsdImage.GlobalAngle.

		using (PsdImage image = (PsdImage)Image.Load("4.psd"))

		{

    		image.GlobalAngle = 30;

    		image.Save("output.psd");

		}

{{< /highlight >}}