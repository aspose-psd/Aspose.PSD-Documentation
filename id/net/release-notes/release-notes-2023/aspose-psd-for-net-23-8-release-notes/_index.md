---
title: Catatan Rilis Aspose.PSD untuk .NET 23.8
type: docs
weight: 50
url: /id/net/aspose-psd-untuk-net-23-8-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                                  | **Kategori** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Tambahkan tipe warp baru (Flag) | Fitur |
| PSDNET-1621 | Tambahkan tipe warp baru: arc atas, arc bawah, bola | Fitur |
| PSDNET-1682 | Implementasikan metode baru PsdImage.AddPosterizeAdjustmentLayer untuk menambahkan lapisan Posterize baru | Fitur |
| PSDNET-913  | Informasi PSD hilang saat hanya dibuka dan disimpan | Bug     |
| PSDNET-1352 | Gagal memuat gambar | Bug     |
| PSDNET-1553 | Gagal memuat gambar: Tidak dapat melempar objek dari tipe UnknownStructure ke tipe DescriptorStructure | Bug     |
| PSDNET-1631 | Berkas berubah di pustaka pihak ketiga merusak berkas PSD tetapi dapat dibuka di Photoshop | Bug     |

## Perubahan API Publik
# **API Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-913. Informasi PSD hilang saat hanya dibuka dan disimpan**

{{< highlight csharp >}}
string src = "BerkasAsli.psd";
string outputPsd = "keluar_BerkasAsli.psd";
string outputPng = "keluar_BerkasAsli.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Gagal memuat gambar**

{{< highlight csharp >}}
string srcFile1 = "tes_teks.psd";
string srcFile2 = "tes_objek_pintar.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}

**PSDNET-1553. Gagal memuat gambar: Tidak dapat melempar objek dari tipe UnknownStructure ke tipe DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // Seharusnya dapat dimuat dengan benar
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. Berkas berubah di pustaka pihak ketiga merusak berkas PSD tetapi dapat dibuka di Photoshop**

{{< highlight csharp >}}
string sourceFile = "output.psd";
string outputFile = "ekspor.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Tambahkan tipe warp baru (Flag)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "ekspor_bendera.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Tambahkan tipe warp baru: arc atas, arc bawah, bola**

{{< highlight csharp >}}
string sourceFileArcUpper = "arc_upper_warp.psd";
string sourceFileArcLower = "arc_lower_warp.psd";
string sourceFileBulge =  "bulge_warp.psd";

string outputFileArcUpper ="ekspor_ArcAtas.png";
string outputFileArcLower = "ekspor_ArcBawah.png";
string outputFileBulge = "ekspor_Bulge.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Implementasikan metode baru PsdImage.AddPosterizeAdjustmentLayer untuk menambahkan lapisan Posterize baru**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// Periksa perubahan yang disimpan
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objek tidak sama.");
    }
}
{{< /highlight >}}
