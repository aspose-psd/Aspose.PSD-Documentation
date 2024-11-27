---
title: Catatan Rilis Aspose.PSD Adapters untuk .NET 24.4
type: docs
weight: 100
url: /id/net/adapters/aspose-psd-adapters-untuk-net-24-4-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD Adapters untuk .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Kunci**    | **Ringkasan**                                                        | **Kategori** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Penerbitan awal Aspose.PSD.Adapters.Imaging ke Nuget                  | Peningkatan |


## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada

# **API Dihapus:**
- Tidak ada

## **Contoh Penggunaan:**

Silakan cek [halaman dokumentasi Aspose.PSD.Adapters](/psd/id/net/adapters)

**PSDNET-1985. Contoh penggunaan paling lengkap dari Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Tambahkan pengaktifan adapters dalam konfigurasi awal Anda 
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FileFormat.Bmp,
   FileFormat.Gif,
   FileFormat.Jpeg2000,
   FileFormat.Jpeg,
   FileFormat.Png,
   FileFormat.Svg,
   FileFormat.Tiff,
   FileFormat.Webp);
            
// tambahkan pengaktifan Exporters
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Untuk bekerja dengan adapters, Anda memerlukan Lisensi Aspose.PSD dan adaptee
// Berikut adalah cara menerapkan Lisensi Aspose.PSD
var license = new Aspose.PSD.License();
license.SetLicense(@"Aspose.PSD.NET.lic");

// Berikut adalah contoh cara menerapkan Lisensi Adaptee untuk Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Kemudian Anda dapat menjalankan kode apa pun dari adapter atau perpustakaan PSD atau Imaging

// Setelah ini, semua file ini dapat dibuka oleh Aspose.PSD tanpa kode tambahan hanya dengan menggunakan
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Setelah menjalankan kode ini, Anda akan mendapatkan File PSD yang dibuat dari WEBP dan dapat menerapkan Filter, Layer, dan Penyesuaian Aspose.PSD apa pun termasuk Transformasi Warp
}

// Anda juga dapat Membuat Gambar Adaptee Ekspor ke Format PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Gunakan API Aspose.Imaging untuk Mengedit file WEBP dengan fitur khusus Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Kemudian cukup gunakan metode ToPsdImage() dan edit file seperti PSD dengan fitur mirip Photoshop termasuk layer, filter cerdas, dan objek cerdas.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Some text", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Simpan file PSD akhir menggunakan Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Jika Anda tidak perlu menggunakan Loaders atau Exporters yang disediakan oleh Adapters, cukup nonaktifkan mereka
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
