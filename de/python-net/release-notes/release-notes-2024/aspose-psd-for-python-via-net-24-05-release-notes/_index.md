---
title: Aspose.PSD für Python via .NET 24.5 - Versionshinweise
type: docs
weight: 10
url: /de/python-net/aspose-psd-fur-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

Diese Seite enthält Versionshinweise für [Aspose.PSD für Python via .NET 24.5](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Schlüssel**  | **Zusammenfassung**                                                                      | **Kategorie** |
|:--------------|:------------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-60  | [AI-Format] Hinzufügen der Unterstützung zur Behandlung von AI-Dateien mit EPSF-Header     | Funktion      |
| PSDPYTHON-59  | Halbtransparenz wird falsch in der PSD-Dateivorschau verarbeitet                           | Fehler        |
| PSDPYTHON-61  | Rendering des Formebene teilweise inkorrekt                                               | Fehler        |
| PSDPYTHON-62  | Ausnahme beim Speichern von PSD-Dateien mit einer Größe von mehr als 200 MB und großen Dimensionen  | Fehler        |
| PSDPYTHON-63  | Fehler beim Speichern des Bildes als PDF nach dem Update von 23.7 auf 24.3               | Fehler        |
| PSDPYTHON-64  | Beheben des Problems in der GetFontInfoRecords-Methode für die chinesischen Schriftarten  | Fehler        |

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **Entfernte APIs:**
- Keine

## **Beispiele für die Verwendung:**

**PSDPYTHON-59. Halbtransparenz wird falsch in der PSD-Dateivorschau verarbeitet**

{{< highlight python >}}
// Halbtransparenz wird falsch in der PSD-Dateivorschau verarbeitet.
// BackgroundContents auf Weiß gesetzt. Transparente Bereiche sollten weiße Farbe haben.

        sourceFile = "frosch_nosymb.psd"
        outputFile = "frosch_nosymb_backgroundcontents_output.psd"

        with PsdImage.load(sourceFile) as psdImage:

            backgroundColor = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            argbWert = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            backgroundColor.set_as_int(argbWert)  # Weiß

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.RGB
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4
            psdOptions.background_contents = backgroundColor

            psdImage.save(outputFile, psdOptions)
{{< /highlight >}}

**PSDPYTHON-60. [AI-Format] Hinzufügen der Unterstützung zur Behandlung von AI-Dateien mit EPSF-Header**

{{< highlight python >}}
        sourceFile = "beispiel.ai"
        outputFilePath = "beispiel.png"
       
        def assert_are_equal(expected, actual):
            if expected != actual:
                raise Exception("Objekte sind nicht gleich.")

        with AiImage.load(sourceFile) as img:
            image = cast(AiImage, img)
            assert_are_equal(len(image.layers), 2)
            assert_are_equal(image.layers[0].has_multi_layer_masks, False)
            assert_are_equal(image.layers[0].color_index, -1)
            assert_are_equal(image.layers[1].has_multi_layer_masks, False)
            assert_are_equal(image.layers[1].color_index, -1)

            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. Rendering des Formebene teilweise inkorrekt**

{{< highlight python >}}
        sourceFile = "ShapeLayerTest.psd"
        outputFile = "ShapeLayerTest_output.psd"

        with PsdImage.load(sourceFile) as image:
            im = cast(PsdImage, image)
            shapeLayer = cast(ShapeLayer, im.layers[2])
            path = shapeLayer.path
            pathShapes = path.get_items()
            knotsList = []
            for pathShape in pathShapes:
                knots = pathShape.get_items()
                knotsList.extend(knots)

            newShape = PathShape()

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

            newShape.set_items(bezierKnots)

            newShapes = list(pathShapes)
            newShapes.append(newShape)

            pathShapeNew = newShapes
            path.set_items(pathShapeNew)

            shapeLayer.update()

            im.save(outputFile, PsdOptions())

        with PsdImage.load(outputFile) as image:
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

**PSDPYTHON-62. Ausnahme beim Speichern von PSD-Dateien mit einer Größe von mehr als 200 MB und großen Dimensionen**

{{< highlight python >}}
        sourceFile = "großeDatei.psd"
        outputFile = "output_raw.psd"
        referenceFile = "output_raw.psd"

        loadOptions = PsdLoadOptions()
        loadOptions.load_effects_resource = True
        loadOptions.use_disk_for_load_effects_resource = True

        with PsdImage.load(sourceFile, loadOptions) as psdImage:
            opt = PsdOptions()
            opt.compression_method = CompressionMethod.RLE
            psdImage.save(outputFile, opt)
{{< /highlight >}}

**PSDPYTHON-63. Fehler beim Speichern des Bildes als PDF nach dem Update von 23.7 auf 24.3**

{{< highlight python >}}
        sourceFile = "CVFlor.psd"
        outputFile = "_export.pdf"

        with PsdImage.load(sourceFile) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(outputFile, saveOptions)
{{< /highlight >}}

**PSDPYTHON-64. Beheben des Problems in der GetFontInfoRecords-Methode für die chinesischen Schriftarten**

{{< highlight python >}}
        fontOrdner = "Schriftart"
        sourceFile = "bd-worlds-best-pink.psd"

        psdLadeoptionen = PsdLoadOptions()
        psdLadeoptionen.load_effects_resource = True
        psdLadeoptionen.allow_warp_repaint = True

        try:
            FontSettings.set_fonts_folders([fontOrdner], True)
            FontSettings.update_fonts()

            with PsdImage.load(sourceFile, psdLadeoptionen) as img:
                image = cast(PsdImage, img)
                for layer in image.layers:
                    if is_assignable(layer, TextLayer):
                        textLayer = cast(TextLayer, layer)
                        if textLayer.text == "best":
                            # Ohne diese Korrektur würde hier eine Ausnahme aufgrund der chinesischen Schriftart auftreten.
                            textLayer.update_text("ERFOLG")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}
