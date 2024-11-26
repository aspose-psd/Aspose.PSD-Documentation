---
title: Aspose.PSD Python ile .NET 24.5 - Sürüm Notları
type: docs
weight: 10
url: /tr/python-net/aspose-psd-python-ile-net-24-5-surum-notlari/
---

{{% alert color="primary" %}}

Bu sayfa, [Aspose.PSD Python ile .NET 24.5 için sürüm notlarını](https://pypi.org/project/aspose-psd/) içermektedir.

{{% /alert %}}

| **Anahtar**   | **Özet**                                                                              | **Kategori** |
|:--------------|:--------------------------------------------------------------------------------------|:------------|
| PSDPYTHON-60  | [AI Formatı] EPSF başlıklı AI Dosyalarının işlenmesi için destek ekleyin               | Özellik     |
| PSDPYTHON-59  | PSD dosya önizlemesinde yarı saydamlık yanlış işlenir                                  | Hata        |
| PSDPYTHON-61  | Şekil Katmanının Kısmen Yanlış Render Edilmesi                                       | Hata        |
| PSDPYTHON-62  | 200 MB ve büyük boyutlu boyutları olan PSD dosyalarını kaydederken istisna oluşması    | Hata        |
| PSDPYTHON-63  | 23.7'den 24.3'e güncellemeden sonra PDF'ye kaydederken görüntünün kaydedilememesi istisnası | Hata        |
| PSDPYTHON-64  | Çince Yazı Tipleri için GetFontInfoRecords yöntemindeki sorunu düzeltin              | Hata        |

## **Genel API Değişiklikleri**
# **Eklenen API'lar:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **Kaldırılan API'lar:**
- Hiçbiri

## **Kullanım örnekleri:**

**PSDPYTHON-59. Yarı saydamlık, PSD dosya önizlemesinde yanlış işlenir**

{{< highlight python >}}
// PSD dosya önizlemesinde yarı saydamlık yanlış işlenir.
// Arka plan içeriği Beyaz olarak atandı. Şeffaf alanlar beyaz renkte olmalı.

        kaynakDosya = "frog_nosymb.psd"
        çıktıDosyası = "frog_nosymb_backgroundcontents_output.psd"

        with PsdImage.load(kaynakDosya) as psdImage:

            arkaPlanRengi = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            argbDegeri = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            arkaPlanRengi.set_as_int(argbDegeri)  # Beyaz

            psdSeçenekleri = PsdOptions(psdImage)
            psdSeçenekleri.color_mode = ColorModes.RGB
            psdSeçenekleri.compression_method = CompressionMethod.RLE
            psdSeçenekleri.channels_count = 4
            psdSeçenekleri.background_contents = arkaPlanRengi

            psdImage.save(çıktıDosyası, psdSeçenekleri)
{{< /highlight >}}

**PSDPYTHON-60. [AI Formatı] EPSF başlıklı AI Dosyalarının işlenmesi için destek ekleyin**

{{< highlight python >}}
        kaynakDosya = "örnek.ai"
        çıktıDosyaYolu = "örnek.png"
       
        def eşit_mi(beklenen, gerçek):
            if beklenen != gerçek:
                raise Exception("Nesneler eşit değil.")

        with AiImage.load(kaynakDosya) as img:
            image = cast(AiImage, img)
            eşit_mi(len(image.layers), 2)
            eşit_mi(image.layers[0].has_multi_layer_masks, False)
            eşit_mi(image.layers[0].color_index, -1)
            eşit_mi(image.layers[1].has_multi_layer_masks, False)
            eşit_mi(image.layers[1].color_index, -1)

            image.save(çıktıDosyaYolu, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. Şekil Katmanının Kısmen Yanlış Render Edilmesi**

{{< highlight python >}}
        kaynakDosya = "ShapeLayerTest.psd"
        çıktıDosya = "ShapeLayerTest_output.psd"

        with PsdImage.load(kaynakDosya) as image:
            im = cast(PsdImage, image)
            shapeLayer = cast(ShapeLayer, im.layers[2])
            path = shapeLayer.path
            pathShapes = path.get_items()
            knotsList = []
            for pathShape in pathShapes:
                knots = pathShape.get_items()
                knotsList.extend(knots)

            yeniŞekil = PathShape()

            bezierKnot1 = BezierKnotRecord()
            bezierKnot1.is_linked=True
            bezierKnot1.points=[
                    PointFToResourcePoint(PointF(100, 100), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(100, 100), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(100, 100), shapeLayer.container.size)
                ]

            bezierKnot2 = BezierKnotRecord()
            bezierKnot2.is_linked=True
            bezierKnot2.points=[
                    PointFToResourcePoint(PointF(50, 490), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(100, 490), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(150, 490), shapeLayer.container.size)
                ]

            bezierKnot3 = BezierKnotRecord()
            bezierKnot3.is_linked=True
            bezierKnot3.points=[
                    PointFToResourcePoint(PointF(490, 150), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(490, 50), shapeLayer.container.size),
                    PointFToResourcePoint(PointF(490, 20), shapeLayer.container.size)
                ]

            bezierKnots = [
                bezierKnot1,
                bezierKnot2,
                bezierKnot3
            ]

            yeniŞekil.set_items(bezierKnots)

            newShapes = list(pathShapes)
            newShapes.append(yeniŞekil)

            pathShapeNew = newShapes
            path.set_items(pathShapeNew)

            shapeLayer.update()

            im.save(çıktıDosya, PsdOptions())

        with PsdImage.load(çıktıDosya) as image:
            im = cast(PsdImage, image)
            shapeLayer = cast(ShapeLayer, im.layers[2])
            path = shapeLayer.path
            pathShapes = path.get_items()
            knotsList = []
            for pathShape in pathShapes:
                knots = pathShape.get_items()
                knotsList.extend(knots)

            assert len(pathShapes) == 3
            assert shapeLayer.left == 42
            assert shapeLayer.top == 14
            assert shapeLayer.bounds.width == 1600
            assert shapeLayer.bounds.height == 1086
{{< /highlight >}}

**PSDPYTHON-62. 200 MB ve büyük boyutlu boyutları olan PSD dosyalarını kaydederken istisna oluşması**

{{< highlight python >}}
        kaynakDosya = "bigfile.psd"
        çıktıDosyası = "output_raw.psd"
        referansDosya = "output_raw.psd"

        yüklemeSeçenekleri = PsdLoadOptions()
        yüklemeSeçenekleri.load_effects_resource = True
        yüklemeSeçenekleri.use_disk_for_load_effects_resource = True

        with PsdImage.load(kaynakDosya, yüklemeSeçenekleri) as psdImage:
            seçenek = PsdOptions()
            seçenek.compression_method = CompressionMethod.RLE
            psdImage.save(çıktıDosyası, seçenek)
{{< /highlight >}}

**PSDPYTHON-63. 23.7'den 24.3'e güncellemeden sonra PDF'ye kaydederken görüntünün kaydedilememesi istisnası**

{{< highlight python >}}
        kaynakDosya = "CVFlor.psd"
        çıktıDosyası = "_export.pdf"

        with PsdImage.load(kaynakDosya) as psdImage:
            kaydetmeSeçenekleri = PdfOptions()
            kaydetmeSeçenekleri.pdf_core_options = PdfCoreOptions()

            psdImage.save(çıktıDosyası, kaydetmeSeçenekleri)
{{< /highlight >}}

**PSDPYTHON-64. Çince Fontlar için GetFontInfoRecords yöntemindeki sorunu düzeltin**

{{< highlight python >}}
        fontKlasörü = "Font"
        kaynakDosya = "bd-worlds-best-pink.psd"

        psdYüklemeSeçenekleri = PsdLoadOptions()
        psdYüklemeSeçenekleri.load_effects_resource = True
        psdYüklemeSeçenekleri.allow_warp_repaint = True

        try:
            FontSettings.set_fonts_folders([fontKlasörü], True)
            FontSettings.update_fonts()

            with PsdImage.load(kaynakDosya, psdYüklemeSeçenekleri) as img:
                image = cast(PsdImage, img)
                for katman in image.layers:
                    if is_assignable(katman, TextLayer):
                        textLayer = cast(TextLayer, katman)
                        if textLayer.text == "best":
                            # Buradaki düzeltme yapılmazsa Çince fonttan dolayı bir istisna oluşur.
                            textLayer.update_text("BAŞARILI")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}
