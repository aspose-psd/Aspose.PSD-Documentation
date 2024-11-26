---
title: Aspose.PSD for Java 23.6 -发布说明
type: docs
weight: 40
url: /zh/java/aspose-psd-for-java-23-6-release-notes/
---

{{% alert color="primary" %}} 本页面包含 [Aspose.PSD for Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) 的发布说明 {{% /alert %}}

| **关键字**   | **摘要**                                                                                       | **类别**     |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | 重构 TimeLine API                                                                              | 增强功能      |
| PSDJAVA-480 | 渲染变形时去除伪影                                                                               | 增强功能      |
| PSDJAVA-481 | 优化变形渲染                                                                                   | 增强功能      |
| PSDJAVA-482 | 支持阈值调整图层                                                                               | 功能特性      |
| PSDJAVA-483 | 支持选择性颜色调整图层                                                                         | 功能特性      |
| PSDJAVA-484 | 能够将 PSD TimeLine 导出为动态 GIF 文件                                                         | 功能特性      |
| PSDJAVA-485 | 添加支持无矩形边框的文本层                                                                     | 功能特性      |
| PSDJAVA-486 | 支持形状图层                                                                                   | 功能特性      |
| PSDJAVA-487 | 替换智能对象中的图像不会更新                                                                   | 错误修复      |
| PSDJAVA-488 | PSD 文件无法保存为 PSD，出现以下异常:Rgb 和 Lab 模式不能包含少于 3 个通道和多于 4 个通道  | 错误修复      |
| PSDJAVA-489 | 通过 Photoshop 的编辑模式打开文本图层会丢失文本对齐                                      | 错误修复      |
| PSDJAVA-490 | 保存 PSD 文件时出现空引用异常                                                                   | 错误修复      |
| PSDJAVA-491 | 加载 ShapeLayer 时出现异常：矢量原点边界的点尚不受支持                                       | 错误修复      |
| PSDJAVA-492 | 加载 VogkResource 时出现异常：点被保存为 DoubleStructures，但我们读取为 UnitStructures | 错误修复      |
| PSDJAVA-493 | ShapeLayer 的图层类型为空                                                                      | 错误修复      |

## **公共 API 更改**
# **添加的 API:**
- M:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet

# **已删除的 API:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

## **使用示例:**

