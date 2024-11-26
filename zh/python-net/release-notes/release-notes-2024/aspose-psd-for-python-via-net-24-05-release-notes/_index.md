---
title: Aspose.PSD for Python via .NET 24.5 - 发行说明
type: docs
weight: 10
url: /zh/python-net/aspose-psd-for-python-via-net-24-5-release-notes/
---

{{% alert color="primary" %}}

本页面包含[Aspose.PSD for Python via .NET 24.5](https://pypi.org/project/aspose-psd/)的发行说明

{{% /alert %}}

| **关键字**   | **摘要**                                                                                   | **类别**   |
|:------------|:-----------------------------------------------------------------------------------------|:-----------|
| PSDPYTHON-60 | [AI格式] 增加对带有EPSF标头的AI文件处理的支持                                                   | 功能     |
| PSDPYTHON-59 | PSD文件预览中半透明度处理错误                                                                  | 缺陷     |
| PSDPYTHON-61 | 形状图层的渲染部分不正确                                                                      | 缺陷     |
| PSDPYTHON-62 | 保存大小超过200MB且具有大尺寸的PSD文件时出现异常                                            | 缺陷     |
| PSDPYTHON-63 | 从23.7升级到24.3后，保存为PDF时出现图像保存失败的异常                                     | 缺陷     |
| PSDPYTHON-64 | 修复GetFontInfoRecords方法对中文字体的问题                                                 | 缺陷     |

## **公共API更改**
# **已添加的API:**
- P:Aspose.PSD.ImageOptions.PsdOptions.BackgroundContents
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.HasMultiLayerMasks
- P:Aspose.PSD.FileFormats.Ai.AiLayerSection.ColorIndex

# **已移除的API:**
- 无

## **使用示例:**

**PSDPYTHON-59. PSD文件预览中半透明度处理错误**

{{< highlight python >}}
// 在PSD文件预览中，半透明处理不正确。
// BackgroundContents指定为白色。透明区域应为白色。

sourceFile = "frog_nosymb.psd"
outputFile = "frog_nosymb_backgroundcontents_output.psd"

with PsdImage.load(sourceFile) as psdImage:

    backgroundColor = RawColor(PixelDataFormat.rgb_32_bpp, 0)

    argbValue = ctypes.c_int32(255 << 24 | 255 << 16 | 255 << 8 | 255).value

    backgroundColor.set_as_int(argbValue)  # 白色

    psdOptions = PsdOptions(psdImage)
    psdOptions.color_mode = ColorModes.RGB
    psdOptions.compression_method = CompressionMethod.RLE
    psdOptions.channels_count = 4
    psdOptions.background_contents = backgroundColor

    psdImage.save(outputFile, psdOptions)
{{< /highlight >}}

**PSDPYTHON-60. [AI Format] 增加对带有EPSF标头的AI文件处理的支持**

{{< highlight python >}}
sourceFile = "example.ai"
outputFilePath = "example.png"
       
def assert_are_equal(expected, actual):
    if expected != actual:
        raise Exception("对象不相等。")

with AiImage.load(sourceFile) as img:
    image = cast(AiImage, img)
    assert_are_equal(len(image.layers), 2)
    assert_are_equal(image.layers[0].has_multi_layer_masks, False)
    assert_are_equal(image.layers[0].color_index, -1)
    assert_are_equal(image.layers[1].has_multi_layer_masks, False)
    assert_are_equal(image.layers[1].color_index, -1)

    image.save(outputFilePath, PngOptions())

{{< /highlight >}}

**PSDPYTHON-61. 形状图层的渲染部分不正确**

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

**PSDPYTHON-62. 保存大小超过200MB且具有大尺寸的PSD文件时出现异常**

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

**PSDPYTHON-63. 升级自23.7到24.3后，保存为PDF时出现图像保存失败的异常**

{{< highlight python >}}
sourceFile = "CVFlor.psd"
outputFile = "_export.pdf"

with PsdImage.load(sourceFile) as psdImage:
    saveOptions = PdfOptions()
    saveOptions.pdf_core_options = PdfCoreOptions()

    psdImage.save(outputFile, saveOptions)
{{< /highlight >}}

**PSDPYTHON-64. 修复GetFontInfoRecords方法对中文字体的问题**

{{< highlight python >}}
fontFolder = "字体"
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
                    # 在此修复之前，由于中文字体，这里将会出现异常。
                    textLayer.update_text("成功")
finally:
    FontSettings.reset()
    FontSettings.update_fonts()
{{< /highlight >}}
