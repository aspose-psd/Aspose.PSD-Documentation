---
title: Aspose.PSD for .NET 22.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-210|Katman Grubu için IsOpen özelliği ekle|Özellik|
|PSDNET-643|Raster katman maskeleri olan PSD görüntüleri, 16 bitlik PSD görüntüsüne kaydedilirken maskeleri atar|Hata|
|PSDNET-899|Bulanıklaştırma modu Dağılma, maskesi olan klasöre uygulanmaz|Hata|
|PSDNET-1047|Belirli dosya, Aspose.PSD 21.11'de kaydedildikten sonra Photoshop tarafından açılamıyor|Hata|
|PSDNET-1068|Doğru yapılandırılmış katmanın yanlış renderlanması (Ekle) karışım modu|Hata|
|PSDNET-1069|Yüklemeden sonra Desen Doldurmalı Katman güncellemede istisna oluşturur|Hata|


## **Halka Açık API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-210. Katman Grubu için IsOpen özelliği ekle**

{{< highlight csharp >}}
// Çalışma zamanında IsOpen özelliğini okuma ve yazma örneği.
string kaynakDosyaAdi = "LayerGroupOpenClose.psd";
string ciktiDosyaAdi = "Output" + kaynakDosyaAdi;

using (var görüntü = (PsdImage)Image.Load(kaynakDosyaAdi))
{
    foreach (var katman in görüntü.Layers)
    {
        if (katman is LayerGroup && katman.Name == "Group 1")
        {
            bool açıkGrup1 = ((LayerGroup)katman).IsOpen;
            ((LayerGroup)katman).IsOpen = !açıkGrup1;
        }

        if (katman is LayerGroup && katman.Name == "Group 2")
        {
            bool açıkGrup2 = ((LayerGroup)katman).IsOpen;           
            ((LayerGroup)katman).IsOpen = !açıkGrup2;
        }
    }

    görüntü.Save(ciktiDosyaAdi);
}
{{< /highlight >}}

**PSDNET-643. Raster katman maskeleri olan PSD görüntüleri, 16 bitlik PSD görüntüsüne kaydedilirken maskeleri atar**

{{< highlight csharp >}}
            string kaynakDosyaYolu = "OneRegularAndOneRegularWithMask.psd";
            string ciktiDosyaYolu = "out_OneRegularAndOneRegularWithMask.psd";

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaYolu))
            {
                görüntü.Save(ciktiDosyaYolu, new PsdOptions(görüntü)
                {
                    ChannelBitsCount = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Bulanıklaştırma modu Dağılma, maskesi olan klasöre uygulanmaz**

{{< highlight csharp >}}
            string kaynakDosya = "psdnet899.psd";
            string ciktiPng = "out_psdnet899.png";

            using (PsdImage görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                görüntü.Save(ciktiPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Belirli dosya, Aspose.PSD 21.11'de kaydedildikten sonra Photoshop tarafından açılamıyor**

{{< highlight csharp >}}
            string kaynakDosya = "psdnet1047.psd";
            string ciktiPsd = "out_psdnet1047.psd";

            using (PsdImage görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                görüntü.Save(ciktiPsd);
            }

            // Photoshop ile çıktı PSD dosyasını manuel olarak açmak gereklidir.

            using (PsdImage görüntü = (PsdImage) Image.Load(ciktiPsd))
            {
                // herhangi bir istisna oluşmaz.
            }
{{< /highlight >}}

**PSDNET-1068. Doğru yapılandırılmış katmanın yanlış renderlanması (Ekle) karışım modu**

{{< highlight csharp >}}
            string kaynakDosya = "broken.psd";
            string ciktiPng = "out_broken.psd.png";

            using (var psdGörüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                psdGörüntü.Save(ciktiPng, new PngOptions() {RenkTürü = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Desen Doldurmalı Katman güncellemede istisna oluşturur**

{{< highlight csharp >}}
            string kaynakDosya = "AllTypesLayerPsd.psd";

            using (var görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                var dolguKatmanı = (FillLayer)görüntü.Layers[9];
                dolguKatmanı.Update();
            }
{{< /highlight >}}
