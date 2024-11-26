---
title: Aspose.PSD için .NET 21.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-21-8-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD için .NET 21.8](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-698|ZipWithPrediction Sıkıştırma yöntemlerini destekleme|Özellik|
|PSDNET-663|Oluşturulan PSD'de metin boşluğu yanlış|Hata|
|PSDNET-685|PSD'yi kaydederken istisna|Hata|
|PSDNET-927|Lisanssız kullanım durumunda Aspose.PSD'de satırlar ve semboller arasındaki doğru mesafe|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-663. Oluşturulan PSD'de metin boşluğu yanlış**

{{< highlight csharp >}}
            string kaynakDosyaAdi = "kaynak.psd";
            string ciktiDosyaAdi = "cikti.png";

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdi))
            {
                görüntü.Save(ciktiDosyaAdi, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-685. PSD'yi kaydederken istisna**

{{< highlight csharp >}}
            string kaynakDosyaAdi = "Dosya.psd";
            string ciktiDosyaAdi = "Dosya2.psd";

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdi))
            {
                var katman1 = (TextLayer)görüntü.Layers[1];
                katman1.TextData.UpdateLayerData();

                görüntü.Save(ciktiDosyaAdi);
            }
{{< /highlight >}}

**PSDNET-698. ZipWithPrediction Sıkıştırma yöntemlerini destekleme**

{{< highlight csharp >}}
            string girişDosyaYolu = "zipTest698.psd";

            string ciktiPng = "cikti.png";
            string ciktiHam = "cikti_Ham.psd";
            string ciktiZip = "cikti_Zip.psd";

            using (Image görüntü = Image.Load(girişDosyaYolu))
            {
                görüntü.Save(ciktiPng, new PngOptions());

                görüntü.Save(ciktiHam, new PsdOptions() { CompressionMethod = CompressionMethod.Raw });
                görüntü.Save(ciktiZip, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction });
            }
{{< /highlight >}}

**PSDNET-927. Lisanssız kullanım durumunda Aspose.PSD'de satırlar ve semboller arasındaki doğru mesafe**

{{< highlight csharp >}}
            bool[] lisansDurumları = new bool[] { false, true };
            for (int i = 0; i < lisansDurumları.Length; i++)
            {
                bool testLisansı = lisansDurumları[i];
                if (testLisansı)
                {
                    License lisans = new License();
                    lisans.SetLicense("Conholdate.Total.Product.Family.lic");
                }

                string kaynakDosya = "psdnetTest927.psd";
                string çıktıDosya = "çıktı_" + testLisansı.ToString() + "_psdnetTest927.png";

                using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
                {
                    görüntü.Save(çıktıDosya, new PngOptions());
                }
            }
{{< /highlight >}}
