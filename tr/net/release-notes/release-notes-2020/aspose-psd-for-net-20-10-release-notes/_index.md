---
title: Aspose.PSD .NET için 20.10 Sürüm Notları
type: docs
weight: 30
url: /tr/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD için .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-565|Metin katmanları olan belirli PSD dosyasını kaydederken hata oluşur|Hata|
|PSDNET-680|Aspose.PSD ile dönüşümlerden sonra yazı tipi kaybolur|Hata|
|PSDNET-704|Akıllı Nesne Katmanının Render Edilmesi|Özellik|
|PSDNET-707|Akıllı Nesne zarar vermeden dönüşümleri destekler|Özellik|
|PSDNET-711|Değişiklik yapılmadan kaydedildikten sonra Metin Katmanı Kayması|Hata|
|PSDNET-720|Aspose.PSD 20.8: Psd'ten Tiff'e dönüştürme istisnası|Hata|

## **Halka Açık API Değişiklikleri**
# **Eklenen API'ler:**
- Hiçbiri
# **Kaldırılan API'ler:**
- Hiçbiri

## **Kullanım Örnekleri:**
**PSDNET-565. Metin katmanları olan belirli PSD dosyasını kaydederken hata meydana gelir**
{{< highlight csharp >}}
            string kaynakDosyaYolu = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string ciktiDosyasi = "sonuc.psd";

            using (PsdImage resim = (PsdImage)Image.Load(kaynakDosyaYolu))
            {
                resim.Save(ciktiDosyasi, new PsdOptions(resim));
            }
{{< /highlight >}}

