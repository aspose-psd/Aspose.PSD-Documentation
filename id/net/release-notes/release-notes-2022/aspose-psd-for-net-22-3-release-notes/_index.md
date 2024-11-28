---
title: Catatan Rilis Aspose.PSD untuk .NET 22.3
type: docs
weight: 100
url: /id/net/aspose-psd-untuk-net-22-3-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-210|Menambahkan properti IsOpen untuk Grup Layer|Fitur|
|PSDNET-643|Gambar PSD dengan masker layer raster menghapus masker saat disimpan ke gambar PSD 16 bit|Bug|
|PSDNET-899|Mode campuran Dissolve tidak diterapkan ke folder dengan masker|Bug|
|PSDNET-1047|File tertentu tidak dapat dibuka oleh Photoshop setelah disimpan dalam Aspose.PSD 21.11|Bug|
|PSDNET-1068|Rendering yang tidak tepat dari layer dengan mode campuran Linear Dodge (Tambah)|Bug|
|PSDNET-1069|Layer Pengisian Pola memunculkan pengecualian saat diperbarui setelah dimuat|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **API Dihapus:**
- Tidak Ada


## **Contoh Penggunaan:**

**PSDNET-210. Menambahkan properti IsOpen untuk Grup Layer**

{{< highlight csharp >}}
// Contoh membaca dan menulis properti IsOpen saat runtime.
string namaFileSumber = "LayerGroupOpenClose.psd";
string namaFileOutput = "Output" + namaFileSumber;

using (var gambar = (PsdImage)Image.Load(namaFileSumber))
{
    foreach (var layer in gambar.Layers)
    {
        if (layer is LayerGroup && layer.Name == "Group 1")
        {
            bool isOpenedGroup1 = ((LayerGroup)layer).IsOpen;
            ((LayerGroup)layer).IsOpen = !isOpenedGroup1;
        }

        if (layer is LayerGroup && layer.Name == "Group 2")
        {
            bool isOpenedGroup2 = ((LayerGroup)layer).IsOpen;           
            ((LayerGroup)layer).IsOpen = !isOpenedGroup2;
        }
    }

    gambar.Save(namaFileOutput);
}
{{< /highlight >}}

**PSDNET-643. Gambar PSD dengan masker layer raster menghapus masker saat disimpan ke gambar PSD 16 bit**

{{< highlight csharp >}}
            string jalurFileSumber = "SatuRegulerDanSatuRegulerDenganMasker.psd";
            string jalurFileOutput = "out_SatuRegulerDanSatuRegulerDenganMasker.psd";

            using (PsdImage gambar = (PsdImage)Image.Load(jalurFileSumber))
            {
                gambar.Save(jalurFileOutput, new PsdOptions(gambar)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Mode campuran Dissolve tidak diterapkan ke folder dengan masker**

{{< highlight csharp >}}
            string fileSumber = "psdnet899.psd";
            string outputPng = "out_psdnet899.png";

            using (PsdImage gambar = (PsdImage) Image.Load(fileSumber))
            {
                gambar.Save(outputPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Spesifik file tidak dapat dibuka oleh Photoshop setelah disimpan dalam Aspose.PSD 21.11**

{{< highlight csharp >}}
            string fileSumber = "psdnet1047.psd";
            string outputPsd = "out_psdnet1047.psd";

            using (PsdImage gambar = (PsdImage) Image.Load(fileSumber))
            {
                gambar.Save(outputPsd);
            }

            // Perlu membuka PSD output secara manual oleh Photoshop.

            using (PsdImage gambar = (PsdImage) Image.Load(outputPsd))
            {
                // tanpa pengecualian.
            }
{{< /highlight >}}

**PSDNET-1068. Rendering yang tidak tepat dari layer dengan mode campuran Linear Dodge (Tambah)**

{{< highlight csharp >}}
            string fileSumber = "broken.psd";
            string outputPng = "out_broken.psd.png";

            using (var psdImage = (PsdImage) Image.Load(fileSumber))
            {
                psdImage.Save(outputPng, new PngOptions() {ColorType = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Layer Pengisian Pola memunculkan pengecualian saat diperbarui setelah dimuat**

{{< highlight csharp >}}
            string fileSumber = "AllTypesLayerPsd.psd";

            using (var gambar = (PsdImage) Image.Load(fileSumber))
            {
                var fillLayer = (FillLayer)gambar.Layers[9];
                fillLayer.Update();
            }
{{< /highlight >}}
