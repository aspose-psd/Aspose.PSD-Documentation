---
title: یادداشت های نسخه Aspose.PSD برای پایتون از طریق .NET 24.5
type: docs
weight: 10
url: /fa/python-net/aspose-psd-for-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

این صفحه شامل یادداشت های نسخه برای [Aspose.PSD برای پایتون از طریق .NET 24.5](https://pypi.org/project/aspose-psd/) می‌باشد.

{{% /alert %}}

| **کلید**      | **خلاصه**                                                                         | **دسته‌بندی** |
|:-------------|:------------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-60 | اضافه کردن پشتیبانی برای پردازش پرونده‌های AI با هدر EPSF                      | ویژگی      |
| PSDPYTHON-59 | نیمه شفافیت به طور اشتباه در پیش نمایش فایل psd پردازش می‌شود                        | باگ      |
| PSDPYTHON-61 | رندر کردن لایه شکل جزئاً اشتباه                                        | باگ      |
| PSDPYTHON-62 | استثنا هر زمانی که فایل‌های PSD با اندازه بیشتر از 200 مگابایت و ابعاد بزرگ ذخیره می‌شوند | باگ      |
| PSDPYTHON-63 | استثنای عدم موفقیت در ذخیره سازی تصویر هنگام ذخیره سازی به فرمت PDF پس از به‌روزرسانی از 23.7 به 24.3     | باگ      |
| PSDPYTHON-64 | رفع مشکل در متد GetFontInfoRecords برای فونت‌های چینی                    | باگ      |

## **تغییرات API عمومی**
# **API‌های افزوده شده:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **API‌های حذف شده:**
- هیچکدام

## **مثال‌های استفاده:**

**PSDPYTHON-59. نیمه شفافیت به طور اشتباه در پیش نمایش فایل psd پردازش می‌شود**

{{< highlight python >}}
// نیمه شفافیت به طور اشتباه در پیش نمایش فایل psd پردازش می‌شود.
// BackgroundContents به سفید اختصاص یافته است. مناطق شفاف باید رنگ سفید داشته باشند.

        sourceFile = "frog_nosymb.psd"
        outputFile = "frog_nosymb_backgroundcontents_output.psd"

        with PsdImage.load(sourceFile) as psdImage:

            backgroundColor = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            argbValue = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            backgroundColor.set_as_int(argbValue)  # سفید

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.RGB
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4
            psdOptions.background_contents = backgroundColor

            psdImage.save(outputFile, psdOptions)
{{< /highlight >}}

**PSDPYTHON-60. [فرمت AI] اضافه کردن پشتیبانی برای پردازش پرونده‌های AI با هدر EPSF**

{{< highlight python >}}
        sourceFile = "مثال.ai"
        outputFilePath = "مثال.png"
       
        def assert_are_equal(expected, actual):
            if expected != actual:
                raise Exception("اشیاء برابر نیستند.")

        with AiImage.load(sourceFile) as img:
            image = cast(AiImage, img)
            assert_are_equal(len(image.layers), 2)
            assert_are_equal(image.layers[0].has_multi_layer_masks, False)
            assert_are_equal(image.layers[0].color_index, -1)
            assert_are_equal(image.layers[1].has_multi_layer_masks, False)
            assert_are_equal(image.layers[1].color_index, -1)

            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. رندر کردن لایه شکل جزئاً اشتباه**

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

**PSDPYTHON-62. استثنای هر زمانی که فایل‌های PSD با اندازه بیشتر از 200 مگابایت و ابعاد بزرگ ذخیره می‌شوند**

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

**PSDPYTHON-63. استثنای عدم موفقیت در ذخیره سازی تصویر هنگام ذخیره سازی به فرمت PDF پس از به‌روزرسانی از 23.7 به 24.3**

{{< highlight python >}}
        sourceFile = "CVFlor.psd"
        outputFile = "_export.pdf"

        with PsdImage.load(sourceFile) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(outputFile, saveOptions)
{{< /highlight >}}

**PSDPYTHON-64. رفع مشکل در متد GetFontInfoRecords برای فونت‌های چینی**

{{< highlight python >}}
        fontFolder = "فونت"
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
                        if textLayer.text == "بهترین":
                            # بدون این تغییر در اینجا اشکالی وجود خواهد داشت به دلیل فونت چینی.
                            textLayer.update_text("موفقیت")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}
