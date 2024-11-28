---
title: Aspose.PSD for .NET 22.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-22-3-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-210|Katman Grubu için IsOpen özelliği eklendi|Özellik|
|PSDNET-643|Rastgele katman maskeleri olan PSD görüntüsü, 16 bitlik PSD görüntüsüne kaydedilirken maskeleri atar|Hata|
|PSDNET-899|Bulanıklık modu Dissolve, maskeli klasöre uygulanmaz|Hata|
|PSDNET-1047|Belirli bir dosya, Aspose.PSD 21.11'de kaydedildikten sonra Photoshop tarafından açılamaz|Hata|
|PSDNET-1068|Linear Dodge (Ekle) karışım moduna sahip katmanın yanlış şekilde işlenmesi|Hata|
|PSDNET-1069|Yüklemeden sonra Desen Doldurma Katmanı güncelleme sırasında istisna fırlatır|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.IsOpen


# **Kaldırılan API'ler:**
- Yok


## **Kullanım örnekleri:**

**PSDNET-210. Katman Grubu için IsOpen özelliği ekleme**

{{< highlight csharp >}}
// Çalışma zamanında IsOpen özelliğini okuma ve yazma örneği.
string kaynakDosyaAdı = "LayerGroupOpenClose.psd";
string çıktıDosyaAdı = "Çıkış" + kaynakDosyaAdı;

using (var görüntü = (PsdImage)Image.Load(kaynakDosyaAdı))
{
    foreach (var katman in görüntü.Layers)
    {
        if (katman is LayerGroup && katman.Name == "Grup 1")
        {
            bool açıkGrup1 = ((LayerGroup)katman).IsOpen;
            ((LayerGroup)katman).IsOpen = !açıkGrup1;
        }

        if (katman is LayerGroup && katman.Name == "Grup 2")
        {
            bool açıkGrup2 = ((LayerGroup)katman).IsOpen;           
            ((LayerGroup)katman).IsOpen = !açıkGrup2;
        }
    }

    görüntü.Save(çıktıDosyaAdı);
}
{{< /highlight >}}

**PSDNET-643. Rastgele katman maskeleri olan PSD görüntüsü, 16 bitlik PSD görüntüsüne kaydedilirken maskeleri atar**

{{< highlight csharp >}}
            string kaynakDosyaYolu = "BirDüzenliVeBirDüzenliMaskeli.psd";
            string çıktıDosyaYolu = "çıktı_BirDüzenliVeBirDüzenliMaskeli.psd";

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaYolu))
            {
                görüntü.Save(çıktıDosyaYolu, new PsdOptions(görüntü)
                {
                    KanalBitSayısı = 16
                });
            }
{{< /highlight >}}

**PSDNET-899. Bulanıklık modu Dissolve, maskeli klasöre uygulanmaz**

{{< highlight csharp >}}
            string kaynakDosya = "psdnet899.psd";
            string çıktıPng = "çıktı_psdnet899.png";

            using (PsdImage görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                görüntü.Save(çıktıPng, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-1047. Aspose.PSD 21.11'de kaydedildikten sonra belirli bir dosya Photoshop tarafından açılamaz**

{{< highlight csharp >}}
            string kaynakDosya = "psdnet1047.psd";
            string çıktıPsd = "çıktı_psdnet1047.psd";

            using (PsdImage görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                görüntü.Save(çıktıPsd);
            }

            // Photoshop tarafından çıktı PSD dosyasının manuel olarak açılması gerekir.

            using (PsdImage görüntü = (PsdImage) Image.Load(çıktıPsd))
            {
                // hiçbir istisna fırlatılmaz.
            }
{{< /highlight >}}

**PSDNET-1068. Linear Dodge (Ekle) karışım moduna sahip katmanın yanlış şekilde işlenmesi**

{{< highlight csharp >}}
            string kaynakDosya = "bozuk.psd";
            string çıktıPng = "çıktı_bozuk.psd.png";

            using (var psdGörüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                psdGörüntü.Save(çıktıPng, new PngOptions() {RenkTürü = PngColorType.Truecolor});
            }
{{< /highlight >}}

**PSDNET-1069. Yüklemeden sonra Desen Doldurma Katmanı güncelleme sırasında istisna fırlatır**

{{< highlight csharp >}}
            string kaynakDosya = "TümTiplerLayerPsd.psd";

            using (var görüntü = (PsdImage) Image.Load(kaynakDosya))
            {
                var doldurmaKatmanı = (FillLayer)görüntü.Layers[9];
                doldurmaKatmanı.Update();
            }
{{< /highlight >}}
