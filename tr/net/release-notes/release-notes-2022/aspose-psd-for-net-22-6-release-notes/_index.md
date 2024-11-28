---
title: Aspose.PSD for .NET 22.6 - Sürüm Notları
type: docs
weight: 70
url: /tr/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-940|Farklı dosyalardaki benzer katmanlar için benzersiz karmayı almak için API oluşturma|Geliştirme|
|PSDNET-678|Desenle Doldurma Katmanının yanlış renderlanması, desenler birden fazla olduğunda ve katmanların sırası değiştiğinde|Hata|
|PSDNET-1125|Belirli CMYK renk modunda PSD dosyasının yüklenmesinde istisna|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Kaldırılan API'ler:**
- Hiçbiri


## **Kullanım Örnekleri:**

**PSDNET-678. Desenle Doldurma Katmanının yanlış renderlanması, desenler birden fazla olduğunda ve katmanların sırası değiştiğinde**

{{< highlight csharp >}}
string kaynakDosya = "badPattern.psd";
string ciktiPng = "out_678.png";

using (var psdResim = (PsdResim)Resim.Yükle(kaynakDosya))
{
    DoldurmaKatmanı katman1 = (DoldurmaKatmanı)psdResim.Katmanlar[1];
    DoldurmaKatmanı katman2 = (DoldurmaKatmanı)psdResim.Katmanlar[2];

    katman1.Güncelle();
    katman2.Güncelle();

    psdResim.Kaydet(ciktiPng, new PngSeçenekleri());
}
{{< /highlight >}}

**PSDNET-940. Farklı dosyalardaki benzer katmanlar için benzersiz karmayı almak için API oluşturma**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.GörüntüYüklemeSeçenekleri;

public class Program
{
    static void Main()
    {
        RegularKatmanİçerikKarmaTest("OnlyRegular.psd");
        FillKatmanİçerikKarmaTest("FillSmartGroup.psd");
        SmartObjectKatmanİçerikKarmaTest("FillSmartGroup.psd");
        AdjustmentKatmanlarıİçerikKarmaTest("AllAdjustments.psd");
        TextKatmanlarıİçerikKarmaTest("TextLayers.psd");
        GroupKatmanİçerikKarmaTest("FillSmartGroup.psd");

        var içerikTestDosyaları = new string[] { "OnlyRegular.psd", "FillSmartGroup.psd", "TextLayers.psd", "AllAdjustments.psd" };

        foreach (var dosya in içerikTestDosyaları)
        {
            RegularKatmanİçerikFarklıDosyalardanKarmaTest(dosya);
        }
    }

    // Diğer yöntemler
}
{{< /highlight >}}

**PSDNET-1125. Belirli CMYK renk modundaki PSD dosyasının yüklenmesinde istisna**

{{< highlight csharp >}}
string kaynakDosya = "02_alpha-channels.psd";
string ciktiPng = "out_1125.png";

using (PsdResim resim = (PsdResim)Resim.Yükle(kaynakDosya))
{
    resim.Kaydet(ciktiPng, new PngSeçenekleri());
}
{{< /highlight >}}