---
title: Catatan Rilis Aspose.PSD for .NET 24.3
type: docs
weight: 100
url: /id/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD for .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                      | **Kategori**   |
|:------------|:------------------------------------------------------------------|:---------------|
| PSDNET-1914 | [Format AI] Mengurangi waktu pemuatan gambar AI multipage besar   | Peningkatan    |
| PSDNET-1905 | File PSD setelah diubah dari 8 bit ke 16 bit menjadi tidak terbaca | Kesalahan      |
| PSDNET-1906 | File PSD setelah diubah dari 8 bit ke 32 bit menjadi tidak terbaca | Kesalahan      |
| PSDNET-1921 | [Format AI] Perbaiki render Short Curve pada file AI               | Kesalahan      |

## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

**PSDNET-1905. File PSD setelah diubah dari 8 bit ke 16 bit menjadi tidak terbaca**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdImage8.Save(outputFile, psdOptions16);
}

using (var psdImage16 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage16.GlobalLayerResources[0] is Lr16Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Sumber daya global salah, sumber daya pertama harus Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. File PSD setelah diubah dari 8 bit ke 32 bit menjadi tidak terbaca**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // is ok
    }
    else
    {
        throw new Exception("Sumber daya global salah, sumber daya pertama harus Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [Format AI] Perbaiki render Short Curve pada file AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
