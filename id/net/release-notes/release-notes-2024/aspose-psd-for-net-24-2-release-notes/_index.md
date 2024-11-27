---
title: Catatan Rilis Aspose.PSD untuk .NET 24.2
type: dokumen
weight: 110
url: /id/net/aspose-psd-untuk-net-24-2-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                             | **Kategori**  |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDNET-1503 | Menangani Properti Sudut untuk Pengaturan Isi Pola                        | Fitur        |
| PSDNET-1719 | Mendukung skala vertikal dan horizontal untuk TextLayer                  | Fitur        |
| PSDNET-1783 | [Format AI] Melaksanakan tampilan latar yang benar dalam Format AI Berbasis PDF | Fitur        |
| PSDNET-1611 | Mengubah mekanisme Distorsi dalam warp                                    | Peningkatan  |
| PSDNET-1802 | Mempercepat warp                                                          | Peningkatan  |
| PSDNET-995  | Pengecualian "Pemuatan gambar gagal." saat membuka dokumen                | Bug          |
| PSDNET-1491 | Memperbaiki penyimpanan file psd dengan Pola Stroke                      | Bug          |
| PSDNET-1642 | Gaya teks tidak benar dalam objek pintar ketika kami menggunakan ReplaceContents | Bug          |
| PSDNET-1884 | [Format AI] Memperbaiki tampilan Cubic Bezier pada file AI               | Bug          |

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-1503. Menangani Properti Sudut untuk Pengaturan Isi Pola**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. Mendukung skala vertikal dan horisontal untuk TextLayer**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [Format AI] Melaksanakan tampilan latar yang benar dalam Format AI Berbasis PDF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. Pengecualian "Pemuatan gambar gagal." saat membuka dokumen**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "PRODUCT.ai");
string outputFile1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(sourceFile1))
{
    image.Save(outputFile1, new PngOptions());
}

// Kode lainnya diabaikan untuk kepentingan singkat.
{{< /highlight >}}

**(lanjutan pada file selanjutnya...)**
