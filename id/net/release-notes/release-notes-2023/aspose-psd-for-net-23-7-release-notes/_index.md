---
title: Catatan Rilis Aspose.PSD untuk .NET 23.7
type: docs
weight: 60
url: /id/net/aspose-psd-for-net-23-7-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 23.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Kunci**   | **Ringkasan**                                                                                               | **Kategori** |
|:------------|:------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-802  | Tambahkan kemampuan Untuk mengekspor setiap lapisan File PSD ke File Gif Animasi                            | Fitur   |
| PSDNET-1441 | Tetapkan properti Isi lapisan Bentuk dari sumber vscg                                                      | Fitur   |
| PSDNET-1534 | Tambahkan tipe warp baru (arc & arch)                                                                      | Fitur   |
| PSDNET-1543 | Ganti aplikasi yang menyimpan File PSD ke Aspose.PSD jika properti UpdateMetadata diatur ke true          | Fitur   |
| PSDNET-1567 | Tingkatkan area perhitungan gambar warp                                                                    | Fitur   |
| PSDNET-1471 | Koreksi Lapisan Penyesuaian Hitam dan Putih memproses semi-transparansi salah                              | Bug     |
| PSDNET-1505 | SmartObject ReplaceContents (ketika opsi AllowWarpRepaint aktif) gagal setelah 2 menit menghitung           | Bug     |
| PSDNET-1585 | Tambahkan kemampuan untuk mendapatkan Posisi Kiri dan Atas LayerGroup yang sebenarnya                     | Bug     |
| PSDNET-1589 | Resize dari lapisan berfungsi dengan salah ketika file psd memiliki VogkResource dengan struktur dalam titik | Bug     |
| PSDNET-1608 | TextBound tidak berfungsi seperti yang diharapkan                                                        | Bug     |
| PSDNET-1612 | Menambahkan lapisan yang dibuat dengan konstruktor default ke gambar PSD tidak menambahkan sumber daya default kepadanya | Bug     |
| PSDNET-1623 | Timeline.LoopesCount diabaikan saat diekspor ke GIF animasi                                              | Bug     |


## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD. ImageOptions.PsdOptions.UpdateMetadata
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf16
- F:Aspose.PSD.FileFormats.Ai.AiFormatVersion.Pdf17
- P:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.Item(System.String)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.SetValue(System.String,Aspose.PSD.Xmp.IXmlValue)
- M:Aspose.PSD.Xmp.Schemas.XmpBaseSchema.XmpBasicPackage.ContainsKey(System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Fill


# **API Dihapus:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPath.FillColor


## **Contoh Penggunaan:**

**PSDNET-802. Tambahkan kemampuan Untuk mengekspor setiap lapisan File PSD ke File Gif Animasi**

{{< highlight csharp >}}
string src = "EachLayerIsFrame.psd";
string outputGif = "out_EachLayerIsFrame.gif";
string outputPsd = "out_EachLayerIsFrame.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    // Membuat bingkai untuk setiap lapisan.
    int jumlahFrame = psdImage.Layers.Length;
    var timeline = psdImage.Timeline;

    Frame[] frames = new Frame[jumlahFrame];
    for (int i = 0; i < jumlahFrame; i++)
    {
        frames[i] = new Frame();
        LayerState[] stateLapisan = new LayerState[jumlahFrame];

        for (int j = 0; j < jumlahFrame; j++)
        {
            stateLapisan[j] = new LayerState();
            stateLapisan[j].Aktif = i == j;
        }

        frames[i].StateLayer = stateLapisan;
    }

    timeline.Frames = frames;

    // Memperbarui status saat ini
    Layer[] lapisan = psdImage.Layers;
    LayerState[] states = timeline.Frames[timeline.ActiveFrameIndex].StateLayer;
    for (int i = 0; i < jumlahFrame; i++)
    {
        lapisan[i].Terlihat = states[i].Aktif;
    }

    timeline.Simpan(outputGif, new GifOptions());
    psdImage.Simpan(outputPsd);
}
{{< /highlight >}}
... (skipped)
