---
title: Catatan Rilis Aspose.PSD untuk .NET 20.6
type: docs
weight: 70
url: /id/net/aspose-psd-for-net-20-6-release-notes/
---

{{% alert color="primary" %}} 

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 20.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-606 |Dukungan untuk Sumber LnkE|Fitur|
|PSDNET-386 |Dukungan untuk britResource (Sumber dari Lapisan Penyesuaian Ke cerahan/Kontras)|Fitur|
|PSDNET-219|Pindahkan pengaturan DefaultReplacementFont ke dalam kelas ImageOptionsBase|Peningkatan|
|PSDNET-596|Grup Lapisan dengan Mode Perata Tidak Melewati Tampilan|Bug|
|PSDNET-610|NullReference Exception saat mencoba mengonversi file Psd tertentu ke gambar|Bug|
|PSDNET-636|Perubahan Ukuran berkas PSD tidak berfungsi dengan benar jika terdapat masker pada lapisan penyesuaian yang memiliki batas kosong|Bug|
|PSDNET-611|OverflowException saat mencoba membuka file Psd tertentu|Bug|
|PSDNET-565|Gambar Psd dengan mode RGB 16 bit/channel hanya memperbarui lapisan pada pratinjau|Bug|
|PSDNET-652|Exception saat memuat file PSD tertentu dengan Sumber LnkE berkompaun dan properti adobeStockLicenseState|Bug|
|PSDNET-640|Perubahan Masker Lapisan PSD diabaikan saat disimpan|Bug|
|PSDNET-593|Menyimpan Berkas AI ke Format Jpeg2000 tidak berhasil|Bug|
|PSDNET-638|Urutan Lapisan Tidak Benar setelah menambahkan Grup Lapisan ke Grup Lapisan kosong|Bug|

## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.MaskRectangle
- P:Aspose.PSD.ImageOptionsBase.DefaultReplacementFont
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Type
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.UniqueId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalFileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileType
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.FileCreator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.ChildDocId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetModTime
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.AssetLockedState
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.IsLibraryLink
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.CompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.OriginalCompId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.HasFileOpenDescriptor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource.Length
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.None
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFD
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFE
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSourceType.liFA
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.Date
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileSize
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FileName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.FullPath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.RelativePath
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementRef
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.ElementName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFeDataSource.AdobeStockLicenseState
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LiFdDataSource.#ctor(System.Int32,System.Guid,System.String,System.String,System.String)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.IsEmpty
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.DataSourceCount
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lnk2Resource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkDataSource[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.TypeToolKey
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LnkeResource.Item(System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.TypeToolInfoStructures.StringStructure.#ctor(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ClassID,System.String)
# **API Dihapus:**
- P:Aspose.PSD.ImageLoadOptions.PsdLoadOptions.DefaultReplacementFont

## **Contoh Penggunaan:**
**PSDNET-606. Dukungan untuk Sumber LnkE**

{{< highlight java >}}

 string pesan = "ExampleOfLnkEResourceSupport tidak bekerja dengan benar.";

void AssertIsTrue(bool kondisi)

{

    if (!kondisi)

    {

        throw new FormatException(pesan);

    }

}

void AssertAreEqual(object aktual, object diharapkan)

{

    if (!object.Equals(aktual, diharapkan))

    {

        throw new FormatException(pesan);

    }

}

// Contoh ini menunjukkan bagaimana cara mendapatkan dan mengatur properti dari Sumber LnkE Photoshop yang berisi informasi tentang sebuah berkas terkait eksternal.

void ExampleOfLnkEResourceSupport(

    string lokasiBerkas,

    int panjang,

    int panjang2,

    int panjang3,

    int panjang4,

    string fullPath,

    string date,

    double assetModTime,

    string childDocId,

    bool terkunci,

    string uid,

    string nama,

    string originalFileName,

    string fileType,

    long ukuran)

{

    string namaBerkas = Path.GetFileName(lokasiBerkas);

    string outputPath = @"Output\" + namaBerkas;

    using (PsdImage image = (PsdImage)Image.Load(lokasiBerkas))

    {

        LnkeResource lnkeResource = null;

        foreach (var sumber in image.GlobalLayerResources)

        {

            lnkeResource = sumber as LnkeResource;

            if (lnkeResource != null)

            {

                AssertAreEqual(lnkeResource.Length, panjang);

                AssertAreEqual(lnkeResource.UniqueId, new Guid(uid));

                AssertAreEqual(lnkeResource.FullPath, fullPath);

                AssertAreEqual(lnkeResource.Date.ToString(CultureInfo.InvariantCulture), date);

                AssertAreEqual(lnkeResource.AssetModTime, assetModTime);

                AssertAreEqual(lnkeResource.AssetLockedState, terkunci);

                AssertAreEqual(lnkeResource.FileName, nama);

                AssertAreEqual(lnkeResource.FileSize, ukuran);

                AssertAreEqual(lnkeResource.ChildDocId, childDocId);

                AssertAreEqual(lnkeResource.Version, 7);

                AssertAreEqual(lnkeResource.FileType, fileType);

                AssertAreEqual(lnkeResource.FileCreator, string.Empty);

                AssertAreEqual(lnkeResource.OriginalFileName, originalFileName);

                AssertAreEqual(lnkeResource.CompId, -1);

                AssertAreEqual(lnkeResource.OriginalCompId, -1);

                AssertIsTrue(lnkeResource.HasFileOpenDescriptor);

                AssertIsTrue(!lnkeResource.IsEmpty);

                AssertIsTrue(lnkeResource.Type == LinkResourceType.liFE);

                lnkeResource.FullPath =

                    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png";

                AssertAreEqual(lnkeResource.Length, panjang2);

                lnkeResource.FileName = "rgb8_2x23.png";

                AssertAreEqual(lnkeResource.Length, panjang3);

                lnkeResource.ChildDocId = Guid.NewGuid().ToString();

                AssertAreEqual(lnkeResource.Length, panjang4);

                lnkeResource.Date = DateTime.Now;

                lnkeResource.AssetModTime = double.MaxValue;

                lnkeResource.FileSize = long.MaxValue;

                lnkeResource.FileType = "test";

                lnkeResource.FileCreator = "file";

                lnkeResource.CompId = int.MaxValue;

                break;

            }

        }

        AssertIsTrue(lnkeResource != null);

        image.Save(outputPath, new PsdOptions(image));

    }

    using (PsdImage image = (PsdImage)Image.Load(outputPath))

    {

        image.Save(

            Path.ChangeExtension(outputPath, "png"),

            new PngOptions

            {

                ColorType = PngColorType.TruecolorWithAlpha

            });

    }

}

// Contoh ini menunjukkan bagaimana cara mendapatkan dan mengatur properti dari Sumber LnkE PSD yang berisi informasi tentang berkas JPEG terkait eksternal.

this.ExampleOfLnkEResourceSupport(

    @"..\..\..\Issues\IMAGINGNET-2375\photooverlay_5_new.psd",

    0x21c,

    0x26c,

    0x274,

    0x27c,

    @"file:///C:/Users/cvallejo/Desktop/photo.jpg",

    "05/09/2017 22:24:51",

    0,

    "F062B9DB73E8D124167A4186E54664B0",

    false,

    "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

    "photo.jpg",

    "photo.jpg",

    "JPEG",

    0x1520d);

// Contoh ini menunjukkan bagaimana cara mendapatkan dan mengatur properti dari Sumber LnkE PSD yang berisi informasi tentang berkas PNG terkait eksternal.

this.ExampleOfLnkEResourceSupport(

    "rgb8_2x2_linked.psd",

    0x284,

    0x290,

    0x294,

    0x2dc,

    @"file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

    "04/14/2020 14:23:44",

    0,

    "",

    false,

    "5867318f-3174-9f41-abca-22f56a75247e",

    "rgb8_2x2.png",

    "rgb8_2x2.png",

    "png",

    0x53);

// Contoh ini menunjukkan bagaimana cara mendapatkan dan mengatur properti dari Sumber LnkE Photoshop yang berisi informasi tentang Aset Perpustakaan CC terkait eksternal.

this.ExampleOfLnkEResourceSupport(

    "rgb8_2x2_asset_linked.psd",

    0x398,

    0x38c,

    0x388,

    0x3d0,

    @"CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Fitur tersedia di Photoshop CC 2015)",

    "01/01/0001 00:00:00",

    1588890915488.0d,

    "",

    false,

    "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

    "rgb8_2x2_linked",

    "rgb8_2x2.png",

    "png",

    0);

{{< /highlight >}}

**PSDNET-201. Dukungan untuk kemajuan konversi dokumen**

{{< highlight java >}}

 string lokasiBerkasSumber = "Apple.psd";

Stream outputStream = new MemoryStream();

ProgressEventHandler localProgressEventHandler = delegate(ProgressEventHandlerInfo infoKemajuan)

{

      string pesan = string.Format(

           "{0} {1}: {2} dari {3}",

           infoKemajuan.Description,

           infoKemajuan.EventType,

           infoKemajuan.Value,

           infoKemajuan.MaxValue);

      Console.WriteLine(pesan);

};

Console.WriteLine("---------- Memuat Apple.psd ----------");

var loadOptions = new PsdLoadOptions() { ProgressEventHandler = localProgressEventHandler };

using (PsdImage gambar = (PsdImage)Image.Load(lokasiBerkasSumber, loadOptions))

{

      Console.WriteLine("---------- Menyimpan Apple.psd ke format PNG ----------");

      gambar.Save(

           outputStream,

           new PngOptions()

           {

                 ColorType = PngColorType.Truecolor, ProgressEventHandler = localProgressEventHandler

           });

      Console.WriteLine("---------- Menyimpan Apple.psd ke format PSD ----------");

      gambar.Save(

           outputStream,

           new PsdOptions()

           {

                 ColorMode = ColorModes.Rgb,

                 ChannelsCount = 4,

                 ProgressEventHandler = localProgressEventHandler

           });

}

{{< /highlight >}}

**PSDNET-386. Dukungan untuk britResource (Sumber dari Lapisan Penyesuaian Ke cerahan/Kontras)**

{{< highlight java >}}

 /* Contoh ini menunjukkan bagaimana Anda dapat mengubah secara terprogramatik Sumber Lapisan Kearahan/Kontras PSD - BritResource

   Ini adalah API Aspose.PSD tingkat rendah. Anda dapat menggunakan Lapisan Kearahan/Kontras melalui API-nya, yang akan jauh lebih mudah, 

   tetapi pengeditan sumber langsung PhotoShop memberi Anda lebih banyak kontrol atas konten berkas PSD.  */

string jalur = @"BrightnessContrastPS6.psd";

string outputPath = @"BrightnessContrastPS6_output.psd";

using (PsdImage im = (PsdImage)Image.Load(jalur))

{

    foreach (var lapisan in im.Layers)

    {

        if (lapisan is BrightnessContrastLayer)

        {

            foreach (var sumberLapisan in lapisan.Resources)

            {

                if (sumberLapisan is BritResource)

                {

                    var sumber = (BritResource)sumberLapisan;

                    isRequiredResourceFound = true;

                    if (sumber.Brightness != -40 ||

                        sumber.Contrast != 10 ||

                        sumber.LabColor != false ||

                        sumber.MeanValueForBrightnessAndContrast != 127)

                    {

                        throw new Exception("BritResource dibaca secara salah");

                    }

                    // Uji mengedit dan menyimpan

                    sumber.Brightness = 25;

                    sumber.Contrast = -14;

                    sumber.LabColor = true;

                    sumber.MeanValueForBrightnessAndContrast = 200;

                    im.Save(outputPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

{{< /highlight >}}

**PSDNET-596. Grup lapisan dengan Mode Tidak Melewati tidak Dirender**

{{< highlight java >}}

 string lokasiBerkasSumber = "MaskTestNormalBlendMaskOnGroup.psd";

string lokasiBerkasKeluaran = "MaskTestNormalBlendMaskOnGroup.png";

using (var input = (PsdImage)Image.Load(lokasiBerkasSumber))

{

    input.Save(lokasiBerkasKeluaran, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-610. NullReference Exception saat mencoba mengonversi file Psd tertentu ke gambar**

{{< highlight java >}}

 using (var psdImage = (PsdImage)Image.Load