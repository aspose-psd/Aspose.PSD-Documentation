---
title: Aspose.PSD for .NET 18.8 - Sürüm Notları
type: docs
weight: 50
url: /tr/net/aspose-psd-for-net-18-8-release-notes/
---

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-68|KatmanOluşturmaTarihözelliğinin Desteklenmesi|Özellik|
|PSDNET-67|SheetColor Vurgulama Desteklenmesi|Özellik|
|PSDNET-66|Katmanların Birbirine Birleştirme Yeteneği|Özellik|
|PSDNET-65|Metin Katmanı BoundBox Özelliğinin Kısmi Destek Eklenmesi|Özellik|
|PSDNET-64|IopaResource Desteğinin Eklenmesi|Özellik|
|PSDNET-56|PSD Biçimi İçin Katman Efektlerinin Desteklenmesi|Özellik|
|PSDNET-55|.Net İçin InterruptMonitor Desteği|Özellik|
|PSDNET-50|Katmanları Düzleştirmek İçin Olasılık Oluşturulması|Özellik|
|PSDNET-49|Katmanlarda Dolgu Opaklığı Özelliğinin Yeniden Olarak Eklenmesi|Özellik|
|PSDNET-43|Curves Ayar Katmanı Rendere Etme Uygulaması|Özellik|
|PSDNET-42|Curves Ayar Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-41|Levels Ayar Katmanı Rendere Etme Uygulaması|Özellik|
|PSDNET-40|Levels Ayar Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-37|Channel Mixer Ayar Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-35|Renk Tonu / Doyma Ayarlama Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-34|Maruz Kalma Ayar Katmanı İhracı İçin Uygulama|Özellik|
|PSDNET-31|ChannelMixer Ayarlama Katmanını İhracat İçin Desteğin Eklenmesi|Özellik|
|PSDNET-26|Kırpma Maskesi Desteğinin Eklenmesi|Özellik|
|PSDNET-13|Katman Maskesi Desteğinin Eklenmesi|Özellik|
|PSDNET-9|Fotograf Filtre Ayarlama Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-8|Channel Mixer Ayar Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-7|Maruz Kalma Ayar Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-6|Parlaklık / Kontrast Ayarlama Katmanı Desteğinin Eklenmesi|Özellik|
|PSDNET-5|Düzeltmeler Katmanlarına Kısmi Destek Eklenmesi|Özellik|
|PSDNET-3|PSD NoBreak metin seçeneği desteğinin eklenmesi|Özellik|
|PSDNET-2|Çalışma Zamanında Metin Katmanı Ekleme Yeteneği|Özellik|
|PSDNET-62|TIFF Codec'un 16-bit kanal görüntüsünü kaydedememesi|Geliştirme|
|PSDNET-61|PSD görüntüsünün geçersiz renkler üretmesi|Geliştirme|
|PSDNET-60|Sol üst köşe koordinatı güncellemesinde hata|Geliştirme|
|PSDNET-59|Metin katmanlarını güncelleme sırasında hata|Geliştirme|
|PSDNET-58|JPEG2000 görüntüsünün Codec özelliğinin kamuya açılması|Geliştirme|
|PSDNET-57|24bpp seçeneklerinin BMP'ye ihracat için düzeltilmesi|Geliştirme|
|PSDNET-46|CMYK PSD dönüşümü sırasında Ayar Katmanının göz ardı edilmesi|Geliştirme|

## **Kullanım Örnekleri:**

**PSDNET-68 KatmanOluşturmaTarihözelliğinin Desteklenmesi**

{{< highlight java >}}

 // KatmanOluşturmaTarihözelliğinin kullanım örneği

string kaynakDosyaAdı = "OneLayer.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var katman = im.Layers[0];

    var oluşturmaTarih = katman.LayerCreationDateTime;

    var beklenenTarih = new DateTime(2018, 7, 17, 8, 57, 24, 769);

    Assert.AreEqual(beklenenTarih, oluşturmaTarih);

    var şimdi = DateTime.Now;

    var oluşturulanKatman = im.AddLevelsAdjustmentLayer();

    // Yeni oluşturulan katmanlarda Oluşturma Tarihini kontrol et

    Assert.True(şimdi <= oluşturulanKatman.LayerCreationDateTime);

}

