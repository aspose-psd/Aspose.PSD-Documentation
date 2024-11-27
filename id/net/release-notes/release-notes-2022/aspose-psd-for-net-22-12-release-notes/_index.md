---
title: Catatan Rilis Aspose.PSD untuk .NET 22.12
type: docs
weight: 10
url: /id/net/aspose-psd-untuk-net-22-12-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- Pada rilis ini diperbaiki regresi dengan ekspor 16-bit.

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1336|Tambahkan properti TextOrientation yang dapat diedit ke antarmuka IText|Fitur|
|PSDNET-725|Merubah ukuran file PSD tertentu dengan masker lapisan menghasilkan masker yang tidak benar|Bug|
|PSDNET-1277|Tambahkan kemampuan untuk menyimpan dan memuat masker untuk 16 gambar|Bug|
|PSDNET-1281|Ketidaktransparanan yang tidak benar saat menyimpan gambar 16 bit ke gambar 16 atau 8 bit|Bug|
|PSDNET-1375|Perbaikan CMYK dalam warna 16 bit|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDNET-725. Merubah ukuran file PSD tertentu dengan masker lapisan menghasilkan masker yang tidak benar**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Membuka file PSD sumber
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Melakukan perubahan ukuran
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Membuka file PSD yang diubah ukurannya
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Merender ke PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Tambahkan kemampuan untuk menyimpan dan memuat masker untuk 16 gambar**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Opsi memungkinkan penyimpanan warna 16 bit
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // File PSD akan disimpan dengan transparansi
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Ketidaktransparanan yang tidak benar saat menyimpan gambar 16 bit menjadi gambar 16 atau 8 bit**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// File psd warna 16 bit (dengan transparansi) akan dibuka dan disimpan ke warna 16 bit 
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// File psd warna 16 bit yang disimpan akan dirender ke file png dengan transparansi
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Tambahkan properti TextOrientation yang dapat diedit ke antarmuka IText**

{{< highlight csharp >}}
// Kode berikut menunjukkan kemampuan untuk mengedit properti TextOrientation baru.
// Hal ini tidak berpengaruh pada penggambaran saat ini, tetapi hanya memungkinkan Anda untuk mengedit nilai properti.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Pembacaan yang benar
    }
    else
    {
        throw new Exception("Pembacaan nilai properti TextOrientation salah");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Pembacaan yang benar
    }
    else
    {
        throw new Exception("Pembacaan nilai properti TextOrientation salah");
    }
}
{{< /highlight >}}

**PSDNET-1375. Perbaikan CMYK dalam warna 16 bit**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Mengatur opsi konversi
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Mengonversi dan menyimpan
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Membuka file yang telah dikonversi dan merender ke PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
