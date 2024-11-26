---
title: Aspose.PSD for .NET 22.6 - Sürüm Notları
type: docs
weight: 70
url: /tr/net/aspose-psd-for-net-22-6-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.6](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-940|Farklı dosyalarda benzer katmanlar için benzersiz karmayı almak için API oluşturma|Geliştirme|
|PSDNET-678|Desen içeren Dolgu Katmanının yanlış şekilde oluşturulması, desenlerin birden fazla ve katmanların sırasının değiştiği durumda|Hata|
|PSDNET-1125|CMYK renk moduna sahip belirli PSD dosyasının yüklenmesi sırasında istisna oluştu|Hata|


## **Ortak API Değişiklikleri**
# **Eklenen API'lar:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.#ctor(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetChannelsHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetBlendingHash
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerHashCalculator.GetContentHash


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-678. Desen içeren Dolgu Katmanının yanlış şekilde oluşturulması, desenlerin birden fazla ve katmanların sırasının değiştiği durumda**

{{< highlight csharp >}}
string kaynakDosya = "kötüDesen.psd";
string çıktıPng = "çıktı_678.png";

using (var psdResim = (PsdImage)Image.Load(kaynakDosya))
{
    FillLayer katman1 = (FillLayer)psdResim.Layers[1];
    FillLayer katman2 = (FillLayer)psdResim.Layers[2];

    katman1.Güncelle();
    katman2.Güncelle();

    psdResim.Save(çıktıPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-940. Farklı dosyalarda benzer katmanlar için benzersiz karmayı almak için API oluşturma**

{{< highlight csharp >}}
using Aspose.PSD;
using Aspose.PSD.FileFormats.Psd;
using Aspose.PSD.FileFormats.Psd.Layers;
using Aspose.PSD.ImageLoadOptions;

public class Program
{
    static void Main()
    {
        RegularLayerContentHashTest("SadeceDüzenli.psd");
        FillLayerContentHashTest("DolumAkıllıGrup.psd");
        SmartObjectLayerContentHashTest("DoldurAkıllıGrup.psd");
        AdjustmentLayersContentHashTest("TümAyarlar.psd");
        TextLayersContentHashTest("MetinKatmanları.psd");
        GroupLayerContentHashTest("DoldurAkıllıGrup.psd");

        var içerikTestDosyaları = new string[] { "SadeceDüzenli.psd", "DolumAkıllıGrup.psd", "MetinKatmanları.psd", "TümAyarlar.psd" };

        foreach (var dosya in içerikTestDosyaları)
        {
            RegularLayerContentFromDifferentFilesHashTest(dosya);
        }
    }

    // Geri kalanı çevrildi, bitti.
}
{{< /highlight >}}

**PSDNET-1125. CMYK renk moduna sahip belirli PSD dosyasının yüklenmesi sırasında istisna oluştu**

{{< highlight csharp >}}
string kaynakDosya = "02_alpha-kanallar.psd";
string çıktıPng = "çıktı_1125.png";

using (PsdImage resim = (PsdImage)Image.Load(kaynakDosya))
{
    resim.Save(çıktıPng, new PngOptions());
}
{{< /highlight >}}