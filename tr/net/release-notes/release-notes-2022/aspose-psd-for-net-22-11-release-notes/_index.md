---
title: Aspose.PSD için .NET 22.11 - Sürüm Notları
type: docs
weight: 20
url: /tr/net/aspose-psd-icin-net-22-11-sürüm-notları/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

{{% alert color="warning" %}}

- Bu sürümde 16 bitlik dışa aktarmalarda bir gerileme var, bu nedenle bu özelliği kullanırken dikkatli olmanızı öneririz.
Lütfen 16 bitlik görüntü işleme temel işleviniz ise Aspose.PSD'yi 22.9-22.11 sürümlerine güncellemeyin.

Bu sorunlara çözüm üzerinde çalışıyoruz.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1320|Son derece büyük PSB dosyaları dışa aktarılamaz|Geliştirme|
|PSDNET-659|Dairesel gradyanın merkezini taşınabilir hale getirin|Özellik|
|PSDNET-1330|Belirli dosyalar için ZipWithoutPrediction sıkıştırma yöntemi desteklenmiyor|Özellik|
|PSDNET-735|Yalnızca bir katman için bir dönüşüm yöntemi kullandıktan sonra kaydedilen katmanın yanlış sınırlama kutusu var|Hata|
|PSDNET-1234|Desen içeren PSD görüntüsünü yüklerken istisna oluştu|Hata|
|PSDNET-1244|Çince semboller içeren PSD dosyasının kaydedilmesi sırasında Görüntü dışa aktarma hatası (IndexOutOfRangeException)|Hata|
|PSDNET-1303|Zaman Çizelgesi Etkin Çerçevesi yanlış uygulanıyor|Hata|
|PSDNET-1307|22.7'de Regression: Arap karakterleri içeren metnin yanlış oluşturulması|Hata|
|PSDNET-1321|Grup Katmanı üzerindeki Vektör Maskesi yanlış çalışıyor. Nihai görüntü siyah delik barındırıyor olmalı ama içermemeli|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-659. Dairesel gradyanın merkezini taşınabilir hale getirin**

{{< highlight csharp >}}
string kaynakDosya = "psdnet659.psd";
string çıktıDosyası = "çıktı.png";

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosya))
{
    DolguKatmanı daireselKatman = (DolguKatmanı)psdGörüntü.Layers[5];
    GradientDoldurmaAyarları ayarlar = (GradientDoldurmaAyarları)daireselKatman.FillSettings;

    // Ofset noktasını güncelle
    ayarlar.HorizontalOffset = 10;
    ayarlar.VerticalOffset = -25;

    psdGörüntü.Save(çıktıDosyası, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Yalnızca bir katman için bir dönüşüm yöntemi kullandıktan sonra kaydedilen katmanın yanlış sınırlama kutusu var**

{{< highlight csharp >}}
string kaynakDosyaAdı = @"TextLayer.psd";
string çıktıDosyası = "TextLayerResized_output.psd";

using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdı, new PsdLoadOptions()))
{
    TextLayer metinKatmanı = (TextLayer)görüntü.Layers[1];

    // Metin katmanının yeni boyutunu ayarlar
    const int YeniGenişlik = 250;
    const int YeniYükseklik = 250;

    // Yeniden boyutlandırma işleminin katmanı nasıl yeniden boyutlandıracağı mekanizmasını ayarlar (varsayılan değer)
    ResizeType yenidenBoyutlandırmaTipi = ResizeType.NearestNeighbourResample;

    // Burada metin katmanının yeniden boyutlandırılması için yeni mekanizma kullanılıyor
    // Sadece katman değil, aynı zamanda metin katmanının dönüşüm matrisi de değişecek
    metinKatmanı.Resize(YeniGenişlik, YeniYükseklik, yenidenBoyutlandırmaTipi);

    görüntü.Save(çıktıDosyası, new PsdOptions(görüntü));
}

