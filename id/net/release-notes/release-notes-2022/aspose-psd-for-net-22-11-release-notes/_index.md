---
title: Catatan Rilis Aspose.PSD untuk .NET 22.11
type: docs
weight: 20
url: /id/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Rilis ini memiliki regresi dalam kasus ekspor 16-bit, oleh karena itu kami menyarankan untuk berhati-hati saat menggunakan fitur ini dalam rilis ini. Mohon untuk tidak memperbarui Aspose.PSD ke 22.9-22.11 jika pemrosesan gambar 16-bit adalah fungsionalitas utama Anda.

Kami sedang mengupayakan solusi untuk masalah-masalah ini.

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1320|Tidak dapat mengekspor file PSB yang sangat besar|Peningkatan|
|PSDNET-659|Membuat pusat gradasi radial dapat dipindahkan|Fitur|
|PSDNET-1330|Metode kompresi ZipWithoutPrediction tidak didukung untuk file-file tertentu|Fitur|
|PSDNET-735|Setelah menggunakan metode transformasi hanya untuk sebuah lapisan, lapisan yang disimpan memiliki kotak pembatas yang salah|Bug|
|PSDNET-1234|Exception saat memuat gambar PSD dengan pola|Bug|
|PSDNET-1244|Ekspor gambar gagal (IndexOutOfRangeException) saat menyimpan file PSD dengan simbol Tiongkok|Bug|
|PSDNET-1303|TimeLine ActiveFrame diterapkan secara tidak benar|Bug|
|PSDNET-1307|Regresi 22.7: rendering teks dengan karakter Arab yang tidak benar|Bug|
|PSDNET-1321|Masker Vektor pada Layer Grup bekerja dengan tidak benar. Gambar akhir memiliki lubang hitam tetapi seharusnya tidak|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDNET-659. Membuat pusat gradasi radial dapat dipindahkan**

{{< highlight csharp >}}
string fileSumber = "psdnet659.psd";
string fileKeluaran = "output.png";

using (var gambarPsd = (PsdImage)Image.Load(fileSumber))
{
    FillLayer lapisanGradien = (FillLayer)gambarPsd.Layers[5];
    GradientFillSettings pengaturan = (GradientFillSettings)lapisanGradien.FillSettings;

    // Memperbarui titik offset
    pengaturan.HorizontalOffset = 10;
    pengaturan.VerticalOffset = -25;

    gambarPsd.Save(fileKeluaran, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Setelah menggunakan metode transformasi hanya untuk sebuah lapisan, lapisan yang disimpan memiliki kotak pembatas yang salah**

{{< highlight csharp >}}
string namaFileSumber = @"TextLayer.psd";
string fileKeluaran = "TextLayerResized_output.psd";

using (PsdImage gambar = (PsdImage)Image.Load(namaFileSumber, new PsdLoadOptions()))
{
    TextLayer lapisanTeks = (TextLayer)gambar.Layers[1];

    // Menetapkan ukuran baru untuk lapisan teks
    const int LebarBaru = 250;
    const int TinggiBaru = 250;

    // Menetapkan mekanisme bagaimana fungsi resize akan mengubah ukuran lapisan (default)
    ResizeType jenisResize = ResizeType.NearestNeighbourResample;

    // Mekanisme baru dari resizing untuk lapisan teks digunakan di sini
    // Tidak hanya lapisan tetapi juga matriks transformasi dari lapisan teks akan berubah
    lapisanTeks.Resize(LebarBaru, TinggiBaru, jenisResize);

    gambar.Save(fileKeluaran, new PsdOptions(gambar));
}

using (PsdImage gambar = (PsdImage)Image.Load(fileKeluaran, new PsdLoadOptions()))
{
    TextLayer lapisanTeks = (TextLayer)gambar.Layers[1];

    // Alasan delta adalah font default yang berbeda
    if (lapisanTeks.TransformMatrix[4] >= 65 
        && lapisanTeks.TransformMatrix[4] <= 67
        && lapisanTeks.TransformMatrix[5] >= 234
        && lapisanTeks.TransformMatrix[5] <= 237)
    {
        // Semuanya baik-baik saja
    }
    else
    {
        throw new Exception("Titik lokasi salah");
    }
}
{{< /highlight >}}

**PSDNET-1234. Exception saat memuat gambar PSD dengan pola**

{{< highlight csharp >}}
string fileSumber = "test.psd";
string keluaran = "output1234.png";

using (PsdImage gambarPsd = (PsdImage)PsdImage.Load(fileSumber,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pengaturanPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    gambarPsd.Save(keluaran, pengaturanPng);
}
{{< /highlight >}}

**PSDNET-1244. Ekspor gambar gagal (IndexOutOfRangeException) saat menyimpan file PSD dengan simbol Tiongkok**

{{< highlight csharp >}}
string fileSumber = "input.psd";
string jalurKeluaran = "output.psd";

var opsiMuat = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var gambar = (PsdImage)Image.Load(fileSumber, opsiMuat))
{
    foreach (var lapisan in gambar.Layers)
    {
        if (lapisan.Name == "1")
        {
            var lapisanTeks = (TextLayer)lapisan;

            lapisanTeks.UpdateText("测试测试");
        }
    }

    // Di sini seharusnya tidak ada pengecualian.
    gambar.Save(jalurKeluaran, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame diterapkan secara tidak benar**

{{< highlight csharp >}}
string sumber = "timeline1303.psd";
string keluaran = "out_timeline.psd";

using (var gambarPsd = (PsdImage)Image.Load(sumber))
{
    TimeLine timeLine = TimeLine.InitializeFrom(gambarPsd);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(gambarPsd);

    gambarPsd.Save(keluaran);
}
{{< /highlight >}}

**PSDNET-1307. Regresi 22.7: rendering teks dengan karakter Arab yang tidak benar**

{{< highlight csharp >}}
string folderFontUji = "Fonts";
FontSettings.SetFontsFolder(folderFontUji);
FontSettings.UpdateFonts();

string jalurFileSumber = "sarbarg.fin12.psd";
string jalurFileKeluaran = "result.tiff";

using (var gambarPsd = (PsdImage)Image.Load(jalurFileSumber))
{
    gambarPsd.Save(jalurFileKeluaran, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Tidak dapat mengekspor file PSB yang sangat besar**

{{< highlight csharp >}}
string fileSumber = "hf-mim-liman-han-guc-art-kuvvet.psb";
string jalurPengeksporanPsd = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var gambar = (PsdImage)Image.Load(fileSumber, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    gambar.Save(jalurPengeksporanPsd, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Masker Vektor pada Layer Grup bekerja dengan tidak benar. Gambar akhir memiliki lubang hitam tetapi seharusnya tidak**

{{< highlight csharp >}}
string fileSumber = "demo.psd";
string keluaran = "demo_net.png";

using (PsdImage gambar = (PsdImage)PsdImage.Load(fileSumber))
{
    PngOptions pengaturanPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    gambar.Save(keluaran, pengaturanPng);
}
{{< /highlight >}}

**PSDNET-1330. Metode kompresi ZipWithoutPrediction tidak didukung untuk file-file tertentu**

{{< highlight csharp >}}
string fileSumber = "20221017_220706_0000.psd";
string keluaranFile = "20221017_220706_0000.jpg";

using (var gambar = (PsdImage)Image.Load(fileSumber, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase opsiGambar = new JpegOptions() { Quality = 80 };
    gambar.Save(keluaranFile, opsiGambar);
}
{{< /highlight >}}
