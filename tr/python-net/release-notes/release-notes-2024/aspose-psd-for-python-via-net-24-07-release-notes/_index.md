---
title: Aspose.PSD Python via .NET 24.7 - Sürüm Notları
type: docs
weight: 10
url: /tr/python-net/aspose-psd-python-via-net-24-7-s%C3%BCr%C3%BCm-notlar%C4%B1/
---

{{% alert color="primary" %}}

Bu sayfa [Aspose.PSD Python via .NET 24.7](https://pypi.org/project/aspose-psd/) sürümü için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                                                                 | **Kategori** |
|:------------|:--------------------------------------------------------------------------------------------------------|:------------|
| PSDPYTHON-86 | AI belgesi açıldığında "Resim yükleme başarısız oldu." istisnası                                    | Hata         |
| PSDPYTHON-87 | Metinlerin çıktı PDF dosyalarında yanlış şekilde render edilmesi                                      | Hata         |
| PSDPYTHON-88 | Linux'ta belirtilen dosya için Resim dışa aktarma başarısız oldu hatasını düzeltme                    | Hata         |
| PSDPYTHON-89 | Aspose.Drawing kullanılırken yazı tiplerinin yüklenmesini düzeltme                                    | Hata         |
| PSDPYTHON-90 | Büyük JPEG kullanılarak akıllı nesne katmanı oluşturulurken 'Aritmetik işlem taşma hatası'             | Hata         |
| PSDPYTHON-91 | AI dosyasının JPG dosyasına dönüştürülememesi                                                       | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.NoiseGradientFillSettings.ExpansionCount
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddGradientMapAdjustmentLayer
- T:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.AdjustmentLayers.GradientMapLayer.GradientSettings
- P:Aspose.PSD.FileFormats.Ai.AiImage.XmpData

# **Kaldırılan API'lar:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDPYTHON-86. AI belgesi açıldığında "Resim yükleme başarısız oldu" istisnası**
{{< highlight python >}}
        kaynakDosya = self.GetFileInBaseFolder("[SA]_ID_card_template.ai")
        çıktıDosyası = self.GetFileInOutputFolder("[SA]_ID_card_template.png")

        with AiImage.load(kaynakDosya) as resim:
            resim.save(çıktıDosyası, PngOptions())
{{< /highlight >}}

**PSDPYTHON-87. Metinlerin çıktı PDF dosyalarında yanlış şekilde render edilmesi**
{{< highlight python >}}
        kaynak = self.GetFileInBaseFolder("CVFlor.psd")
        çıktı = self.GetFileInOutputFolder("çıktı.pdf")

        with PsdImage.load(kaynak) as psdResim:
            kaydetmeSeçenekleri = PdfOptions()
            kaydetmeSeçenekleri.pdf_core_options = PdfCoreOptions()

            psdResim.save(çıktı, kaydetmeSeçenekleri)
{{< /highlight >}}

**PSDPYTHON-88. Linux'ta belirtilen dosya için Resim dışa aktarma başarısız oldu hatasını düzeltme**
{{< highlight python >}}
        kaynakDosya = self.GetFileInBaseFolder("Bed_Roll-Sticker4_1.psd")
        çıktıDosya = self.GetFileInOutputFolder("çıktı.jpg")

        yüklemeSeçenekleri = PsdLoadOptions()
        yüklemeSeçenekleri.load_effects_resource = True
        kaydetmeSeçenekleri = JpegOptions()
        kaydetmeSeçenekleri.quality = 70
        with PsdImage.load(kaynakDosya, yüklemeSeçenekleri) as psdResim:
            psdResim.save(çıktıDosya, kaydetmeSeçenekleri)
{{< /highlight >}}

**PSDPYTHON-89. Aspose.Drawing kullanılırken yazı tiplerinin yüklenmesini düzeltme**
{{< highlight python >}}
        InstalledFontCollection ile kuruluYazıTipleri:
            print("- Güncellemeden önce. Yüklü yazı tipleri sayısı: " + str(len(kuruluYazıTipleri.families)))
            print("- 'Arial' için Adobe yazı tip adını alarak font önbelleğini yenile: ")
            FontSettings.get_adobe_font_name("Arial")
            print("- Güncellemeden sonra. Yüklü yazı tipleri sayısı: " + str(len(kuruluYazıTipleri.families))

            assert len(kuruluYazıTipleri.families) > 1
{{< /highlight >}}

**PSDPYTHON-90. Büyük JPEG kullanılarak akıllı nesne katmanı oluşturulurken 'Aritmetik işlem taşma hatası'**
{{< highlight python >}}
        # Düzeltme yapıldı, ancak bu testi kısıtlayan Aspose.PSD for Python'da başka bir sorun var
        #kaynakDosya = self.GetFileInBaseFolder("source.psd")
        #görselJpg = self.GetFileInBaseFolder("test.jpg")

        #yüklemeSeçenekleri = PsdLoadOptions()
        #yüklemeSeçenekleri.data_recovery_mode = DataRecoveryMode.MAXIMAL_RECOVER
        #with PsdImage.load(kaynakDosya, yüklemeSeçenekleri) as resim:
            #with open(görselJpg, "rb", buffering=0) as akış:
                #eklenenKatman = SmartObjectLayer(akış)
                #eklenenKatman.Name = "Test Katman"
                #resim.AddLayer(eklenenKatman)
{{< /highlight >}}

**PSDPYTHON-91. AI dosyasının JPG dosyasına dönüştürülememesi**
{{< highlight python >}}
        kaynakDosya = self.GetFileInBaseFolder("aaa.ai")
        çıktıDosyası = self.GetFileInOutputFolder("aaa.png")

        with AiImage.load(kaynakDosya) as resim:
            resim.save(çıktıDosyası, PngOptions())
{{< /highlight >}}
