---
title: Aspose.PSD for Python via .NET 24.4 - リリースノート
type: docs
weight: 10
url: /ja/python-net/aspose-psd-for-python-via-net-24-4-release-notes/
---

{{% alert color="primary" %}}

このページには、[Aspose.PSD for Python via .NET 24.4](https://pypi.org/project/aspose-psd/) のリリースノートが含まれています。

{{% /alert %}}

| **キー**      | **概要**                                                          | **カテゴリ**|
|:-------------|:--------------------------------------------------------------------|:------------|
| PSDPYTHON-50 | [AI形式] XObjectFormリソース処理の追加                        | 機能     |
| PSDPYTHON-51 | ShapeLayerのためのコンストラクタを追加                                   | 機能     |
| PSDPYTHON-52 | RGBからCMYKへのPsdファイルの変換を修正                         | 不具合         |
| PSDPYTHON-53 | 特定のPSDファイルをAspose.PSDを使用してエクスポートできない         | 不具合         |



## **パブリックAPIの変更**
# **追加されたAPI:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddShapeLayer

# **削除されたAPI:**
- なし


## **使用例:**

**PSDPYTHON-50. [AI形式] XObjectFormリソース処理の追加**

{{< highlight python >}}
        sourceFileName = "example.ai"
        outputFilePath = "example_output.png"

        with AiImage.load(sourceFileName) as image:
            image.save(outputFilePath, PngOptions())
{{< /highlight >}}

**PSDPYTHON-51. ShapeLayerのためのコンストラクタを追加**

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
            raise Exception(message or "オブジェクトが等しくありません。")
			
{{< /highlight >}}

**PSDPYTHON-52. RGBからCMYKへのPsdファイルの変換を修正**

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
                raise Exception(message or "オブジェクトが等しくありません。")			

    def assert_are_equal(expected, actual, message=None):
        if expected != actual:
            raise Exception(message or "オブジェクトが等しくありません。")
				
{{< /highlight >}}

**PSDPYTHON-53. 特定のPSDファイルをAspose.PSDを使用してエクスポートできない**

{{< highlight python >}}
        sourceFile = "1966source.psd"
        outputPng = "output.png"

        loadOpt = PsdLoadOptions()
        loadOpt.load_effects_resource = True

        with PsdImage.load(sourceFile, loadOpt) as psdImage:
            psdImage.save(outputPng, PngOptions())
			
{{< /highlight >}}

