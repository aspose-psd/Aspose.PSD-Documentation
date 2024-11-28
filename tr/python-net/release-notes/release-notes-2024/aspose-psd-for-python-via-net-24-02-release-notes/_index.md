---
title: Aspose.PSD Python için .NET Aracılığıyla 24.2 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-python-uzerinden-net-24-2-surum-notlari/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD Python için .NET 24.2](https://pypi.org/project/aspose-psd/) için sürüm notlarını içermektedir.

{{% /alert %}}

| **Anahtar** | **Özet** | **Kategori** |
|:-------------|:-----------------------------------------------------------------------------|:------------|
| PSDPYTHON-28 | PatternFillSettings için Açı özelliğini işle |   Özellik   |
| PSDPYTHON-29 | TextLayer için dikey ve yatay ölçek desteği |   Özellik   |
| PSDPYTHON-33 | [AI Formatı] PDF Tabanlı AI Formatında arka planın doğru şekilde oluşturulması |   Özellik   |
| PSDPYTHON-34 | Warp'da Distort mekanizmasını değiştir | Geliştiri   |
| PSDPYTHON-35 | Warp'ı hızlandır | Geliştiri   |
| PSDPYTHON-36 | Belge açıldığında "Resim yüklenemedi." istisnasını ele al |     Hata     |
| PSDPYTHON-37 | Stroke Pattern'e sahip psd dosyalarının kaydedilmesini düzelt |     Hata     |
| PSDPYTHON-38 | ReplaceContents kullanıldığında akıllı nesnede metin stili yanlış |     Hata     |
| PSDPYTHON-39 | [AI Formatı] AI dosyasında Kübik Bezier çiziminin düzeltilmesi |     Hata     |



## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Açı

# **Kaldırılan API'ler:**
- Hiçbiri


## **Kullanım örnekleri:**

**Kullanım örnekleri:**

**PSDPYTHON-28. PatternFillSettings için Açı özelliğini işle**

{{< highlight python >}}

	    dosyaAdı = "PatternFillLayerWide_0"
        kaynakDosya = dosyaAdı + ".psd"
        çıktıDosyası = dosyaAdı + "_çıktı.psd"

        yüklemeSeçenekleri = PsdYüklemeSeçenekleri()
        yüklemeSeçenekleri.load_effects_resource = True
        with PsdResmi.load(kaynakDosya, yüklemeSeçenekleri) as img:
            resim = cast(PsdResmi, img)
            doldurKatmanı = cast(DoldurKatmanı, resim.katmanlar[1])
            doldurAyarları = doldurKatmanı.doldur_ayarları
            doldurAyarları.angle = 70
            doldurKatmanı.update()
            resim.save(çıktıDosyası, PsdSeçenekleri())

        with PsdResmi.load(çıktıDosyası, yüklemeSeçenekleri) as img:
            resim = cast(PsdResmi, img)
            doldurKatmanı = cast(DoldurKatmanı, resim.katmanlar[1])
            doldurAyarları = doldurKatmanı.doldur_ayarları

            assert doldurAyarları.angle == 70

{{< /highlight >}}

**PSDPYTHON-29. TextLayer için dikey ve yatay ölçek desteği**

{{< highlight python >}}

           kaynakDosya = "1719_kaynak.psd"
           çıktıDosyası = "çıktı.png"

           # Birkaç yazı tipi ekle
           yazıTipiKlasörü = "1719_YazıTipleri"
           yazıTipiKlasörleri = list(YazıTipiAyarları.get_fonts_folders())
           yazıTipiKlasörleri.ekle(yazıTipiKlasörü)
           YazıTipiAyarları.set_fonts_folders(yazıTipiKlasörleri, True)

           with PsdResmi.load(kaynakDosya) as resim:
               resim.save(çıktıDosyası, PngSeçenekleri())

{{< /highlight >}}

**PSDPYTHON-33. [AI Formatı] PDF Tabanlı AI Formatında arka planın doğru şekilde oluşturulması**

{{< highlight python >}}

           kaynakDosya = "ananaslar.ai"
           çıktıDosyası  = "ananaslar.png"

           with AiResmi.load(kaynakDosya) as resim:
               resim.save(çıktıDosyası, PngSeçenekleri())

{{< /highlight >}}

**PSDPYTHON-34. Distort mekanizmasını warp'ta değiştir**

{{< highlight python >}}

        kaynakDosya = "crow_grid.psd"       
        çıktıDosyası = self.GetFileInOutputFolder("çıkış.png")

        seçenek = PsdYüklemeSeçenekleri()
        seçenek.load_effects_resource = True
        seçenek.allow_warp_repaint = True

        pngSeçenek = PngSeçenekleri()
        pngSeçenek.compression_level = 9
        pngSeçenek.color_type = PngRenkTipi.ALFA İLE GERÇEK RENKLİ
        with PsdResmi.load(kaynakDosya, seçenek) as resim:
            resim.save(çıktıDosyası, pngSeçenek)

{{< /highlight >}}

**PSDPYTHON-35. Warp'ı hızlandır**

{{< highlight python >}}

        kaynakDosya = "çıktı.psd"
        çıktıDosyası = "çıkış.png"

        seçenek = PsdYüklemeSeçenekleri()
        seçenek.load_effects_resource = True
        seçenek.allow_warp_repaint = True

        başlangıç_zamanı = time.time()

        pngSeçenek = PngSeçenekleri()
        pngSeçenek.compression_level = 9
        pngSeçenek.color_type = PngRenkTipi.ALFA İLE GERÇEK RENKLİ

        with PsdResmi.load(kaynakDosya, seçenek) as resim:
            resim.save(çıktıDosyası, pngSeçenek)

        geçen_zaman = time.time() - başlangıç_zamanı

        # eski değer = 193300
        # yeni değer =  55500
        saniye_cinsinden_zaman = int(geçen_zaman * 1000)
        if saniye_cinsinden_zaman > 100000:
            raise Exception("İşlem zamanı çok uzun")        
			
{{< /highlight >}}

**PSDPYTHON-36. Belge açıldığında "Resim yüklenemedi." istisnasını ele al**

{{< highlight python >}}
        kaynakDosya1 = "ÜRÜN.ai"
        çıktıDosyası1 = "ÜRÜN.png"

        with AiResmi.load(kaynakDosya1) as resim:
            resim.save(çıktıDosyası1, PngSeçenekleri())

        kaynakDosya2 = "Dolota.ai"
        çıktıDosyası2 = "Dolota.png"

        with AiResmi.load(kaynakDosya2) as resim:
            resim.save(çıktıDosyası2, PngSeçenekleri())       

        kaynakDosya3 = "ARS_novelty_2108_out_01(1).ai"
        çıktıDosyası3 = "ARS_novelty_2108_out_01(1).png"

        with AiResmi.load(kaynakDosya3) as resim:
            resim.save(çıktıDosyası3, PngSeçenekleri())

        kaynakDosya4 = "bit_gear.ai"      
        çıktıDosyası4 = "bit_gear.png"

        with AiResmi.load(kaynakDosya4) as resim:
            resim.save(çıktıDosyası4, PngSeçenekleri())

        kaynakDosya5 = "test.ai"
        çıktıDosyası5 = "test.png"

        with AiResmi.load(kaynakDosya5) as resim:
            resim.save(çıktıDosyası5, PngSeçenekleri())
{{< /highlight >}}

**PSDPYTHON-37. Stoke Pattern'a sahip psd dosyalarının kaydedilmesini düzelt**

{{< highlight python >}}
	    kaynakDosya = "StrokeShapePattern.psd"
        çıktıDosyası = "StrokeShapePattern_çıktı.psd"

        yeniDesenKöşeleri = Dikdörtgen(0, 0, 4, 4)
        guid = str(uuid.uuid4())
        yeniDesenAdı = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0"
        yeniDesen = [
            Renk.cyan.rgb_to_argb(), Renk.kırmızı.rgb_to_argb(), Renk.kırmızı.rgb_to_argb(), Renk.cyan.rgb_to_argb(),
            Renk.cyan.rgb_to_argb(), Renk.beyaz.rgb_to_argb(), Renk.beyaz.rgb_to_argb(), Renk.cyan.rgb_to_argb(),
            Renk.cyan.rgb_to_argb(), Renk.beyaz.rgb_to_argb(), Renk.beyaz.rgb_to_argb(), Renk.cyan.rgb_to_argb(),
            Renk.cyan.rgb_to_argb(), Renk.kırmızı.rgb_to_argb(), Renk.kırmızı.rgb_to_argb(), Renk.cyan.rgb_to_argb(),
        ]

        with PsdResmi.load(kaynakDosya) as img:
            resim = cast(PsdResmi, img)
            şekilKatmanı = cast(ŞekilKatmanı, resim.katmanlar[1])
            strokeInternalDoldurAyarları = şekilKatmanı.doldur

            pattResource = None
            for globalLayerResource in resim.global_katman_kaynakları:
                pattResource = as_of(globalLayerResource, PattResource)
                if pattResource is not None:
                    patternItem = pattResource.patterns[0]  # Stroke iç desen verisi

                    patternItem.desen_id = guid
                    patternItem.adı = yeniDesenAdı
                    patternItem.set_pattern(yeniDesen, yeniDesenKöşeleri)
                    break

            strokeInternalDoldurAyarları.pattern_adı = yeniDesenAdı
            strokeInternalDoldurAyarları.desen_id = guid + "\0"

            şekilKatmanı.update()

            resim.save(çıktıDosyası)

        # Değişen verileri kontrol et.
        with PsdResmi.load(çıktıDosyası) as img:
            resim = cast(PsdResmi, img)
            şekilKatmanı = cast(ŞekilKatmanı, resim.katmanlar[1])
            strokeInternalDoldurAyarları = şekilKatmanı.doldur

            assert guid.yukarı() == strokeInternalDoldurAyarları.desen_id
            assert yeniDesenAdı == strokeInternalDoldurAyarları.pattern_adı + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. ReplaceContents kullanıldığında akıllı nesnede metin stili yanlış**

{{< highlight python >}}
        girişDosyası = "kaynak.psd"
        çıktı2 = "çıktı.png"

        psdYüklemeSeçenekleri = PsdYüklemeSeçenekleri()
        psdYüklemeSeçenekleri.load_effects_resource = True

        with PsdResmi.load(girişDosyası, psdYüklemeSeçenekleri) as resim:
            psdResim = cast(PsdResmi, resim)
            akıllıNesne = cast(AkıllıNesneKatmanı, psdResim.katmanlar[1])

            akıllıNesneResmi = cast(PsdResmi, akıllıNesne.içeriği_yükle(psdYüklemeSeçenekleri))

            with akıllıNesneResmi:
                akıllıNesne.replace_contents(akıllıNesneResmi)

            pngSeçenek = PngSeçenekleri()
            pngSeçenek.color_type = PngRenkTipi.ALFA İLE GERÇEK RENKLİ
            psdResim.save(çıktı2, pngSeçenek)

{{< /highlight >}}

**PSDPYTHON-39. [AI Formatı] AI dosyasında Kübik Bezier çiziminin düzeltilmesi**

{{< highlight python >}}

        kaynakDosya = "Typography.ai"
        çıkışDosyaYolu = "Typography.png"

        with AiResmi.load(kaynakDosya) as resim:
            resim.save(çıkışDosyaYolu, PngSeçenekleri())

{{< /highlight >}}
