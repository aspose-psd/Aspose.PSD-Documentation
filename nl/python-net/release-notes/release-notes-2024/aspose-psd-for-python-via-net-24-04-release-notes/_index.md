---
title: Aspose.PSD voor Python via .NET 24.4 - Release-opmerkingen
type: docs
weight: 10
url: /nl/python-net/aspose-psd-voor-python-via-net-24-4-release-opmerkingen/
---

{{% alert color="primary" %}}

Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Python via .NET 24.4](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                      | **Categorie**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [AI-indeling] Toevoegen van XObjectForm-bronverwerking               | Functie     |
| PSDPYTHON-51 | Toevoegen van Constructor voor de ShapeLayer                         | Functie     |
| PSDPYTHON-52 | Oplossing conversiefout Psd-bestand van RGB naar CMYK                | Fout        |
| PSDPYTHON-53 | Bepaald PSD-bestand kan niet worden geëxporteerd met Aspose.PSD      | Fout        |



## **Wijzigingen in openbare API**
# **Toegevoegde API's:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **Verwijderde API's:**
- Geen


## **Gebruik voorbeelden:**

**PSDPYTHON-50. [AI-indeling] Toevoegen van XObjectForm-bronverwerking**

{{< highlight python >}}
        sourceFileName = "voorbeeld.ai"
        outputFilePath = "voorbeeld_output.png"

        with AiImage.load(sourceFileName) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. Toevoegen van Constructor voor de ShapeLayer**

{{< highlight python >}}
     def controleer ShapeLayerConstructor():
        outputFile = "AddShapeLayer_output.psd"

        with PsdImage(600, 400) as newPsd:
            shapeLayer = newPsd.add_shape_layer()

            newShape = genereer_nieuwe_vorm(newPsd.size)
            newShapes = [newShape]
            shapeLayer.path.set_items(newShapes)

            shapeLayer.update()

            newPsd.save(outputFile)

        with PsdImage.load(outputFile) as img:
            image = cast(PsdImage, img)
            assert len(image.layers) == 2

            shapeLayer = cast(ShapeLayer, image.layers[1])
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
			
    def genereer_nieuwe_vorm(afbeeldingsgrootte):
        nieuweVorm = PathShape()

        punt1 = PointF(20, 100)
        punt2 = PointF(200, 100)
        punt3 = PointF(300, 10)

        knoop1 = BezierKnotRecord()
        knoop1.is_linked = True
        knoop1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punt1, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt1, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt1, afbeeldingsgrootte)
                ]

        knoop2 = BezierKnotRecord()
        knoop2.is_linked = True
        knoop2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punt2, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt2, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt2, afbeeldingsgrootte)
                ]

        knoop3 = BezierKnotRecord()
        knoop3.is_linked = True
        knoop3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(punt3, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt3, afbeeldingsgrootte),
                    Release_24_04_Tests.PointFToResourcePoint(punt3, afbeeldingsgrootte)
                ]

        bezierknopen = [
            knoop1,
            knoop2,
            knoop3
        ]

        nieuweVorm.set_items(bezierknopen)

        return nieuweVorm
		
    def PointFToResourcePoint(punt, afbeeldingsgrootte):
        ImgToPsdVerhouding = 256 * 65535
        return Punt(
            int(round(punt.y * (ImgToPsdVerhouding / afbeeldingsgrootte.height))),
            int(round(punt.x * (ImgToPsdVerhouding / afbeeldingsgrootte.width)))
        )

    def assert_zijn_gelijk(verwacht, werkelijk, bericht=None):
        if verwacht != werkelijk:
            raise Uitzondering(bericht or "Objecten zijn niet gelijk.")
			
{{< /highlight >}}

**PSDPYTHON-52. Oplossing conversiefout Psd-bestand van RGB naar CMYK**

{{< highlight python >}}
     def controleerConversieVanRgbNaarCmyk():
        bronBestand = "kikker_nosymb.psd"
        uitvoerBestand = "kikker_nosymb_uitvoer.psd"

        with PsdImage.load(bronBestand) as afbeelding:
            psdAfbeelding = cast(PsdImage, afbeelding)
            psdAfbeelding.has_transparency_data = False

            psdOpties = PsdOptions(psdAfbeelding)
            psdOpties.color_mode = ColorModes.CMYK
            psdOpties.compression_method = CompressionMethod.RLE
            psdOpties.channels_count = 4

            psdAfbeelding.save(uitvoerBestand, psdOpties)

        with PsdImage.load(uitvoerBestand) as afbeelding:
            psdAfbeelding = cast(PsdImage, afbeelding)
            assert not psdAfbeelding.has_transparency_data
            assert psdAfbeelding.layers[0].channels_count == 4

        def assert_zijn_gelijk(verwacht, werkelijk, bericht=None):
            if verwacht != werkelijk:
                raise Uitzondering(bericht or "Objecten zijn niet gelijk.")			

    def assert_zijn_gelijk(verwacht, werkelijk, bericht=None):
        if verwacht != werkelijk:
            raise Uitzondering(bericht or "Objecten zijn niet gelijk.")
				
{{< /highlight >}}

**PSDPYTHON-53. Specifiek PSD-bestand kan niet worden geëxporteerd met Aspose.PSD**

{{< highlight python >}}
        bronBestand = "1966bron.psd"
        uitvoerPng = "uitvoer.png"

        laadopties = PsdLoadOptions()
        laadopties.load_effects_resource = True

        with PsdImage.load(bronBestand, laadopties) as psdAfbeelding:
            psdAfbeelding.save(uitvoerPng, PngOptions())
			
{{< /highlight >}}