**PSDJAVA-482. 支持阈值调整图层**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
    String outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
    String outputPngWithThresholdLayer = "flowers_threshold_output.png";

    String sourceFileWithoutThresholdLayer = "flowers_source.psd";
    String outputPsdWithoutThresholdLayer = "flowers_output.psd";
    String outputPngWithoutThresholdLayer = "flowers_output.png";

    // 获取、检查和更改图像中的阈值调整图层。
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithThresholdLayer)) {
        for (Layer layer : image.getLayers()) {
            if (layer instanceof ThresholdLayer) {
                // 获取阈值调整图层。
                ThresholdLayer thrsLayer = (ThresholdLayer) layer;
                short level = thrsLayer.getLevel();

                // 检查图层参数。
                assertAreEqual(level, (short) 115);

                // 设置图层参数。
                thrsLayer.setLevel((short) 50);

                image.save(outputPsdWithThresholdLayer);
                image.save(outputPngWithThresholdLayer, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // 添加并设置阈值调整图层到图像中。
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithoutThresholdLayer)) {
        // 添加阈值调整图层。
        ThresholdLayer thresholdLayer = image.addThresholdAdjustmentLayer();

        // 设置图层参数。
        thresholdLayer.setLevel((short) 115);

        image.save(outputPsdWithoutThresholdLayer);
        image.save(outputPngWithoutThresholdLayer, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}
{{< /highlight >}}
... (continues)... (continued from the previous part)

**PSDJAVA-483. 支持选择性颜色调整图层**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String sourceFileWithSelectiveColorLayer = "houses_selectiveColor_source.psd";
    String outputPsdWithSelectiveColorLayer = "houses_selectiveColor_output.psd";
    String outputPngWithSelectiveColorLayer = "houses_selectiveColor_output.png";

    String sourceFileWithoutSelectiveColorLayer = "houses_source.psd";
    String outputPsdWithoutSelectiveColorLayer = "houses_output.psd";
    String outputPngWithoutSelectiveColorLayer = "houses_output.png";

    // 获取、检查和更改图像中的选择性颜色调整图层。
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithSelectiveColorLayer)) {
        for (Layer layer : image.getLayers()) {
            if (layer instanceof SelectiveColorLayer) {
                // 获取选择性颜色调整图层。
                SelectiveColorLayer selcLayer = (SelectiveColorLayer) layer;
                CmykCorrection redCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Reds);
                CmykCorrection yellowCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Yellows);
                CmykCorrection greenCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Greens);
                CmykCorrection blueCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Blues);

                // 检查图层参数。
                assertAreEqual(CorrectionMethodTypes.Absolute, selcLayer.getCorrectionMethod());

                assertAreEqual(redCorrection.getCyan(), (short) -31);
                assertAreEqual(redCorrection.getMagenta(), (short) -12);
                assertAreEqual(redCorrection.getYellow(), (short) 27);
                assertAreEqual(redCorrection.getBlack(), (short) 33);

                assertAreEqual(yellowCorrection.getCyan(), (short) -22);
                assertAreEqual(yellowCorrection.getMagenta(), (short) -19);
                assertAreEqual(yellowCorrection.getYellow(), (short) 8);
                assertAreEqual(yellowCorrection.getBlack(), (short) 0);

                assertAreEqual(greenCorrection.getCyan(), (short) 0);
                assertAreEqual(greenCorrection.getMagenta(), (short) 0);
                assertAreEqual(greenCorrection.getYellow(), (short) 0);
                assertAreEqual(greenCorrection.getBlack(), (short) 0);

                assertAreEqual(blueCorrection.getCyan(), (short) 58);
                assertAreEqual(blueCorrection.getMagenta(), (short) 18);
                assertAreEqual(blueCorrection.getYellow(), (short) 1);
                assertAreEqual(blueCorrection.getBlack(), (short) 7);

                // 更改图层参数。
                selcLayer.setCorrectionMethod(CorrectionMethodTypes.Relative);
                CmykCorrection redsCmykCorrection = new CmykCorrection();
                redsCmykCorrection.setCyan((short) 12);
                redsCmykCorrection.setMagenta((short) -20);
                redsCmykCorrection.setYellow((short) 10);
                redsCmykCorrection.setBlack((short) -15);
                selcLayer.setCmykCorrection(SelectiveColorsTypes.Reds, redsCmykCorrection);

                CmykCorrection whitesCmykCorrection = new CmykCorrection();
                whitesCmykCorrection.setCyan((short) 15);
                whitesCmykCorrection.setMagenta((short) 20);
                whitesCmykCorrection.setYellow((short) -75);
                whitesCmykCorrection.setBlack((short) 42);
                selcLayer.setCmykCorrection(SelectiveColorsTypes.Whites, whitesCmykCorrection);

                image.save(outputPsdWithSelectiveColorLayer);
                image.save(outputPngWithSelectiveColorLayer, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // 添加并设置选择性颜色调整图层到图像中。
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithoutSelectiveColorLayer)) {
        // 添加选择性颜色调整图层。
        SelectiveColorLayer selectiveColorLayer = image.addSelectiveColorAdjustmentLayer();

        // 设置图层参数。
        selectiveColorLayer.setCorrectionMethod(CorrectionMethodTypes.Absolute);

        CmykCorrection whiteCmykCorrection = new CmykCorrection();
        whiteCmykCorrection.setCyan((short) 100);
        whiteCmykCorrection.setMagenta((short) -100);
        whiteCmykCorrection.setYellow((short) 100);
        whiteCmykCorrection.setBlack((short) 0);
        selectiveColorLayer.setCmykCorrection(SelectiveColorsTypes.Whites, whiteCmykCorrection);

        CmykCorrection blacksCmykCorrection = new CmykCorrection();
        blacksCmykCorrection.setCyan((short) 10);
        blacksCmykCorrection.setMagenta((short) 15);
        blacksCmykCorrection.setYellow((short) 17);
        blacksCmykCorrection.setBlack((short) -3);
        selectiveColorLayer.setCmykCorrection(SelectiveColorsTypes.Blacks, blacksCmykCorrection);

        CmykCorrection neutralsCmykCorrection = new CmykCorrection();
        neutralsCmykCorrection.setCyan((short) 45);
        neutralsCmykCorrection.setMagenta((short) 21);
        neutralsCmykCorrection.setYellow((short) -14);
        neutralsCmykCorrection.setBlack((short) 0);
        selectiveColorLayer.setCmykCorrection(SelectiveColorsTypes.Neutrals, neutralsCmykCorrection);

        CmykCorrection magentasCmykCorrection = new CmykCorrection();
        magentasCmykCorrection.setCyan((short) 8);
        magentasCmykCorrection.setMagenta((short) -10);
        magentasCmykCorrection.setYellow((short) -14);
        magentasCmykCorrection.setBlack((short) 25);
        selectiveColorLayer.setCmykCorrection(SelectiveColorsTypes.Magentas, magentasCmykCorrection);

        image.save(outputPsdWithoutSelectiveColorLayer);
        image.save(outputPngWithoutSelectiveColorLayer, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}
{{< /highlight >}}

**PSDJAVA-484. 能够将 PSD TimeLine 导出为动态 GIF 文件**

{{< highlight java >}}
    String sourceFile = "4_animated.psd";
    String outputGif = "out_4_animated.psd.gif";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        psdImage.getTimeline().save(outputGif, new GifOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-487. 替换智能对象中的图像不会更新**

{{< highlight java >}}
    String sourceFile = "neiyi.psd";
    String changeFile = "bg6.png";

    String exportFile = "export.psd";
    String exportImgBefore = "export_before.png";
    String exportImgAfter = "export_after.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof SmartObjectLayer && layer.getName().equals("sucai1")) {
                SmartObjectLayer smartObjectLayer = (SmartObjectLayer) layer;
                smartObjectLayer.replaceContents(changeFile);
                smartObjectLayer.embedLinked();

                break;
            }
        }

        psdImage.save(exportFile, new PsdOptions());
        psdImage.save(exportImgBefore, new PngOptions());
    }

    try (PsdImage psdImage = (PsdImage) Image.load(exportFile)) {
    {
        psdImage.save(exportImgAfter, new PngOptions());
    }
{{< /highlight >}}