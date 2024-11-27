---
title: Catatan Rilis Aspose.PSD for Java 20.6
type: docs
weight: 50
url: /id/java/aspose-psd-for-java-20-6-catatan-rilis/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-216|Dukungan untuk LnkEResource (Sumber Daya Layer Objek Pintar)|Fitur|
|PSDJAVA-219|Dukungan untuk britResource (Sumber Daya Layer Penyesuaian Kecerahan/Kontras)|Fitur|
|PSDJAVA-222|Pindahkan pengaturan DefaultReplacementFont ke dalam kelas ImageOptionsBase|Perbaikan|
|PSDJAVA-217|Pengubahan ukuran file PSD tidak berfungsi dengan benar jika terdapat masker dalam layer penyesuaian yang memiliki batas kosong|Bug|
|PSDJAVA-218|Gambar Psd dengan mode RGB 16 bit/channel hanya memperbarui layer pada pratinjau|Bug|
|PSDJAVA-220|Perubahan Masker Layer PSD diabaikan saat disimpan|Bug|
|PSDJAVA-221|Urutan Layer Tidak Tepat setelah menambahkan Layer Group ke Layer Group kosong|Bug|
|PSDJAVA-223|Pengecualian saat memuat file PSD khusus dengan compound LnkE Resource dan properti adobeStockLicenseState|Bug|
|PSDJAVA-224|Penyimpanan Berkas AI ke Format Jpeg2000 tidak berfungsi|Bug|
|PSDJAVA-225|Layer Group dengan Mode Pencampuran Bukan PassThrough Tidak Dirender|Bug|
|PSDJAVA-226|Pengecualian NullReference saat mencoba mengonversi file Psd tertentu ke gambar|Bug|
|PSDJAVA-227|OverflowException saat mencoba membuka file Psd tertentu|Bug|

# **Perubahan API Publik**
# **API Ditambahkan:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **API Dihapus:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Contoh Penggunaan:**

**PSDJAVA-216: Dukungan untuk LnkEResource (Sumber Daya Layer Objek Pintar)**

{{< highlight java >}}

 // Sebuah contoh tentang mengaitkan berbagai jenis aset (gambar raster, perpustakaan CC) ke PSD.

// Juga API dari LnkeResource dipertimbangkan.

// Sebuah kelas yang menyimpan metode dalam cakupan lokal

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("ExampleOfLnkEResourceSupport bekerja tidak benar.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Contoh ini mendemonstrasikan bagaimana mendapatkan dan mengatur properti dari Photoshop Psd LnkE

    // Resource yang berisi informasi tentang file terkait eksternal.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Memuat PSD yang telah ditentukan sebelumnya

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Mencari LnkeResource di antara sumber daya layer global

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Memverifikasi properti LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Memperbarui properti LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Pastikan LnkeResource didukung

            assertIsTrue(lnkeResource != null);

            // Simpan salinan PSD yang dimuat

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Memuat salinan yang disimpan

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Mengonversi PSD ke format file PNG (dengan saluran alpha untuk transparansi)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Contoh ini mendemonstrasikan cara mendapatkan dan menetapkan properti dari Psd LnkE Resource yang

// berisi informasi tentang file JPEG eksternal yang terkait.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Contoh ini mendemonstrasikan cara mendapatkan dan menetapkan properti dari LnkE Resource PSD yang

// berisi informasi tentang file PNG eksternal yang terkait.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Contoh ini mendemonstrasikan cara mendapatkan dan menetapkan properti dari Psd LnkE Resource Photoshop

// yang berisi informasi tentang Aset Perpustakaan CC terkait eksternal.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (Fitur tersedia di Photoshop CC 2015)",

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

**PSDJAVA-219: Dukungan untuk britResource (Sumber Daya Layer Penyesuaian Kecerahan/Kontras)**

{{< highlight java >}}

 // Contoh ini menunjukkan bagaimana Anda dapat mengubah Layer Sumber Daya Kecerahan/Kontras PSD secara pemrograman.

// Ini adalah API Aspose.PSD Level Rendah.

// Anda dapat menggunakan Layer Kecerahan/Kontras melalui API-nya, yang akan jauh lebih mudah,

// tetapi pengeditan sumber daya langsung PhotoShop memberi Anda lebih banyak kontrol atas konten berkas PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Memuat dokumen Photoshop yang berisi lapisan penyesuaian Kecerahan / Kontras

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Mencari BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Memverifikasi properti sumber daya

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource dibaca dengan salah");

                    }

                    // Memperbarui properti sumber daya

                    resource.setBrightness((short)-40);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Menyimpan salinan PSD yang telah diperbarui

                    psdImage.save(dstPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-217: Pengubahan ukuran file PSD tidak berfungsi dengan benar jika terdapat masker dalam layer penyesuaian yang memiliki batas kosong**

{{< highlight java >}}

 // Contoh pengubahan ukuran gambar yang berisi masker layer penyesuaian dengan batas kosong.

// Program memuat PSD yang telah ditentukan sebelumnya hanya untuk memeriksa apakah tidak ada pengecualian.

final int skala = 2; // koefisien arbitrer

String[] nama = {

        "OneRegularAndOneAdjustmentWithVectorAndLayerMask",

        "LevelsLayerWithLayerMaskRgb",

        "LevelsLayerWithLayerMaskCmyk",

};

for (String nama : nama)

{

    String srcFilePath = nama + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + nama + ".png";

    // Memuat PSD yang telah ditentukan sebelumnya yang berisi masker layer penyesuaian yang memiliki batas kosong

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();

    psdLoadOptions.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, psdLoadOptions);

    try

    {

        // Mengubah ukuran gambar

        image.resize(image.getWidth() * skala, image.getHeight() * skala);

        // Menyimpan salinan PSD yang dimuat

        image.save(dstFilePath, new PsdOptions());

        // Eksport PSD ke format file PNG (dengan saluran alpha untuk transparansi)

        PngOptions pngOptions = new PngOptions();

        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, pngOptions);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}

