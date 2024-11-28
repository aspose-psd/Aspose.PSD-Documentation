---
title: Aspose.PSD for .NET 19.12 - Sürüm Notları
type: docs
weight: 10
url: /tr/net/aspose-psd-for-net-19-12-release-notes/
---

{{% alert color="primary" %}} 

Bu sayfa, [Aspose.PSD for .NET 19.12](https://www.nuget.org/packages/Aspose.PSD/) için sürüm notlarını içermektedir.

{{% /alert %}} 

|**Anahtar**|**Özet**|**Kategori**|
| :- | :- | :- |
|PSDNET-11|[Bağlantılı Katman Desteği](/psd/tr/net/working-with-layers/#workingwithlayers-supportoflinkedlayers)|Özellik|
|PSDNET-131|[SoCoResource Desteği](/psd/tr/net/support-of-socoresource/)|Özellik|
|PSDNET-115|Metin Katmanı bir dize ile güncellendiği zaman mevcut Satır Sonlarına Satır Sonları eklenmektedir|Hata|
|PSDNET-157|PSB olarak kaydetme sırasında PNG'in donması|Hata|
|PSDNET-250|RLE sıkıştırması olan katmansız CMYK PSD dosyasının yüklenirken istisna alınması|Hata|
|PSDNET-161|Metin katmanları güncellenirken istisna alınması|Hata|
|PSDNET-222|Katman maskeleri olan bazı PSD dosyalarının yanlış işlenmesi|Hata|
|PSDNET-244|Belirli Globalization.CultureInfo.CurrentCulture ile PSD kaydetme işlemi yapılırsa yükleme sırasında istisnaların alınması|Hata|

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.FileFormats.Psd.PsdImage.LinkedLayersManager
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskDataFull.UserMaskData
- T:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.LinkLayers(Aspose.PSD.FileFormats.Psd.Layers.Layer[])
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.UnlinkLayer(Aspose.PSD.FileFormats.Psd.Layers.Layer)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLayersByLinkGroupId(System.Int16)
- M:Aspose.PSD.FileFormats.Psd.Layers.LinkedLayersManager.GetLinkGroupId(Aspose.PSD.FileFormats.Psd.Layers.Layer)

# **Kaldırılan API'lar:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerMaskData.ImageDataVector

## **Kullanım örnekleri:**
**PSDNET-11. Bağlantılı Katman Desteği**

{{< highlight java >}}

           using (var psd = (PsdImage)Image.Load("ornek.psd"))

            {

                Layer[] layers = psd.Layers;

                // tüm katmanları bir bağlantılı grup içinde bağlayın

                short layersLinkGroupId = psd.LinkedLayersManager.LinkLayers(layers);

                // bir katman için kimlik alın

                short linkGroupId = psd.LinkedLayersManager.GetLinkGroupId(layers[0]);

                if (layersLinkGroupId != linkGroupId)

                {

                    throw new Exception("layersLinkGroupId ve linkGroupId eşit değil.");

                }

                // belirli link grup kimliği ile tüm bağlantılı katmanlar alın.

                Layer[] linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                // her katmanı gruptan bağlantısız hale getir

                foreach (var linkedLayer in linkedLayers)

                {

                    psd.LinkedLayersManager.UnlinkLayer(linkedLayer);

                }

                // grupta hiç katman olmayan bir link grubu kimliği için NULL al

                linkedLayers = psd.LinkedLayersManager.GetLayersByLinkGroupId(linkGroupId);

                if (linkedLayers != null)

                {

                    throw new Exception("linkedLayers alanı NULL değil.");

                }

                psd.Save("psdnet11_output.psd");

            }

{{< /highlight >}}

**PSDNET-131. SoCoResource Desteği**

{{< highlight java >}}

      // SoCoResource Desteği

    string sourceFileName = "RenkDolguKatmanı.psd";

    string exportPath = "SoCoResource_Düzenlenmiş.psd";

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

        foreach (var layer in im.Layers)

        {

            if (layer is FillLayer)

            {

                var fillLayer = (FillLayer)layer;

                foreach (var resource in fillLayer.Resources)

                {

                    if (resource is SoCoResource)

                    {

                        var socoResource = (SoCoResource)resource;

                        Assert.AreEqual(Color.FromArgb(63, 83, 141), socoResource.Color);

                        socoResource.Color = Color.Red;

                        break;

                    }

                 }

                 break;

             }

            im.Save(exportPath);

        }

    }

{{< /highlight >}}

**PSDNET-115. Metin Katmanı bir dize ile güncellendiği zaman mevcut Satır Sonlarına Satır Sonları eklenmektedir**

{{< highlight java >}}

           const string YeniMetin = "abcdef\rzxcvbn";

        string kaynakDosyaYolu = "AsyaKarakterleriIçinTestDosyası.psd";

        string çıktıDosyaYolu = "sonuç.psd";

        using (var görüntü = (PsdImage)Image.Load(kaynakDosyaYolu))

        {

            var katman = (TextLayer)görüntü.Layers[0];

            var görüntüSeçenekleri = new PsdOptions(görüntü);

            katman.UpdateText(YeniMetin);

            görüntü.Save(çıktıDosyaYolu, görüntüSeçenekleri);

        }

        using (var oluşturulanGörüntü = (PsdImage)Image.Load(çıktıDosyaYolu))

        {

            var oluşturulanKatman = (TextLayer)oluşturulanGörüntü.Layers[0];

            if (YeniMetin != oluşturulanKatman.Text)

            {

                throw new InvalidDataException("Güncellenmiş metin geçersiz");

            }

        }

{{< /highlight >}}

**PSDNET-157. PSB olarak kaydetme sırasında PNG'in donması**

{{< highlight java >}}

       // PSB'yi PNG olarak Kaydetme

    string kaynakDosyaAdı = "örnek.psb";

    string çıkışDosyaAdı = "örnek.png";

    using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdı))

    {

        PngOptions seçenekler = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

        görüntü.Save(çıkışDosyaAdı, seçenekler);

    }

