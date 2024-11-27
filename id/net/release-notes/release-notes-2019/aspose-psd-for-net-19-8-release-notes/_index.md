---
title: Catatan Rilis Aspose.PSD untuk .NET 19.8
type: docs
weight: 50
url: /id/net/aspose-psd-untuk-net-19-8-catatan-rilis/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk Aspose.PSD untuk .NET 19.8

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-184|Memuat file gambar JPEG, PNG, dan lainnya ke PsdImage dari stream|Fitur|
|PSDNET-134|Mengimplementasikan rendering Fill Layer: Gradient|Fitur|
|PSDNET-166|Menyimpan PSD ke PDF tanpa menyediakan teks yang dapat dipilih|Fitur|
|PSDNET-158|Dukungan untuk menyimpan PSB sebagai PDF|Fitur|
|PSDNET-189|Penggunaan memori tinggi saat memuat PSD dengan Mode Baca Saja|Perbaikan|
|PSDNET-171|Setelah membuat TextLayer baru, file PSD menjadi tidak terbaca oleh PS|Bug|
|PSDNET-156|Exception saat memuat PSD|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **API Dihapus:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Contoh Penggunaan:**
**PSDNET-184. Memuat file gambar JPEG, PNG, dan lainnya ke PsdImage dari stream**

{{< highlight java >}}

    // load JPEG, PNG, dan file gambar lainnya ke PsdImage dari stream

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

**PSDNET-134. Mengimplementasikan rendering Fill Layer: Gradient**

{{< highlight java >}}

             // Implementasikan rendering Fill Layer: Gradient

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

**PSDNET-166. Menyimpan PSD ke PDF tanpa menyediakan teks yang dapat dipilih**

{{< highlight java >}}

  // Menyimpan PSD ke PDF tanpa menyediakan teks yang dapat dipilih

    string sourceFileName = "text.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "text.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Setelah membuat TextLayer baru, file PSD menjadi tidak terbaca oleh PS**

{{< highlight java >}}

 // Setelah membuat TextLayer baru di Build Server, File PSD menjadi tidak terbaca oleh PS

    string sourceFileName = "OneLayer.psd";

    string outFileName = "OneLayerWithAddedText.psd";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        image.AddTextLayer("Some text", new Rectangle(50, 50, 100, 100));

        PsdOptions options = new PsdOptions(image);

        image.Save(outFileName, options);

    }

{{< /highlight >}}



**PSDNET-156. Exception saat memuat PSD**

{{< highlight java >}}

 using (var image = Image.Load("isolated_Copy.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Penggunaan memori tinggi saat memuat PSD dengan Mode Baca Saja**

{{< highlight java >}}

 // Penggunaan memori tinggi dari Aspose.PSD saat memuat PSD dengan Mode Baca Saja

            string sourceFileName = "White 3D Text Effect.psd";

            string outFileName = "Exported.png";

            LoadOptions loadOptions = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase saveOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

            {

                image.Save(outFileName, saveOptions);

            }

            double memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Penggunaan memori harus kurang dari 100 MB untuk contoh ini

            if (memoryUsed > 100)

            {

                throw new Exception("Penggunaan memori terlalu besar");

            }

{{< /highlight >}}

**PSDNET-158. Dukungan untuk menyimpan PSB sebagai PDF**

{{< highlight java >}}

 // Dukungan untuk menyimpan PSB sebagai PDF

    string sourceFileName = "sample.psb";

    using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

    {

        string outFileName = "sample.pdf";

        image.Save(outFileName, new PdfOptions());

    }

{{< /highlight >}}
