---
title: Catatan Rilis Aspose.PSD untuk Java 20.5
type: docs
weight: 40
url: /id/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-188|Dukungan untuk kemajuan konversi dokumen|Fitur|
|PSDJAVA-197|Dukungan untuk Penyimpanan Gambar PSD Mode Warna Grayscale dengan 16 bit per channel|Fitur|
|PSDJAVA-198|Dukungan untuk Sumber Daya Nvrt (Penyesuaian Lapisan Balik Invert)|Fitur|
|PSDJAVA-200|Dukungan untuk Masker Lapisan untuk Kelompok Lapisan|Fitur|
|PSDJAVA-195|Perbaikan saat menyimpan gambar PSD dengan Mode Warna Grayscale 16 bit per channel menjadi format PSD RGB 16 bit per channel|Kesalahan|
|PSDJAVA-196|Perbaikan saat menyimpan gambar PSD dengan Mode Warna Grayscale 16 bit per channel menjadi format PSD Grayscale 8 bit per channel|Kesalahan|
|PSDJAVA-199|Pengaturan Teks melalui ITextPortion tidak berfungsi untuk bahasa kanan-ke-kiri. Berkas keluaran rusak.|Kesalahan|
|PSDJAVA-201|Pengecualian saat mencoba membuka file Psd tertentu dengan Warna Lab dan 8 bit/channel|Kesalahan|
# **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada
## **API Dihapus:**
- Tidak ada
# **Contoh Penggunaan:**

**PSDJAVA-188. Dukungan untuk kemajuan konversi dokumen**

{{< highlight java >}}

 // Contoh penggunaan penangan progres untuk operasi memuat dan menyimpan.

// Program menggunakan opsi penyimpanan yang berbeda untuk memunculkan peristiwa progres.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// Buat penangan progres yang menulis info progres ke konsol

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s dari %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

};

System.out.println("---------- Memuat Apple.psd ----------");

PsdLoadOptions loadOptions = new PsdLoadOptions();

// Bind penangan progres untuk menampilkan progres memuat

loadOptions.setProgressEventHandler(localProgressEventHandler);

// Memuat PSD menggunakan opsi memuat spesifik

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- Menyimpan Apple.psd ke format PNG ----------");

    PngOptions pngOptions = new PngOptions();

    // Buat gambar output berwarna dan tidak transparan

    pngOptions.setColorType(PngColorType.Truecolor);

    // Bind penangan progres untuk menampilkan progres penyimpanan

    pngOptions.setProgressEventHandler(localProgressEventHandler);

    // Konversi PSD ke PNG dengan karakteristik spesifik

    image.save(outputStream, pngOptions);

    System.out.println("---------- Menyimpan Apple.psd ke format PSD ----------");

    PsdOptions psdOptions = new PsdOptions();

    // Buat PSD output berwarna

    psdOptions.setColorMode(ColorModes.Rgb);

    // Tetapkan satu saluran untuk setiap warna (merah, hijau, dan biru) ditambah saluran komposit

    psdOptions.setChannelsCount((short)4);

    // Bind penangan progres untuk menampilkan progres penyimpanan

    psdOptions.setProgressEventHandler(localProgressEventHandler);

    // Simpan salinan PSD dengan karakteristik spesifik

    image.save(outputStream, psdOptions);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-197. Dukungan Penyimpanan Gambar Mode Warna Grayscale PSD dengan 16 bit per channel**

{{< highlight java >}}

 // Contoh penerapan kombinasi mode warna, bit per channel, hitung saluran, dan kompresi untuk lapisan spesifik.

// Buat sebuah metode dapat diakses dari cakupan lokal

class LocalScopeExtension

{

    void saveToPsdThenLoadAndSaveToPng(

            String file,

            short colorMode,

            short channelBitsCount,

            short channelsCount,

            short compression,

            int layerNumber)

