---
title: Aspose.PSD for .NET 24.7 - Sürüm Notları
type: docs
weight: 60
url: /tr/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                        | **Kategori** |
|:------------ |:------------------------------------------------------------------------------------------------- |:-------------|
| PSDNET-1029  | AI belgesi açıldığında "Görüntü yüklenemedi." istisnası                                           | Hata         |
| PSDNET-2022  | Metinlerin çıktı PDF dosyalarında yanlış şekilde oluşturulması                                      | Hata         |
| PSDNET-2061  | Linux üzerinde verilen dosya için Görsel dışa aktarma başarısız oldu hatasını düzelt                | Hata         |
| PSDNET-2080  | Aspose.Drawing kullanılırken yazı tiplerinin yüklenmesini düzelt                                    | Hata         |
| PSDNET-2085  | Büyük boyutlu JPEG kullanılarak akıllı nesne katmanı oluşturulduğunda 'Aritmetik işlem, taşma ile sonuçlandı' hatası | Hata         |
| PSDNET-2100  | AI dosyası JPG dosyasına dönüştürülemez                                                           | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Hiçbiri

# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-1029. AI belgesi açıldığında "Görüntü yüklenemedi." istisnası**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string çıktıDosyası = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage görüntü = (AiImage)Image.Load(kaynakDosya))
{
    görüntü.Save(çıktıDosyası, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Metinlerin çıktı PDF dosyalarında yanlış şekilde oluşturulması**

{{< highlight csharp >}}
string kaynak = Path.Combine(baseFolder, "CVFlor.psd");
string çıktı = Path.Combine(outputFolder, "output.pdf");

using (var psdGörüntü = (PsdImage)Image.Load(kaynak))
{
    PdfOptions kaydetmeSeçenekleri = new PdfOptions();
    kaydetmeSeçenekleri.PdfCoreOptions = new PdfCoreOptions();

    psdGörüntü.Save(çıktı, kaydetmeSeçenekleri);
}
{{< /highlight >}}

**PSDNET-2061. Linux üzerinde verilen dosya için Görsel dışa aktarma başarısız oldu hatasını düzelt**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string çıktıDosyası = Path.Combine(outputFolder, "output.jpg");

using (var psdGörüntü = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var kaydetmeSeçenekleri = new JpegOptions() { Quality = 70 };
    psdGörüntü.Save(çıktıDosyası, kaydetmeSeçenekleri);
}
{{< /highlight >}}

**PSDNET-2080. Aspose.Drawing kullanılırken yazı tiplerinin yüklenmesini düzelt**

{{< highlight csharp >}}
using (var yüklüYazıTipleri = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Güncellemeden önce. Yüklü yazı tiplerinin sayısı: " + yüklüYazıTipleri.Families.Length);
    Console.WriteLine("- Platform: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- 'Arial' için Adobe yazı tipi adını alarak yazı tipi önbelleğini yenileyin: "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Güncellemeden sonra. Yüklü yazı tiplerinin sayısı: " + yüklüYazıTipleri.Families.Length);

    Assert.Greater(yüklüYazıTipleri.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. Büyük boyutlu JPEG kullanılarak akıllı nesne katmanı oluşturulduğunda 'Aritmetik işlem, taşma ile sonuçlandı' hatası**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "source.psd");
string resimJpg = Path.Combine(baseFolder, "test.jpg");

using (var resim = (PsdImage)Image.Load(kaynakDosya, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var akış = new FileStream(resimJpg, FileMode.Open))
    {
        var eklenenKatman = new SmartObjectLayer(akış);
        eklenenKatman.Name = "Test Katmanı";
        resim.AddLayer(eklenenKatman);
    }
}
{{< /highlight >}}

**PSDNET-2100. AI dosyası JPG dosyasına dönüştürülemez**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "aaa.ai");
string çıktıDosyası = Path.Combine(outputFolder, "aaa.png");

using (AiImage görüntü = (AiImage)Image.Load(kaynakDosya))
{
    görüntü.Save(çıktıDosyası, new PngOptions());
}
{{< /highlight >}}
