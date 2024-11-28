---
title: Catatan Rilis Aspose.PSD untuk .NET 22.10
type: docs
weight: 30
url: /id/net/aspose-psd-untuk-net-22-10-catatan-rilis/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Rilis ini memiliki regresi dalam kasus ekspor 16-bit, jadi kami menyarankan untuk berhati-hati saat menggunakan fitur ini dalam rilis ini.
Tolong jangan perbarui Aspose.PSD ke 22.9-22.10 jika pemrosesan gambar 16-bit adalah fungsi utama Anda.

Kami sedang bekerja pada solusi untuk masalah-masalah ini.

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1287|Hapus properti usang dalam Lfx2Resource|Peningkatan|
|PSDNET-1071|Aspose.PSD tidak bisa membuka PSD (RGB/16bit) dengan kompresi ZipWithoutPrediction|Bug|
|PSDNET-1257|Efek timeline hilang dan ditampilkan dengan cara yang aneh. (di Photoshop)|Bug|
|PSDNET-1278|Transparansi tidak berfungsi untuk efek Stroke dengan Posisi Inside|Bug|
|PSDNET-1279|Regresi: Kesalahan saat membuka File PSD|Bug|
|PSDNET-1284|Pembaruan teks gagal dengan beberapa simbol Asia. Kesalahan saat menguraikan simbol khusus|Bug|
|PSDNET-1291|Pembaruan teks gagal dengan beberapa simbol Asia. Kesalahan dalam merender simbol tertentu|Bug|
|PSDNET-1292|Kesalahan saat membuka file yang diekspor oleh Photoshop setelah menyimpan simbol Asia tertentu|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- Tidak ada


# **API Dihapus:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Contoh Penggunaan:**

**PSDNET-1071. Aspose.PSD tidak bisa membuka PSD (RGB/16bit) dengan kompresi ZipWithoutPrediction**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Efek timeline hilang dan ditampilkan dengan cara yang aneh. (di Photoshop)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Buat timeline dengan beberapa frame.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. Transparansi tidak berfungsi untuk efek Stroke dengan Posisi Inside**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regresi: Kesalahan saat membuka File PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Pembaruan teks gagal dengan beberapa simbol Asia. Kesalahan saat menguraikan simbol khusus**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // pilih simbol bermasalah

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Hapus properti usang dalam Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Perbarui opsi BlendMode efek
    effect.BlendMode = BlendMode.Darken;

    // Perbarui opsi Opacity efek
    effect.Opacity = 128; // 50%

    // Perbarui opsi Warna isi efek stroke
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Pembaruan teks gagal dengan beberapa simbol Asia. Kesalahan saat merender simbol tertentu**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // pilih simbol bermasalah

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Kesalahan saat membuka file yang diekspor oleh Photoshop setelah menyimpan simbol Asia tertentu**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
