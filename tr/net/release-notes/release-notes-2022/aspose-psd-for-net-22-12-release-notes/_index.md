---
title: Aspose.PSD .NET 22.12 Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

{{% alert color="success" %}}

- Bu sürümde, 16 bit ihraç ile ilgili bir regresyon düzeltildi.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1336|IText arabirimine düzenlenebilir TextOrientation özelliği ekle|Özellik|
|PSDNET-725|Belirtilen PSD dosyasının bir katman maskesi ile yeniden boyutlandırılması yanlış maskeli çıkarır|Hata|
|PSDNET-1277|16 resim için maske kaydetme ve yükleme yeteneği ekle|Hata|
|PSDNET-1281|16 veya 8 bitlik bir görüntünün kaydedilmesinde yanlış şeffaflık|Hata|
|PSDNET-1375|16 bit renkteki CMYK’yi düzelt|Hata|


## **Halka Açık API Değişiklikleri**
# **Eklenen API'lar:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDNET-725. Belirtilen PSD dosyasının bir katman maskesi ile yeniden boyutlandırılması yanlış maskesi çıkıyor**

{{< highlight csharp >}}
string kaynakDosya = "kaynak.psd";
string psdDışaAktarmaYolu = "çıktı.psd";
string pngDışaAktarmaYolu = "çıktı.png";

// Kaynak PSD dosyasını açar
using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    const int Ölçek = 4;

    int yeniGenişlik = görüntü.Width * Ölçek;
    int yeniYükseklik = görüntü.Height * Ölçek;

    // Yeniden boyutlandırma işlemi yapar
    görüntü.Resize(yeniGenişlik, yeniYükseklik);
    görüntü.Save(psdDışaAktarmaYolu, new PsdOptions(görüntü));
}

// Yeniden boyutlandırılmış PSD dosyasını açar
using (PsdImage görüntü = (PsdImage)Image.Load(psdDışaAktarmaYolu))
{
    // PNG'ye dönüştürür
    görüntü.Save(pngDışaAktarmaYolu, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. 16 resim için maske kaydetme ve yükleme yeteneği ekle**

{{< highlight csharp >}}
string 8bitRenkliPsdDosyası = @"giriş_8bitRenkli.psd";
string 16bitRenkliPsdDosyası = @"çıktı_16bitRenkli.psd";

using (var görüntü = (PsdImage)Image.Load(8bitRenkliPsdDosyası))
{
    // Seçeneklerle 16 bit renkte kaydetmeye olanak tanır
    PsdOptions seçenekler16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // PSD dosyası şeffaflıkla kaydedilecek
    görüntü.Save(16bitRenkliPsdDosyası, seçenekler16);
}
{{< /highlight >}}

**PSDNET-1281. 16 bit görüntüyü 16 veya 8 bit görüntüye kaydederken yanlış şeffaflık**

{{< highlight csharp >}}
string kaynakDosya = @"Örnek_16bit.psd";
string yenidenKaydedilenDosya = @"YenidenKaydet_16bit.psd";
string görüntüDosyası = @"ToplamGörüntü_16bit.png";

// (şeffaflık ile) 16 bit renk psd dosyası 16 bit renge açılacak ve kaydedilecek
using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    PsdOptions seçenekler16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    görüntü.Save(yenidenKaydedilenDosya, seçenekler16);
}

// 16 bit renk psd dosyası kaydedildikten sonra şeffaflık ile png dosyasına dönüştürülür
using (var görüntü = (PsdImage)Image.Load(yenidenKaydedilenDosya))
{
    görüntü.Save(görüntüDosyası, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Düzenlenebilir TextOrientation özelliği IText arabirimine eklendi**

{{< highlight csharp >}}
// Aşağıdaki kod, yeni TextOrientation özelliğini düzenleme yeteneğini gösterir.
// Bu, şu anda render etkilemez, sadece özellik değerini düzenlemenize olanak tanır.

string src = "1336test.psd";
string çıktı = "çıkış_1336test.psd";

using (var görüntü = (PsdImage)Image.Load(src))
{
    TextLayer olarak textKatmanı = image.Layers[1] as TextLayer;
    if (textKatmanı.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Doğru okuma
    }
    else
    {
        throw new Exception("TextOrientation özelliği değerinin yanlış okunması");
    }

    textKatmanı.TextData.TextOrientation = TextOrientation.Horizontal;
    textKatmanı.TextData.UpdateLayerData();

    görüntü.Save(çıktı);
}

using (var görüntü = (PsdImage)Image.Load(çıktı))
{
    TextLayer olarak textKatmanı = image.Layers[1] as TextLayer;
    if (textKatmanı.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Doğru okuma
    }
    else
    {
        throw new Exception("TextOrientation özelliği değerinin yanlış okunması");
    }
}
{{< /highlight >}}

**PSDNET-1375. CMYK'yi 16 bit renkte düzelt**

{{< highlight csharp >}}
string kaynakDosya = @"ClippingMaskRegular.psd";
string dışaAktarmaYolu = @"çıktı.psd";
string pngDışaAktarmaYolu = @"çıktı.png";

// Dönüştürme seçeneklerini ayarlar
PsdOptions psdSeçenekleri = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Dönüştürme ve kaydetme işlemleri
using (var görüntü = (PsdImage)Image.Load(kaynakDosya))
{
    image.Convert(psdSeçenekleri);
    image.Save(dışaAktarmaYolu);
}

// Dönüştürülen dosyayı açar ve PNG'ye dönüştürür
using (PsdImage görüntü = (PsdImage)Image.Load(dışaAktarmaYolu))
{
    image.Save(pngDışaAktarmaYolu, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
