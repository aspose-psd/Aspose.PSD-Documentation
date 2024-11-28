---
title: Catatan Rilis Aspose.PSD untuk Java 20.4
type: docs
weight: 30
url: /id/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDJAVA-156|Dukungan dari sumber 'Data Asal Vektor'|Fitur|
|PSDJAVA-171|Dukungan lclrResource (Pengaturan warna lembar)|Fitur|
|PSDJAVA-157|Dukungan properti dari data LengthRecord. (Operasi jalur (operasi boolean), indeks bentuk dalam lapisan, jumlah rekaman simpul bezier)|Fitur|
|PSDJAVA-158|Dukungan dari Sumber Gambar Bagian #1010 Warna Latar Belakang|Fitur|
|PSDJAVA-161|Penambahan Lapisan Isi saat runtime|Fitur|
|PSDJAVA-168|Dukungan dari Sumber Gambar Bagian #1009 Informasi Border.|Fitur|
|PSDJAVA-169|Dukungan Lapisan dalam Berkas Format AI|Fitur|
|PSDJAVA-163|Dukungan Membaca dan Mengedit Efek Lapisan Gaya Overlay Gradien|Fitur|
|PSDJAVA-164|Rendering Efek Lapisan Overlay Gradien|Fitur|
|PSDJAVA-149|Aspose.PSD untuk java error saat mendapatkan properti teksData.items dari lapisan teks|Bug|
|PSDJAVA-166|Perbaikan penyimpanan gambar PSD dengan Grayscale ColorMode dan 16 bit per saluran ke format PSD Grayscale|Bug|
|PSDJAVA-167|Perbaikan penyimpanan gambar PSD dengan Grayscale ColorMode dan 16 bit per saluran ke format PNG|Bug|
|PSDJAVA-159|Perubahan properti The GradientOverlayEffect.BlendMode tidak ditampilkan di Photoshop.|Bug|
# **Perubahan API Publik**
# **API Ditambahkan:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.getBlendModeKey
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesContinuousManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesDiscreteManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.getChannelsCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.CurvesManager.isChannelUsed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LayerSectionResource.setBlendModeKey(long)
- M:com.aspose.psd.fileformats.psd.layers.text.IText.producePortions(java.lang.String[],com.aspose.psd.fileformats.psd.layers.text.ITextStyle,com.aspose.psd.fileformats.psd.layers.text.ITextParagraph)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getBaselineShift
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxBold
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFauxItalic
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontBaseline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getFontCaps
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getStrikethrough
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.getUnderline
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setBaselineShift(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxBold(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFauxItalic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontBaseline(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setFontCaps(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setLeading(double)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setStrikethrough(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.setUnderline(boolean)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Subscript
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontBaseline.Superscript
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.AllCaps
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.None
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.FontCaps.SmallCaps
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream)
- M:com.aspose.psd.sources.StreamSource.#ctor(java.io.OutputStream,boolean)
## **API Dihapus:**
- M:com.aspose.psd.fileformats.psd.layers.Layer.#ctor(com.aspose.psd.internal.ij.k,com.aspose.psd.IColorPalette)
- M:com.aspose.psd.xmp.schemas.xmpdm.XmpDynamicMediaPackage.setAudioSampleType(com.aspose.psd.xmp.schemas.xmpdm.AudioSampleType)
# **Contoh Penggunaan:**

**PSDJAVA-156. Dukungan dari sumber 'Data Asal Vektor'**

{{< highlight java >}}

 /*

Sebuah contoh membaca dan memodifikasi sumber Data Asal Vektor.

*/

// Simpan metode dalam ruang lingkup lokal untuk kesederhanaan

class LocalScopeExtension

{

    VogkResource findFirstVogkResource(LayerResource[] layerResources)

    {

        VogkResource vogkResource = null;

        for (LayerResource layerResource : layerResources)

        {

            if (layerResource instanceof VogkResource)

            {

                vogkResource = (VogkResource)layerResource;

                break;

            }

        }

        if (vogkResource == null)

        {

            throw new Exception("VogkResource tidak ditemukan.");

        }

        return vogkResource;

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "VectorOriginationDataResource.psd";

String outPsdFilePath = "out_VectorOriginationDataResource_.psd";

// Muat file PSD yang berisi sumber VOGK yang telah ditentukan

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Temukan VogkResource pertama di sumber lapisan yang telah ditentukan

    VogkResource vogkResource = $.findFirstVogkResource(

            psdImage.getLayers()[1].getResources());

    // Verifikasi properti sumber yang telah ditentukan

    if (vogkResource.getShapeOriginSettings().length != 1 ||

            !vogkResource.getShapeOriginSettings()[0].isShapeInvalidated() ||

            vogkResource.getShapeOriginSettings()[0].getOriginIndex() != 0)

    {

        throw new Exception("VogkResource salah dibaca.");

    }

    // Modifikasi beberapa properti VogkResource

    vogkResource.setShapeOriginSettings(new VectorShapeOriginSettings[]

            {

                    vogkResource.getShapeOriginSettings()[0],

                    new VectorShapeOriginSettings(true, 1)

            });

    // Simpan salinan yang telah dimodifikasi dari file PSD yang dimuat pada jalur

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-171. Dukungan lclrResource (Pengaturan warna lembar)**

{{< highlight java >}}

 /*

Sebuah contoh penggunaan Warna Lembar Lapisan untuk menyoroti visual lapisan. Sebagai contoh, Anda dapat

memperbarui beberapa lapisan dalam PSD dan kemudian menyoroti dengan warna lapisan yang ingin Anda tarik

perhatian.

*/

class LocalScopeExtension

{

    void checkSheetColorsAndRerverse(Short[] sheetColors, PsdImage psdImage)

    {

        int layersCount = psdImage.getLayers().length;

        for (int layerIndex = 0; layerIndex < layersCount; layerIndex++)

        {

            Layer layer = psdImage.getLayers()[layerIndex];

            for (LayerResource layerResource : layer.getResources())

            {

                if (!(layerResource instanceof LclrResource))

                {

                    continue;

                }

                // Sumber lcrl selalu hadir dalam daftar sumber file psd.

                LclrResource resource = (LclrResource)layerResource;

                if (resource.getColor() != sheetColors[layerIndex])

                {

                    throw new Exception("Warna Lembar salah dibaca");

                }

                // Pembalikan warna latar belakang lapisan. Menyiapkan lapisan sorot warna.

                resource.setColor(sheetColors[layersCount - layerIndex - 1]);

                break;

            }

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

String inPsdFilePath = "AllLclrResourceColors.psd";

String outPsdFilePath = "AllLclrResourceColorsReversed.psd";

// Pada berkas warna lapisan adalah urutan ini

Short[] sheetColors = new Short[] {

        SheetColorHighlightEnum.Merah,

        SheetColorHighlightEnum.Oranye,

        SheetColorHighlightEnum.Kuning,

        SheetColorHighlightEnum.Hijau,

        SheetColorHighlightEnum.Biru,

        SheetColorHighlightEnum.Ungu,

        SheetColorHighlightEnum.Abu_Abu,

        SheetColorHighlightEnum.Tanpa_Warna

};

// Muat file PSD yang berisi sumber LclrResource yang telah ditentukan

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    $.checkSheetColorsAndRerverse(sheetColors, psdImage);

    psdImage.save(outPsdFilePath, new PsdOptions());

}

finally

{

    psdImage.dispose();

}

// Muat file PSD yang baru disimpan

PsdImage psdImage1 = (PsdImage)Image.load(outPsdFilePath);

try

{

    // Balik warna

    List<Short> sheetColorList = Arrays.asList(sheetColors);

    Collections.reverse(sheetColorList);

    $.checkSheetColorsAndRerverse(sheetColorList.toArray(new Short[0]), psdImage1);

}

finally

{

    psdImage1.dispose();

}

{{< /highlight >}}

**PSDJAVA-157. Dukungan properti dari data LengthRecord. (Operasi jalur (operasi boolean), indeks bentuk dalam lapisan, jumlah rekaman simpul bezier)**

{{< highlight java >}}

 /*

Sebuah contoh mengubah operasi jalur saat bekerja dengan bentuk. Program membaca

rekaman jalur vektor yang telah ditentukan (LengthRecord) dan mengubah operasi jalur mereka kemudian menyimpan

salinan yang dimodifikasi dari dokumen sebagai file PSD baru.

*/

String inPsdFilePath = "PathOperationsShape.psd";

String outPsdFilePath = "out_" + inPsdFilePath;

// Muat berkas PSD yang berisi sumber vsms yang telah ditentukan

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    // Temukan VsmsResource pertama di sumber lapisan yang telah ditentukan

    VsmsResource resource = null;

    for (LayerResource layerResource : psdImage.getLayers()[1].getResources())

    {

        if (layerResource instanceof VsmsResource)

        {

            resource = (VsmsResource)layerResource;

            break;

        }

    }

    LengthRecord lengthRecord0 = (LengthRecord)resource.getPaths()[2];

    LengthRecord lengthRecord1 = (LengthRecord)resource.getPaths()[7];

    LengthRecord lengthRecord2 = (LengthRecord)resource.getPaths()[11];

    // Mengubah cara bentuk digabungkan

    lengthRecord0.setPathOperations(PathOperations.ExcludeOverlappingShapes);

    lengthRecord1.setPathOperations(PathOperations.IntersectShapeAreas);

    lengthRecord2.setPathOperations(PathOperations.SubtractFrontShape);

    // Simpan salinan yang dimodifikasi dari file PSD yang dimuat pada jalur

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}

**PSDJAVA-158. Dukungan dari Sumber Gambar Bagian #1010 Warna Latar Belakang**

{{< highlight java >}}

 /*

Sebuah contoh membaca dan memodifikasi sumber warna latar belakang.

*/

String inPsdFilePath = "input.psd";

String outPsdFilePath = "output.psd";

// Muat berkas PSD yang berisi sumber warna latar belakang yang sudah ditentukan

PsdImage psdImage = (PsdImage)Image.load(inPsdFilePath);

try

{

    BackgroundColorResource backgroundColorResource = null;

    for (ResourceBlock imageResource : psdImage.getImageResources())

    {

        if (imageResource instanceof BackgroundColorResource)

        {

            backgroundColorResource = (BackgroundColorResource)imageResource;

            break;

        }

    }

    if (backgroundColorResource == null)

    {

        throw new Exception("Sumber Warna Latar Belakang tidak ditemukan");

    }

    // Perbarui warna dari sumber warna latar belakang

    backgroundColorResource.setColor(Color.getDarkRed());

    // Simpan salinan yang dimodifikasi dari file PSD yang dimuat pada jalur

    psdImage.save(outPsdFilePath);

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}