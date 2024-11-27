---
title: Catatan Rilis Aspose.PSD for .NET 24.7
type: docs
weight: 60
url: /id/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}
Halaman ini berisi catatan rilis untuk [Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                     | **Kategori** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | "Image loading failed." exception saat membuka dokumen AI                                        | Bug          |
| PSDNET-2022 | Teks dirender dengan tidak benar dalam file PDF keluaran                                          | Bug          |
| PSDNET-2061 | Memperbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux           | Bug          |
| PSDNET-2080 | Memperbaiki pemuatan font saat menggunakan Aspose.Drawing                                         | Bug          |
| PSDNET-2085 | 'Operasi aritmatika menghasilkan kelebihan' saat membuat lapisan objek pintar menggunakan JPEG besar | Bug     |
| PSDNET-2100 | File AI tidak dapat dikonversi menjadi file JPG                                                  | Bug          |

## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-1029. "Image loading failed." exception saat membuka dokumen AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Teks dirender dengan tidak benar dalam file PDF keluaran**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Memperbaiki ImageSaveException: Ekspor gambar gagal untuk file yang diberikan di Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Memperbaiki pemuatan font saat menggunakan Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Sebelum pembaruan. Jumlah font yang terpasang: " + installedFonts.Families.Length);
    Console.WriteLine("- Platform: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Perbarui cache font dengan mencoba mendapatkan nama font Adobe untuk 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Setelah pembaruan. Jumlah font yang terpasang: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Operasi aritmatika menghasilkan kelebihan' saat membuat lapisan objek pintar menggunakan JPEG besar**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. File AI tidak dapat dikonversi menjadi file JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
