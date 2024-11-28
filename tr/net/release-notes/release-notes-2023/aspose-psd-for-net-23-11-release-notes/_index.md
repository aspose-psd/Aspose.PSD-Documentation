---
title: Aspose.PSD for .NET 23.11 - Sürüm Notları
type: docs
weight: 20
url: /tr/net/aspose-psd-for-net-23-11-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 23.11](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:------------|:----------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-412 | LMskResource Desteği | Özellik |
| PSDNET-1669 | [AI Formatı] PDF tabanlı AI dosyasını Aspose.PSD ile render etme yeteneği eklendi | Özellik |
| PSDNET-1702 | [AI Formatı] "cm" PostScript operatörü desteği eklendi | Özellik |
| PSDNET-1752 | Yeni warp türleri eklendi: Dalga, kabuk yukarı, kabuk aşağı | Özellik |
| PSDNET-1797 | Dikey warp desteği eklendi | Özellik |
| PSDNET-1756 | System.ArgumentNullException: 'Değer boş olamaz. (Parametre 'anahtar')' metodu çağrılırken TextLayer.GetFonts() çağrısında hata alınır | Hata |


## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M:Aspose.PSD.FontSettings.RemoveFontCacheFile
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorSpace
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent1
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent2
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent3
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.ColorComponent4
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Opacity
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Flag
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LmskResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.CMYK
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.Lab
- F:Aspose.PSD.FileFormats.Psd.Resources.Enums.ColorSpace.GrayScale


# **Kaldırılan API'lar:**
- Yok


## **Kullanım örnekleri:**
**PSDNET-412. LMskResource Desteği**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "kaynakDosya.psd");
string ciktiPsd = Path.Combine(outputFolder, "kaynakDosya_cikti.psd");

void AssertAreEqual(object expected, object actual)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception("Objeler eşit değil.");
    }
}

// 16-bit imajı yükle.
using (PsdImage imaj = (PsdImage)Image.Load(kaynakDosya))
{
    // LmskResource bul.
    LmskResource lmskResource = new LmskResource();
    foreach (var res in imaj.GlobalLayerResources)
    {
        if (res is LmskResource)
        {
            lmskResource = (LmskResource)res;
            break;
        }
    }

    // LmskResource özelliklerini kontrol et.
    AssertAreEqual(lmskResource.ColorSpace, PSD.FileFormats.Psd.Resources.Enums.ColorSpace.RGB);
    AssertAreEqual(lmskResource.ColorComponent1, (ushort)65535);
    AssertAreEqual(lmskResource.ColorComponent2, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent3, (ushort)0);
    AssertAreEqual(lmskResource.ColorComponent4, (ushort)0);
    AssertAreEqual(lmskResource.Opacity, (short)45);
    AssertAreEqual(lmskResource.Flag, (byte)128);

    // LmskResource özelliklerini değiştir.
    lmskResource.ColorSpace = PSD.FileFormats.Psd.Resources.Enums.ColorSpace.HSB;
    lmskResource.ColorComponent1 = 7854;
    lmskResource.ColorComponent2 = 10;
    lmskResource.ColorComponent3 = 15484;
    lmskResource.Opacity = 85;

    // İmajı kaydet.
    imaj.Save(ciktiPsd);
}
{{< /highlight >}}

**PSDNET-1669. [AI Formatı] Aspose.PSD ile PDF tabanlı AI dosyasını render etme yeteneği eklendi**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "ai_bir.ai");
string ciktiPng = Path.Combine(outputFolder, "ai_bir_cikti.png");

// PDF tabanlı AI imajı yükle.
using (AiImage imaj = (AiImage)Image.Load(sourceFile))
{
    // AI imajını PNG imaj olarak kaydet.
    image.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1702. [AI Formatı] "cm" PostScript operatörü desteği eklendi**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "ai_iki.ai");
string ciktiPng = Path.Combine(outputFolder, "ai_iki_cikti.png");

// AI imajı yükle.
using (AiImage imaj = (AiImage)Image.Load(sourceFile))
{
    // AI imajını PNG imaj olarak kaydet.
    imaj.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1752. Yeni warp türleri eklendi: Dalga, kabuk yukarı, kabuk aşağı**

{{< highlight csharp >}}
var yuklemeSecenekleri = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var kaydetmeSecenekleri = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string kaynakDosyaBalik = Path.Combine(baseFolder, "1752_balik_warp.psd");
string kaynakDosyaYükseliş = Path.Combine(baseFolder, "1752_yukselis_warp.psd");
string kaynakDosyaDalga = Path.Combine(baseFolder, "1752_dalga_warp.psd");

string ciktiDosyaBalik = Path.Combine(outputFolder, "1752_cikti_balik.png");
string ciktiDosyaYükseliş = Path.Combine(outputFolder, "1752_cikti_yukselis.png");
string ciktiDosyaDalga = Path.Combine(outputFolder, "1752_cikti_dalga.png");

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaBalik, yuklemeSecenekleri))
{
    psdImage.Save(ciktiDosyaBalik, kaydetmeSecenekleri);
}

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaYükseliş, yuklemeSecenekleri))
{
    psdImage.Save(ciktiDosyaYükseliş, kaydetmeSecenekleri);
}

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaDalga, yuklemeSecenekleri))
{
    psdImage.Save(ciktiDosyaDalga, kaydetmeSecenekleri);
}
{{< /highlight >}}

**PSDNET-1756. TextLayer.GetFonts() metodu çağrılırken System.ArgumentNullException hatası alınır**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "BasitMetin.psd");

FontSettings.RemoveFontCacheFile();

using (var psdImage = (PsdImage)Image.Load(src))
{
    foreach (var layer in psdImage.Layers)
    {
        if (layer is TextLayer textLayer)
        {
            textLayer.GetFonts();
        }
    }
}
{{< /highlight >}}

**PSDNET-1797. Dikey warp desteği eklendi**

{{< highlight csharp >}}
var yuklemeSecenekleri = new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true };
var kaydetmeSecenekleri = new PngOptions { ColorType = PngColorType.TruecolorWithAlpha };

string kaynakDosyaAsagiYay = Path.Combine(baseFolder, "1797_asagi_yay_v.psd");
string kaynakDosyaYukariYay = Path.Combine(baseFolder, "1797_yukari_yay_v.psd");
string kaynakDosyaKemer = Path.Combine(baseFolder, "1797_kemer_v.psd");
string kaynakDosyaBatakhane = Path.Combine(baseFolder, "1797_batakhane_v.psd");
string kaynakDosyaBayrak = Path.Combine(baseFolder, "1797_bayrak_v.psd");
string kaynakDosyaBalik = Path.Combine(baseFolder, "1797_balik_v.psd");
string kaynakDosyaYükseliş = Path.Combine(baseFolder, "1797_yukselis_v.psd");
string kaynakDosyaDalga = Path.Combine(baseFolder, "1797_dalga_v.psd");

string ciktiDosyaAsagiYay = Path.Combine(outputFolder, "1797_cikti_asagi_yay_v.png");
string ciktiDosyaYukariYay = Path.Combine(outputFolder, "1797_cikti_yukari_yay_v.png");
string ciktiDosyaKemer = Path.Combine(outputFolder, "1797_cikti_kemer_v.png");
string ciktiDosyaBatakhane = Path.Combine(outputFolder, "1797_cikti_batakhane_v.png");
string ciktiDosyaBayrak = Path.Combine(outputFolder, "1797_cikti_bayrak_v.png");
string ciktiDosyaBalik = Path.Combine(outputFolder, "1797_cikti_balik_v.png");
string ciktiDosyaYükseliş = Path.Combine(outputFolder, "1797_cikti_yukselis_v.png");
string ciktiDosyaDalga = Path.Combine(outputFolder, "1797_cikti_dalga_v.png");

using (var psdImage = (PsdImage)Image.Load(kaynakDosyaAsagiYay, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaAsagiYay, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaYukariYay, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaYukariYay, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaKemer, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaKemer, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaBatakhane, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaBatakhane, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaBayrak, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaBayrak, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaBalik, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaBalik, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaYükseliş, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaYükseliş, kaydetmeSecenekleri); }
using (var psdImage = (PsdImage)Image.Load(kaynakDosyaDalga, yuklemeSecenekleri)) { psdImage.Save(ciktiDosyaDalga, kaydetmeSecenekleri); }
{{< /highlight >}}
