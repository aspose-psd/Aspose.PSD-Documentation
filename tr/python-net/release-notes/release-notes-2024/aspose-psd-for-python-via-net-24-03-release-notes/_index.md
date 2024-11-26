---
title: Aspose.PSD for Python via .NET 24.3 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-for-python-via-net-24-3-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa [Aspose.PSD for Python via .NET 24.3](https://pypi.org/project/aspose-psd/) için sürüm notlarını içerir.

{{% /alert %}}


| **Anahtar**  | **Özet**                                                               | **Kategori** |
|:------------|:-----------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI Format] Büyük çoklu sayfalı AI görüntülerinin yükleme süresini azalt | Geliştirme  |
| PSDPYTHON-45 | 8 bitten 16 bite dönüştürüldükten sonra PSD Dosyası okunamaz hale geldi | Hata        |
| PSDPYTHON-46 | 8 bitten 32 bite dönüştürüldükten sonra PSD Dosyası okunamaz hale geldi | Hata        |
| PSDPYTHON-47 | [AI Format] AI dosyasında Kısa Eğri renderini düzelt                     | Hata        |


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- Yok

# **Kaldırılan API'ler:**
- Yok


## **Kullanım örnekleri:**

**PSDPYTHON-42. [AI Format] Büyük çoklu sayfalı AI görüntülerinin yükleme süresini azalt**

{{< highlight python >}}
   # Örnek yok
{{< /highlight >}}

**PSDPYTHON-45. 8 bitten 16 bite dönüştürüldükten sonra PSD Dosyası okunamaz hale geldi**

{{< highlight python >}}
        kaynakDosya = "test_smart_layer.psd"
        çıktıDosyası = "export.psd"

        with PsdImage.load(kaynakDosya) as psdImage8:
            psdOptions16 = PsdOptions()
            psdOptions16.channel_bits_count = 16

            psdImage8.save(çıktıDosyası, psdOptions16)

        with PsdImage.load(çıktıDosyası) as imaj:
            psdImaj16 = cast(PsdImage, imaj)

            testKaynak = as_of(psdImaj16.global_layer_resources[5], Lr16Resource)
            if testKaynak is not None:
                # sorun yok
                pass
            else:
                raise Exception("Yanlış global kaynak, ilk kaynak Lr16Resource olmalı")
{{< /highlight >}}


**PSDPYTHON-46. 8 bitten 32 bite dönüştürüldükten sonra PSD Dosyası okunamaz hale geldi**

{{< highlight python >}}
        kaynakDosya = "test_smart_layer.psd"
        çıktıDosyası = "export.psd"

        with PsdImage.load(kaynakDosya) as psdImage8:
            psdOptions32 = PsdOptions()
            psdOptions32.channel_bits_count = 32

            psdImage8.save(çıktıDosyası, psdOptions32)

        with PsdImage.load(çıktıDosyası) as imaj:
            psdImaj32 = cast(PsdImage, imaj)

            testKaynak = as_of(psdImaj32.global_layer_resources[5], Lr32Resource)
            if testKaynak is not None:
                # sorun yok
                pass
            else:
                raise Exception("Yanlış global kaynak, ilk kaynak Lr32Resource olmalı")
{{< /highlight >}}


**PSDPYTHON-47. [AI Format] AI dosyasında Kısa Eğri renderini düzelt**

{{< highlight python >}}
        kaynakDosya = "shortCurve.ai"
        çıktıDosyaYolu = "shortCurve.png"

        with AiImage.load(kaynakDosya) as imaj:
            imaj.save(çıktıDosyaYolu, PngOptions())
{{< /highlight >}}