**PSDJAVA-218: Gambar Psd dengan mode RGB 16 bit/channel hanya memperbarui layer pada pratinjau**

{{< highlight java >}}

 // Contoh memperbarui layer reguler untuk gambar RGB 16 bit. Program menggambar sesuatu

// pada setiap layer hanya untuk memastikan bahwa seluruh layer diperbarui dengan benar.

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

// Memuat PSD yang telah ditentukan sebelumnya dalam mode RGB 16 bit

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // Menggambar nama layer dan batas dalam untuk layer reguler

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Menyimpan salinan PSD yang dimuat

    image.save(outputFilePath, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-220: Perubahan Masker Layer PSD diabaikan saat disimpan**

{{< highlight java >}}

 // Sebuah kelas yang menyimpan metode dalam cakupan lokal

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("Contoh bekerja tidak benar.");

        }

    }

    // Mendapatkan nilai int yang dikonversi ke urutan byte big-endian.

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Mendapatkan nilai yang dikonversi dari big endian ke Int32.

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("index", "Indeks jatuh di luar array byte.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // Mendapatkan masker raster dari layer pada gambar PSD dan menyimpannya ke berkas

    void saveRasterMask(String maskFilePath, Layer layer)

    {

        LayerMaskDataShort maskData = (LayerMaskDataShort)layer.getLayerMaskData();

        FileStreamContainer container = FileStreamContainer.createFileStream(maskFilePath, false);

        try

        {

            container.write(getBigEndianBytesInt32(maskData.getTop()));

            container.write(getBigEndianBytesInt32(maskData.getLeft()));

            container.write(getBigEndianBytesInt32(maskData.getBottom()));

            container.write(getBigEndianBytesInt32(maskData.getRight()));

            container.writeByte(maskData.getDefaultColor());

            container.writeByte((byte)maskData.getFlags());

            container.write(getBigEndianBytesInt32(maskData.getImageData().length));

            container.write(maskData.getImageData(), 0, maskData.getImageData().length);

        }

        finally

        {

            container.dispose();

        }

    }

    // Menambahkan masker raster dari berkas ke layer dan menyimpannya ke gambar format PSD

    void addRasterMask(Layer layer, String maskSourcePath)

    {

        LayerMaskDataShort maskData = new LayerMaskDataShort();

        FileStreamContainer container = FileStreamContainer.openFileStream(maskSourcePath);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(container.read(bytes), 22);

            maskData.setTop(fromBigEndianToInt32(bytes, 0));

            maskData.setLeft(fromBigEndianToInt32(bytes, 4));

            maskData.setBottom(fromBigEndianToInt32(bytes, 8));

            maskData.setRight(fromBigEndianToInt32(bytes, 12));

            maskData.setDefaultColor(bytes[16]);

            maskData.setFlags(bytes[17]);

            int imageDataLength = fromBigEndianToInt32(bytes, 18);

            byte[] data = new byte[imageDataLength];

            assertAreEqual(maskData.getMaskRectangle().getWidth() *

                    maskData.getMaskRectangle().getHeight(), imageDataLength);

            assertAreEqual(container.read(data), imageDataLength);

            maskData.setImageData(data);

        }

        finally

        {

            container.dispose();

        }

        // Menambahkan LayerMaskData saja tidak cukup untuk penyimpanan yang benar karena channel tidak diperbarui;

        // layer.setLayerMaskData(mask); // Ini tidak menambahkan saluran masker

        // Menambahkan (atau memperbarui) masker

        layer.addLayerMask(maskData); // Tapi ini menambah/memperbarui kedua masker dan saluran! 

        }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Contoh ini menunjukkan bagaimana mendapatkan, memperbarui, menghapus, dan menambahkan masker layer raster

