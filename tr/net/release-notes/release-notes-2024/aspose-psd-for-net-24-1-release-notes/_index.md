---
title: Aspose.PSD for .NET 24.1 - Sürüm Notları
type: docs
weight: 120
url: /tr/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                      | **Kategori** |
|:------------|:-----------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [AI Format] Çoklu sayfalı AI görüntülerine temel işleme ekle                                   | Özellik     |
| PSDNET-718  | Eğirme Metin Etkisi metne uygulanmaz                                                          | Hata        |
| PSDNET-1620 | Belirli dosyadaki maskeyi yanlış şekilde oluşturma                                             | Hata        |
| PSDNET-1855 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor'da NullReferenceException | Hata        |
| PSDNET-1883 | [AI Format] AiExporterUtils'da bellek kullanımını düzeltme                                    | Hata        |



## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Kaldırılan API'lar:**
- Yok


## **Kullanım Örnekleri:**

**PSDNET-718. Eğirme Metin Etkisi metne uygulanmaz**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "text_warp.psd");
string çıktıDosyası = Path.Combine(outputFolder, "export.png");

var seçenekler = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(kaynakDosya, seçenekler))
{
    img.Save(çıktıDosyası, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Belirli dosyadaki maskeyi yanlış şekilde oluşturma**

{{< highlight csharp >}}
string kaynakDosya1 = Path.Combine(baseFolder, "mask_problem.psd");
string kaynakDosya2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string çıktıDosyası1 = Path.Combine(outputFolder, "mask_export.png");
string çıktıDosyası2 = Path.Combine(outputFolder, "puh_export.png");

var seçenekler = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(kaynakDosya1, seçenekler))
{
    img.Save(çıktıDosyası1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(kaynakDosya2, seçenekler))
{
    img.Save(çıktıDosyası2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [AI Format] Çoklu sayfalı AI görüntülerine temel işleme ekle**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "threePages.ai");
string ilkSayfaÇıktıPng = Path.Combine(outputFolder, "firstPageOutput.png");
string ikinciSayfaÇıktıPng = Path.Combine(outputFolder, "secondPageOutput.png");
string üçüncüSayfaÇıktıPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// AI görüntüsünü yükle.
using (AiImage görüntü = (AiImage)Image.Load(kaynakDosya))
{
    // Varsayılan olarak, ActivePageIndex 0'dır.
    // Dolayısıyla bu özellik değiştirilmeden AI görüntüsünü kaydederseniz, ilk sayfa açılır ve kaydedilir.
    görüntü.Save(ilkSayfaÇıktıPng, new PngOptions());

    // Aktif sayfa indeksini ikinci sayfaya değiştirin.
    görüntü.ActivePageIndex = 1;

    // AI görüntüsünün ikinci sayfasını PNG görüntüsü olarak kaydedin.
    görüntü.Save(ikinciSayfaÇıktıPng, new PngOptions());

    // Aktif sayfa indeksini üçüncü sayfaya değiştirin.
    görüntü.ActivePageIndex = 2;

    // AI görüntüsünün üçüncü sayfasını PNG görüntüsü olarak kaydedin.
    görüntü.Save(üçüncüSayfaÇıktıPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor'da NullReferenceException**

{{< highlight csharp >}}
string fontlarKlasörü = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontlarKlasörü }, true);

string girişDosyası = Path.Combine(baseFolder, "1.psd");
string çıktıDosyası = Path.Combine(outputFolder, "out_1855.png");
using (var psdGörüntü = (PsdImage)Image.Load(girişDosyası))
{
    psdGörüntü.Save(çıktıDosyası, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [AI Format] AiExporterUtils'da bellek kullanımını düzeltme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "threePages.ai");
string ilkSayfaÇıktıPng = Path.Combine(outputFolder, "firstPageOutput.png");
string ikinciSayfaÇıktıPng = Path.Combine(outputFolder, "secondPageOutput.png");
string üçüncüSayfaÇıktıPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double BellekSınırı = 220;
double kullanılanBellek = double.MaxValue;

// AI görüntüsünü yükle.
using (AiImage görüntü = (AiImage)Image.Load(kaynakDosya))
{
    // AI görüntüsünün ilk sayfasını PNG görüntüsü olarak kaydedin.
    görüntü.Save(ilkSayfaÇıktıPng, new PngOptions());

    // Aktif sayfa indeksini ikinci sayfaya değiştirin.
    görüntü.ActivePageIndex = 1;

    // AI görüntüsünün ikinci sayfasını PNG görüntüsü olarak kaydedin.
    görüntü.Save(ikinciSayfaÇıktıPng, new PngOptions());

    // Aktif sayfa indeksini üçüncü sayfaya değiştirin.
    görüntü.ActivePageIndex = 2;

    // AI görüntüsünün üçüncü sayfasını PNG görüntüsü olarak kaydedin.
    görüntü.Save(üçüncüSayfaÇıktıPng, new PngOptions());
}

GC.Collect();

kullanılanBellek = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (kullanılanBellek > BellekSınırı)
{
    throw new Exception("Bellek kullanımı çok büyük. " + kullanılanBellek + " yerine " + BellekSınırı.ToString("F1"));
}
{{< /highlight >}}