{{< /highlight >}}



` `**PSDNET-250. RLE sıkıştırmalı katmansız CMYK PSD dosyasını yüklerken istisna**

{{< highlight java >}}

     void LoadRawDataFromPsd()

        {

            string kaynakYol = "CmykVeAlphaOlan.psd";

            using (RasterImage görüntü = (RasterImage)Image.Load(kaynakYol))

            {

                var hamVeriAyarları = görüntü.RawDataSettings;

                RawDataTester yükleyici = new RawDataTester();

                görüntü.LoadRawData(görüntü.Bounds, hamVeriAyarları, yükleyici);

            }

        }

        class RawDataTester : IPartialRawDataLoader

        {

            public void Process(Rectangle dikdörtgen, byte[] pikseller, Point başlangıç, Point son)

            {

            }

            public void Process(Rectangle dikdörtgen, byte[] pikseller, Point başlangıç, Point son, LoadOptions yüklemeSeçenekleri)

            {

            }

        }

{{< /highlight >}}

` `**PSDNET-161. Metin katmanlarını güncellerken istisna**

{{< highlight java >}}

      // Bir PSD dosyasını görüntü olarak yükleyin ve PsdImage'a dönüştürün

    using (PsdImage psdGörüntü = (PsdImage)Image.Load("örnek.psd"))

    {

        foreach (var katman in psdGörüntü.Layers)

        {

            if (katman is TextLayer)

            {

                TextLayer metinKatmanı = katman as TextLayer;

                metinKatmanı.UpdateText("test güncelleme", new Point(0, 0), 15.0f, Color.Purple);

            }

        }

        psdGörüntü.Save("PSDdosyasındaMetinKatmanıGüncelleme_out.psd");

    }

{{< /highlight >}}



**PSDNET-222. Katman maskeleri olan bazı PSD dosyalarının yanlış işlenmesi**

{{< highlight java >}}

     int ölçek = 2;

        string[] isimler = {

                             "BirNormalVeDüzenlemeVeKatmanMaskesiVeVektörleBirTane",

                             "KatmanMaskesiRgbleBirlikteDüzeylerKapasitesi",

                             "KatmanMaskesiCmykleDüzeylerKapasitesi",

                             "RenkDengesiDüzenlemeKatmanı"

                         };

        for (int i = 0; i < isimler.Length; i++)

        {

            string kaynakDosyaYolu = isimler[i] + ".psd";

            string çıktıDosyaYolu = "çıktı_" + kaynakDosyaYolu;

            string çıktıPngDosyaYolu = "çıktı_" + isimler[i] + ".png";

            var psdYüklemeSeçenekleri = new PsdLoadOptions() { LoadEffectsResource = true };

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaYolu, psdYüklemeSeçenekleri))

            {

                görüntü.Resize(görüntü.Width * ölçek, görüntü.Height * ölçek);

                görüntü.Save(çıktıDosyaYolu, new PsdOptions());

                görüntü.Save(çıktıPngDosyaYolu, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

        }

{{< /highlight >}}



**PSDNET-244. Belirli Globalization.CultureInfo.CurrentCulture ile PSD kaydetme işlemi yapılırsa yükleme sırasında istisnaların alınması**

{{< highlight java >}}

     for (int i = 0; i <= 6; i++)

        {

            string kaynakDosyaAdı = string.Format("örnek-{0}.psd", i);

            var psdYüklemeSeçenekleri = new PsdLoadOptions() { LoadEffectsResource = true };

            var psdKaydetmeSeçenekleri = new PsdOptions();

            var kültür = new System.Globalization.CultureInfo("ru-RU");

            System.Threading.Thread.CurrentThread.CurrentCulture = kültür;

            System.Threading.Thread.CurrentThread.CurrentUICulture = kültür;

            string çıktıDosyaAdı = "çıktı-" + kaynakDosyaAdı;

            // Bir PSD dosyasını görüntü olarak yükleyin ve PsdImage'a dönüştürün

            using (PsdImage görüntü = (PsdImage)Image.Load(kaynakDosyaAdı, psdYüklemeSeçenekleri))

            {

                görüntü.Resize(160, 120);

                görüntü.Save(çıktıDosyaAdı, psdKaydetmeSeçenekleri);

            }

            kültür = new System.Globalization.CultureInfo("en-US");

            System.Threading.Thread.CurrentThread.CurrentCulture = kültür;

            System.Threading.Thread.CurrentThread.CurrentUICulture = kültür;

            // Bir PSD dosyasını görüntü olarak yükleyin ve PsdImage'a dönüştürün

            using (PsdImage görüntü2 = (PsdImage)Image.Load(kaynakDosyaAdı, psdYüklemeSeçenekleri))

            {

                görüntü2.Resize(160, 120);

                görüntü2.Save(çıktıDosyaAdı, psdKaydetmeSeçenekleri);

            }

        }

{{< /highlight >}}