{{< /highlight >}}

**PSDNET-67 SheetColor Vurgulama Desteklenmesi**

{{< highlight java >}}

 // SheetColorHighlight özelliği örnek kullanımı

string kaynakDosyaAdı = "SheetColorHighlightExample.psd";

string ihraçYolu = "SheetColorHighlightExampleChanged.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var katman1 = im.Layers[0];

    Assert.AreEqual(SheetColorHighlightEnum.Violet, katman1.SheetColorHighlight);

    var katman2 = im.Layers[1];

    Assert.AreEqual(SheetColorHighlightEnum.Orange, katman2.SheetColorHighlight);



    katman1.SheetColorHighlight = SheetColorHighlightEnum.Yellow;



    im.Save(ihraçYolu);	

}

{{<highlight java >}}

**PSDNET-66 Katmanları Birbirine Birleştirme Yeteneği**

{{< highlight java >}}

 // İki katmanı birleştirme örneği

var kaynakDosya1 = "FillOpacitySample.psd";

var kaynakDosya2 = "ThreeRegularLayersSemiTransparent.psd";

var ihraçYolu = "TwoDifferentPsdMergedLayers.psd" 

using (var im1 = (PsdImage)(Image.Load(kaynakDosya1))

{

    var katman1 = im1.Layers[1];

    using (var im2 = (PsdImage)(Image.Load(kaynakDosya2))

    {

        var katman2 = im2.Layers[0];

        katman1.MergeLayerTo(katman2);

	im2.Save(ihraçYolu);	

    }

}

{{< /highlight >}}

**PSDNET-65 Metin Katmanı BoundBox Özelliğinin Kısmi Destek Eklenmesi**

{{< highlight java >}}

 // Metin BoxBounds Örneği

string kaynakDosyaAdı = "LayerWithText.psd";

var doğruOptikBoyut = new Size(127, 45);

var doğruSınırlayıcıKutu = new Size(172, 62);

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var metinKatmanı = (TextLayer)im.Layers[1];

    // Katmanın boyutu, render edilen alanın boyutudur

    var optikBoyut = metinKatmanı.Size;

    Assert.AreEqual(doğruOptikBoyut, optikBoyut);

    // TextBoundBox, Metin Katmanı için maksimum katman boyutudur. 

    // Bu alanda PS metninizi sığdırmaya çalışacaktır.

    var sınırlayıcıKutu = metinKatmanı.TextBoundBox;

    Assert.AreEqual(doğruSınırlayıcıKutu, sınırlayıcıKutu);

}

{{< /highlight >}}

**PSDNET-64 IopaResource Desteğinin Eklenmesi**

{{< highlight java >}}

 // Fill Opacity özelliğini IopaResource değişikliği ile değiştirme

string kaynakDosyaAdı = "FillOpacitySample.psd";

string ihraçYolu = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var katman = im.Layers[2];



    var kaynaklar = katman.Resources;

    foreach (var kaynak in kaynaklar)

    {

        if (kaynak is IopaResource)

        {

            var iopaKaynak = (IopaResource)kaynak;

            iopaKaynak.FillOpacity = 200;

        }

    }



    im.Save(ihraçYolu);	

}

{{< /highlight >}}

**PSDNET-56 PSD Biçimi İçin Katman Efektlerinin Desteklenmesi**

{{< highlight java >}}

 using (

    PsdImage görüntü =

        (PsdImage)

        Aspose.PSD.Image.Load(

            kaynakDosyaAdı,

            new Aspose.PSD.ImageLoadOptions.PsdLoadOptions()

            {

                LoadEffectsResource = true,

                UseDiskForLoadEffectsResource = true

            }))

{

    image.Save(

                çıktı,

                new Aspose.PSD.ImageOptions.PngOptions()

                {

                    ColorType =

                            Aspose.PSD.FileFormats.Png

                            .PngColorType

                            .TruecolorWithAlpha

                });

}

{{< /highlight >}}

