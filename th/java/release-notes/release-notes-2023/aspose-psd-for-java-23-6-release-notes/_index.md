---
title: Aspose.PSD for Java 23.6 - บันทึกการอัปเดต
type: docs
weight: 40
url: /th/java/aspose-psd-for-java-23-6-release-notes/
---

{{% alert color="primary" %}} หน้านี้มีบันทึกการอัปเดตสำหรับ [Aspose.PSD for Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Key**     | **สรุป**                                                                                                                                      | **หมวดหมู่** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | ปรับเปลี่ยน TimeLine API                                                                                                                    | สร้างความปรับปรุง  |
| PSDJAVA-480 | ลบอาร์ติฟัคต์เมื่อแสดงภาพพล็อต                                                                                                          | สร้างความปรับปรุง  |
| PSDJAVA-481 | การปรับปรุงการแสดงภาพพล็อต                                                                                                                | สร้างความปรับปรุง  |
| PSDJAVA-482 | รองรับการปรับเปลี่ยนชั้นการปรับปรุงค่าความสะท้อน                                                            | คุณสมบัติ      |
| PSDJAVA-483 | รองรับการปรับเปลี่ยนสีที่เลือกได้ของชั้นการปรับปรุง                                                         | คุณสมบัติ      |
| PSDJAVA-484 | สามารถส่งออก PSD TimeLine เป็นไฟล์ Animated Gif                                                                  | คุณสมบัติ      |
| PSDJAVA-485 | เพิ่มการสนับสนุน TextLayer โดยไม่มีเส้นขอบบริเวณ                                                                   | คุณสมบัติ      |
| PSDJAVA-486 | รองรับ ShapeLayer                                                                                                                     | คุณสมบัติ      |
| PSDJAVA-487 | การเปลี่ยนภาพใน Smart object ไม่ได้รับการอัพเดต                                                                 | ช่องข้อผิดพลาด   |
| PSDJAVA-488 | ไฟล์ PSD ไม่สามารถบันทึกเป็น PSD ด้วยข้อยกเว้นต่อไป: โหมด Rgb และ Lab ไม่สามารถมีน้อยกว่า 3 ช่องและมากกว่า 4 ช่อง  | ช่องข้อผิดพลาด   |
| PSDJAVA-489 | การจัดบังคุณสมบัติของข้อความหายไปหากเปิด TextLayer โดยโหมดแก้ไขของ Photoshop                                        | ช่องข้อผิดพลาด   |
| PSDJAVA-490 | ข้อยกเว้นอ้างอิง Null ในขณะบันทึกไฟล์ PSD                                                                                 | ช่องข้อผิดพลาด   |
| PSDJAVA-491 | ข้อยกเว้นในการโหลด ShapeLayer: จุดสำหรับการกำหนดของเวกเตอร์ไม่ได้รับการรองรับ  | ช่องข้อผิดพลาด   |
| PSDJAVA-492 | ข้อยกเว้นในการโหลด VogkResource: จุดถูกบันทึกเป็น DoubleStructures แต่เราอ่านเป็น UnitStructures  | ช่องข้อผิดพลาด   |
| PSDJAVA-493 | LayerType ของ ShapeLayer ไม่แสดงข้อความ                                                                                     | ช่องข้อผิดพลาด   |

## **การเปลี่ยนแปลงของ Public API**
# **เพิ่ม APIs:**
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
- T:com.aspose.psd.fileformats.psd.layers.animation.Frame
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDelay
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDisposalMethod
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getFrGA
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getId
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.getLayerStates
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDelay(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDisposalMethod(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setFrGA(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setId(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Frame.setLayerStates(com.aspose.psd.fileformats.psd.layers.animation.LayerState[])
- T:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Dispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.DoNotDispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Automatic
- T:com.aspose.psd.fileformats.psd.layers.animation.LayerState
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getFillOpacity
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getHorizontalFXRf
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getId
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getPositionOffset
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getStateEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getVerticalFXRf
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setFillOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setHorizontalFXRf(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setId(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setPositionOffset(com.aspose.psd.Point)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setVerticalFXRf(double)
- T:com.aspose.psd.fileformats.psd.layers.animation.Timeline
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.#ctor
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getAFSt
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getActiveFrameIndex
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrame(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrames
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFramesList
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFsID
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getLoopesCount
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getPsdImage
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(java.lang.String,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(com.aspose.psd.system.io.Stream,com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setAFSt(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFrames(com.aspose.psd.fileformats.psd.layers.animation.Frame[])
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFsID(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setLoopesCount(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setPsdImage(com.aspose.psd.fileformats.psd.PsdImage)
- M:com.aspose.psd.fileformats.psd.layers.animation.Timeline.switchActiveFrame(int)
- T:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addColorOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addDropShadow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addGradientOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addInnerShadow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOuterGlow
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOrReplaceEffect(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addPatternOverlay
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getEffects
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getLayerStyleFX
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getScale
**- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setScale(double)**
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setVisible(boolean)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.clearLayerStyle
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.removeEffectAt(int)
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.isVisible
- T:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getIntensity
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getJitter
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getNoise
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getRange
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSpread
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isAntiAliasing
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isSoftBlend
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isVisible
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setAntiAliasing(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setFillColor(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setIntensity(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setJitter(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setNoise(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setOpacity(byte)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setRange(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSpread(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSoftBlend(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setVisible(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

# **APIs ที่ถูกนำออก:** 

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

## **ตัวอย่างการใช้:**

**PSDJAVA-482. การสนับสนุนโครงสร้างการปรับเปลี่ยน Threshold**

{{< highlight java >}}
    public static void main(String[] args) throws Exception {
        String sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
        String outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
        String outputPngWithThresholdLayer = "flowers_threshold_output.png";

        String sourceFileWithoutThresholdLayer = "flowers_source.psd";
        String outputPsdWithoutThresholdLayer = "flowers_output.psd";
        String outputPngWithoutThresholdLayer = "flowers_output.png";

        // Get, check, and change the Threshold adjustment layer from the image.
        try (PsdImage image = (PsdImage) Image.load(sourceFileWithThresholdLayer)) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof ThresholdLayer) {
                    // Get Threshold adjustment layer.
                    ThresholdLayer thrsLayer = (ThresholdLayer) layer;
                    short level = thrsLayer.getLevel();

                    // Check layers parameters.
                    assertAreEqual(level, (short) 115);

                    // Set layers parameters.
                    thrsLayer.setLevel((short) 50);

                    image.save(outputPsdWithThresholdLayer);
                    image.save(outputPngWithThresholdLayer, new PngOptions());
                }
            }
        } catch (Exception e) {
            e.printStackTrace();
        }

        // Add and set the Threshold adjustment layer to the image.
        try (PsdImage image = (PsdImage) Image.load(sourceFileWithoutThresholdLayer)) {
            // Add Threshold Adjustment layer.
            ThresholdLayer thresholdLayer = image.addThresholdAdjustmentLayer();

            // Set layers parameters.
            thresholdLayer.setLevel((short) 115);

            image.save(outputPsdWithoutThresholdLayer);
            image.save(outputPngWithoutThresholdLayer, new PngOptions());
        } catch (Exception e) {
            e.printStackTrace();
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objects are not equal.");
    }
{{< /highlight >}}

**PSDJAVA-483. การสนับสนุนโครงสร้างการปรับเปลี่ยนสีที่เลือกได้**

{{< highlight java >}}
    public static void main(String[] args) throws Exception {
        String sourceFileWithSelectiveColorLayer = "houses_selectiveColor_source.psd";
        String outputPsdWithSelectiveColorLayer = "houses_selectiveColor_output.psd";
        String outputPngWithSelectiveColorLayer = "houses_selectiveColor_output.png";

        String sourceFileWithoutSelectiveColorLayer = "houses_source.psd";
        String outputPsdWithoutSelectiveColorLayer = "houses_output.psd";
        String outputPngWithoutSelectiveColorLayer = "houses_output.png";

        // Get, check, and change the Selective Color adjustment layer from the image.
        try (PsdImage image = (PsdImage) Image.load(sourceFileWithSelectiveColorLayer)) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof SelectiveColorLayer) {
                    // Get Selective Color adjustment layer.
                    SelectiveColorLayer selcLayer = (SelectiveColorLayer) layer;
                    CmykCorrection redCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Reds);
                    CmykCorrection yellowCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Yellows);
                    CmykCorrection greenCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Greens);
                    CmykCorrection blueCorrection = selcLayer.getCmykCorrection(SelectiveColorsTypes.Blues);

                    // Check layers parameters.
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

                    // Change layers parameters.
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

        // Add and set the Selective color adjustment layer to the image.
        try (PsdImage image = (PsdImage) Image.load(sourceFileWithoutSelectiveColorLayer)) {
            // Add Selective Color Adjustment layer.
            SelectiveColorLayer selectiveColorLayer = image.addSelectiveColorAdjustmentLayer();

            // Set layers parameters.
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
            magentasCmykCorrection.setY
        image.save(outputPsdWithoutSelectiveColorLayer);
        image.save(outputPngWithoutSelectiveColorLayer, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}
{{< /highlight >}}