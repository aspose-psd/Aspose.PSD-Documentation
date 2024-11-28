---
title: Aspose.PSD için .NET 22.12 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-icin-net-22-12-s%C3%BCr%C3%BCm-notlar%C4%B1/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

{{% alert color="success" %}}

- Bu sürümde 16 bitlik ihraçta yaşanan bir regresyon düzeltildi.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1336|İText arabirimine düzenlenebilir TextOrientation özelliğini ekle|Özellik|
|PSDNET-725|Belirtilen PSD dosyasının bir katman maskesi ile boyutlandırılması yanlış maskeler üretir|Hata|
|PSDNET-1277|16 resim için bir maskeyi kaydetme ve yükleme yeteneği ekle|Hata|
|PSDNET-1281|16 bitlik bir görüntüyü 16 veya 8 bitlik bir görüntüye kaydederken yanlış şeffaflık|Hata|
|PSDNET-1375|16 bit renkteki CMYK'yi düzelt|Hata|


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım Örnekleri:**

**PSDNET-725. Belirtilen PSD dosyasının bir katman maskesi ile boyutlandırılması yanlış maskeler üretir**

{{< highlight csharp >}}
string kaynakDosya = "kaynak.psd";
string psdDışaAktarılmaYolu = "çıktı.psd";
string pngDışaAktarılmaYolu = "çıktı.png";

// Kaynak PSD dosyasını açar
using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    const int Ölçek = 4;

    int yeniGenişlik = görüntü.Width * Ölçek;
    int yeniYükseklik = görüntü.Height * Ölçek;

    // Yeniden boyutlandırma yapar
    görüntü.Resize(yeniGenişlik, yeniYükseklik);
    görüntü.Save(psdDışaAktarılmaYolu, new PsdOptions(görüntü));
}

// Yeniden boyutlandırılan PSD dosyasını açar
using (PsdImage görüntü = (PsdImage)Image.Load(psdDışaAktarılmaYolu))
{
    // PNG'ye dönüştürülür
    görüntü.Save(pngDışaAktarılmaYolu, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. 16 resim için bir maskeyi kaydetme ve yükleme yeteneği ekle**

{{< highlight csharp >}}
string 8bitPsdDosyası = @"giriş_8bitRenk.psd";
string 16bitPsdÇıktıDosyası = @"çıktı_16bitRenk.psd";

using (var görüntü = (PsdImage)Image.Load(8bitPsdDosyası))
{
    // Seçenekler 16 bit renkli kaydetmeyi sağlar
    PsdOptions seçenekler16 = new PsdOptions { KanalBitSayısı = 16, RenkModu = ColorModes.Rgb};

    // PSD dosyası şeffaflıkla kaydedilecektir
    görüntü.Save(16bitPsdÇıktıDosyası, seçenekler16);
}
{{< /highlight >}}

**PSDNET-1281. 16 bitlik bir görüntüyü 16 veya 8 bitlik bir görüntüye kaydederken yanlış şeffaflık**

{{< highlight csharp >}}
string kaynakDosya = @"Örnek_16bit.psd";
string tekrarKaydedilmişDosya = @"YenidenKaydet_16bit.psd";
string görüntüDosyası = @"ToplamGörüntü_16bit.png";

// 16 bitlik renkli psd dosyası (şeffaflıkla) açılacak ve 16 bit renge kaydedilecektir
using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    PsdOptions seçenekler16 = new PsdOptions() { KanalBitSayısı = 16, RenkModu = ColorModes.Rgb };
    görüntü.Save(tekrarKaydedilmişDosya, seçenekler16);
}

// 16 bitlik renkli psd dosyası kaydedilip şeffaflıkla png dosyasına dönüştürülecektir
using (var görüntü = (PsdImage)Image.Load(tekrarKaydedilmişDosya))
{
    görüntü.Save(görüntüDosyası, new PngOptions() { RenkTipi = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. IText arabirimine düzenlenebilir TextOrientation özelliğini ekle**

{{< highlight csharp >}}
// Aşağıdaki kod, yeni TextOrientation özelliğini düzeltebilme yeteneğini göstermektedir.
// Bu, şu anda işlemi etkilemez, sadece özellik değerini düzenlemenize olanak tanır.

string kaynak = "1336test.psd";
string çıktı = "çık_1336test.psd";

using (var görüntü = (PsdImage)Image.Load(kaynak))
{
    var metinKatmanı = görüntü.Layers[1] as TextLayer;
    if (metinKatmanı.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Doğru okuma
    }
    else
    {
        throw new Exception("TextOrientation özelliği değerinin yanlış okunması");
    }

    metinKatmanı.TextData.TextOrientation = TextOrientation.Horizontal;
    metinKatmanı.TextData.UpdateLayerData();

    görüntü.Save(çıktı);
}

using (var görüntü = (PsdImage)Image.Load(çıktı))
{
    var metinKatmanı = görüntü.Layers[1] as TextLayer;
    if (metinKatmanı.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Doğru okuma
    }
    else
    {
        throw new Exception("TextOrientation özelliği değerinin yanlış okunması");
    }
}
{{< /highlight >}}

**PSDNET-1375. 16 bit renkli CMYK'yi düzelt**

{{< highlight csharp >}}
string kaynakDosya = @"ClippingMaskRegular.psd";
string dışaAktarılmaYolu = @"çıktı.psd";
string pngDışaAktarılmaYolu = @"çıktı.png";

// Dönüştürme seçeneklerini ayarlar
PsdOptions psdSeçenekleri = new PsdOptions()
{
    RenkModu = ColorModes.Cmyk,
    KanalBitSayısı = 16,
    KanalSayısı = 5,
    SıkıştırmaYöntemi = CompressionMethod.Raw
};

// Dönüştürür ve kaydeder
using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    görüntü.Convert(psdSeçenekleri);
    görüntü.Save(dışaAktarılmaYolu);
}

// Dönüştürülen dosyayı açar ve PNG'ye dönüştürür
using (PsdImage görüntü = (PsdImage)Image.Load(dışaAktarılmaYolu))
{
    görüntü.Save(pngDışaAktarılmaYolu, new PngOptions() { RenkTipi = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
