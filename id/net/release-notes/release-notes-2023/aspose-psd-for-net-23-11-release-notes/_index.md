---
title: Catatan Rilis Aspose.PSD untuk .NET 23.11
type: docs
weight: 20
url: /id/net/aspose-psd-untuk-net-23-11-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**     | **Ringkasan**                                                                                               | **Kategori** |
|:------------|:----------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412  | Dukungan LMskResource                                                                                   | Fitur |
| PSDNET-1669 | [Format AI] Menambahkan kemampuan untuk merender file AI berbasis PDF dengan Aspose.PSD                                       | Fitur |
| PSDNET-1702 | [Format AI] Menambahkan dukungan untuk operator PostScript "cm"                                                      | Fitur |
| PSDNET-1752 | Menambahkan jenis warp baru: Gelombang, cangkang atas, cangkang bawah                                                         | Fitur |
| PSDNET-1797 | Menambahkan dukungan warp vertikal                                                                                 | Fitur |
| PSDNET-1756 | System.ArgumentNullException: 'Nilai tidak dapat null. (Parameter 'kunci')' saat memanggil TextLayer.GetFonts() | Bug |


## **Perubahan API Publik**
# **API Ditambahkan:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale


# **API Dihapus:**
- Tidak Ada


## **Contoh Penggunaan:**
**PSDNET-412. Dukungan LMskResource**

{{< highlight csharp >}}
string fileSumber = Path.Combine(baseFolder, "fileSumber.psd");
string outputPsd = Path.Combine(outputFolder, "fileSumber_output.psd");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objek tidak sama.");
    }
}

// Memuat gambar 16-bit.
using (PsdImage gambar = (PsdImage)Image.Load(fileSumber))
{
    // Temukan LmskResource.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in gambar.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // Periksa properti LmskResource.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // Mengubah properti LmskResource.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // Simpan gambar.
    gambar.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1669. [Format AI] Menambahkan kemampuan untuk merender file AI berbasis PDF dengan Aspose.PSD**

{{< highlight csharp >}}
string fileSumber = Path.Combine(baseFolder, "ai_satu.ai");
string outputPng = Path.Combine(outputFolder, "ai_satu_output.png");

// Memuat gambar AI berbasis PDF.
using (AiImage gambar = (AiImage)Image.Load(fileSumber))
{
    // Simpan gambar AI sebagai gambar PNG.
    gambar.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [Format AI] Menambahkan dukungan untuk operator "cm" PostScript**

{{< highlight csharp >}}
string fileSumber = Path.Combine(baseFolder, "ai_dua.ai");
string outputPng = Path.Combine(outputFolder, "ai_dua_output.png");

// Memuat gambar AI.
using (AiImage gambar = (AiImage)Image.Load(fileSumber))
{
    // Simpan gambar AI sebagai gambar PNG.
    gambar.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Menambahkan jenis warp baru: Gelombang, cangkang atas, cangkang bawah**

{{< highlight csharp >}}
var opsiMuat = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var opsiSimpan = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string fileIkan = Path.Combine(baseFolder, "1752_warp_ikan.psd");
string fileNaik = Path.Combine(baseFolder, "1752_warp_naik.psd");
string fileGelombang = Path.Combine(baseFolder, "1752_warp_gelombang.psd");

string fileKeluaranIkan = Path.Combine(outputFolder, "1752_output_ikan.png");
string fileKeluaranNaik = Path.Combine(outputFolder, "1752_output_naik.png");
string fileKeluaranGelombang = Path.Combine(outputFolder, "1752_output_gelombang.png");

using (var gambarPsd = (PsdImage)Image.Load(fileIkan, opsiMuat))
{
    gambarPsd.Save(fileKeluaranIkan, opsiSimpan);
}

using (var gambarPsd = (PsdImage)Image.Load(fileNaik, opsiMuat))
{
    gambarPsd.Save(fileKeluaranNaik, opsiSimpan);
}

using (var gambarPsd = (PsdImage)Image.Load(fileGelombang, opsiMuat))
{
    gambarPsd.Save(fileKeluaranGelombang, opsiSimpan);
}
{{< /highlight >}}

**PSDNET-1756. System.ArgumentNullException: 'Nilai tidak dapat null. (Parameter 'kunci')' saat memanggil TextLayer.GetFonts()**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "TeksSederhana.psd");

FontSettings.RemoveFontCacheFile();

using (var gambarPsd = (PsdImage)Image.Load(src))
{
    foreach (var layer in gambarPsd.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Menambahkan dukungan warp vertikal**

{{< highlight csharp >}}
var opsiMuat = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var opsiSimpan = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string fileBusurBawah = Path.Combine(baseFolder, "1797_warp_busur_bawah_v.psd");
string fileBusurAtas = Path.Combine(baseFolder, "1797_warp_busur_atas_v.psd");
string fileLengkung = Path.Combine(baseFolder, "1797_warp_lengkung_v.psd");
string fileMembengkak = Path.Combine(baseFolder, "1797_warp_membengkak_v.psd");
string fileBendera = Path.Combine(baseFolder, "1797_warp_bendera_v.psd");
string fileIkan = Path.Combine(baseFolder, "1797_warp_ikan_v.psd");
string fileNaik = Path.Combine(baseFolder, "1797_warp_naik_v.psd");
string fileGelombang = Path.Combine(baseFolder, "1797_warp_gelombang_v.psd");

string fileKeluaranBusurBawah = Path.Combine(outputFolder, "1797_warp_busur_bawah_v.png");
string fileKeluaranBusurAtas = Path.Combine(outputFolder, "1797_warp_busur_atas_v.png");
string fileKeluaranLengkung = Path.Combine(outputFolder, "1797_warp_lengkung_v.png");
string fileKeluaranMembengkak = Path.Combine(outputFolder, "1797_warp_membengkak_v.png");
string fileKeluaranBendera = Path.Combine(outputFolder, "1797_warp_bendera_v.png");
string fileKeluaranIkan = Path.Combine(outputFolder, "1797_output_ikan_v.png");
string fileKeluaranNaik = Path.Combine(outputFolder, "1797_output_naik_v.png");
string fileKeluaranGelombang = Path.Combine(outputFolder, "1797_output_gelombang_v.png");

using (var gambarPsd = (PsdImage)Image.Load(fileBusurBawah, opsiMuat)) { gambarPsd.Save(fileKeluaranBusurBawah, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileBusurAtas, opsiMuat)) { gambarPsd.Save(fileKeluaranBusurAtas, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileLengkung, opsiMuat)) { gambarPsd.Save(fileKeluaranLengkung, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileMembengkak, opsiMuat)) { gambarPsd.Save(fileKeluaranMembengkak, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileBendera, opsiMuat)) { gambarPsd.Save(fileKeluaranBendera, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileIkan, opsiMuat)) { gambarPsd.Save(fileKeluaranIkan, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileNaik, opsiMuat)) { gambarPsd.Save(fileKeluaranNaik, opsiSimpan); }
using (var gambarPsd = (PsdImage)Image.Load(fileGelombang, opsiMuat)) { gambarPsd.Save(fileKeluaranGelombang, opsiSimpan); }
{{< /highlight >}}
