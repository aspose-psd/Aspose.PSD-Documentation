---
title: Aspose.PSD for .NET 24.6 - Yayın Notları
type: docs
weight: 70
url: /tr/net/aspose-psd-for-net-24-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.6 için](https://www.nuget.org/packages/Aspose.PSD/) yayın notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                                               | **Kategori** |
|:------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDNET-1450 | Gradient harita katmanı desteğini uygulayın                                            | Özellik      |
| PSDNET-1670 | [AI Format] XPacket Metadata desteği ekleme                                                         | Özellik      |
| PSDNET-1831 | Şişirme, Sıkıştırma ve Burulma türlerini uygulayın                                            | Özellik      |
| PSDNET-1653 | Rgb ve Lab modları, Sanat Tabakası Katmanları içeren dosyalarda 3 kanaldan az ve 4 kanaldan fazla içerebilir                 | Hata      |
| PSDNET-1775 | İşleme alanı üstü pozitif olmalı. Belirli dosyanın işlenmesinde ('areaToProcess' parametresi)                                                                               | Hata      |
| PSDNET-2052 | Genişletilmiş kanvas resmi kaydedildikten sonra kırpılır. Veri kaybolur ancak Önizleme doğru görünüyor                                                                               | Hata      |

## **Kullanıcı API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-1450. Gradient harita katmanı desteğini uygulayın**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "gradient_map_src.psd");
string çıktıDosyası = Path.Combine(outputFolder, "gradient_map_src_output.psd");

using (PsdImage im = (PsdImage)Image.Load(kaynakDosya))
{
    // Gradient harita ayar katmanı ekle.
    GradientMapLayer katman = im.AddGradientMapAdjustmentLayer();
    katman.GradientSettings.Reverse = true;

    im.Save(çıktıDosyası);
}

// Kaydedilen değişiklikleri kontrol et
using (PsdImage im = (PsdImage)Image.Load(çıktıDosyası))
{
    GradientMapLayer gradientHaritaKatmanı = im.Layers[1] as GradientMapLayer;
    GradientFillSettings gradientAyarları = (GradientFillSettings)gradientHaritaKatmanı.GradientSettings;

    AssertAreEqual(0.0, gradientAyarları.Angle);
    AssertAreEqual((short)4096, gradientAyarları.Interpolation);
    AssertAreEqual(true, gradientAyarları.Reverse);
    AssertAreEqual(false, gradientAyarları.AlignWithLayer);
    AssertAreEqual(false, gradientAyarları.Dither);
    AssertAreEqual(GradientType.Linear, gradientAyarları.GradientType);
    AssertAreEqual(100, gradientAyarları.Scale);
    AssertAreEqual(0.0, gradientAyarları.HorizontalOffset);
    AssertAreEqual(0.0, gradientAyarları.VerticalOffset);
    AssertAreEqual("Özel", gradientAyarları.GradientName);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1670. [AI Format] XPacket Metadata desteği ekleme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "ai_one.ai");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Nesneler eşit değil.");
    }
}

void AssertIsNotNull(object testNesnesi)
{
    if (testNesnesi == null)
    {
        throw new Exception("Test nesneleri null.");
    }
}

string creatorToolAnahtarı = ":CreatorTool";
string nPagesAnahtarı = "xmpTPg:NPages";
string unitAnahtarı = "stDim:unit";
string heightAnahtarı = "stDim:h";
string widthAnahtarı = "stDim:w";

string beklenenCreatorTool = "Adobe Illustrator CC 22.1 (Windows)";
string beklenenNPages = "1";
string beklenenUnit = "Piksel";
double beklenenHeight = 768;
double beklenenWidth = 1366;

using (AiImage resim = (AiImage)Aspose.PSD.Image.Load(kaynakDosya))
{
    // Xmp Metadata eklendi.
    var xmpMetaData = resim.XmpData;

    AssertIsNotNull(xmpMetaData);

    // Şimdi AI dosyalarının Xmp Paketlerine erişebiliriz.
    var temelPaket = xmpMetaData.GetPackage(Namespaces.XmpBasic) as XmpBasicPackage;
    var paket = xmpMetaData.Packages[4];

    // Ve bu paketlerin içeriğine erişimimiz var.
    var creatorTool = temelPaket[creatorToolAnahtarı].ToString();
    var nPages = paket[nPagesAnahtarı];
    var unit = paket[unitAnahtarı];
    var height = double.Parse(paket[heightAnahtarı].ToString(), CultureInfo.InvariantCulture);
    var width = double.Parse(paket[widthAnahtarı].ToString(), CultureInfo.InvariantCulture);

    AssertAreEqual(creatorTool, beklenenCreatorTool);
    AssertAreEqual(nPages, beklenenNPages);
    AssertAreEqual(unit, beklenenUnit);
    AssertAreEqual(height, beklenenHeight);
    AssertAreEqual(width, beklenenWidth);
}
{{< /highlight >}}

**PSDNET-1831. Şişirme, Sıkıştırma ve Burulma türlerini uygulayın**

{{< highlight csharp >}}
string[] dosyalar = { "Twist", "Squeeze", "Squeeze_vert", "Inflate" };

foreach (string önEk in dosyalar)
{
    string kaynakDosya = Path.Combine(baseFolder, önEk + ".psd");
    string çıktıDosyası = Path.Combine(outputFolder, önEk + "_export.png");

    using (var psdImage = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
    {
        psdImage.Save(çıktıDosyası, new PngOptions
        {
            ColorType = PngColorType.TruecolorWithAlpha
        });
    }
}
{{< /highlight >}}

**PSDNET-1653. Rgb ve Lab modları, Sanat Tabakası Katmanları içeren dosyalarda 3 kanaldan az ve 4 kanaldan fazla içerebilir**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "Rgb5Channels.psb");
string çıktıDosyası = Path.Combine(outputFolder, "Rgb5Channels_output.psd");

using (PsdImage image = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya))
{
    // Burada istisna olmamalı
    image.Save(çıktıDosyası);
}
{{< /highlight >}}

**PSDNET-1775. İşleme alanı üstü pozitif olmalı. Belirli dosyanın işlenmesinde ('areaToProcess' parametresi)**

{{< highlight csharp >}}
string kaynakDosya = @"BANNERS_2_Intel-Gamer_psak.psd";
string çıktıDosyası = @"BANNERS_2_Intel-Gamer_psak_out.psd";
PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.LoadEffectsResource = true;
psdLoadOptions.AllowWarpRepaint = true;
using (PsdImage image = (PsdImage)PsdImage.Load(kaynakDosya, psdLoadOptions))
{
    image.Save(çıktıDosyası);
    // İstisna olmamalı
}
{{< /highlight >}}

**PSDNET-2052. Genişletilmiş kanvas resmi kaydedildikten sonra kırpılır. Veri kaybolur ancak Önizleme doğru görünüyor**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "bigfile.psd");

string çıktıDosyası = Path.Combine(outputFolder, "bigfile_output.psd");
string çıktıResim = Path.Combine(outputFolder, "bigfile.png");

PsdLoadOptions loadOptions = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, loadOptions))
{
    // Burada hata olmamalı
    psdImage.Save(çıktıDosyası, new PsdOptions { CompressionMethod = CompressionMethod.RLE });
}

using (var psdImage = (PsdImage)Image.Load(çıktıDosyası, loadOptions))
{
    psdImage.Resize(psdImage.Width / 10, psdImage.Height / 10);

    // Burada hata olmamalı
    psdImage.Save(çıktıResim, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
