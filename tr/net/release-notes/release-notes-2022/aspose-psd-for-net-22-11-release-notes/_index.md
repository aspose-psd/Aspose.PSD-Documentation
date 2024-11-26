---
title: Aspose.PSD for .NET 22.11 - Sürüm Notları
type: docs
weight: 20
url: /tr/net/aspose-psd-for-net-22-11-s%C3%BCr%C3%BCm-notlar%C4%B1/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}}

{{% alert color="warning" %}}

- Bu sürümde, 16 bit dışa aktarmalarda bir regresyon mevcuttur, bu nedenle bu özelliği kullanırken dikkatli olmanızı öneririz.
Lütfen 16 bit görüntü işleme, ana işlevselliğiniz ise Aspose.PSD’yi 22.9-22.11’e güncelleştirmeyin.

Bu sorunlara çözüm üzerinde çalışıyoruz.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1320|Son derece büyük PSB dosyaları dışa aktarılamaz|Geliştirme|
|PSDNET-659|Yayıcı gradyanın merkezini hareketli yapın|Özellik|
|PSDNET-1330|Belirli dosyalar için ZipWithoutPrediction sıkıştırma yöntemi desteklenmiyor|Özellik|
|PSDNET-735|Bir katman için yalnızca bir dönüşüm yöntemi kullandıktan sonra kaydedilen katmanda yanlış sınırlayıcı kutusu bulunur|Hata|
|PSDNET-1234|Desenli PSD görüntüsü yüklenirken istisna oluşur|Hata|
|PSDNET-1244|Çin sembolleri olan PSD dosyasını kaydederken Görüntü aktarımı başarısız oldu (IndexOutOfRangeException)|Hata|
|PSDNET-1303|TimeLine ActiveFrame yanlış uygulanır|Hata|
|PSDNET-1307|Regresyon 22.7: Arap karakterler içeren metnin yanlış şekilde işlenmesi|Hata|
|PSDNET-1321|Grup Katmanındaki Vektör Maskesi yanlış çalışır. Son görüntü siyah delikle doludur, ancak olmamalıdır|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Kaldırılan API'ler:**
- Yok


## **Kullanım örnekleri:**

**PSDNET-659. Yayıcı gradyanın merkezini hareketli yapın**

{{< highlight csharp >}}
string kaynakDosya = "psdnet659.psd";
string çıktıDosyası = "çıktı.png";

using (var psdGörüntü = (PsdGörüntü)Görüntü.Yükle(kaynakDosya))
{
    DolguKatmanı yayıcıKatman = (DolguKatmanı)psdGörüntü.Katmanlar[5];
    GradyanDolguAyarları ayarlar = (GradyanDolguAyarları)yayıcıKatman.DolguAyarları;

    // Ofset noktasını güncelle
    ayarlar.YatayOfset = 10;
    ayarlar.DikeyOfset = -25;

    psdGörüntü.Kaydet(çıktıDosyası, yeni PngSeçenekleri());
}
{{< /highlight >}}

**PSDNET-735. Bir katman için yalnızca bir dönüşüm yöntemi kullandıktan sonra kaydedilen katmanda yanlış sınırlayıcı kutusu bulunur**

{{< highlight csharp >}}
string kaynakDosyaAdı = @"MetinKatmanı.psd";
string çıktıDosyası = "MetinKatmanıYenidenBoyutlandırılmış_çıktı.psd";

using (PsdGörüntü görüntü = (PsdGörüntü)Görüntü.Yükle(kaynakDosyaAdı, yeni PsdYüklemeSeçenekleri()))
{
    MetinKatmanı metinKatmanı = (MetinKatmanı)görüntü.Katmanlar[1];

    // Metin katmanının yeni boyutunu ayarlar
    const int YeniGenişlik = 250;
    const int YeniYükseklik = 250;

    // Yeniden boyutlandırma işleminin katmanı nasıl yeniden boyutlandıracağını belirleyen mekanizmayı ayarlar (varsayılan değer)
    YenidenBoyutlandırmaTipi yenidenBoyutlandırmaTipi = YenidenBoyutlandırmaTipi.TetikiciKomşulukOrantılaması;

    // Metin katmanı için yeni yeniden boyutlandırma mekanizması burada kullanılır
    // Sadece katman değil, ayrıca metin katmanının dönüşüm matrisi de değişir
    metinKatmanı.YenidenBoyutlandır(YeniGenişlik, YeniYükseklik, yenidenBoyutlandırmaTipi);

    görüntü.Kaydet(çıktıDosyası, yeni PsdSeçenekleri(görüntü));
}

