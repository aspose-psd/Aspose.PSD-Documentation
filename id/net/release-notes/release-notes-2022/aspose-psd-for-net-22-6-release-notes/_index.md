---
title: Catatan Rilis Aspose.PSD for .NET 22.6
type: dokumen
weight: 70
url: /id/net/aspose-psd-for-net-22-6-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-940|Buat API untuk mendapatkan hash unik untuk lapisan serupa di file yang berbeda|Peningkatan|
|PSDNET-678|Rendering yang tidak tepat dari FillLayer dengan pola dalam kasus ketika pola lebih dari satu dan urutan lapisan diubah|Bug|
|PSDNET-1125|Exception saat memuat file PSD tertentu dengan mode warna CMYK|Bug|


## **Perubahan API Publik**
# **API yang Ditambahkan:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **API yang Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDNET-678. Rendering yang tidak tepat dari FillLayer dengan pola dalam kasus ketika pola lebih dari satu dan urutan lapisan diubah**

{{< highlight csharp >}}
string sourceFile = "badPattern.psd";
string outputPng = "out_678.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer layer1 = (FillLayer)psdImage.Layers[1];
    FillLayer layer2 = (FillLayer)psdImage.Layers[2];

    layer1.Update();
    layer2.Update();

    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Buat API untuk mendapatkan hash unik untuk lapisan serupa di file yang berbeda**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    // Konten tidak diubah karena merupakan contoh penggunaan metode yang ada.
}
{{< /highlight >}}

**PSDNET-1125. Exception saat memuat file PSD tertentu dengan mode warna CMYK**

{{< highlight csharp >}}
string sourceFile = "02_alpha-channels.psd";
string outputPng = "out_1125.png";

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}