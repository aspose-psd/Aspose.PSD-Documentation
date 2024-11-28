---
title: Aspose.PSD for Python via .NET 24.5 - 릴리스 노트
type: 문서
weight: 10
url: /ko/python-net/aspose-psd-for-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for Python via .NET 24.5](https://pypi.org/project/aspose-psd/)에 대한 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**       | **개요**                                                                      | **카테고리** |
|:------------|:-----------------------------------------------------------------------------|:-----------|
| PSDPYTHON-60 | [AI 형식] AI 파일의 EPSF 헤더 처리 지원 추가                                 | 기능      |
| PSDPYTHON-59 | psd 파일 미리보기에서 반투명 처리 오류                                        | 버그      |
| PSDPYTHON-61 | 모양 레이어 렌더링 일부 오류                                               | 버그      |
| PSDPYTHON-62 | 200 MB 이상 및 큰 크기를 가진 PSD 파일 저장시 예외 발생                   | 버그      |
| PSDPYTHON-63 | 23.7에서 24.3으로 업데이트 후 PDF로 저장할 때 이미지 저장 실패 예외 발생 | 버그      |
| PSDPYTHON-64 | 중국어 폰트에 대한 GetFontInfoRecords 메서드의 문제 수정                   | 버그      |

## **공개 API 변경**
# **추가된 API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **제거된 API:**
- 없음

## **사용 예시:**

**PSDPYTHON-59. psd 파일 미리보기에서 반투명 처리 오류**

{{< highlight python >}}
// psd 파일 미리보기에서 반투명 처리 오류.
// BackgroundContents가 White로 할당됩니다. 반투명 영역은 흰색이어야 합니다.

        sourceFile = "frog_nosymb.psd"
        outputFile = "frog_nosymb_backgroundcontents_output.psd"

        with PsdImage.load(sourceFile) as psdImage:

            backgroundColor = RawColor(PixelDataFormat.rgb_32_bpp, 0)

            argbValue = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

            backgroundColor.set_as_int(argbValue)  # White

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.RGB
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4
            psdOptions.background_contents = backgroundColor

            psdImage.save(outputFile, psdOptions)
{{< /highlight >}}

**PSDPYTHON-60. [AI 형식] AI 파일의 EPSF 헤더 처리 지원 추가**

{{< highlight python >}}
        sourceFile = "example.ai"
        outputFilePath = "example.png"
       
        def assert_are_equal(expected, actual):
            if expected != actual:
                raise Exception("객체가 동일하지 않습니다.")

        with AiImage.load(sourceFile) as img:
            image = cast(AiImage, img)
            assert_are_equal(len(image.layers), 2)
            assert_are_equal(image.layers[0].has_multi_layer_masks, False)
            assert_are_equal(image.layers[0].color_index, -1)
            assert_are_equal(image.layers[1].has_multi_layer_masks, False)
            assert_are_equal(image.layers[1].color_index, -1)

            image.save(outputFilePath, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. 모양 레이어 렌더링 부분적으로 잘못됨**

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

**PSDPYTHON-62. 200 MB 이상 및 큰 크기를 가진 PSD 파일 저장시 예외 발생**

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

**PSDPYTHON-63. 23.7에서 24.3으로 업데이트 후 PDF로 저장할 때 이미지 저장 실패 예외 발생**

{{< highlight python >}}
        sourceFile = "CVFlor.psd"
        outputFile = "_export.pdf"

        with PsdImage.load(sourceFile) as psdImage:
            saveOptions = PdfOptions()
            saveOptions.pdf_core_options = PdfCoreOptions()

            psdImage.save(outputFile, saveOptions)
{{< /highlight >}}

**PSDPYTHON-64. 중국어 폰트에 대한 GetFontInfoRecords 메서드의 문제 수정**

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
                            # 중국어 폰트로 인한 예외를 방지하기 위해 여기서 수정이 필요합니다.
                            textLayer.update_text("SUCCESS")
        finally:
            FontSettings.reset()
            FontSettings.update_fonts()
{{< /highlight >}}
