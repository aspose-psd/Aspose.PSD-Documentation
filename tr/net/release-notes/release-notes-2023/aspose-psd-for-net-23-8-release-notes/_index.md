---
title: Aspose.PSD for .NET 23.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                      | **Kategori** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | Yeni bir eğim türü eklendi (Bayrak) | Özellik |
| PSDNET-1621 | Yeni eğim türleri eklendi: yukarı yay, aşağı yay, küre | Özellik |
| PSDNET-1682 | Yeni Metodu Uygula PsdImage.AddPosterizeAdjustmentLayer yeni Posterize katmanı eklemek için | Özellik |
| PSDNET-913  | Sadece açılıp kaydedildiğinde PSD bilgileri kaybedildi | Hata     |
| PSDNET-1352 | Resim yüklenemedi | Hata     |
| PSDNET-1553 | Resim yükleme başarısız oldu: Tip Bilinmeyen Yapıdan Tanımlayıcı Yapı Türüne Dönüştürülemiyor | Hata     |
| PSDNET-1631 | 3. taraf kütüphanede değiştirilen dosya PSD dosyasını bozar ancak Photoshop'ta açılabilir | Hata     |


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **Kaldırılan API'lar:**
- Yok


## **Kullanım örnekleri:**

**PSDNET-913. Sadece açılıp kaydedildiğinde PSD bilgileri kaybolur**

{{< highlight csharp >}}
string kaynak = "Orijinal dosya.psd";
string ciktiPsd = "çıkış_Orijinal dosya.psd";
string ciktiPng = "çıkış_Orijinal dosya.png";

using (var psdImage = (PsdImage)Image.Load(kaynak))
{
    psdImage.Save(ciktiPsd);
    psdImage.Save(ciktiPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1352. Resim yükleme başarısız oldu**

{{< highlight csharp >}}
string kaynakDosya1 = "test_metin.psd";
string kaynakDosya2 = "test_akıllı_nesne.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(kaynakDosya2))
{
}
{{< /highlight >}}

**PSDNET-1553. Resim yükleme başarısız oldu: Bilinmeyen Yapı Türü Tanımlayıcı Yapı Türüne Dönüştürülemiyor**

{{< highlight csharp >}}
using (PsdImage yeniPsd = (PsdImage)new PsdImage(10, 10))
{
    yeniPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memAkımı = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        yeniPsd.Save(memAkımı);

        memAkımı.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memAkımı.Write(new byte[1]);
        memAkımı.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memAkımı))
        {
            // Doğru şekilde yüklenmeli
        }
    }
}
{{< /highlight >}}

**PSDNET-1631. 3. taraf kütüphanede değiştirilen dosya PSD dosyasını bozar ancak Photoshop'ta açılabilir**

{{< highlight csharp >}}
string kaynakDosya = "çıktı.psd";
string çıktıDosyası = "dışa_çıkart.png";

using (PsdImage img = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(çıktıDosyası, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1566. Yeni eğim türü eklendi (Bayrak)**

{{< highlight csharp >}}
string kaynakDosya = "bayrak_eğim.psd";
string çıktıDosyası = "bayrak_dışarı çıkart.png";

using (var psdImage = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(çıktıDosyası, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}

**PSDNET-1621. Yeni eğim türleri eklendi: yukarı yay, aşağı yay, küre**

{{< highlight csharp >}}
string kaynakDosyaYukarı = "yukarı_yay_eğim.psd";
string kaynakDosyaAşağı = "aşağı_yay_eğim.psd";
string kaynakDosyaŞişme =  "şişme_eğim.psd";

string çıktıDosyasıYukarı = "YukarıEğri_dışa_çıkart.png";
string çıktıDosyasıAşağı = "AşağıEğri_dışa_çıkart.png";
string çıktıDosyasıŞişme = "Şişme_dışa_çıkart.png";

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaYukarı, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(çıktıDosyasıYukarı, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaAşağı, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(çıktıDosyasıAşağı, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaŞişme, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(çıktıDosyasıŞişme, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1682. Uygulama yeni methodu PsdImage.AddPosterizeAdjustmentLayer yeni Posterize katmanı eklemek için**

{{< highlight csharp >}}
string kaynakDosya = "zendeya.psd";
string çıktıDosyası = "zendeya.psd.çıktı.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(kaynakDosya))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(çıktıDosyası);
}

// Kaydedilen değişiklikleri kontrol et
using (PsdImage image = (PsdImage)Image.Load(
    çıktıDosyası,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Objeler eşit değil.");
    }
}
{{< /highlight >}}