// dalam file Photoshop® PSD secara pemrograman.

PngOptions pngOptions = new PngOptions();

pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

String sourceFilePath = "FourWithMasks.psd";

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    Layer layer = image.getLayers()[2];

    // Dapatkan masker raster dari layer dan simpan ke berkas

    $.saveRasterMask("FourWithMasks2.msk", layer);

    // Ubah masker layer (balik) dan simpan gambar

    LayerMaskData mask = layer.getLayerMaskData();

    byte[] maskData = mask.getImageData();

    for (int i = 0; i < maskData.length; i++)

    {

        maskData[i] = (byte)~maskData[i];

    }

    // Hanya mengubah LayerMaskData cukup untuk efek rendering

    image.save("FourWithMasksUpdated2.png", pngOptions);

    // Tetapi hanya mengubah LayerMaskData tidak cukup untuk penyimpanan yang benar karena channel tidak diperbarui;

    layer.setLayerMaskData(mask); // Ini juga tidak berhasil

    layer.addLayerMask(mask); // Tapi ini mengupdate kedua masker dan saluran!

    image.save("FourWithMasksUpdated2.psd");

    // Hapus masker raster dari layer dan simpan gambar

    layer.setLayerMaskData(null); // Hanya menghapus LayerMaskData cukup untuk efek rendering tetapi tidak untuk penyimpanan ke format PSD

    image.save("FourWithMasksRemoved2.png", pngOptions);

    layer.addLayerMask(null); // Tetapi ini menghapus baik masker maupun saluran masker!

    image.save("FourWithMasksRemoved2.psd");

    // Tambahkan masker raster dari berkas ke layer dan simpan gambar

    $.addRasterMask(layer, "raster.msk");

    image.save("FourWithMasksAdded2.png", pngOptions);

    image.save("FourWithMasksAdded2.psd");

}

finally

{

    image.dispose();

}

{{< /highlight >}}

**PSDJAVA-221: Urutan Layer Tidak Tepat setelah menambahkan Layer Group ke Layer Group kosong**

{{< highlight java >}}

 // Contoh mendemonstrasikan cara menambahkan layer group bersarang ke PSD secara pemrograman.

String dstPsdPath = "output.psd";

// Membuat gambar dengan ukuran 1x1 piksel untuk bekerja

PsdImage psdImage = new PsdImage(1, 1);

try

{

    // Menambahkan layer group induk ("true" berarti membuka layer group saat dimulai)

    LayerGroup group1 = psdImage.addLayerGroup("Grup 1", 0, true);

    // Menambahkan layer group bersarang

    LayerGroup group2 = group1.addLayerGroup("Grup 2", 0);

    if (group1.getLayers().length != 2)

    {

        throw new RuntimeException("Grup 1 harus berisi dua layer Grup 2.");

    }

    // Memverifikasi bahwa tidak ada pengecualian saat menyimpan layer group yang baru saja dibuat

    psdImage.save(dstPsdPath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-223: Pengecualian saat memuat file PSD khusus dengan compound LnkE Resource dan properti adobeStockLicenseState**

{{< highlight java >}}

 // Contoh mendemonstrasikan cara membaca dan mengubah sumber daya tautan eksternal Adobe® Photoshop®

// (LnkeResource) dengan berbagai sumber daya (gambar, perpustakaan CC) secara pemrograman.

// Kelas yang menyimpan metode dalam cakupan lokal

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("Contoh bekerja tidak benar.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    void exampleOfComplexLnkEResourceSupport(String srcPsdPath, int length, int length2, Object[] dataSourceExpectedValues)

    {

        // Memuat PSD yang telah ditentukan sebelumnya yang berisi LayerResource dengan beberapa sumber daya

        PsdImage image = (PsdImage)Image.load(srcPsdPath);

        try

        {

            // Mencari LnkeResource

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources