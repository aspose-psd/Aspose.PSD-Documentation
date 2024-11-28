---
title: Aspose.PSD for .NET 24.3 - Sürüm Notları
type: docs
weight: 100
url: /tr/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD for .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar** | **Özet**                                                          | **Kategori** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [AI Format] Büyük çok sayfalı AI resimlerinin yükleme süresini azalt | Geliştirme |
| PSDNET-1905 | 8 bittten 16 bite dönüştürüldükten sonra PSD dosyası okunamaz hale geldi | Hata |
| PSDNET-1906 | 8 bit'ten 32 bite dönüştürüldükten sonra PSD dosyası okunamaz hale geldi | Hata |
| PSDNET-1921 | [AI Format] AI dosyasındaki Kısa Eğri çizimini düzelt                  | Hata |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-1905. 8 bittten 16 bite dönüştürüldükten sonra PSD dosyası okunamaz hale geldi**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "test_smart_layer.psd");
string çıktıDosyası = Path.Combine(outputFolder, "export.psd");

using (var psdResim8 = (PsdImage)Image.Load(kaynakDosya))
{
    var psdSeçenekler16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    psdResim8.Save(çıktıDosyası, psdSeçenekler16);
}

using (var psdResim16 = (PsdImage)Image.Load(çıktıDosyası))
{
    if (psdResim16.GlobalLayerResources[0] is Lr16Resource)
    {
        // sorun yok
    }
    else
    {
        throw new Exception("Yanlış global kaynak, ilk kaynak Lr16Resource olmalıdır");
    }
}
{{< /highlight >}}

**PSDNET-1906. 8 bittten 32 bite dönüştürüldükten sonra PSD dosyası okunamaz hale geldi**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "test_smart_layer.psd");
string çıktıDosyası = Path.Combine(outputFolder, "export.psd");

using (var psdResim8 = (PsdImage)Image.Load(kaynakDosya))
{
    var psdSeçenekler32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdResim8.Save(çıktıDosyası, psdSeçenekler32);
}

using (var psdResim8 = (PsdImage)Image.Load(çıktıDosyası))
{
    if (psdResim8.GlobalLayerResources[0] is Lr32Resource)
    {
        // sorun yok
    }
    else
    {
        throw new Exception("Yanlış global kaynak, ilk kaynak Lr32Resource olmalıdır");
    }
}
{{< /highlight >}}

**PSDNET-1921. [AI Format] AI dosyasındaki Kısa Eğri çizimini düzeltme**

{{< highlight csharp >}}
string kaynakDosya = Path.Combine(baseFolder, "shortCurve.ai");
string çıktıDosyaYolu = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage resim = (AiImage)Image.Load(kaynakDosya))
{
    resim.Save(çıktıDosyaYolu, new PngOptions());
}
{{< /highlight >}}
