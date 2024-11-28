---
title: Aspose.PSD for .NET 22.10 - Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

{{% alert color="warning" %}}

- Bu sürümde, 16 bit ihracatta bir regresyon bulunmaktadır, bu nedenle bu özelliği kullanırken dikkatli olmanızı öneririz.
Lütfen 16 bit görüntü işleme temel işlevinizse Aspose.PSD'yi 22.9-22.10 sürümlerine güncellemeyin.

Bu sorunlara çözüm bulmaya çalışıyoruz.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
| :- | :- | :- |
|PSDNET-1287| Lfx2Resource içindeki eski özellikler kaldırıldı | Geliştirme |
|PSDNET-1071| Aspose.PSD, ZipWithoutPrediction sıkıştırması ile PSD (RGB/16 bit) dosyalarını açamıyor | Hata |
|PSDNET-1257| Zaman çizelgesi efektleri Photoshop'ta kaybolur ve garip bir şekilde görünür | Hata |
|PSDNET-1278| Şeffaflık, İç Konum ile Stroke efektinde çalışmıyor | Hata |
|PSDNET-1279| Regresyon: PSD Dosyasının Açılmasında Hata | Hata |
|PSDNET-1284| Metin güncelleme, bazı Asya sembolleriyle başarısız olur. Belirli sembolün ayrıştırılmasında hata | Hata |
|PSDNET-1291| Metin güncelleme, bazı Asya sembolleriyle başarısız olur. Belirli sembolün oluşturulmasında hata | Hata |
|PSDNET-1292| Belirli Asya sembollerini kaydettikten sonra Photoshop tarafından dışa aktarılan dosyanın açılmasında hata | Hata |


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Yok


# **Kaldırılan API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **Kullanım örnekleri:**

**PSDNET-1071. Aspose.PSD, ZipWithoutPrediction sıkıştırması olan PSD'yi (RGB/16 bit) açamıyor**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. Zaman çizelgesi efektleri Photoshop'ta kaybolur ve garip bir şekilde görünür**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // Birkaç kare ile zaman çizelgesi oluştur.
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

**PSDNET-1278. Şeffaflık, İç Konum ile Stroke efektinde çalışmıyor**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. Regresyon: PSD Dosyasının Açılmasında Hata**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. Metin güncelleme, bazı Asya sembolleriyle başarısız olur. Belirli sembolün ayrıştırılmasında hata**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔尕尖尗尘尙尚尛尜尝尞尟尠尡尢尣尤尥尦尧尨尩尪尫尬尭尮尯尰就尲尳尴尵尶尷尸尹尺尻尼尽尾尿局屁层屃屄居屆屇屈屉届屋屌屍屎屏";

testData = testData.Substring(25, 1); // Sorunlu sembolü seç

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. Lfx2Resource içindeki eski özellikler kaldırıldı**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // Efektin BlendMode seçeneğini güncelle
    effect.BlendMode = BlendMode.Darken;

    // Efektin Opacity seçeneğini güncelle
    effect.Opacity = 128; // %50

    // Stroke efektinin dolgu Rengini güncelle
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. Metin güncelleme, bazı Asya sembolleriyle başarısız olur. Belirli sembollerin renderlanmasında hata**

{{< highlight csharp >}}
string testData = @"咐咑咒咓咔咕咖咗咘咙咚咛咜咝咞咟咠咡咢咣咤咥咦咧咨咩咪咫咬咭咮咯咰咱咲咳咴咵咶咷咸咹咺咻咼咽咾咿
哀品哂哃哄哅哆哇哈哉哊哋哌响哎哏";

testData = testData.Substring(40, 25); // Sorunlu sembolleri seç

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. Belirli Asya sembollerini kaydettikten sonra Photoshop tarafından dışa aktarılan dosyanın açılmasında hata**

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
