---
title: Примітки до версії Aspose.PSD для Python via .NET 24.5
type: docs
weight: 10
url: /uk/python-net/aspose-psd-for-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до версії [Aspose.PSD для Python via .NET 24.5](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                                                  | **Категорія** |
|:------------:|:------------------------------------------------------------------------------------------|:-------------:|
| PSDPYTHON-60 | [Формат AI] Додана підтримка для обробки файлів AI з заголовком EPSF                           | Функціонал   |
| PSDPYTHON-59 | Помилка обробки напівпрозорості на попередньому перегляді файлу psd                        | Помилка       |
| PSDPYTHON-61 | Частково неправильна відтворення завершеного шару форми                                     | Помилка       |
| PSDPYTHON-62 | Виняток при збереженні файлів PSD з розміром більше 200 МБ та великими розмірами           | Помилка       |
| PSDPYTHON-63 | Виняток невдалого збереження зображення при збереженні у PDF після оновлення з 23.7 на 24.3 | Помилка       |
| PSDPYTHON-64 | Виправлено проблему у методі GetFontInfoRecords для китайських шрифтів                       | Помилка       |

## **Зміни у Публічному API**
# **Додані API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **Вилучені API:**
- Жодних

## **Приклади використання:**

**PSDPYTHON-59. Помилка обробки напівпрозорості на попередньому перегляді файлу psd**

{{< highlight python >}}
// Помилка обробки напівпрозорості на попередньому перегляді файлу psd.
// BackgroundContents призначений білому кольору. Прозорі області повинні мати білий колір.

        sourceFile = "frog_nosymb.psd"
        outputFile = "frog_nosymb_backgroundcontents_output.psd"

        with PsdImage.load(sourceFile) as psdImage:

            backgroundColor = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            argbValue = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            backgroundColor.set_as_int(argbValue)  # Білий

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.RGB
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4
            psdOptions.background_contents = backgroundColor

            psdImage.save(outputFile, psdOptions)
{{< /highlight >}}

**PSDPYTHON-60. [Формат AI] Додана підтримка для обробки файлів AI з заголовком EPSF**

{{< highlight python >}}
        sourceFile = "example.ai"
        outputFilePath = "example.png"
       
        def assert_are_equal(expected, actual):
            if expected != actual:
                raise Exception("Об'єкти не рівні.")

        with AiImage.load(sourceFile) as img:
            image = cast(AiImage, img)
            assert_are_equal(len(image.layers), 2)
            assert_are_equal(image.layers[0].has_multi_layer_masks, False)
            assert_are_equal(image.layers[0].color_index, -1)
            assert_are_equal(image.layers[1].has_multi_layer_masks, False)
            assert_are_equal(image.layers[1].color_index, -1)

            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. Частково неправильна відтворення завершеного шару форми**

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

**PSDPYTHON-62. Виняток при збереженні файлів PSD з розміром більше 200 МБ та великими розмірами**

{{< highlight python >}}
        sourceFile = "bigfile.psd"
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

**PSDPYTHON-63. Виняток невдалого збереження зображення при збереженні у PDF після оновлення з 23.7 на 24.3**

{{< highlight python >}}
        sourceFile = "CVFlor.psd"
        outputFile = "_export.pdf"

        with PsdImage.load(sourceFile) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(outputFile, saveOptions)
{{< /highlight >}}

**PSDPYTHON-64. Виправлено проблему у методі GetFontInfoRecords для китайських шрифтів**

{{< highlight python >}}
        fontFolder = "Font"
        sourceFile = "bd-worlds-best-pink.psd"

        psdLoadOptions = PsdLoadOptions()
        psdLoadOptions.load_effects_resource = True
        psdLoadOptions.allow_warp_repaint = True

        try:
            FontSettings.set_fonts_folders([fontFolder], True)
            FontSettings.update_fonts()

            with PsdImage.load(sourceFile, psdLoadOptions) as img:
                image = cast(PsdImage, img)
                for layer in image.layers:
                    if is_assignable(layer, TextLayer):
                        textLayer = cast(TextLayer, layer)
                        if textLayer.text == "best":
                            # Без виправлення тут буде виняток через китайський шрифт.
                            textLayer.update_text("УСПІХ")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}
