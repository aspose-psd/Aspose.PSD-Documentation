---
title: Catatan Rilis Aspose.PSD untuk .NET 20.9
type: docs
weight: 40
url: /id/net/aspose-psd-untuk-net-20-9-catatan-rilis/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-408|Dukungan untuk SoLEResource (Sumber Eksternal Lapisan Objek Pintar)|Fitur|
|PSDNET-614|Dukungan untuk Objek Pintar Terhubung|Fitur|
|PSDNET-615|Dukungan untuk Objek Pintar Tertanam|Fitur|
|PSDNET-690|Pembaruan teks pada file PSD tertentu dan menyimpannya merusak beberapa lapisan dan banyak parameter teks|Bug|
|PSDNET-696|FillLayer tidak diperbarui setelah dibuat dan tidak dapat dirender dengan benar|Bug|
|PSDNET-712|Regresi: Aspose.PSD 20.8.0 tidak dapat membuka file|Bug|
|PSDNET-714|Dalam file PSD spesifik, meresize TextLayer mematahkan nilai lokasi|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.IndeksBahasa
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.SkalaVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.SkalaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Pecahan
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metrik
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optik
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.PlacedId
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Versi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.IsKustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.HalamanNomor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TotalHalaman
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.KebijaksanaanAntiAlias
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TipeLapisanDitempatkan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Kiri
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Atas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Kanan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Bawah
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Batas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.MatriksTransformasi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UnitTitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UnitTitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.TandaTangan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Nilai
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Perspektif
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.PerspektifLainnya
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UrutanU
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.UrutanV
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource.Barang
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.HalamanNomor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TotalHalaman
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.KebijaksanaanAntiAlias
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TipeLapisanDitempatkan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.MatriksTransformasi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.MatriksNonAffineTransform
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.TandaTangan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Panjang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.VersiPsd
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Barang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Lebar
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Tinggi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PembejaanFrameLangkahPembilang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PembejaanFrameLangkahPenyebut
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PembejaanDurasiPembilang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.PembejaanDurasiPenyebut
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Simpan(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SOleResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SOleResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SOleResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SOleResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SOleResource.KunciPeralatanTipe
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlacedResource)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.HasilkanSumberDitempatkan
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.HasilkanSumberYangDisematkanPintar
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PembuatSumberPintar.HasilkanSumberEksternalPintar
- T:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar
- P:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.BatasIsi
- P:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.SumberKonten
- P:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.Konten
- P:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.JenisKonten
- P:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.PenyediaObjekPintar
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.EksporKonten(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.MuatKonten(Aspose.PSD.LoadOptions)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.GantiKonten(Aspose.PSD.Gambar)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.GantiKonten(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.SematkanTerhubung
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.KonversiMenjadiTerhubung(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.HubungkanKembaliKeBerkas(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintar.PerbaruiKontenYangDimodifikasi
- T:Aspose.PSD.FileFormats.Psd.PenyediaSumberPintar
- M:Aspose.PSD.FileFormats.Psd.PenyediaSumberPintar.SematkanSemuaTerhubung
- M:Aspose.PSD.FileFormats.Psd.PenyediaSumberPintar.PerbaruiSemuaKontenYangDimodifikasi
- T:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintarTipe
- F:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintarTipe.Ditetapkan
- F:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintarTipe.TersediaTerhubung
- F:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintarTipe.TidakTersediaTerhubung
- F:Aspose.PSD.FileFormats.Psd.Layers.LapisanObjekPintarPintarTipe.PustakaTautan
- P:Aspose.PSD.FileFormats.Psd.PsdImage.PenyediaObjekPintar

# **API Dihapus:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Versi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.IsKustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.HalamanNomor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TotalHalaman
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.KebijaksanaanAntiAlias
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TipeLapisanDitempatkan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Kiri
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Atas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Kanan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Bawah
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Batas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.MatriksTransformasi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.TitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UnitTitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UnitTitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Nilai
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UrutanU
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.UrutanV
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PlLdResource.Barang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Versi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PlacedId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.IsKustom
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.HalamanNomor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TotalHalaman
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.KebijaksanaanAntiAlias
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TipeLapisanDitempatkan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Kiri
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Atas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Kanan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Bawah
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Batas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.MatriksTransformasi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.MatriksNonAffineTransform
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UnitTitikMeshHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UnitTitikMeshVertikal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.TandaTangan
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Panjang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.VersiPsd
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Nilai
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Perspektif
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PerspektifLainnya
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UrutanU
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.UrutanV
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Barang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Lebar
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.Tinggi
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PembejaanFrameLangkahPembilang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PembejaanFrameLangkahPenyebut
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PembejaanDurasiPembilang
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLdResource.PembejaanDurasiPenyebut
-