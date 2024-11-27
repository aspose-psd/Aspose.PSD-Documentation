---
title: Catatan Rilis Aspose.PSD untuk .NET 20.4
type: docs
weight: 90
url: /id/net/aspose-psd-for-net-20-4-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 20.4](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-567|Dukungan untuk sumber daya 'Vector Origination Data'|Fitur|
|PSDNET-373|Dukungan untuk lclrResource (Pengaturan warna lembaran)|Fitur|
|PSDNET-563|Dukungan untuk properti dari data LengthRecord. (Operasi jalur (operasi boolean), indeks bentuk dalam lapisan, jumlah catatan simpul bezier)|Fitur|
|PSDNET-425|Dukungan untuk Warna Latar Belakang dari Sumber Daya Bagian Gambar #1010|Fitur|
|PSDNET-530|Penambahan Layer Isi secara dinamis|Fitur|
|PSDNET-424|Dukungan untuk Informasi Tepi dari Sumber Daya Bagian Gambar #1009|Fitur|
|PSDNET-592|Dukungan untuk Lapisan dalam File Format AI|Fitur|
|PSDNET-256|Dukungan Membaca dan Mengedit Efek Lapisan Gradient Overlay|Fitur|
|PSDNET-257|Pencitraan Efek Lapisan Gradient Overlay|Fitur|
|PSDNET-585|Perubahan properti GradientOverlayEffect.BlendMode tidak ditampilkan di Photoshop|Bug|
|PSDNET-561|Memperbaiki penyimpanan gambar PSD dengan ColorMode Grayscale dan 16 bit per saluran ke format PSD grayscale|Bug|
|PSDNET-560|Memperbaiki penyimpanan gambar PSD dengan ColorMode Grayscale dan 16 bit per saluran ke format PNG|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Name
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsTemplate
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsLocked
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsShown
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPrinted
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsPreview
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.IsImagesDimmed
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.DimValue
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorNumber
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Red
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Green
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.Blue
- M:Aspose.PSD.FileFormats.Psd.Layers.FillLayers.FillLayer.CreateInstance(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- T:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BackgroundColorResource.Color
- T:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource
- M:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Width
- P:Aspose.PSD.FileFormats.Psd.Resources.BorderInformationResource.Unit
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.BezierKnotRecord.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.InitialFillRuleRecord.#ctor(System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.BezierKnotRecordsCount
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.PathOperations
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.LengthRecord.ShapeIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VogkResource.ShapeOriginSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.#ctor(System.Boolean,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.IsShapeInvalidated
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.VectorShapeOriginSettings.OriginIndex
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.ExcludeOverlappingShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.CombineShapes
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.SubtractFrontShape
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPaths.PathOperations.IntersectShapeAreas
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.FillSettings.GradientColorPoint.#ctor(Aspose.PSD.Color,System.Int32,System.Int32)
# **API Dihapus:**
- Tidak Ada

## **Contoh Penggunaan:**
**PSDNET-567. Dukungan untuk sumber daya 'Vector Origination Data'**

{{< highlight java >}}

         // Dukungan VogkResource

        static void ContohDukunganVogkResource()

        {

            string namaFile = "VectorOriginationDataResource.psd";

            string namaKeluaranFile = "keluaran_VectorOriginationDataResource_.psd";

            using (var gambarPsd = (PsdImage)Image.Load(namaFile))

            {

                var sumberDaya = GetVogkResource(gambarPsd);

                // Membaca

                if (sumberDaya.ShapeOriginSettings.Length != 1 ||

                    !sumberDaya.ShapeOriginSettings[0].IsShapeInvalidated ||

                    sumberDaya.ShapeOriginSettings[0].OriginIndex != 0)

                {

                    throw new Exception("VogkResource dibaca salah.");

                }

                // Mengedit

                sumberDaya.ShapeOriginSettings = new[]

                {

                    sumberDaya.ShapeOriginSettings[0],

                    new VectorShapeOriginSettings(true, 1)

                };

                gambarPsd.Save(namaKeluaranFile);

            }

        }

        static VogkResource GetVogkResource(PsdImage gambar)

        {

            var lapisan = gambar.Layers[1];

            VogkResource sumberDaya = null;

            var sumberDayaLayer = lapisan.Resources;

            for (int i = 0; i < sumberDayaLayer.Length; i++)

            {

                if (sumberDayaLayer[i] is VogkResource)

                {

                    sumberDaya = (VogkResource)sumberDayaLayer[i];

                    break;

                }

            }

            if (sumberDaya == null)

            {

                throw new Exception("SumberDaya VogkResource tidak ditemukan.");

            }

            return sumberDaya;

        }   

{{< /highlight >}}

**PSDNET-373. Dukungan untuk lclrResource (Pengaturan warna lembaran)**

{{< highlight java >}}

         static void PeriksaWarnaLembaranDanBalik(SheetColorHighlightEnum[] warnaLembaran, PsdImage img)

        {

            int jumlahLayer = img.Layers.Length;

            for (int indeksLapisan = 0; indeksLapisan < jumlahLayer; indeksLapisan++)

            {

                Layer lapisan = img.Layers[indeksLapisan];

                LayerResource[] sumberDaya = lapisan.Resources;

                foreach (LayerResource sumberDayaLapisan in sumberDaya)

                {

                    // Sumber daya lcrl selalu ada dalam daftar sumber daya file psd.

                    LclrResource sumberDaya = sumberDayaLapisan as LclrResource;

                    if (sumberDaya != null)

                    {

                        if (sumberDaya.Color != warnaLembaran[indeksLapisan])

                        {

                            throw new Exception("Warna Lembaran dibaca salah");

                        }

                        // Pembalikan warna lembaran gaya. Atur Penyorotan Warna Lapisan.

                        sumberDaya.Color = warnaLembaran[jumlahLayer - indeksLapisan - 1];

                        break;

                    }

                }

            }

        }

            string berkasSumber = "SemuaWarnaLclrResource.psd";

            string berkasKeluaran = "SemuaWarnaLclrResourceBalik.psd";

            // Dalam berkas warna penyorotan lapisan berada dalam urutan ini

            SheetColorHighlightEnum[] warnaLembaran = new SheetColorHighlightEnum[] {

                SheetColorHighlightEnum.Red,

                SheetColorHighlightEnum.Orange,

                SheetColorHighlightEnum.Yellow,

                SheetColorHighlightEnum.Green,

                SheetColorHighlightEnum.Blue,

                SheetColorHighlightEnum.Violet,

                SheetColorHighlightEnum.Gray,

                SheetColorHighlightEnum.NoColor

            };            

            // Warna Lembaran digunakan untuk menyoroti lapisan secara visual. 

            // Sebagai contoh Anda dapat memperbarui beberapa lapisan dalam PSD dan kemudian menyoroti warna lapisan yang ingin menarik perhatian.

            using (PsdImage img = (PsdImage)Image.Load(berkasSumber))

            {

                PeriksaWarnaLembaranDanBalik(warnaLembaran, img);

                img.Save(berkasKeluaran, new PsdOptions());

            }

            using (PsdImage img = (PsdImage)Image.Load(berkasKeluaran))

            {

                // Warna harus dibalik

                Array.Reverse(warnaLembaran);

                PeriksaWarnaLembaranDanBalik(warnaLembaran, img);

            }

{{< /highlight >}}

**PSDNET-563. Dukungan properti dari data LengthRecord. (Operasi jalur (operasi boolean), indeks bentuk dalam lapisan, jumlah catatan simpul bezier)**

{{< highlight java >}}

            string namaBerkas = "PathOperationsShape.psd";

            using (var im = (PsdImage)Image.Load(namaBerkas))

            {

                VsmsResource sumberDaya = null;

                foreach (var sumberDayaLapisan in im.Layers[1].Resources)

                {

                    if (sumberDayaLapisan is VsmsResource)

                    {

                        sumberDaya = (VsmsResource)sumberDayaLapisan;

                        break;

                    }

                }

                LengthRecord lengthRecord0 = (LengthRecord)sumberDaya.Paths[2];

                LengthRecord lengthRecord1 = (LengthRecord)sumberDaya.Paths[7];

                LengthRecord lengthRecord2 = (LengthRecord)sumberDaya.Paths[11];

                // Disini kita mengubah metode penggabungan antara bentuk.

                lengthRecord0.PathOperations = PathOperations.ExcludeOverlappingShapes;

                lengthRecord1.PathOperations = PathOperations.IntersectShapeAreas;

                lengthRecord2.PathOperations = PathOperations.SubtractFrontShape;

                im.Save("keluaran_" + namaBerkas);

            }

{{< /highlight >}}

**PSDNET-425. Dukungan untuk Warna Latar Belakang dari Sumber Daya Bagian Gambar #1010**

{{< highlight java >}}

             string berkasSumber = "input.psd";

            string berkasKeluaran = "output.psd";

            using (var gambar = (PsdImage)Image.Load(berkasSumber))

            {

                ResourceBlock[] sumberDayaGambar = gambar.ImageResources;

                BackgroundColorResource sumberDayaWarnaLatarBelakang = null;

                foreach (var sumberDayaGambarSatu in sumberDayaGambar)

                {

                    if (sumberDayaGambarSatu is BackgroundColorResource)

                    {

                        sumberDayaWarnaLatarBelakang = (BackgroundColorResource)sumberDayaGambarSatu;

                        break;

                    }

                }

                // memperbarui BackgroundColorResource

                sumberDayaWarnaLatarBelakang.Color = Color.DarkRed;

                gambar.Save(berkasKeluaran);

            }

{{< /highlight >}}

**PSDNET-530. Penambahan Layer Isi secara dinamis**

{{< highlight java >}}

             string psdKeluaran = "output.psd";

            using (var gambar = new PsdImage(100, 100))

            {

                FillLayer layerIsiWarna = FillLayer.CreateInstance(FillType.Color);

                layerIsiWarna.DisplayName = "Layer Isi Warna";

                gambar.AddLayer(layerIsiWarna);

                FillLayer layerIsiGradien = FillLayer.CreateInstance(FillType.Gradient);

                layerIsiGradien.DisplayName = "Layer Isi Gradien";

                gambar.AddLayer(layerIsiGradien);

                FillLayer layerIsiPola = FillLayer.CreateInstance(FillType.Pattern);

                layerIsiPola.DisplayName = "Layer Isi Pola";

                layerIsiPola.Opacity = 50;

                gambar.AddLayer(layerIsiPola);

                gambar.Save(psdKeluaran);

            }

{{< /highlight >}}

**PSDNET-424. Dukungan untuk Informasi Tepi dari Sumber Daya Bagian Gambar #1009**

{{< highlight java >}}

             string berkasSumber = "input.psd";

            string berkasKeluaran = "output.psd";

            using (var gambar = (PsdImage)Image.Load(berkasSumber))

            {

                ResourceBlock[] sumberDayaGambar = gambar.ImageResources;

                BorderInformationResource sumberDayaInfoTepi = null;

                foreach (var sumberDayaGambarSatu in sumberDayaGambar)

                {

                    if (sumberDayaGambarSatu is BorderInformationResource)

                    {

                        sumberDayaInfoTepi = (BorderInformationResource)sumberDayaGambarSatu;

                        break;

                    }

                }

                // memperbarui BorderInformationResource

                sumberDayaInfoTepi.Width = 0.1;

                sumberDayaInfoTepi.Unit = PhysicalUnit.Inches;

                gambar.Save(berkasKeluaran);

            }

{{< /highlight >}}

**PSDNET-592. Dukungan untuk Lapisan dalam File Format AI**

{{< highlight java >}}

         void PeriksaBenar(bool kondisi, string pesan)

        {

            if (!kondisi)

            {

                throw new FormatException(pesan);

            }

        }

        string namaBerkasSumber = "form_8_2l3_7.ai";

        string namaBerkasKeluaran = "form_8_2l3_7_ekspor";

        using (AiImage gambar = (AiImage)Image.Load(namaBerkasSumber))

        {

            AiLayerSection layer0 = gambar.Layers[0];

            PeriksaBenar(layer0 != null, "Layer 0 seharusnya tidak null.");

            PeriksaBenar(layer0.Name == "Layer 4", "Properti Nama dari layer 0 seharusnya adalah Layer 4");

            PeriksaBenar(!layer0.IsTemplate, "Properti IsTemplate dari layer 0 seharusnya false.");

            PeriksaBenar(layer0.IsLocked, "Properti IsLocked dari layer 0 seharusnya true.");

            PeriksaBenar(layer0.IsShown, "Properti IsShown dari layer 0 seharusnya true.");

            PeriksaBenar(layer0.IsPrinted, "Properti IsPrinted dari layer 0 seharusnya true.");

            PeriksaBenar(!layer0.IsPreview, "Properti IsPreview dari layer 0 seharusnya false.");

            PeriksaBenar