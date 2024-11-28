---
title: Aspose.PSD for Python via .NET 24.4 - 릴리스 노트
type: docs
weight: 10
url: /ko/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

이 페이지에는 [Aspose.PSD for Python via .NET 24.4](https://pypi.org/project/aspose-psd/)의 릴리스 노트가 포함되어 있습니다.

{{% /alert %}}

| **키**        | **요약**                                                      | **범주**   |
|:-------------|:-----------------------------------------------------------|:--------|
| PSDPYTHON-50 | [AI 형식] XObjectForm 리소스 처리 추가                           | 기능      |
| PSDPYTHON-51 | ShapeLayer를 위한 생성자 추가                                  | 기능      |
| PSDPYTHON-52 | RGB에서 CMYK로 PSD 파일 변환 수정                                | 버그      |
| PSDPYTHON-53 | 특정 PSD 파일을 Aspose.PSD를 사용하여 내보내지 못함                | 버그      |



## **공개 API 변경 사항**
# **추가된 API:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **제거된 API:**
- 없음


## **사용 예시:**

**PSDPYTHON-50. [AI 형식] XObjectForm 리소스 처리 추가**

{{< highlight python >}}
        sourceFileName = "example.ai"
        outputFilePath = "example_output.png"

        with AiImage.load(sourceFileName) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. ShapeLayer를 위한 생성자 추가**

{{< highlight python >}}
     def check ShapeLayerConstructor():
        outputFile = "AddShapeLayer_output.psd"

        with PsdImage(600, 400) as newPsd:
            shapeLayer = newPsd.add_shape_layer()

            newShape = generate_new_shape(newPsd.size)
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
			
    def generate_new_shape(imageSize):
        newShape = PathShape()

        point1 = PointF(20, 100)
        point2 = PointF(200, 100)
        point3 = PointF(300, 10)

        knot1 = BezierKnotRecord()
        knot1.is_linked = True
        knot1.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point1, imageSize)
                ]

        knot2 = BezierKnotRecord()
        knot2.is_linked = True
        knot2.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point2, imageSize)
                ]

        knot3 = BezierKnotRecord()
        knot3.is_linked = True
        knot3.points = [
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize),
                    Release_24_04_Tests.PointFToResourcePoint(point3, imageSize)
                ]

        bezierKnots = [
            knot1,
            knot2,
            knot3
        ]

        newShape.set_items(bezierKnots)

        return newShape
		
    def PointFToResourcePoint(point, imageSize):
        ImgToPsdRatio = 256 * 65535
        return Point(
            int(round(point.y * (ImgToPsdRatio / imageSize.height))),
            int(round(point.x * (ImgToPsdRatio / imageSize.width)))
        )

    def assert_are_equal(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "Objects are not equal.")
			
{{< /highlight >}}

**PSDPYTHON-52. RGB에서 CMYK로의 변환 수정**

{{< highlight python >}}
     def checkConversionFromRgbToCmyk():
        sourceFile = "frog_nosymb.psd"
        outputFile = "frog_nosymb_output.psd"

        with PsdImage.load(sourceFile) as image:
            psdImage = cast(PsdImage, image)
            psdImage.has_transparency_data = False

            psdOptions = PsdOptions(psdImage)
            psdOptions.color_mode = ColorModes.CMYK
            psdOptions.compression_method = CompressionMethod.RLE
            psdOptions.channels_count = 4

            psdImage.save(outputFile, psdOptions)

        with PsdImage.load(outputFile) as image:
            psdImage = cast(PsdImage, image)
            assert not psdImage.has_transparency_data
            assert psdImage.layers[0].channels_count == 4

        def assert_are_equal(expected, actual, message=None):
            if expected != actual:
                raise Exception(message or "Objects are not equal.")			

    def assert_are_equal(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "Objects are not equal.")
				
{{< /highlight >}}

**PSDPYTHON-53. 특정 PSD 파일을 Aspose.PSD를 사용하여 내보내지 못함**

{{< highlight python >}}
        sourceFile = "1966source.psd"
        outputPng = "output.png"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True

        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputPng, PngOptions())
			
{{< /highlight >}}