using (PsdGörüntü görüntü = (PsdGörüntü)Görüntü.Yükle(çıktıDosyası, yeni PsdYüklemeSeçenekleri()))
{
    MetinKatmanı txtKatmanı = (MetinKatmanı)görüntü.Katmanlar[1];

    // Farkın nedeni varsayılan fontun farklı olmasıdır
    if (txtKatmanı.DönüşümMatrisi[4] >= 65 
        && txtKatmanı.DönüşümMatrisi[4] <= 67
        && txtKatmanı.DönüşümMatrisi[5] >= 234
        && txtKatmanı.DönüşümMatrisi[5] <= 237)
    {
        // Her şey yolunda
    }
    else
    {
        throw new Exception("Konum noktası yanlış");
    }
}
{{< /highlight >}}

**PSDNET-1234. Desenli PSD görüntüsü yüklenirken istisna oluşur**

{{< highlight csharp >}}
string kaynakDosya = "test.psd";
string çıktı = "çıktı1234.png";

using (PsdGörüntü psdGörüntü = (PsdGörüntü)PsdGörüntü.Yükle(kaynakDosya,
new PsdYüklemeSeçenekleri() { EfektKaynağınıYükle = true }))
{
    PngSeçenekleri pngSeçenekleri = new PngSeçenekleri() { RenkTipi = PngRenkTipi.GerçekRenkAlfa };
    psdGörüntü.Kaydet(çıktı, pngSeçenekleri);
}
{{< /highlight >}}

**PSDNET-1244. Çin sembolleri olan PSD dosyasını kaydederken Görüntü aktarımı başarısız oldu (IndexOutOfRangeException)**

{{< highlight csharp >}}
string kaynakDosyası = "girdi.psd";
string çıktıYolu = "çıktı.psd";

var yüklemeSeçenekleri = new PsdYüklemeSeçenekleri
{
    EfektKaynağınıYükle = true,
    EfektKaynağıİçinDiskKullan = true
};

using (var görüntü = (PsdGörüntü)Görüntü.Yükle(kaynakDosyası, yüklemeSeçenekleri))
{
    foreach (var katman in görüntü.Katmanlar)
    {
        if (katman.Adı == "1")
        {
            var txtKatman = (MetinKatmanı)katman;

            txtKatman.MetniGüncelle("测试测试");
        }
    }

    // Burada istisna olmamalıdır.
    görüntü.Kaydet(çıktıYolu, yeni PsdSeçenekleri() { SıkıştırmaYöntemi = SıkıştırmaYöntemi.RLE, RenkModu = RenkModları.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame yanlış uygulanır**

{{< highlight csharp >}}
string kaynak = "zamançizelgesi1303.psd";
string çıktı = "çıktı_zamançizelgesi.psd";

using (var psdGörüntü = (PsdGörüntü)Görüntü.Yükle(kaynak))
{
    ZamanÇizelgesi zamanÇizelgesi = ZamanÇizelgesi.Başlat(psdGörüntü);

    zamanÇizelgesi.ActiveFrame = 2;
    zamanÇizelgesi.Uygulamak(psdGörüntü);

    psdGörüntü.Kaydet(çıktı);
}
{{< /highlight >}}

**PSDNET-1307. Regresyon 22.7: Arap karakterler içeren metnin yanlış şekilde işlenmesi**

{{< highlight csharp >}}
string testYazıTipleriKlasörü = "YazıTipleri";
YazıTipleri.Ayarlar.YazıTipleriKlasörüBelirle(testYazıTipleriKlasörü);
YazıTipleri.Ayarlar.YazıTipleriniGüncelle();

string kaynakDosyaYolu = "örnekfin12.psd";
string çıktıDosyaYolu = "sonuç.tiff";

using (var psdGörüntü = (PsdGörüntü)Görüntü.Yükle(kaynakDosyaYolu))
{
    psdGörüntü.Kaydet(çıktıDos