**PSDNET-55 .Net İçin InterruptMonitor Desteği**

{{< highlight java >}}

         public void InterruptMonitorTest(string dizin, string çıktıDizin)

        {

            ImageOptionsBase kaydetmeSeçenekleri = new ImageOptions.PngOptions();

            Multithreading.InterruptMonitor monitor = new Multithreading.InterruptMonitor();

            SaveImageWorker worker = new SaveImageWorker(dizin + "büyük.psb", dizin + "büyük_dışa.png", kaydetmeSeçenekleri, monitor);

            System.Threading.Thread thread = new System.Threading.Thread(new System.Threading.ThreadStart(worker.ThreadProc));

            try

            {

                thread.Start();

                // Geçerli bir resmin tam dönüşüm süresinden daha kısa bir sürede olmalı.

                System.Threading.Thread.Sleep(3000);

                // İşlemi kes

                monitor.Interrupt();

                System.Console.WriteLine("Kaydetme iş parçası #{0}'ü {1}'de kes", thread.ManagedThreadId, System.DateTime.Now);

                // Kesilmiş işlemi bekleyin...

                thread.Join();

            }

            finally

            {

                // Silinecek dosya mevcut değilse, hiçbir istisna fırlatılmaz.

                System.IO.File.Delete(dizin + "büyük_dışa.png");

            }

        }

        /// <summary>

        /// Resmin dönüşümünü başlatır ve kesilmesini bekler.

        /// </summary>

        private class SaveImageWorker

        {

            /// <summary>

            /// Giriş resminin yolu.

            /// </summary>

            private readonly string girişYolu;

            /// <summary>

            /// Çıkış resminin yolu.

            /// </summary>

            private readonly string çıkışYolu;

            /// <summary>

            /// Kesme monitörü.

            /// </summary>

            private readonly Multithreading.InterruptMonitor monitor;

            /// <summary>

            /// Kaydetme seçenekleri.

            /// </summary>

            private readonly ImageOptionsBase kaydetmeSeçenekleri;

            /// <summary>

            /// <see cref="SaveImageWorker"/> sınıfının yeni bir örneğini başlatır.

            /// </summary>

            /// <param name="girişYolu">Giriş resminin yolu.</param>

            /// <param name="çıkışYolu">Çıkış resminin yolu.</param>

            /// <param name="kaydetmeSeçenekleri">Kaydetme seçenekleri.</param>

            /// <param name="monitor">Kesme monitörü.</param>

            public SaveImageWorker(string girişYolu, string çıkışYolu, ImageOptionsBase kaydetmeSeçenekleri, Multithreading.InterruptMonitor monitor)

            {

                this.girişYolu = girişYolu;

                this.çıkışYolu = çıkışYolu;

                this.kaydetmeSeçenekleri = kaydetmeSeçenekleri;

                this.monitor = monitor;

            }

            /// <summary>

            /// Basit bir formattan diğerine resim dönüştürmeyi deneme. Kesintiyi işler. 

            /// </summary>

            public void ThreadProc()

            {

                using (Image image = Image.Load(this.girişYolu))

                {

                    Multithreading.InterruptMonitor.ThreadLocalInstance = this.monitor;

                    try

                    {

                        image.Save(this.çıkışYolu, this.kaydetmeSeçenekleri);

                        Assert.Fail("Kesinti bekleniyor.");

                    }

                    catch (CoreExceptions.OperationInterruptedException e)

                    {

                        System.Console.WriteLine("Dışa kaydetme iş parçası #{0} {1}'de bitirir", System.Threading.Thread.CurrentThread.ManagedThreadId, System.DateTime.Now);

                        System.Console.WriteLine(e);

                    }

                    catch (System.Exception e)

                    {

                        System.Console.WriteLine(e);

                    }

                    finally

                    {

                        Multithreading.InterruptMonitor.ThreadLocalInstance = null;

                    }

                }

            }

        }

{{< /highlight >}}

**PSDNET-50 Katmanları Düzleştirmek İçin Olasılık Oluşturması**

{{< highlight java >}}

 // Tüm PSD'yi düzleştir