    {

        String filePath = file + ".psd";

        String postfix = Enum.getName(ColorModes.class, colorMode) + channelBitsCount + "_" +

                channelsCount + "_" + Enum.getName(CompressionMethod.class, compression);

        String exportPath = file + postfix + ".psd";

        String pngExportPath = file + postfix + ".png";

        // Memuat PSD grayscale 16 bit yang telah ditentukan

        PsdImage image = (PsdImage)Image.load(filePath);

        try

        {

            RasterCachedImage raster = layerNumber >= 0 ? image.getLayers()[layerNumber] : image;

            // Gambar batas dalam abu-abu sekitar perimeter lapisan

            Graphics graphics = new Graphics(raster);

            int width = raster.getWidth();

            int height = raster.getHeight();

            Rectangle rect = new Rectangle(

                    width / 3,

                    height / 3,

                    width - (2 * (width / 3)) - 1,

                    height - (2 * (height / 3)) - 1);

            graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

            // Simpan salinan PSD dengan karakteristik spesifik

            PsdOptions psdOptions = new PsdOptions();

            psdOptions.setColorMode(colorMode);

            psdOptions.setChannelBitsCount(channelBitsCount);

            psdOptions.setChannelsCount(channelsCount);

            psdOptions.setCompressionMethod(compression);

            image.save(exportPath, psdOptions);

        }

        finally

        {

            image.dispose();

        }

        // Memuat PSD yang disimpan

        PsdImage image1 = (PsdImage)Image.load(exportPath);

        try

        {

            // Ubah PSD yang disimpan menjadi gambar PNG grayscale

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

            image1.save(pngExportPath, pngOptions); // di sini tidak boleh ada pengecualian

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

$.saveToPsdThenLoadAndSaveToPng("grayscale5x5", ColorModes.Cmyk, (short)16, (short)5, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, 0);

$.saveToPsdThenLoadAndSaveToPng("argb8bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("cmyk16bit_5x5_no_layers", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

$.saveToPsdThenLoadAndSaveToPng("index8bit_5x5", ColorModes.Grayscale, (short)16, (short)2, CompressionMethod.RLE, -1);

{{< /highlight >}}

**PSDJAVA-198. Dukungan Sumber Daya Nvrt (Penyesuaian Lapisan Balik Invert)**

{{< highlight java >}}

 // Contoh menemukan Sumber Daya Nvrt dari suatu lapisan penyesuaian balik invert.

String inPsdFilePath = "InvertAdjustmentLayer.psd";

NvrtResource nvrtResource = null;

// Memuat PSD yang telah ditentukan berisi lapisan penyesuaian balik invert

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Mencoba menemukan sumber daya dari lapisan penyesuaian balik invert

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof InvertAdjustmentLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof NvrtResource)

                {

                    // Sumber Daya Nvrt ditemukan

                    nvrtResource = (NvrtResource)layerResource;

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-200. Dukungan Masker Lapisan untuk Kelompok Lapisan**

{{< highlight java >}}

 // Contoh dukungan masker lapisan untuk kelompok lapisan. Program memuat dan menyimpan PSD

// ke format output yang berbeda tanpa melemparkan pengecualian.

String srcFile = "psdnet595.psd";

String outputPng = "output.png";

String outputPsd = "output.psd";

// Memuat PSD yang telah ditentukan berisi masker lapisan untuk kelompok lapisan

PsdImage input = (PsdImage)Image.load(srcFile);

try

{

    // Mengonversi PSD yang dimuat ke PNG

    input.save(outputPng, new PngOptions());

    // Simpan salinan dari PSD

    input.save(outputPsd);

}

finally

{

    input.dispose();

}

{{< /highlight >}}

**PSDJAVA-195. Perbaikan saat menyimpan gambar PSD dengan Mode Warna Grayscale 16 bit per channel menjadi format PSD RGB 16 bit per channel**

{{< highlight java >}}

 // Contoh mengonversi PSD grayscale 16 bit ke RGB 16 bit dan kemudian kembali ke

// gambar raster grayscale 16 bit.

String sourceFilePath = "grayscale5x5.psd";

String exportFilePath = "rgb16bit5x5_output.psd";

String pngExportPath = "rgb16bit5x5_output.png";

// Memuat PSD grayscale 16 bit yang telah ditentukan

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Gambar batas abu-abu di sekitar perimeter lapisan

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Simpan salinan PSD dengan mode warna diubah menjadi RBG

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Rgb);

    psdOptions.setChannelBitsCount((short)16);

    psdOptions.setChannelsCount((short)4);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Memuat PSD yang disimpan

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konversi PSD yang disimpan ke gambar PNG grayscale

    image1.save(pngExportPath, pngOptions); // di sini tidak boleh ada pengecualian

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-196. Perbaikan saat menyimpan gambar PSD dengan Mode Warna Grayscale 16 bit per channel menjadi format PSD Grayscale 8 bit per channel**

{{< highlight java >}}

 // Contoh mengonversi PSD grayscale 16 bit ke grayscale 8 bit dan kemudian ke

// gambar raster grayscale 8 bit.

String sourceFilePath = "grayscale16bit.psd";

String exportFilePath = "grayscale16bit_output.psd";

String pngExportPath = "grayscale16bit_output.png";

// Memuat PSD grayscale 16 bit yang telah ditentukan

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    RasterCachedImage raster = image.getLayers()[0];

    // Gambar batas abu-abu di sekitar perimeter lapisan

    Graphics graphics = new Graphics(raster);

    int width = raster.getWidth();

    int height = raster.getHeight();

    Rectangle rect = new Rectangle(width / 3, height / 3, width - (2 * (width / 3)) - 1, height - (2 * (height / 3)) - 1);

    graphics.drawRectangle(new Pen(Color.getDarkGray(), 1), rect);

    // Simpan salinan PSD dengan jumlah saluran diubah menjadi 8-bit

    PsdOptions psdOptions = new PsdOptions();

    psdOptions.setColorMode(ColorModes.Grayscale);

    psdOptions.setChannelBitsCount((short)8);

    psdOptions.setChannelsCount((short)2);

    image.save(exportFilePath, psdOptions);

}

finally

{

    image.dispose();

}

// Memuat PSD yang disimpan

PsdImage image1 = (PsdImage)Image.load(exportFilePath);

try

{

    PngOptions pngOptions = new PngOptions();

    pngOptions.setColorType(PngColorType.GrayscaleWithAlpha);

    // Konversi PSD yang disimpan ke gambar PNG grayscale

    image1.save(pngExportPath, pngOptions); // di sini tidak boleh ada pengecualian

}

finally

{

    image1.dispose();

}

{{< /highlight >}}

**PSDJAVA-199. Pengaturan Teks melalui ITextPortion tidak berfungsi untuk bahasa kanan-ke-kiri. Berkas keluaran rusak.**

{{< highlight java >}}

 // Contoh menyesuaikan lapisan teks RTL melalui ITextPortion. Program memodifikasi

// lapisan teks RTL yang ada di PSD yang dimuat dan menyimpan salinan dokumen yang dimodifikasi.

String sourceFileName = "bidi.psd";

String outputFileName = "bidiOutput.psd";

// Memuat PSD yang telah ditentukan berisi lapisan teks RTL

PsdImage image = (PsdImage)Image.load(sourceFileName);

try

{

    // Dapatkan bagian teks dari lapisan

    TextLayer layer = (TextLayer)image.getLayers()[2];

    ITextPortion[] portions = layer.getTextData().getItems();

    // Ubah penjajaran teks

    portions[0].getParagraph().setJustification(2);

    // Terapkan perubahan ke lapisan

    layer.getTextData().updateLayerData();

    // Simpan salinan yang dimodifikasi dari PSD

    image.save(outputFileName);

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-201. Pengecualian saat mencoba membuka file Psd tertentu dengan Warna Lab dan 8 bit/channel**

{{< highlight java >}}

 // Contoh dukungan dokumen Photoshop 8-bit dalam mode warna LAB.

String srcFile = "Untitled-1.psd";

String outputFilePsd = "output.psd";

// Memuat PSD 8-bit tertentu dalam mode warna LAB

PsdImage psdImage = (PsdImage)Image.load(srcFile);

try

{

    // Simpan salinan dari PSD yang dimuat

    psdImage.save(outputFilePsd);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}