**PSDNET-680. Dönüşümlerden sonra yazı tipleri kaybolur**
{{< highlight csharp >}}
            string kaynakDosyaYolu = "TwoFonts.psd";

            string ciktiPsd1 = "cikti1.psd";
            string ciktiPsd2 = "cikti2.psd";
            string ciktiPng1 = "cikti1.png";
            string ciktiPng2 = "cikti2.png";

            void EsitDegil(int beklenen, int gercek)
            {
                if (beklenen != gercek)
                {
                    throw new Exception("Değerler eşit değil.");
                }
            }

            using (var psdResim = (PsdImage)Image.Load(kaynakDosyaYolu))
            {
                var metinKatmani = (TextLayer)psdResim.Layers[1];

                EsitDegil(1, metinKatmani.TextData.Items[0].Style.FontIndex);
                EsitDegil(0, metinKatmani.TextData.Items[1].Style.FontIndex);

                metinKatmani.TextData.UpdateLayerData();

                EsitDegil(1, metinKatmani.TextData.Items[0].Style.FontIndex);
                EsitDegil(0, metinKatmani.TextData.Items[1].Style.FontIndex);

                psdResim.Save(ciktiPsd1, new PsdOptions(psdResim));
                psdResim.Save(ciktiPng1, new PngOptions());
            }

            using (var psdResim = (PsdImage)Image.Load(ciktiPsd1))
            {
                var metinKatmani = (TextLayer)psdResim.Layers[1];

                EsitDegil(1, metinKatmani.TextData.Items[0].Style.FontIndex);
                EsitDegil(0, metinKatmani.TextData.Items[1].Style.FontIndex);

                metinKatmani.TextData.UpdateLayerData();

                EsitDegil(1, metinKatmani.TextData.Items[0].Style.FontIndex);
                EsitDegil(0, metinKatmani.TextData.Items[1].Style.FontIndex);

                psdResim.Save(ciktiPsd2, new PsdOptions(psdResim));
                psdResim.Save(ciktiPng2, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-704. Akıllı Nesne Katmanının Render Edilmesi**
{{< highlight csharp >}}
            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanının içeriğini değiştirmeyi ve doğru şekilde render etmeyi gösterir.
            string veriDizini = "PSDNET704_1\\";
            string dosyaYolu = veriDizini + "new_panama-papers-4-trans4.psd";
            string pngCiktiYolu = veriDizini + "new_panama-papers-4-trans4_degistirilmis.png";
            string psdCiktiYolu = veriDizini + "new_panama-papers-4-trans4_degistirilmis.psd";
            string yeniIcerikYolu = veriDizini + "new_huset.jpg";
            using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
            {
                var akıllıNesneKatmanı = (SmartObjectLayer)resim.Layers[resim.Layers.Length - 1];
                akıllıNesneKatmanı.ReplaceContents(yeniIcerikYolu);
                resim.Save(pngCiktiYolu, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                resim.Save(psdCiktiYolu, new PsdOptions(resim));
            }

            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanlarının görüntü önbelleğini güncellemeyi ve doğru şekilde render etmeyi gösterir.
            dosyaYolu = veriDizini + "LayeredSmartObjects8bit2.psd";
            pngCiktiYolu = veriDizini + "LayeredSmartObjects8bit2_guncellenmis.png";
            psdCiktiYolu = veriDizini + "LayeredSmartObjects8bit2_guncellenmis.psd";
            using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
            {
                resim.SmartObjectProvider.UpdateAllModifiedContent();
                resim.Save(pngCiktiYolu, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                resim.Save(psdCiktiYolu, new PsdOptions(resim));
            }
{{< /highlight >}}

**PSDNET-707. Akıllı Nesne zarar vermeden dönüşümleri destekler**
{{< highlight csharp >}}
            string veriDizini = "PSDNET707_1\\";
            string ciktiDizini = veriDizini;

            // Bu örnekler, SmartObjectLayer ile PSD dosyasının zarar vermeden dönüşümlerini gösterir.
            // Orjinal resim verileri veya kalitesi etkilenmediği için bir katmanı ölçeklendirebilir, döndürebilir,
            // eğebilir, bozulmadan çevirilebilir, perspektif dönüşümü yapılabilir veya bükülebilir
            // çünkü dönüşümler orijinal verileri etkilemez.

            // Bu örnek, Adobe® Photoshop® imajını akıllı nesne katmanlarıyla yeniden boyutlandırmayı gösterir:
            SmartObjectImageResizeSupportOrnegi("new_panama-papers-8-trans4-linked");
            SmartObjectImageResizeSupportOrnegi("picture-frame-4-linked3");
            SmartObjectImageResizeSupportOrnegi("gorilla");

            // Bu örnek, akıllı nesne katmanları ile PSD dosyasını yeniden boyutlandırmayı gösterir.
            void SmartObjectImageResizeSupportOrnegi(string dosyaAdi)
            {
                const int oran = 4;
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + "Boyutlandır_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + "Boyutlandır_" + dosyaAdi + ".png";
                using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
                {
                    int yeniGenislik = resim.Width * oran;
                    int yeniYukseklik = resim.Height * oran;
                    resim.Resize(yeniGenislik, yeniYukseklik);
                    resim.Save(ciktiYolu, new PsdOptions(resim));
                    resim.Save(ciktiPngYolu, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanını yeniden boyutlandırmayı gösterir.
            SmartObjectLayerResizeSupportOrnegi("new_panama-papers-8-trans4-linked");
            SmartObjectLayerResizeSupportOrnegi("gorilla");

            // Bu örnek, PSD dosyasındaki akıllı nesne katmanını yeniden boyutlandırmayı gösterir.
            void SmartObjectLayerResizeSupportOrnegi(string dosyaAdi)
            {
                const double oran = 3.5;
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + "SonBoyutlandir_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + "SonBoyutlandir_" + dosyaAdi + ".png";
                using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
                {
                    var akıllıNesneKatmani = resim.Layers[resim.Layers.Length - 1];
                    int yeniGenislik = (int)(akıllıNesneKatmani.Width * oran);
                    int yeniYukseklik = (int)(akıllıNesneKatmani.Height * oran);
                    akıllıNesneKatmani.Resize(yeniGenislik, yeniYukseklik);
                    resim.Save(ciktiYolu, new PsdOptions(resim));
                    resim.Save(ciktiPngYolu, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanını kırpamayı gösterir.
            SmartObjectLayerCropSupportOrnegi("new_panama-papers-8-trans4-linked");
            SmartObjectLayerCropSupportOrnegi("gorilla");

            // Bu örnek, PSD dosyasındaki akıllı nesne katmanını kırpamayı gösterir.
            void SmartObjectLayerCropSupportOrnegi(string dosyaAdi)
            {
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + "SonCrop_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + "SonCrop_" + dosyaAdi + ".png";
                using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
                {
                    var akıllıNesneKatmani = resim.Layers[resim.Layers.Length - 1];
                    akıllıNesneKatmani.Crop(25, 15, 30, 10);
                    resim.Save(ciktiYolu, new PsdOptions(resim));
                    resim.Save(ciktiPngYolu, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanını kırpmayı gösterir.
            SmartObjectImageCropSupportOrnegi("new_panama-papers-8-trans4-linked");
            SmartObjectImageCropSupportOrnegi("gorilla");

            // Bu örnek, PSD dosyasını akıllı nesne katmanları ile kırpmayı gösterir.
            void SmartObjectImageCropSupportOrnegi(string dosyaAdi)
            {
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + "Kes_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + "Kes_" + dosyaAdi + ".png";
                using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
                {
                    resim.Crop(25, 10, 30, 5);
                    resim.Save(ciktiYolu, new PsdOptions(resim));
                    resim.Save(ciktiPngYolu, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Bu örnekte, Adobe® Photoshop® resmini akıllı nesne katmanları ile döndürmeyi ve yansıtmayı gösterir:
            SmartObjectImageRotateFlipSupportOrnegi("gorilla", RotateFlipType.Rotate90FlipNone);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            SmartObjectImageRotateFlipSupportOrnegi("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Bu örnek, PSD dosyasındaki akıllı nesne katmanlarını döndürmeyi ve yansıtmayı gösterir.
            void SmartObjectImageRotateFlipSupportOrnegi(string dosyaAdi, RotateFlipType döndürYansı)
            {
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + döndürYansı + "_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + döndürYansı + "_" + dosyaAdi + ".png";
                using (PsdImage resim = (PsdImage)Image.Load(dosyaYolu))
                {
                    resim.RotateFlip(döndürYansı);
                    resim.Save(ciktiYolu, new PsdOptions(resim));
                    resim.Save(ciktiPngYolu, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Bu örnek, Adobe® Photoshop® akıllı nesne katmanını döndürmeyi ve yansıtmayı gösterir.
            SmartObjectLayerRotateFlipSupportOrnegi("gorilla", RotateFlipType.Rotate90FlipNone);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            SmartObjectLayerRotateFlipSupportOrnegi("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Bu örnek, PSD dosyasındaki akıllı nesne katmanını döndürmeyi ve yansıtmayı gösterir.
            void SmartObjectLayerRotateFlipSupportOrnegi(string dosyaAdi, RotateFlipType döndürYansı)
            {
                string dosyaYolu = veriDizini + dosyaAdi + ".psd";
                string ciktiYolu = ciktiDizini + döndürYansı + "Son_" + dosyaAdi + ".psd";
                string ciktiPngYolu = ciktiDizini + döndürYansı + "Son_" + dosyaAdi + ".png";
