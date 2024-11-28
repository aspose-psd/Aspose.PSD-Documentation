---
title: Aspose.PSD for .NET 21.4 - Sürüm Notları
type: docs
weight: 90
url: /tr/net/aspose-psd-for-net-21-4-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 21.4](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-259|Desen Üzerine Görünüm Katmanı Etkinin Render Edilmesi|Özellik|
|PSDNET-861|PSD Görüntüsündeki Vektör Yolları olan şekil katmanlarının yeniden boyutlandırılmasını desteklemek için bilinmeyen Vogk kaynak özelliklerinin eklenmesi|Özellik|
|PSDNET-90|PSD uygun şekilde PDF'ye dönüştürülmedi|Hata|
|PSDNET-830|Belirli PSD dosyasının metin katmanlarıyla kaydedilmesi sırasında istisna oluşturulması|Hata (Daha önceden düzeltildi)

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.OriginBoxCorners
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.Transform
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsOriginBoxCornersPresent
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeOriginSettings.IsTransformPresent
- T:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform
- M:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.#ctor
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Xy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Yy
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Tx
- P:Aspose.PSD.FileFormats.Core.VectorPaths.VectorShapeTransform.Ty

# **Kaldırılan API'lar:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDNET-90. PSD uygun şekilde PDF'ye dönüştürülmedi**

{{< highlight csharp >}}
            string srcFile = "psd_magical.psd";
            string outputJpg = "output.jpg";
            string outputPdf = "output.pdf";

            using (var psdImage = (PsdImage)Image.Load(srcFile))
            {
                JpegOptions jpgOptions = new JpegOptions();
                PdfOptions pdfOptions = new PdfOptions();

                psdImage.Save(outputJpg, jpgOptions);
                psdImage.Save(outputPdf, pdfOptions);
            }
{{< /highlight >}}

**PSDNET-259. Desen Üzerine Görünüm Katmanı Etkisinin Render Edilmesi**

{{< highlight csharp >}}
            string sourceFile = "patternIleResim.psd";
            string outputFile = "output.png";

            using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
            {
                image.Save(outputFile, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-861. PSD görüntüsünde vektör yolları olan şekil katmanlarının yeniden boyutlandırılmasını desteklemek için bilinmeyen Vogk kaynak özelliklerinin eklenmesi**

{{< highlight csharp >}}
            // Bu örnek, PSD dosyasındaki Vogk kaynağında Şekil Başlangıç Ayarları'nın yeni Dönüş ve Köşe Köşeleri özelliklerini alma ve ayarlama şeklini gösterir
            string sourceFileName = Path.Combine("PSDNET861_1", "vektörŞekil_25_50.psd");
            string çıktıYolu = Path.Combine("PSDNET861_1", "sonuç.psd");

            VectorShapeOriginSettings orijinalAyar;
            const int katmanIndeksi = 0;

            // Orijinal görüntüyü yükle
            using (PsdImage görüntü = (PsdImage)Image.Load(sourceFileName)) 
            {
                AssertIsTrue(katmanIndeksi < görüntü.Katmanlar.Uzunluk);
                var katman = görüntü.Katmanlar[katmanIndeksi];
                AssertIsTrue(katman is DoldurKatmanı);
                var kaynak = GetVogkKaynağı((DoldurKatmanı)katman);
                AssertAreEqual(1, kaynak.ŞekilBaşlangıçAyarları.Uzunluk);

                // Okuduktan sonra doğrula
                var ayar = kaynak.ŞekilBaşlangıçAyarları[0];
                AssertAreEqual(false, ayar.HatalıŞekilMıVarPresent);
                AssertAreEqual(false, ayar.BaşlangıçRadyanKöşeleriPresent);
                AssertAreEqual(true, ayar.BaşlangıçİndexiPresent);
                AssertAreEqual(0, ayar.Başlangıçİndexi);
                AssertAreEqual(true, ayar.BaşlangıçTipiPresent);
                AssertAreEqual(5, ayar.BaşlangıçTipi);
                AssertAreEqual(true, ayar.BaşlangıçŞekilBBoxPresent);
                AssertAreEqual(Rectangle.FromLeftTopRightBottom(3, 7, 10, 22), ayar.BaşlangıçŞekilKutusu.Sınırlar);
                AssertAreEqual(true, ayar.BaşlangıçÇözünürlükPresent);
                AssertAreEqual(300d, ayar.BaşlangıçÇözünürlük);

                // Yeni özellikleri doğrula
                AssertAreEqual(true, ayar.DönüşPresent);
                AssertAreEqual(0d, ayar.Dönüş.Tx);
                AssertAreEqual(0d, ayar.Dönüş.Ty);
                AssertAreEqual(0.050000000000000003d, ayar.Dönüş.Xx);
                AssertAreEqual(0d, ayar.Dönüş.Yx);
                AssertAreEqual(0d, ayar.Dönüş.Xy);
                AssertAreEqual(0.1d, ayar.Dönüş.Yy);
                AssertAreEqual(true, ayar.KöşeKöşeleriPresent);
                AssertAreEqual(2.9000000000000004d, ayar.KöşeKöşeleri[0]);
                AssertAreEqual(7.3000000000000007d, ayar.KöşeKöşeleri[1]);
                AssertAreEqual(10.450000000000001d, ayar.KöşeKöşeleri[2]);
                AssertAreEqual(7.3000000000000007d, ayar.KöşeKöşeleri[3]);
                AssertAreEqual(10.450000000000001d, ayar.KöşeKöşeleri[4]);
                AssertAreEqual(22.400000000000002d, ayar.KöşeKöşeleri[5]);
                AssertAreEqual(2.9000000000000004d, ayar.KöşeKöşeleri[6]);
                AssertAreEqual(22.400000000000002d, ayar.KöşeKöşeleri[7]);

                // Yeni özellikleri ayarla
                orijinalAyar = kaynak.ŞekilBaşlangıçAyarları[0];
                orijinalAyar.Dönüş.Tx = 0.2d;
                orijinalAyar.Dönüş.Ty = 0.3d;
                orijinalAyar.Dönüş.Xx = 0.4d;
                orijinalAyar.Dönüş.Xy = 0.5d;
                orijinalAyar.Dönüş.Yx = 0.6d;
                orijinalAyar.Dönüş.Yy = 0.7d;
                orijinalAyar.KöşeKöşeleri = new double[8] { 9, 8, 7, 6, 5, 4, 3, 2 };

                // Bu değiştirilmiş özelliklere sahip PSD görüntüsünü kaydet
                görüntü.Save(çıktıYolu, new PsdOptions(görüntü));
            }

            // Değiştirilmiş özelliklere sahip kaydedilmiş PSD görüntüsünü yükle
            using (PsdImage görüntü = (PsdImage)Image.Load(çıktıYolu))
            {
                var katman = görüntü.Katmanlar[katmanIndeksi];
                AssertIsTrue(katman is DoldurKatmanı);
                var kaynak = GetVogkKaynağı((DoldurKatmanı)katman);
                AssertAreEqual(1, kaynak.ŞekilBaşlangıçAyarları.Uzunluk);

                // Özelliklerin doğru şekilde kaydedildiğini ve yüklendiğini doğrula 
                var ayar = kaynak.ŞekilBaşlangıçAyarları[0];
                AssertAreEqual(true, ayar.BaşlangıçİndexiPresent);
                AssertAreEqual(false, ayar.HatalıŞekilMıVarPresent);
                AssertAreEqual(true, ayar.BaşlangıçÇözünürlükPresent);
                AssertAreEqual(true, ayar.BaşlangıçTipiPresent);
                AssertAreEqual(true, ayar.BaşlangıçŞekilBBoxPresent);
                AssertAreEqual(false, ayar.BaşlangıçRadyanKöşeleriPresent);
                AssertAreEqual(0, ayar.Başlangıçİndexi);
                AssertAreEqual(true, ayar.DönüşPresent);
                AssertAreEqual(0.2d, ayar.Dönüş.Tx);
                AssertAreEqual(0.3d, ayar.Dönüş.Ty);
                AssertAreEqual(0.4d, ayar.Dönüş.Xx);
                AssertAreEqual(0.5d, ayar.Dönüş.Xy);
                AssertAreEqual(0.6d, ayar.Dönüş.Yx);
                AssertAreEqual(0.7d, ayar.Dönüş.Yy);
                AssertAreEqual(true, ayar.KöşeKöşeleriPresent);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[0], ayar.KöşeKöşeleri[0]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[1], ayar.KöşeKöşeleri[1]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[2], ayar.KöşeKöşeleri[2]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[3], ayar.KöşeKöşeleri[3]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[4], ayar.KöşeKöşeleri[4]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[5], ayar.KöşeKöşeleri[5]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[6], ayar.KöşeKöşeleri[6]);
                AssertAreEqual(orijinalAyar.KöşeKöşeleri[7], ayar.KöşeKöşeleri[7]);
            }

            VogkKaynağı GetVogkKaynağı(DoldurKatmanı katman)
            {
                if (katman == null)
                {
                    throw new PsdImageArgumentException("Parametre katman boş olmamalıdır.");
                }

                VogkKaynağı kaynak = null;
                var kaynaklar = katman.Kaynaklar;
                for (int i = 0; i < kaynaklar.Uzunluk; i++)
                {
                    if (kaynaklar[i] is VogkKaynağı)
                    {
                        kaynak = (VogkKaynağı)kaynaklar[i];
                        break;
                    }
                }

                if (kaynak == null)
                {
                    throw new PsdImageException("VogkKaynağı bulunamadı.");
                }

                return kaynak;
            }

            void AssertIsTrue(bool şart)
            {
                if (!şart)
                {
                    throw new FormatException(string.Format("Beklenen doğru"));
                }
            }

            void AssertAreEqual(nesne gerçek, nesne beklenen)
            {
                if (!nesne.Equals(gerçek, beklenen))
                {
                    throw new FormatException(string.Format("Gerçek değer {0}, beklenen {1} ile eşit değil.", gerçek, beklenen));
                }
            }
{{< /highlight >}}