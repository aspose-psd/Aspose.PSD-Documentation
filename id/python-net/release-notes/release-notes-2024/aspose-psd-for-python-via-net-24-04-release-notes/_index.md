---
title: Catatan Rilis Aspose.PSD untuk Python via .NET 24.4
type: docs
weight: 10
url: /id/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Halaman ini berisi catatan rilis untuk [Aspose.PSD untuk Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Kunci**    | **Ringkasan**                                                     | **Kategori**|
|:------------ |:-----------------------------------------------------------------|:------------|
| PSDPYTHON-50 | Menambahkan penanganan sumber XObjectForm pada format AI          | Fitur       |
| PSDPYTHON-51 | Menambahkan Konstruktor untuk ShapeLayer                          | Fitur       |
| PSDPYTHON-52 | Memperbaiki konversi file Psd dari RGB ke CMYK                    | Bug         |
| PSDPYTHON-53 | File PSD spesifik tidak dapat diekspor menggunakan Aspose.PSD      | Bug         |



## **Perubahan API Publik**
# **API Ditambahkan:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **API Dihapus:**
- Tidak ada


## **Contoh Penggunaan:**

**PSDPYTHON-50. [Format AI] Menambahkan penanganan sumber XObjectForm**

{{< highlight python >}}
        namaFileSumber = "contoh.ai"
        jalurKeluarBerkas = "keluaran_contoh.png"

        with AiImage.load(namaFileSumber) as gambar:
            gambar.save(jalurKeluarBerkas, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Menambahkan Konstruktor untuk ShapeLayer**

{{< highlight python >}}
     def cek ShapeLayerConstructor():
        outputBerkas = "keluaran_AddShapeLayer.psd"

        with PsdImage(600, 400) as psdBaru:
            shapeLayer = psdBaru.add_shape_layer()

            bentukBaru = generate_new_shape(psdBaru.size)
            bentukBaruList = [bentukBaru]
            shapeLayer.path.set_items(bentukBaruList)

            shapeLayer.update()

            psdBaru.save(outputBerkas)

        with PsdImage.load(outputBerkas) as img:
            gambar = cast(PsdImage, img)
            assert len(gambar.layers) == 2

            shapeLayer = cast(ShapeLayer, gambar.layers[1])
            internalFill = shapeLayer.fill
            strokeSettings = shapeLayer.stroke
            strokeFill = shapeLayer.stroke.fill

            assert len(shapeLayer.path.get_items()) == 1
            assert len(shapeLayer.path.get_items()[0].get_items()) == 3

            assert internalFill.color.to_argb() == -16127182

            assert strokeSettings.size == 7.41
            assert not strokeSettings.enabled
            assert strokeSettings.line_alignment == StrokePosition.CENTER
            assert strokeSettings.line_cap == LineCapType.BUTT_CAP
            assert strokeSettings.line_join == LineJoinType.MITER_JOIN
            assert strokeFill.color.to_argb() == -16777216
			
    def generate_new_shape(ukuranGambar):
        bentukBaru = PathShape()

        titik1 = PointF(20, 100)
        titik2 = PointF(200, 100)
        titik3 = PointF(300, 10)

        knot1 = BezierKnotRecord()
        knot1.is_linked = True
        knot1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(titik1, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik1, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik1, ukuranGambar)
                ]

        knot2 = BezierKnotRecord()
        knot2.is_linked = True
        knot2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(titik2, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik2, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik2, ukuranGambar)
                ]

        knot3 = BezierKnotRecord()
        knot3.is_linked = True
        knot3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(titik3, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik3, ukuranGambar),
                    Release_24_04_Tests.PointFToResourcePoint(titik3, ukuranGambar)
                ]

        bezierKnots = [
            knot1,
            knot2,
            knot3
        ]

        bentukBaru.set_items(bezierKnots)

        return bentukBaru
		
    def PointFToResourcePoint(titik, ukuranGambar):
        ImgToPsdRatio = 256 * 65535
        return Point(
            int(round(titik.y * (ImgToPsdRatio / ukuranGambar.height))),
            int(round(titik.x * (ImgToPsdRatio / ukuranGambar.width)))
        )

    def assert_sama(expected, actual, pesan=None):
        if expected != actual:
            raise Exception(pesan or "Objek tidak sama.")
			
{{< /highlight >}}

**PSDPYTHON-52. Memperbaiki konversi file Psd dari RGB ke CMYK**

{{< highlight python >}}
     def cekKonversiDariRgbKeCmyk():
        berkasSumber = "katak_nosimbol.psd"
        berkasKeluaran = "katak_nosimbol_keluaran.psd"

        with PsdImage.load(berkasSumber) as gambar:
            psdGambar = cast(PsdImage, gambar)
            psdGambar.has_transparency_data = False

            pilihanPsd = PsdOptions(psdGambar)
            pilihanPsd.color_mode = ColorModes.CMYK
            pilihanPsd.compression_method = CompressionMethod.RLE
            pilihanPsd.channels_count = 4

            psdGambar.save(berkasKeluaran, pilihanPsd)

        with PsdImage.load(berkasKeluaran) as gambar:
            psdGambar = cast(PsdImage, gambar)
            assert not psdGambar.has_transparency_data
            assert psdGambar.layers[0].channels_count == 4

        def assert_sama(expected, actual, pesan=None):
            if expected != actual:
                raise Exception(pesan or "Objek tidak sama.")			

    def assert_sama(expected, actual, pesan=None):
        if expected != actual:
            raise Exception(pesan or "Objek tidak sama.")
				
{{< /highlight >}}

**PSDPYTHON-53. File PSD spesifik tidak dapat diekspor menggunakan Aspose.PSD**

{{< highlight python >}}
        berkasSumber = "1966sumber.psd"
        keluaranPng = "keluaran.png"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True

        with PsdImage.load(berkasSumber, loadOpt) as psdGambar:
            psdGambar.save(keluaranPng, PngOptions())
			
{{< /highlight >}}
