---
title: Aspose.PSD for .NET 22.9 - Sürüm Notları
type: docs
weight: 40
url: /tr/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

{{% alert color="warning" %}}

- Bu sürümde, 16 bit dışa aktarmalarda bir gerileme bulunmaktadır, bu nedenle bu özelliği kullanırken dikkatli olmanızı öneririz.
Lütfen, 16 bit görüntü işleme işleviniz ana işleviniz ise Aspose.PSD'yi 22.9 sürümüne güncellemeyin.
- Photoshop'un birkaç sürümü için kullanıcılar, bir hata okuyan katman ile bir pencere ile karşılaşabilirler, bu durum PSD dosyası ile çalışmayı etkilemeyecektir.

Bu sorunlara çözüm bulmaya çalışıyoruz.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1237|Efektler ve ilgili verileri içerecek iç LayerStyleFX modelini oluşturun; Efekt kaynaklarında tek modeli kullanmak için|Geliştirme|
|PSDNET-1227|Zaman Çizelgesi modellerinde katman durumları için efekt bilgilerine sahip 'Lefx' yapılarının okunması ve yazılması|Özellik|
|PSDNET-1230|TimeLine katman durumunu PsdImage'da uygulama|Özellik|
|PSDNET-1072|PSD dosyasının kaydedilmesinde (RGB/16bit) hatalı şeffaflık (8 bit'e dışa aktarılırken)|Hata|
|PSDNET-1140|PSB belgesi açıldığında küresel katman kaynak adımında istisna|Hata|
|PSDNET-1266|Belirli dosyaların işlenmesinde bellek sızıntısı|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
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


# **Kaldırılan API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **Kullanım örnekleri:**

**PSDNET-1072. PSD dosyasının kaydedilmesinde hatalı şeffaflık (RGB/16bit) 8 bit'e dışa aktarılırken**

{{< highlight csharp >}}
string inputPsdFile    = "Şeffaflıkla8Bit.psd";
string outputPsdFile   = "Şeffaflıkla16Bit.psd";
string outputImageFile = "ŞeffaflıklaÇıktı.png";

using (var img = Image.Load(inputPsdFile))
{
    // 16 bit kaydetme seçenekleri
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // 16 bit renklerle resmi kaydet
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. PSB belgesi açıldığında küresel katman kaynak adımında istisna**

{{< highlight csharp >}}
string sourcePsdFile = "giriş.psb";
string outputImageFile = "çıktı.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // Burada istisna olmamalıdır.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. Zaman Çizelgesi modellerinde katman durumları için efekt bilgilerine sahip 'Lefx' yapılarının okunması ve yazılması**

{{< highlight csharp >}}
string sourceFile = "4_animasyonlu.psd";
string outputFile = "çıktı.psd";

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

**PSDNET-1230. Zaman Çizelgesi katman durumunu PsdImage'a uygulama**

{{< highlight csharp >}}
string sourceFile = "3_animasyonlu.psd";
string outputPsd = "çıktı.psd";
string outputPng = "çıktı.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // Etkin çerçeveyi 0'dan 1'e değiştirerek Katman Durumu'nu Katmana uygulayın
    timeLine.ActiveFrame = 1;

    // Değişiklikleri PsdImage'a uygulayın
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. Belirli dosyaların işlenmesinde bellek sızıntısı**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("Test öncesi kullanılan toplam bayt: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // Açma/Kaydetme kontrolü
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
Console.WriteLine("Test sonrası kullanılan toplam bayt: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "Temel işlevde bellek sızıntısı bulundu!");
{{< /highlight >}}
