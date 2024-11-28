---
title: Catatan Rilis Aspose.PSD untuk Java 19.4
type: docs
weight: 20
url: /id/java/aspose-psd-for-java-19-4-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk Aspose.PSD untuk Java 19.4

{{% /alert %}}

| **Kunci** | **Ringkasan** | **Kategori** |
| :- | :- | :- |
|PSDJAVA-1|Membuat fitur untuk memuat file gambar JPEG/PNG/dll ke PsdImage tanpa memuat langsung (Yang tidak didukung dalam Aspose.PSD)|Fitur|
|PSDJAVA-2|Dukungan untuk Mode Warna RGB dengan 16 bit/channel (64 bit per warna)|Fitur|
|PSDJAVA-3|Dukungan untuk Masker Vector Layer dan Putar Balik Kustom pada Layer Teks|Fitur|
|PSDJAVA-4|Semua karakter Asia tidak dirender dengan benar|Bug|
|PSDJAVA-5|Simbol \r\n diinterpretasikan sebagai double line break yang salah|Bug|
|PSDJAVA-6|Jika TextLayer diperbarui dengan string yang berisi LineBreaks, maka File PSD menjadi tidak dapat dibaca|Bug|
|PSDJAVA-7|Jika TextLayer diperbarui dengan string yang berisi simbol Tab, pemrosesan gagal dengan pengecualian|Bug|
# **Perubahan API Publik**
# **APIs yang Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)
## **APIs yang Dihapus:**
- T:Aspose.PSD.FileFormats.Gif.GifImage
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock)
- M:Aspose.PSD.FileFormats.Gif.GifImage.#ctor(Aspose.PSD.FileFormats.Gif.Blocks.GifFrameBlock,Aspose.PSD.IColorPalette,System.Boolean,System.Byte,System.Byte,System.Byte,System.Boolean)
- P:Aspose.PSD.FileFormats.Gif.GifImage.FileFormat
- P:Aspose.PSD.FileFormats.Gif.GifImage.XmpData
- P:Aspose.PSD.FileFormats.Gif.GifImage.HasTrailer
- ... (lebih lanjut dihapus)
# **Contoh Penggunaan:**

**PSDJAVA-1. Membuat fitur untuk memuat file gambar JPEG/PNG/dll ke PsdImage tanpa memuat langsung (Yang tidak didukung dalam Aspose.PSD)**

{{< highlight java >}}

 String filePath = "PsdExample.psd";

    String outputFilePath = "PsdResult.psd";

    PsdImage image = new PsdImage(200, 200);

    try 

    { 

         PsdImage im = Image.load(filePath);

         try 

         {

              Layer layer = null;

              try

              {

                  layer = new Layer((RasterImage)im);

                  image.addLayer(layer);

                  image.save(outputFilePath);

              }

              catch

              {

                  if (layer != null)

                  {

                       layer.dispose();

                  }

                  throw;

              }

         }    

         finally 
         {
              im.dispose(); 
         }
    }

    finally

    {

         image.dispose();

    }

{{< /highlight >}}

**PSDJAVA-2. Dukungan untuk Mode Warna RGB dengan 16 bit/channel (64 bit per warna)**

{{< highlight java >}}

  // Dukungan untuk Mode Warna RGB dengan 16 bit/channel (64 bit per warna)

        String sourceFileName = "inRgb16.psd.psd";

        String outputFilePathJpg = "outRgb16.jpg";

        String outputFilePathPsd = "outRgb16.psd";

        PsdLoadOptions options = new PsdLoadOptions();

        PsdImage image = (PsdImage)Image.load(sourceFileName, options);

        try

        {

            PsdOptions psdOpt = new PsdOptions(image);

            image.save(outputFilePathPsd, psdOpt);



            JpegOptions jpegOpt = new JpegOptions();

            jpegOpt.setQuality(100);

            image.save(outputFilePathJpg);

        }

        finally 

        {

             image.dispose();

        }

    // File harus dibuka tanpa pengecualian dan harus dapat dibaca oleh Photoshop    

   image = Image.load(outputFilePathPsd));

   image.dispose(); 

{{< /highlight >}}

**PSDJAVA-3. Dukungan untuk Masker Vector Layer dan Putar Balik Kustom pada Layer Teks**

{{< highlight java >}}

 // Operasi RotateFlip tidak berfungsi seperti yang diharapkan dengan PSD

    String sourceFile = "1.psd";

    String pngPath = "RotateFlipTest2617.png";

    String psdPath = "RotateFlipTest2617.psd";

    int flipType = RotateFlipType.Rotate270FlipXY;

    PsdImage im = (PsdImage)(Image.load(sourceFile));


    try

    {

        im.rotateFlip(flipType);

        PngOptions options = new PngOptions();

        options.setColorType(PngColorType.TruecolorWithAlpha);

        im.save(pngPath, options);

        im.save(psdPath);

    }

    finally 

    {

        im.dispose();

    }

{{< /highlight >}}

**PSDJAVA-4. Semua karakter Asia tidak dirender dengan benar**

[**Silakan periksa contoh terlampir**](attachments/92602686/92766213.java)

**PSDJAVA-5. Simbol \r\n diinterpretasikan sebagai double line break yang salah**

{{< highlight java >}}

 // Simbol \r\n diinterpretasikan sebagai double line break yang salah

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";



            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("Paragraf Pertama\r\nParagraf Kedua\rParagraf Ketiga\nParagraf Keempat");

                image.save(exportPath, imageOptions);

                // Gambar yang dibuat harus dibaca oleh Aspose.PSD/Aspose.Imaging dan oleh Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();

            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}



**PSDJAVA-6. Jika TextLayer diperbarui dengan string yang berisi LineBreaks, maka File PSD menjadi tidak dapat dibaca**

{{< highlight java >}}

 // Jika TextLayer diperbarui dengan string yang berisi LineBreaks, maka File PSD menjadi tidak dapat dibaca.

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";



            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {

                layer.updateText("Paragraf Pertama\r\nParagraf Kedua\r\nParagraf Ketiga\r\nParagraf Keempat");

                image.save(exportPath, imageOptions);

                // Gambar yang dibuat harus dibaca oleh Aspose.PSD/Aspose.Imaging dan oleh Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();



            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}



**PSDJAVA-7. Jika TextLayer diperbarui dengan string yang berisi simbol Tab, pemrosesan gagal dengan pengecualian**

{{< highlight java >}}

 // Jika TextLayer diperbarui dengan string yang berisi simbol Tab, pemrosesan gagal dengan pengecualian

            String sourceFileName = "TextTest.psd";

            String exportPath = "Result.psd";



            PsdImage image = (PsdImage)Image.load(sourceFileName);

            TextLayer layer = (TextLayer)image.getLayers()[0];

            PsdOptions imageOptions = new PsdOptions(image);

            try

            {
                layer.UpdateText("Text Awal\tSetelah Tab");

                image.save(exportPath, imageOptions);

                // Gambar yang dibuat harus dibaca oleh Aspose.PSD/Aspose.Imaging dan oleh Photoshop

                PsdImage createdImage = (PsdImage)Image.load(exportPath);

                createdImage.dispose();
            }

            finally

            {

                image.dispose();

            }

{{< /highlight >}}