---
title: Aspose.PSD for .NET 23.10 - Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-psd-for-net-23-10-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.10](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:-------------------------------------------------|:--------|
| PSDNET-692 | Dikey metin yönünün desteklenmesi | Özellik |
| PSDNET-1402 | Şekil Çizgi İçeriğindeki Stroke ayarlarının vstk kaynağından kullanılması | Özellik |
| PSDNET-1607 | Stroke şekillerinin iç alanının render edilmesi | Özellik |
| PSDNET-1644 | Şekil katmanı değişmemişse yeniden boyama yapılmaması | Özellik |
| PSDNET-1696 | [AI Formatı] PDF tabanlı AI Dosyalarından Başlık Okuma Desteği Eklenmesi | Özellik |
| PSDNET-1560 | Psd Dosya Çözünürlüğünü Ayarlamanın Çeşitli Yolları Çalışmıyor | Hata |
| PSDNET-1728 | FontSettings.SetFontsFolders Çalışmıyor veya Aspose.PSD yanlış yazı tipi kullanıyor | Hata |
| PSDNET-1739 | Düzeltilmiş hali. Şekil katmanı olduğunda PsdImage.Save işleminde Null referans istisnası düzeltildi | Hata |


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.ColorFillSettings.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VstkResource.FillSettings
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.IStrokeSettings.LineAlignment
- P:Aspose.PSD.FileFormats.Psd.Layers.ShapeLayer.Stroke
- M:Aspose.PSD.FileFormats.Psd.PsdImage.SetResolution(System.Double,System.Double)
- T:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Path
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Stroke
- P:Aspose.PSD.FileFormats.Psd.Layers.IShapeLayer.Fill
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineCap
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineJoin
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Enabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Size
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineDashSet
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.Fill
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.StrokeSettings.LineAlignment


# **Kaldırılan API'lar:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.IStrokeSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.StrokeResources.VscgResource.Items


## **Kullanım örnekleri:**

**PSDNET-692. Dikey metin yönü desteği**

{{< highlight csharp >}}
string kaynakDosya = "692_lt1.psd";
string çıktıDosya = "692_output.png";
string yazı tipleriDizini = "692_Fonts";

var fontDizinleri = new List<string>(FontSettings.GetFontsFolders());
fontDizinleri.Add(yazıTipleriDizini);
FontSettings.SetFontsFolders(fontDizinleri.ToArray(), true);

using (PsdImage psdResim = (PsdImage)Image.Load(kaynakDosya))
{
    psdResim.Save(çıktıDosya, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1402. Şekil Çizgi İçeriğindeki vstk kaynağındaki Stroke ayarlarının kullanılması**

{{< highlight csharp >}}
string kaynakDosya = "StrokeShapeTest.psd";
string çıktıDosyaPsd = "StrokeShapeTest.out.psd";
string çıktıDosyaPng = "StrokeShapeTest.out.png";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    Layer katman = resim.Layers[1];
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    ColorFillSettings doldurmaAyarları = (ColorFillSettings)şekilKatmanı.Fill;
    doldurmaAyarları.Color = Color.GreenYellow;
    şekilKatmanı.Update();

    ShapeLayer şekilKatmanı2 = (ShapeLayer)resim.Layers[3];
    GradientFillSettings gradientAyarları = (GradientFillSettings)şekilKatmanı2.Fill;
    gradientAyarları.Dither = true;
    gradientAyarları.Reverse = true;
    gradientAyarları.AlignWithLayer = false;
    gradientAyarları.Angle = 20;
    gradientAyarları.Scale = 50;
    gradientAyarları.ColorPoints[0].Location = 100;
    gradientAyarları.ColorPoints[1].Location = 4000;
    gradientAyarları.TransparencyPoints[0].Location = 200;
    gradientAyarları.TransparencyPoints[1].Location = 3800;
    gradientAyarları.TransparencyPoints[0].Opacity = 90;
    gradientAyarları.TransparencyPoints[1].Opacity = 10;
    şekilKatmanı2.Update();

    ShapeLayer şekilKatmanı3 = (ShapeLayer)resim.Layers[5];
    StrokeSettings strokeAyarları = (StrokeSettings)şekilKatmanı3.Stroke;
    strokeAyarları.Size = 15;
    ColorFillSettings strokeDoldurmaAyarları = (ColorFillSettings)strokeAyarları.Fill;
    strokeDoldurmaAyarları.Color = Color.GreenYellow;
    şekilKatmanı3.Update();

    resim.Save(çıktıDosyaPsd);
    resim.Save(çıktıDosyaPng, new PngOptions());
}

// Değişen verileri kontrol et.
using (PsdImage resim = (PsdImage)Image.Load(çıktıDosyaPsd))
{
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    ColorFillSettings doldurmaAyarları = (ColorFillSettings)şekilKatmanı.Fill;
    AssertAreEqual(Color.GreenYellow, doldurmaAyarları.Color);

    ShapeLayer şekilKatmanı2 = (ShapeLayer)resim.Layers[3];
    GradientFillSettings gradientAyarları = (GradientFillSettings)şekilKatmanı2.Fill;
    AssertAreEqual(true, gradientAyarları.Dither);
    AssertAreEqual(true, gradientAyarları.Reverse);
    AssertAreEqual(false, gradientAyarları.AlignWithLayer);
    AssertAreEqual(20.0, gradientAyarları.Angle);
    AssertAreEqual(50, gradientAyarları.Scale);
    AssertAreEqual(100, gradientAyarları.ColorPoints[0].Location);
    AssertAreEqual(4000, gradientAyarları.ColorPoints[1].Location);
    AssertAreEqual(200, gradientAyarları.TransparencyPoints[0].Location);
    AssertAreEqual(3800, gradientAyarları.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, gradientAyarları.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, gradientAyarları.TransparencyPoints[1].Opacity);

    ShapeLayer şekilKatmanı3 = (ShapeLayer)resim.Layers[5];
    StrokeSettings strokeAyarları = (StrokeSettings)şekilKatmanı3.Stroke;
    ColorFillSettings strokeDoldurmaAyarları = (ColorFillSettings)strokeAyarları.Fill;
    AssertAreEqual(15.0, strokeAyarları.Size);
    AssertAreEqual(Color.GreenYellow, strokeDoldurmaAyarları.Color);
}

void AssertAreEqual(object beklenen, object gerçek, string mesaj = null)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception(mesaj ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1607. Stroke şekillerinin iç alanının render edilmesi**

{{< highlight csharp >}}
string kaynakDosya = "ShapeInternalGradient.psd";
string çıktıDosya = "ShapeInternalGradient.out.psd";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    GradientFillSettings doldurmaAyarları = (GradientFillSettings)şekilKatmanı.Fill;
    doldurmaAyarları.Dither = true;
    doldurmaAyarları.Reverse = true;
    doldurmaAyarları.AlignWithLayer = false;
    doldurmaAyarları.Angle = 20.0;
    doldurmaAyarları.Scale = 50;
    doldurmaAyarları.ColorPoints[0].Location = 100;
    doldurmaAyarları.ColorPoints[1].Location = 4000;
    doldurmaAyarları.TransparencyPoints[0].Location = 200;
    doldurmaAyarları.TransparencyPoints[1].Location = 3800;
    doldurmaAyarları.TransparencyPoints[0].Opacity = 90.0;
    doldurmaAyarları.TransparencyPoints[1].Opacity = 10.0;

    şekilKatmanı.Update();

    resim.Save(çıktıDosya);
}

// Değişen verileri kontrol et.
using (PsdImage resim = (PsdImage)Image.Load(çıktıDosya))
{
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    GradientFillSettings doldurmaAyarları = (GradientFillSettings)şekilKatmanı.Fill;

    AssertAreEqual(true, doldurmaAyarları.Dither);
    AssertAreEqual(true, doldurmaAyarları.Reverse);
    AssertAreEqual(false, doldurmaAyarları.AlignWithLayer);
    AssertAreEqual(20.0, doldurmaAyarları.Angle);
    AssertAreEqual(50, doldurmaAyarları.Scale);
    AssertAreEqual(100, doldurmaAyarları.ColorPoints[0].Location);
    AssertAreEqual(4000, doldurmaAyarları.ColorPoints[1].Location);
    AssertAreEqual(200, doldurmaAyarları.TransparencyPoints[0].Location);
    AssertAreEqual(3800, doldurmaAyarları.TransparencyPoints[1].Location);
    AssertAreEqual(90.0, doldurmaAyarları.TransparencyPoints[0].Opacity);
    AssertAreEqual(10.0, doldurmaAyarları.TransparencyPoints[1].Opacity);
}

void AssertAreEqual(object beklenen, object gerçek, string mesaj = null)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception(mesaj ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1644. Şekil katmanı değişmemişse yeniden boyama yapılmaması**

{{< highlight csharp >}}
string kaynakDosya = "ShapeInternalSolid.psd";
string çıktıDosya = "ShapeInternalSolid.out.psd";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    ColorFillSettings doldurmaAyarları = (ColorFillSettings)şekilKatmanı.Fill;
    doldurmaAyarları.Color = Color.Red;

    // Kaydedilmeden önce Shape katmanını güncelleme.

    resim.Save(çıktıDosya);

    // Kaydedilen dosya render edildiğinde kontrol edilir.
}

// Şekil katmanı verisinin değişmediğini kontrol et.
using (PsdImage resim = (PsdImage)Image.Load(çıktıDosya))
{
    ShapeLayer şekilKatmanı = (ShapeLayer)resim.Layers[1];
    ColorFillSettings doldurmaAyarları = (ColorFillSettings)şekilKatmanı.Fill;

    AssertAreEqual(Color.FromArgb(45, 211, 31), doldurmaAyarları.Color);
}

void AssertAreEqual(object beklenen, object gerçek, string mesaj = null)
{
    if (!object.Equals(beklenen, gerçek))
    {
        throw new Exception(mesaj ?? "Nesneler eşit değil.");
    }
}
{{< /highlight >}}

**PSDNET-1696. [AI Format] PDF tabanlı AI Dosyalarından Başlık Okuma Desteği Ekleme**

{{< highlight csharp >}}
string kaynakDosya = "ai_source.ai";

void AssertIsNotNull(object beklenen)
{
    if (beklenen == null)
    {
        throw new Exception("Nesne null.");
    }
}

using (AiImage resim = (AiImage)Image.Load(kaynakDosya))
{
    AssertIsNotNull(resim);
    AssertIsNotNull(resim.Header);
    AssertIsNotNull(resim.Header.BoundingBox);
}
{{< /highlight >}}

**PSDNET-1560. Psd Dosya Çözünürlüğünü Ayarlamanın Çeşitli Yolları Çalışmıyor**

{{< highlight csharp >}}
string çıktı1 = "1560_1_output.psd";
string çıktı2 = "1560_2_output.psd";
string çıktı3 = "1560_3_output.psd";

using (PsdImage yeniPsd = (PsdImage)new PsdImage(600, 400))
{
    yeniPsd.ImageResources = new ResourceBlock[] { new ResolutionInfoResource() };
    yeniPsd.VerticalResolution = 100;
    yeniPsd.HorizontalResolution = 100;
    yeniPsd.Save(çıktı1);
}

using (PsdImage yeniPsd = (PsdImage)new PsdImage(600, 400))
{
    yeniPsd.SetResolution(200, 200);
    yeniPsd.Save(çıktı2);
}

using (PsdImage yeniPsd = (PsdImage)new PsdImage(600, 400))
{
    PsdOptions psdSeçenekleri = new PsdOptions()
    {
        ResolutionSettings = new ResolutionSetting()
        {
            HorizontalResolution = 300,
            VerticalResolution = 300
        }
    };
    yeniPsd.Save(çıktı3, psdSeçenekleri);
}

using (var psdResim1 = (PsdImage)Image.Load(çıktı1))
{
    var çözünürlükKaynağı = psdResim1.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(çözünürlükKaynağı);
    AreEqual(100, çözünürlükKaynağı.VDpi.Integer);
    AreEqual(100, çözünürlükKaynağı.HDpi.Integer);
}

using (var psdResim2 = (PsdImage)Image.Load(çıktı2))
{
    var çözünürlükKaynağı = psdResim2.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(çözünürlükKaynağı);
    AreEqual(200, çözünürlükKaynağı.VDpi.Integer);
    AreEqual(200, çözünürlükKaynağı.HDpi.Integer);
}

using (var psdResim3 = (PsdImage)Image.Load(çıktı3))
{
    var çözünürlükKaynağı = psdResim3.ImageResources[0] as ResolutionInfoResource;

    IsNotNull(çözünürlükKaynağı);
    AreEqual(300, çözünürlükKaynağı.VDpi.Integer);
    AreEqual(300, çözünürlükKaynağı.HDpi.Integer);
}

void IsNotNull(object obje)
{
    if (obje == null)
