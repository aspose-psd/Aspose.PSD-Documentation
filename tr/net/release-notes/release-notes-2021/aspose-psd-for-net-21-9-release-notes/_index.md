---
title: Aspose.PSD için .NET 21.9 - Sürüm Notları
type: docs
weight: 40
url: /tr/net/aspose-psd-for-net-21-9-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD için .NET 21.9](https://www.nuget.org/packages/Aspose.PSD/) sürümü için sürüm notlarını içerir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-574|PSD Kaydetme işlemi için RLE Sıkıştırmasını Varsayılan Yaparak Büyük Çıkış PSD Dosyalarını Önleyin|Özellik|
|PSDNET-747|PSD Dosyasındaki çokkanallı renk modu ile Örtüşme Desen Katman Efektlerini Destekleme|Özellik|
|PSDNET-951|Yeni katman oluşturulduktan sonra kaynakları özellik null olan ve manipülasyonları engelleyen bir hata (Örneğin Yeniden Boyutlandırma)|Hata|
|PSDNET-955|8bit için Sıkıştırma yöntemleri ZipWithPrediction desteklenmemekte|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- Yok

# **Kaldırılan API'lar:**
- Yok

## **Kullanım örnekleri:**

**PSDNET-574. PSD Kaydetme işlemi için RLE Sıkıştırmasını Varsayılan Yaparak Büyük Çıkış PSD Dosyalarını Önleyin**

{{< highlight csharp >}}
            string inputFilePath = "dosya.psd";
            string output1 = "çıktı_orijinal.psd";
            string output2 = "çıktı_psdSecenekleri.psd";

            using (Image image = Image.Load(inputFilePath))
            {
                image.Save(output1);
                image.Save(output2, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-747. PSD Dosyasındaki çokkanallı renk modu ile Örtüşme Desen Katman Efektlerini Destekleme**

{{< highlight csharp >}}
            var dosyaAdı = "TümEfektler.psd";
            var çıktıDosyası = "TümEfektler_çıktı.psd";
            var yüklemeSeçenekleri = new PsdLoadOptions()
            {
                LoadEffectsResource = true
            };

            // Özel bir durum fırlatılmamalı
            using (var im = Image.Load(dosyaAdı, yüklemeSeçenekleri))
            {
                // Özel bir durum fırlatılmamalı
                im.Save(çıktıDosyası);
            }
{{< /highlight >}}

**PSDNET-951. Yeni katman oluşturulduktan sonra kaynakları özellik null olan ve manipülasyonları engelleyen bir hata (Örneğin Yeniden Boyutlandırma)**

{{< highlight csharp >}}
            string PSDDosyası = "Katman1.psd";
            string katman1Dosyası = "Katman2.png";
            string katman2Dosyası = "Katman3.png";
            string çıktıDosyaAdı = "sonçıktı.psd";

            void ReplaceColor(RasterImage image, Color eskiRenk, int fark, Color yeniRenk)
            {
                var pikseller = image.LoadArgb32Pixels(image.Bounds);
                var uzunluk = pikseller.Length;

                var eskiR = eskiRenk.R;
                var eskiG = eskiRenk.G;
                var eskiB = eskiRenk.B;
                var yeniRenkDeğeri = yeniRenk.ToArgb();

                for (int i = 0; i < uzunluk; i++)
                {
                    // Kırmızı
                    var r = (byte)((pikseller[i] >> 16) & 0xff);
                    // Yeşil
                    var g = (byte)((pikseller[i] >> 8) & 0xff);
                    // Mavi
                    var b = (byte)(pikseller[i] & 0xff);

                    int gerçekFark = Math.Abs(r - eskiR) + Math.Abs(g - eskiG) + Math.Abs(b - eskiB);

                    if (gerçekFark <= fark)
                    {
                        pikseller[i] = yeniRenkDeğeri;
                    }
                }

                image.SaveArgb32Pixels(image.Bounds, pikseller);
            }

            Layer Katman2 = null;
            Layer Katman3 = null;
            using (PsdImage image = (PsdImage)Image.Load(PSDDosyası))
            {
                #region Katman 1 Ekleme

                using (var stream = new FileStream(katman1Dosyası, FileMode.Open))
                {
                    Katman2 = new Layer(stream);

                    Katman2.Resize(image.Width, image.Height);
                    var genişlik = Katman2.Width;
                    var yükseklik = Katman2.Height;

                    Katman2.Left = 675;
                    Katman2.Top = 0;

                    Katman2.Right = Katman2.Left + genişlik;
                    Katman2.Bottom = Katman2.Top + yükseklik;

                    image.AddLayer(Katman2);
                }

                #endregion

                using (var stream = new FileStream(katman2Dosyası, FileMode.Open))
                {
                    Katman3 = new Layer(stream);
                    // Beyaz rengi Şeffaf olarak değiştirme
                    ReplaceColor(Katman3, Color.White, 256, Color.Transparent);
                    Katman2.DrawImage(new Point(0, 0), Katman3);
                }

                image.Save(çıktıDosyaAdı, new PsdOptions());
            }
{{< /highlight >}}

**PSDNET-955. 8bit için Sıkıştırma yöntemleri ZipWithPrediction desteklenmemekte**

{{< highlight csharp >}}
            string inputFilePath = "zipTest698.psd";
            string outputZip8 = "çıktı_Zip8bit.psd";
            string outputZip16 = "çıktı_Zip16bit.psd";

            using (PsdImage image = (PsdImage)Image.Load(inputFilePath))
            {
                image.Save(outputZip8, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 8 });
                image.Save(outputZip16, new PsdOptions() { CompressionMethod = CompressionMethod.ZipWithPrediction, ChannelBitsCount = 16 });
            }
{{< /highlight >}}