using (PsdImage görüntü = (PsdImage)Image.Load(çıktıDosyası, new PsdLoadOptions()))
{
    TextLayer txtKatman = (TextLayer)görüntü.Layers[1];

    // Delta nedeni farklı varsayılan yazı tipidir
    if (txtKatman.TransformMatrix[4] >= 65 
        && txtKatman.TransformMatrix[4] <= 67
        && txtKatman.TransformMatrix[5] >= 234
        && txtKatman.TransformMatrix[5] <= 237)
    {
        // Her şey yolunda
    }
    else
    {
        throw new Exception("Konum noktası yanlış");
    }
}
{{< /highlight >}}

**PSDNET-1234. Desen içeren PSD görüntüsünü yüklerken istisna oluştu**

{{< highlight csharp >}}
string srcDosya = "test.psd";
string çıktı = "çıktı1234.png";

using (PsdImage psdGörüntü = (PsdImage)PsdImage.Load(srcDosya,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngSeçenekler = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdGörüntü.Save(çıktı, pngSeçenekler);
}
{{< /highlight >}}

**PSDNET-1244. Çince semboller içeren PSD dosyasının kaydedilmesi sırasında Görüntü dışa aktarma hatası (IndexOutOfRangeException)**

{{< highlight csharp >}}
string kaynakDosya = "input.psd";
string çıktıYolu = "output.psd";

var yüklemeSeçenekleri = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, yüklemeSeçenekleri))
{
    foreach (var katman in görüntü.Layers)
    {
        if (katman.Name == "1")
        {
            var txtKatman = (TextLayer)katman;

            txtKatman.UpdateText("测试测试");
        }
    }

    // Burada hiçbir istisna olmamalı.
    görüntü.Save(çıktıYolu, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. Zaman Çizelgesi Etkin Çerçevesi yanlış uygulanıyor**

{{< highlight csharp >}}
string kaynak = "timeline1303.psd";
string çıktı = "out_timeline.psd";

using (var psdGörüntü = (PsdImage)Image.Load(kaynak))
{
    TimeLine zamanÇizelgesi = TimeLine.InitializeFrom(psdGörüntü);

    zamanÇizelgesi.ActiveFrame = 2;
    zamanÇizelgesi.ApplyTo(psdGörüntü);

    psdGörüntü.Save(çıktı);
}
{{< /highlight >}}

**PSDNET-1307. 22.7'de Regression: Arap karakterleri içeren metnin yanlış oluşturulması**

{{< highlight csharp >}}
string testFontlarKlasörü = "Yazı Tipleri";
FontSettings.SetFontsFolder(testFontlarKlasörü);
FontSettings.UpdateFonts();

string kaynakDosyaYolu = "sarbarg.fin12.psd";
string çıktıDosyaYolu = "sonuç.tiff";

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosyaYolu))
{
    psdGörüntü.Save(çıktıDosyaYolu, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Son derece büyük PSB dosyaları dışa aktarılamaz**

{{< highlight csharp >}}
string kaynakDosya = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdDışaAktarımYolu = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    görüntü.Save(psdDışaAktarımYolu, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Grup Katmanı üzerindeki Vektör Maskesi yanlış çalışıyor. Nihai görüntü siyah delik barındırıyor olmalı ama içermemeli**

{{< highlight csharp >}}
string kaynakDosya = "demo.psd";
string çıktı = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(kaynakDosya))
{
    PngOptions pngSeçenekler = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(çıktı, pngSeçenekler);
}
{{< /highlight >}}

**PSDNET-1330. Belirli dosyalar için ZipWithoutPrediction sıkıştırma yöntemi desteklenmiyor**

{{< highlight csharp >}}
string kaynakDosya = "20221017_220706_0000.psd";
string çıktıDosyası = "20221017_220706_0000.jpg";

using (var görüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase seçeneklerBase = new JpegOptions() { Quality = 80 };
    görüntü.Save(çıktıDosyası, seçeneklerBase);
}
{{< /highlight >}}