string kaynakDosyaAdı = "ThreeRegularLayersSemiTransparent.psd";

string ihraçYolu = "ThreeRegularLayersSemiTransparentDüzleştirilmiş.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    im.FlattenImage();

    im.Save(ihraçYolu);	 

}

// Bir katmanı başka birine birleştir

string kaynakDosyaAdı = "ThreeRegularLayersSemiTransparent.psd";

string ihraçYolu = "ThreeRegularLayersSemiTransparentKatmanKatman.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var altKatman = im.Layers[0];

    var ortaKatman = im.Layers[1];

    var üstKatman = im.Layers[2];

    var katman1 = im.MergeLayers(altKatman, ortaKatman);

    var katman2 = im.MergeLayers(katman1, üstKatman);

    // Birleştirilmiş katmanları ayarla

    im.Layers = new Layer[] { katman2 };

    im.Save(ihraçYolu);	 

}

{{< /highlight >}}

**PSDNET-49 Katmanlarda Dolgu Opaklığı Özelliğinin Yeniden Olarak Eklenmesi**

{{< highlight java >}}

 // Dolgu Opaklığı özelliğini değiştirme

string kaynakDosyaAdı = "FillOpacitySample.psd";

string ihraçYolu = "FillOpacitySampleChanged.psd";

using (var im = (PsdImage)(Image.Load(kaynakDosyaAdı))

{

    var katman = im.Layers[2];

    katman.FillOpacity = 5;

    im.Save(ihraçYolu);	

}

{{< /highlight >}}

**PSDNET-43 Curves Ayar Katmanı Rendere Etme Uygulaması**

{{< highlight java >}}

 // Curves katmanı düzenleme

string kaynakDosyaAdı = "CurvesAdjustmentLayer";

string psdDizinSonraDüzeltme = "CurvesAdjustmentLayerDeğişmiş";

string pngİhracDizin = "CurvesAdjustmentLayerDeğişmiş";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(kaynakDosyaAdı + j.ToString() + ".psd"))

    {

        foreach (var katman in im.Layers)

	{

            if (katman is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)katman;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var yönetici = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           yönetici.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var yönetici = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      yönetici.AddCurvePoint(0, 50, 100);

                      yönetici.AddCurvePoint(0, 150, 130);

                 }

            }

        }

    }



    // PSD'yi Kaydet

    im.Save(psdDizinSonraDüzeltme + j.ToString() + ".psd");



    // PNG'yi Kaydet

    var kaydetmeSeçenekleri = new PngOptions();

    kaydetmeSeçenekleri.ColorType = PngColorType.TruecolorWithAlpha;

    im.Save(pngİhracDizin + j.ToString() + ".png", kaydetmeSeçenekleri);

}

{{< /highlight >}}

**PSDNET-42 Curves Ayar Katmanı Desteğinin Eklenmesi**

{{< highlight java >}}

 // Curves katmanı düzenleme

string kaynakDosyaAdı = "CurvesAdjustmentLayer";

string psdDizinSonraDüzeltme = "CurvesAdjustmentLayerDeğişmiş";

for (int j = 1; j < 2; j++)

{

    using (var im = LoadFile(kaynakDosyaAdı + j.ToString() + ".psd"))

    {

         foreach (var katman in im.Layers)

	 {

            if (katman is CurvesLayer)

            {

                 var curvesLayer = (CurvesLayer)katman;

                 if (curvesLayer.IsDiscreteManagerUsed)

                 {

                      var yönetici = (CurvesDiscreteManager)curvesLayer.GetCurvesManager();

                      for (int i = 10; i < 50; i++)

                      {

                           yönetici.SetValueInPosition(0, (byte)i, (byte)(15 + (i * 2));

                      }

                 }

                 else

                 {

                      var yönetici = (CurvesContinuousManager)curvesLayer.GetCurvesManager();

                      yönetici.AddCurvePoint(0, 50, 100);

                      yönetici.AddCurvePoint(0, 150, 130);

                 }

            }

	}

    }



    // PSD'yi Kaydet

    im.Save(psdDizinSonraDüzeltme + j.ToString() + ".psd");

}

{{< /highlight >}}