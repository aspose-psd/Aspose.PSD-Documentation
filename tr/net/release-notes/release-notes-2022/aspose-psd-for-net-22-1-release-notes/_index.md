---
title: Aspose.PSD for .NET 22.1 - Sürüm Notları
type: dokümanlar
weight: 120
url: /tr/net/aspose-psd-for-net-22-1-release-notes/
---

{{% uyari renk="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 22.1](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /uyari %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-1017|PatternOverlay yalnızca bir kez uygulanabilir|Hata|
|PSDNET-1056|Akıştan bir dosya açıldığında geçici dosyalar taşabilir|Hata|
|PSDNET-991|Gaussian bulanıklığı akıllı filtreye yönelik işlemler için rendering optimizasyonu|Özellik|
|PSDNET-1044|PattResource'da çoklu desen verisinin desteklenmesi|Özellik|


## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Int32,Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Patterns
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey2
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey3
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.ImageMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Length
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.Save(Aspose.PSD.StreamContainer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResourceData.SetPattern(System.Int32[],Aspose.PSD.Rectangle)


# **Kaldırılan API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)


## **Kullanım örnekleri:**
**PSDNET-1017. PatternOverlay yalnızca bir kez uygulanabilir**
{{< vurgu csharp >}}
            string ciktiPsd = "cikti_1017.psd";
            string ciktiPng = "cikti_1017.png";

            using (var psdGoruntu = (PsdGoruntu)Goruntu.Olustur(new PsdSecenekleri() { Kaynak = new AkimKaynak(new HafizaAkimi()), }, 500, 500))
            {
                DolguKatmani katman = DolguKatmani.Olustur(DoldurmaTuru.Renk);
                psdGoruntu.KatmanEkle(katman);
                VektorYol vektorYol = VektorVeriSaglayici.KatmanIcinVektorYolOlustur(katman);
                vektorYol.DolguRengi = Renk.Sari;
                SeçimBicimi şekil2 = yeni SeçimBicimi();
                şekil2.Noktalar.Ekle(yeni BezierNokta(new NoktaF(300, 150), doğru));
                şekil2.Noktalar.Ekle(yeni BezierNokta(new NoktaF(350, 200), doğru));
                şekil2.Noktalar.Ekle(yeni BezierNokta(new NoktaF(250, 200), doğru));
                şekil2.Kapalı = yanlış;
                vektorYol.Şekiller.Ekle(şekil2);

                VektorVeriSaglayici.KatmandanVektörYolunuGüncelle(katman, vektorYol, doğru);

                DesenÖrtüsüEfekti desenÖrtüsü = katman.Bulaniksınıflar.Seçenekleri.DesenÖrtüsüEkle();
                var yeniDesen = yeni int[]
                                        {
                                Renk.Akua.ToArgb(), Renk.Kırmızı.ToArgb(), Renk.Kırmızı.ToArgb(),
                                Renk.Akua.ToArgb(), Renk.Akua.ToArgb(), Renk.Beyaz.ToArgb(),
                                Renk.Beyaz.ToArgb(), Renk.Akua.ToArgb(),
                                        };

                var yeniDesenSınırları = yeni Rectangle(0, 0, 4, 2);
                desenÖrtüsü.Ayarlar.DesenVerisi = yeniDesen;
                desenÖrtüsü.Ayarlar.DesenGenişliği = yeniDesenSınırları.Genişlik;
                desenÖrtüsü.Ayarlar.DesenYüksekliği = yeniDesenSınırları.Yükseklik;
                desenÖrtüsü.Ayarlar.YatayOfset = yeniDesenSınırları.X;
                desenÖrtüsü.Ayarlar.DikeyOfset = yeniDesenSınırları.Y;

                katman.Güncelle();

                var katman2 = DolguKatmani.Olustur(DoldurmaTuru.Renk);
                psdGoruntu.KatmanEkle(katman2);
                VektorYol vektorYol2 = VektorVeriSaglayici.KatmanIcinVektorYolOlustur(katman2);
                vektorYol2.DolguRengi = Renk.Mavi;
                SeçimBicimi şekil3 = yeni SeçimBicimi();
                şekil3.Noktalar.Ekle(yeni BezierNokta(new NoktaF(400, 450), doğru));
                şekil3.Noktalar.Ekle(yeni BezierNokta(new NoktaF(100, 400), doğru));
                şekil3.Noktalar.Ekle(yeni BezierNokta(new NoktaF(250, 100), doğru));
                şekil3.Kapalı = yanlış;
                vektorYol2.Şekiller.Ekle(şekil3);

                VektorVeriSaglayici.KatmandanVektörYolunuGüncelle(katman2, vektorYol2, doğru);

                DesenÖrtüsüEfekti desenÖrtüsü2 = katman2.Bulaniksınıflar.Seçenekleri.DesenÖrtüsüEkle();
                var yeniDesen2 = yeni int[]
                                        {
                                Renk.Yeşil.ToArgb(), Renk.Mor.ToArgb(), Renk.Mor.ToArgb(),
                                Renk.Yeşil.ToArgb(), Renk.Yeşil.ToArgb(), Renk.Siyah.ToArgb(),
                                Renk.Siyah.ToArgb(), Renk.Yeşil.ToArgb(),
                                        };

                var yeniDesenSınırları2 = yeni Rectangle(0, 0, 4, 2);
                desenÖrtüsü2.Ayarlar.DesenVerisi = yeniDesen2;
                desenÖrtüsü2.Ayarlar.DesenGenişliği = yeniDesenSınırları2.Genişlik;
                desenÖrtüsü2.Ayarlar.DesenYüksekliği = yeniDesenSınırları2.Yükseklik;
                desenÖrtüsü2.Ayarlar.YatayOfset = yeniDesenSınırları2.X;
                desenÖrtüsü2.Ayarlar.DikeyOfset = yeniDesenSınırları2.Y;

                psdGörüntü.Kaydet(ciktiPsd);
                psdGörüntü.Kaydet(ciktiPng, yeni PngSecenekleri() { RenkTürü = PngRenkTürü.KesinRenkliAlfa });
{{< /vurgu >}}

**PSDNET-1056. Akıştan bir dosya açıldığında geçici dosyalar taşabilir**
{{< vurgu csharp >}}

            kullanarak (var memAkım = yeni HafızaAkımı())
            {
                byte[] dosyaBaytları = yeni byte[3];
                memAkım.Yaz(dosyaBaytları, 0, dosyaBaytları.Uzunluk);

                // davranışı test et
                Durum istisna = null;
                dene
                {
                    kullanarak (var görüntü = Goruntu.Yükle(memAkım))
                    {
                    }
                }
                yakala (ÇekirdekHataları.GoruntuYüklemeİstisnası anaHata)
                {
                    // en düşük seviye istisnasını ara
                    istisna = anaHata;
                    iken (istisna.İçİstisnası != null)
                    {
                        istisna = istisna.İçİstisnası;
                    }
                }

                // istisnayı kontrol et
                dize türAdı = istisna.Türü.Adı; // hata ayıklama için
                eğer (istisna bir ÇekirdekHataları.GoruntuYüklemeİstisnası)
                {
                    // sorun yok
                }
                başka
                {
                    // sorun yok
                    fırlat istisna;
                }
            }
{{< /vurgu >}}

**PSDNET-991. Gaussian bulanıklığı akıllı filtreye yönelik işlemler için rendering optimizasyonu**
{{< vurgu csharp >}}
          dize kaynakDosya = "psdnet991_katmanlar.psd";
            dize ciktiPsd = "cikti_psdnet991_katmanlar.psd";
            dize ciktiPng = "cikti_psdnet991_katmanlar.png";

            kullanarak (var görüntü = (PsdGoruntu)Goruntu.Yükle(kaynakDosya))
            {
                AkıllıNesneKatmanı akıllıKatman = (AkıllıNesneKatmanı)görüntü.Katmanlar[1];
                Katman maskeKatmanı = görüntü.Katmanlar[2];
                Katman düzenliKatman = görüntü.Katmanlar[3];

                GaussianBulanıklıkAkıllıFiltre gaussianBulanıklaştırıcı = yeni GaussianBulanıklıkAkıllıFiltre();
                gaussianBulanıklaştırıcı.Yarıçap = 10;

                // Filtreyi AkıllıNesne'ye uygula
                gaussianBulanıklaştırıcı.Uygula(akıllıKatman);
                akıllıKatman.SmartFilters.KaynakDeğerleriniGüncelle();
                akıllıKatman.ModifiedContent'ıGüncelle();

                // Maske katmanına filtreyi uygula
                gaussianBulanıklaştırıcı.MaskeyeUygula(maskeKatmanı);

                // Katmana filtreyi uygula
                gaussianBulanıklaştırıcı.Uygula(düzenliKatman);

                görüntü.Kaydet(ciktiPsd);
                görüntü.Kaydet(ciktiPng, yeni PngSecenekleri() { RenkTürü = PngRenkTürü.KesinRenkliAlfa });
            }
{{< /vurgu >}}

**PSDNET-1044. PattResource'da çoklu desen verisinin desteklenmesi**
{{< vurgu csharp >}}
            dize kaynak = "psdnet1044.psd";
            dize cikti = "cikti_psdnet1044.psd";

            kullanarak (var görüntü = (PsdGoruntu)Goruntu.Yükle(kaynak, yeni PsdYükleSecenekleri() { EfektKaynağınıYükle = doğru }))
            {
                PattResource pattKaynak = (PattResource)görüntü.GlobalKatmanKaynakları[0];

                eğer (pattKaynak.Desenler.Uzunluk == 2)
                {
                    Konsol.Yaz("PattResourceData öğelerinin doğru okunması.");
                }

                var dolguKatmanı = DolguKatmani.Oluştur(DoldurmaTuru.Renk);
                görüntü.KatmanEkle(dolguKatmanı);

                IDesenDoldurmaAyarları desenAyarı = dolguKatmanı.Bulaniksınıflar.DesenÖrtüsüEkle().Ayarlar;

                desenAyarı.DesenGenişliği = 3;
                desenAyarı.DesenYüksekliği = 3;
                desenAyarı.DesenVerisi = yeni int[]
                {
                    Renk.Beyaz.ToArgb(), Renk.Beyaz.ToArgb(), Renk.Kırmızı.ToArgb(),
                    Renk.Beyaz.ToArgb(), Renk.Yeşil.ToArgb(), Renk.Beyaz.ToArgb(),
                    Renk.Mavi.ToArgb(), Renk.Beyaz.ToArgb(), Renk.Beyaz.ToArgb(),
                };

                görüntü.Kaydet(cikti);
            }
{{< /vurgu >}}