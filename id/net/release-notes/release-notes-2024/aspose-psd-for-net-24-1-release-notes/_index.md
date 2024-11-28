---
title: Catatan Rilis Aspose.PSD untuk .NET 24.1
type: docs
weight: 120
url: /id/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}
Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                    | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Format AI] Menambahkan penanganan dasar untuk gambar AI multipage                                  | Fitur       |
| PSDNET-718  | Efek Teks Warp tidak berlaku pada teks                                                           | Bug         |
| PSDNET-1620 | Render mask yang tidak tepat dalam file tertentu                                                 | Bug         |
| PSDNET-1855 | NullReferenceException di Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor    | Bug         |
| PSDNET-1883 | [Format AI] Memperbaiki penggunaan memori di AiExporterUtils                                      | Bug         |




## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDNET-718. Efek Teks Warp tidak berlaku pada teks**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Render mask yang tidak tepat dalam file tertentu**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Format AI] Menambahkan penanganan dasar untuk gambar AI multipage**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Memuat gambar AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Secara default, ActivePageIndex adalah 0.
    // Jadi jika Anda menyimpan gambar AI tanpa mengubah properti ini, halaman pertama akan dirender dan disimpan.
    image.Save(firstPageOutputPng, new PngOptions());

    // Ubah indeks halaman aktif menjadi halaman kedua.
    image.ActivePageIndex = 1;

    // Simpan halaman kedua dari gambar AI sebagai gambar PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Ubah indeks halaman aktif menjadi halaman ketiga.
    image.ActivePageIndex = 2;

    // Simpan halaman ketiga dari gambar AI sebagai gambar PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException di Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Format AI] Memperbaiki penggunaan memori di AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Memuat gambar AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Simpan halaman pertama dari gambar AI sebagai gambar PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Ubah indeks halaman aktif menjadi halaman kedua.
    image.ActivePageIndex = 1;

    // Simpan halaman kedua dari gambar AI sebagai gambar PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Ubah indeks halaman aktif menjadi halaman ketiga.
    image.ActivePageIndex = 2;

    // Simpan halaman ketiga dari gambar AI sebagai gambar PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Penggunaan memori terlalu besar. " + memoryUsed + " daripada " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
