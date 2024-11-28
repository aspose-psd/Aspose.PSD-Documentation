---
title: Aspose.PSD Python via .NET ile 24.4 - Sürüm Notları
type: docs
weight: 10
url: /tr/python-net/aspose-psd-python-ile-net-24-4-sürüm-notları/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD Python via .NET 24.4 için](https://pypi.org/project/aspose-psd/) sürüm notlarını içerir.

{{% /alert %}}

| **Anahtar**  | **Özet**                                                           | **Kategori**|
|:------------|:---------------------------------------------------------------------|:-----------|
| PSDPYTHON-50 | [AI Format] XObjectForm kaynağı işleme ekleme                        | Özellik    |
| PSDPYTHON-51 | ShapeLayer için Yapıcı Ekle                                        | Özellik    |
| PSDPYTHON-52 | Psd dosyasının RGB'den CMYK'ya dönüştürülmesini düzeltme            | Hata       |
| PSDPYTHON-53 | Belirli bir PSD dosyası Aspose.PSD ile dışa aktarılamaz               | Hata       |



## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- M: Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Kaldırılan API'lar:**
- Hiçbiri


## **Kullanım örnekleri:**

**PSDPYTHON-50. [AI Format] XObjectForm kaynağı işleme ekleme**

{{< highlight python >}}
        kaynakDosyaAdı = "örnek.ai"
        çıkışDosyaYolu = "örnek_çıktı.png"

        with AiImage.load(kaynakDosyaAdı) as görüntü:
            görüntü.save(çıkışDosyaYolu, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. ShapeLayer için Yapıcı Ekle**

{{< highlight python >}}
      def ShapeLayerYapıcısınıKontrolEt():
        çıkışDosyası = "AddShapeLayer_çıktı.psd"

        with PsdImage(600, 400) as yeniPsd:
            şekilKatmanı = yeniPsd.add_shape_layer()

            yeniŞekil = yeni_şekil_oluştur(yeniPsd.size)
            yeniŞekiller = [yeniŞekil]
            şekilKatmanı.path.set_items(yeniŞekiller)

            şekilKatmanı.güncelle()

            yeniPsd.save(çıkışDosyası)

        with PsdImage.load(çıkışDosyası) as img:
            görüntü = cast(PsdImage, img)
            assert len(görüntü.layers) == 2

            şekilKatmanı = cast(ShapeLayer, görüntü.layers[1])
            iç_Dolum = şekilKatmanı.fill
            vuruşAyarları = şekilKatmanı.stroke
            vuruş_Dolumu = şekilKatmanı.stroke.fill

            assert len(şekilKatmanı.path.get_items()) == 1
            assert len(şekilKatmanı.path.get_items()[0].get_items()) == 3

            assert iç_Dolum.color.to_argb() == -16127182

            assert vuruşAyarları.size == 7.41
            assert not vuruşAyarları.enabled
            assert vuruşAyarları.line_alignment == StrokePosition.CENTER
            assert vuruşAyarları.line_cap == LineCapType.BUTT_CAP
            assert vuruşAyarları.line_join == LineJoinType.MITER_JOIN
            assert vur
	     
     şekil_Dolumu.color.to_argb() == -16777216
			
    def yeni_şekil_oluştur(resimBoyutu):
        yeniŞekil = PathShape()

        nokta1 = PointF(20, 100)
        nokta2 = PointF(200, 100)
        nokta3 = PointF(300, 10)

        düğüm1 = BezierKnotRecord()
        düğüm1.is_linked = True
        düğüm1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(nokta1, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta1, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta1, resimBoyutu)
                ]

        düğüm2 = BezierKnotRecord()
        düğüm2.is_linked = True
        düğüm2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(nokta2, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta2, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta2, resimBoyutu)
                ]

        düğüm3 = BezierKnotRecord()
        düğüm3.is_linked = True
        düğüm3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(nokta3, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta3, resimBoyutu),
                    Release_24_04_Tests.PointFToResourcePoint(nokta3, resimBoyutu)
                ]

        bezierDüğümleri = [
            düğüm1,
            düğüm2,
            düğüm3
        ]

        yeniŞekil.set_items(bezierDüğümleri)

        return yeniŞekil
		
    def PointFToResourcePoint(nokta, resimBoyutu):
        ImgToPsdOranı = 256 * 65535
        return Point(
            int(round(nokta.y * (ImgToPsdOranı / resimBoyutu.height))),
            int(round(nokta.x * (ImgToPsdOranı / resimBoyutu.width)))
        )

    def assert_eşit(amaç, gerçek, mesaj=None):
        if amaç != gerçek:
            raise Exception(mesaj or "Nesneler eşit değil.")
			
{{< /highlight >}}


**PSDPYTHON-52. RGB'den CMYK'ya dosyasının dönüşümünü düzeltme**

{{< highlight python >}}
     def RGBdenCmykyaDönüşümKontrolü():
        kaynakDosya = "frog_nosymb.psd"
        çıkışDosyası = "frog_nosymb_çıktı.psd"

        with PsdImage.load(kaynakDosya) as görüntü:
            psdGörüntüsü = cast(PsdImage, görüntü)
            psdGörüntüsü.has_transparency_data = False

            psdSeçenekleri = PsdOptions(psdGörüntüsü)
            psdSeçenekleri.color_mode = ColorModes.CMYK
            psdSeçenekleri.compression_method = CompressionMethod.RLE
            psdSeçenekleri.channels_count = 4

            psdGörüntüsü.save(çıkışDosyası, psdSeçenekleri)

        with PsdImage.load(çıkışDosyası) as görüntü:
            psdGörüntüsü = cast(PsdImage, görüntü)
            assert not psdGörüntüsü.has_transparency_data
            assert psdGörüntüsü.layers[0].channels_count == 4

        def assert_eşit(amaç, gerçek, mesaj=None):
            if amaç != gerçek:
                raise Exception(mesaj or "Nesneler eşit değil.")			

    def assert_eşit(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "Nesneler eşit değil.")
				
{{< /highlight >}}


**PSDPYTHON-53. Belirli bir PSD dosyası Aspose.PSD ile dışa aktarılamaz**

{{< highlight python >}}
        kaynakDosya = "1966kaynak.psd"
        çıkışPng = "çıktı.png"

        yüklemeSeçenekleri = PsdLoadOptions()
        yüklemeSeçenekleri.load_effects_resource = True

        with PsdImage.load(kaynakDosya, yüklemeSeçenekleri) as psdGörüntü:
            psdGörüntü.save(çıkışPng, PngOptions())
			
{{< /highlight >}}
