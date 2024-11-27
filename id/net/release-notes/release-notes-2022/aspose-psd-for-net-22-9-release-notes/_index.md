---
title: Catatan Rilis Aspose.PSD untuk .NET 22.9
type: docs
weight: 40
url: /id/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Rilis ini memiliki regresi dalam kasus ekspor 16-bit, sehingga kami menyarankan berhati-hati saat menggunakan fitur ini dalam rilis ini. Tolong jangan perbarui Aspose.PSD ke 22.9 jika pemrosesan gambar 16-bit adalah fungsionalitas utama Anda.
- Untuk beberapa versi Photoshop, pengguna mungkin mengalami jendela dengan pesan kesalahan pembacaan lapisan, ini tidak akan mempengaruhi pekerjaan dengan file PSD.

Kami sedang bekerja pada solusi untuk masalah-masalah ini.

{{% /alert %}}

|**Kunci**|**Ringkasan**|**Kategori**|
| :- | :- | :- |
|PSDNET-1237|Membuat model LayerStyleFX internal yang akan berisi efek dan data terkait untuk menggunakan model tunggal di sumber daya efek Lfx2, lmfx, dan mlst|Peningkatan|
|PSDNET-1227|Menambahkan pembacaan dan penulisan struktur 'Lefx' dengan informasi efek untuk status lapisan dalam model TimeLine|Fitur|
|PSDNET-1230|Menerapkan status lapisan TimeLine ke lapisan dalam PsdImage|Fitur|
|PSDNET-1072|Ketidaksesuaian transparansi saat menyimpan file PSD (RGB/16-bit) saat diekspor ke 8-bit|Bug|
|PSDNET-1140|Pengecualian saat memuat langkah sumber daya lapisan global saat membuka dokumen PSB|Bug|
|PSDNET-1266|Kebocoran memori pada pemrosesan file tertentu|Bug|


## **Perubahan API Publik**
# **API Ditambahkan:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **API Dihapus:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Contoh Penggunaan:**

**PSDNET-1072. Ketidaksesuaian transparansi saat menyimpan file PSD (RGB/16-bit) saat diekspor ke 8-bit**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // Opsi simpan 16 bit
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Simpan gambar dengan warna 16 bit
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. Pengecualian saat memuat langkah sumber daya lapisan global saat membuka dokumen PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Di sini seharusnya tidak ada pengecualian.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Menambahkan pembacaan dan penulisan struktur 'Lefx' dengan informasi efek untuk status lapisan dalam model TimeLine**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. Menerapkan status lapisan TimeLine ke lapisan dalam PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // Ubah frame aktif dari 0 menjadi 1 untuk mengaktifkan penerapan LayerState ke Layer
    timeLine.ActiveFrame = 1;

    // Terapkan perubahan ke PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Kebocoran memori pada pemrosesan file tertentu**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total bytes yang digunakan sebelum pengujian: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // CheckOpenSaving
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Total bytes yang digunakan setelah pengujian: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Kebocoran memori dalam fungsionalitas dasar ditemukan!");
{{< /highlight >}}
