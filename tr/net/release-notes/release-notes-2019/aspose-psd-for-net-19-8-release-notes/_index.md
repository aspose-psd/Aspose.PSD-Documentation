---
title: Aspose.PSD’in .NET 19.8 Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-19-8-release-notes/
---

{{% alert color="primary" %}}

Bu sayfa, Aspose.PSD'in .NET 19.8 sürümü için sürüm notlarını içerir.

{{% /alert %}}

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-184|JPEG, PNG ve diğer görüntü dosyalarını akıştan PsdImage'e yükleme|Özellik|
|PSDNET-134|Doldurma Katmanının Renderini Uygulama: Gradyan|Özellik|
|PSDNET-166|PSD'yi PDF olarak kaydetmek seçilebilir metin sağlamaz|Özellik|
|PSDNET-158|PSB'yi PDF olarak kaydetmeyi destekleme|Özellik|
|PSDNET-189|Salt Okunur Modda PSD'nin yüklenmesinde yüksek bellek kullanımı|Geliştirme|
|PSDNET-171|Yeni TextLayer oluşturulduktan sonra, PSD dosyası PS için okunamaz hale geldi|Hata|
|PSDNET-156|PSD yüklemede istisna oluştu|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(System.IO.Stream)
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage,System.Boolean)
# **Kaldırılan API'ler:**
- M:Aspose.PSD.FileFormats.Psd.Layers.Layer.#ctor(Aspose.PSD.RasterImage)

## **Kullanım örnekleri:**
**PSDNET-184. JPEG, PNG ve diğer görüntü dosyalarını akıştan PsdImage'e yükleme**

{{< highlight java >}}

    // JPEG, PNG ve diğer görüntü dosyalarını akıştan PsdImage'e yükleme

    string outputFilePath = "PsdSonucu.psd";

    var filesList = new string[]

    {

        "OrnekPsd.psd",

        "OrnekBmp.bmp",

        "OrnekGif.gif",

        "OrnekJpeg2000.jpf",

        "OrnekJpeg.jpg",

        "OrnekPng.png",

        "OrnekTiff.tif",

    };

    using (var image = new PsdImage(200, 200))

    {

        foreach (var fileName in filesList)

        {

            string filePath = fileName;

            using (var stream = new FileStream(filePath, FileMode.Open))

            {

                Layer layer = null;

                try

                {

                     layer = new Layer(stream);

                     image.AddLayer(layer);

                }

                catch (Exception e)

                {

                    if (layer != null)

                    {

                        layer.Dispose();

                    }

                    throw e;

                }

            }

        }

        image.Save(outputFilePath);

    }

{{< /highlight >}}

**PSDNET-134. Doldurma Katmanının Renderini Uygulama: Gradyan**

{{< highlight java >}}

             // Doldurma Katmanının Renderini Uygulama: Gradyan

            string dosyaAdi = "DoldurmaKatmanGradyan.psd";

            GradientType[] gradyanTipleri = new[]

            {

                GradientType.Linear, GradientType.Radial, GradientType.Angle, GradientType.Reflected, GradientType.Diamond

            };

            using (var image = Image.Load(dosyaAdi))

            {

                PsdImage psdImage = (PsdImage)image;

                FillLayer fillLayer = (FillLayer)psdImage.Layers[0];

                GradientFillSettings fillSettings = (GradientFillSettings)fillLayer.FillSettings;

                foreach (var gradientType in gradyanTipleri)

                {

                    fillSettings.GradientType = gradientType;

                    fillLayer.Update();

                    psdImage.Save(dosyaAdi + "_" + gradientType.ToString() + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

                }

            }

{{< /highlight >}}

**PSDNET-166. PSD'yi PDF olarak kaydetmek seçilebilir metin sağlamaz**

{{< highlight java >}}

  // PSD'yi PDF olarak kaydetmek seçilebilir metin sağlamaz

    string kaynakDosyaAdi = "metin.psd";

    using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdi))

    {

        string ciktiDosyaAdi = "metin.pdf";

        image.Save(ciktiDosyaAdi, new PdfOptions());

    }

{{< /highlight >}}

**PSDNET-171. Yeni TextLayer oluşturulduktan sonra, PSD dosyası PS için okunamaz hale geldi**

{{< highlight java >}}

 // Yapı Sunucusunda yeni TextLayer oluşturulduktan sonra, PSD Dosyası PS için okunamaz hale geldi

    string kaynakDosyaAdi = "BirKatman.psd";

    string ciktiDosyaAdi = "MetinEklenmisBirKatman.psd";

    using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdi))

    {

        image.AddTextLayer("Bazı metin", new Rectangle(50, 50, 100, 100));

        PsdOptions secenekler = new PsdOptions(image);

        image.Save(ciktiDosyaAdi, secenekler);

    }

{{< /highlight >}}

**PSDNET-156. PSD yüklemede istisna oluştu**

{{< highlight java >}}

 using (var image = Image.Load("izole_Kopya.psd"))

{

}

{{< /highlight >}}

**PSDNET-189. Salt Okunur Modda PSD'nin yüklenmesinde yüksek bellek kullanımı**

{{< highlight java >}}

 // Salt Okunur Modda PSD'nin yüklenmesinde Aspose.PSD'nin yüksek bellek kullanımı

            string kaynakDosyaAdi = "Beyaz 3D Metin Efekti.psd";

            string ciktiDosyaAdi = "DışaAktarilan.png";

            LoadOptions yuklemeSecenekleri = new PsdLoadOptions() { ReadOnlyMode = true };

            ImageOptionsBase kaydetmeSecenekleri = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

            using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdi))

            {

                image.Save(ciktiDosyaAdi, kaydetmeSecenekleri);

            }

            double kullanilanBellek = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

            // Bu örnekler için bellek kullanımı 100 MB'den az olmalı

            if (kullanilanBellek > 100)

            {

                throw new Exception("Bellek kullanımı çok fazla");

            }

{{< /highlight >}}

**PSDNET-158. PSB'yi PDF olarak kaydetmeyi destekleme**

{{< highlight java >}}

 // PSB'yi PDF olarak kaydetmeyi destekleme

    string kaynakDosyaAdi = "ornek.psb";

    using (PsdImage image = (PsdImage)Image.Load(kaynakDosyaAdi))

    {

        string ciktiDosyaAdi = "ornek.pdf";

        image.Save(ciktiDosyaAdi, new PdfOptions());

    }

{{< /highlight >}}
