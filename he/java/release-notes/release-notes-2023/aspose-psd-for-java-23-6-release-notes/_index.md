---
title: Aspose.PSD for Java 23.6 - הערות לגרסה
type: docs
weight: 40
url: /he/java/aspose-psd-for-java-23-6-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל הערות לגרסה עבור [Aspose.PSD for Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}


| **מפתח**     | **סיכום**                                                                                                                                      | **קטגוריה** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Refactor API של TimeLine                                                                                                                            | שיפור  |
| PSDJAVA-480 | מהפך אפקטים בעת עיבוד של קערה                                                                                                             | שיפור  |
| PSDJAVA-481 | אופטימיזציה של עיבוד של קערה                                                                                                                      | שיפור  |
| PSDJAVA-482 | תמיכה בשכבת התאמת סף                                                                                                            | תכונה      |
| PSDJAVA-483 | תמיכה בשכבת התיקון בצבעים באופן סלקטיבי                                                                                                      | תכונה      |
| PSDJAVA-484 | אפשרות לייצא זמן PSD לקובץ Gif מונפש                                                                                          | תכונה      |
| PSDJAVA-485 | הוספת תמיכה לשכבת טקסט ללא גבולות מרחביים                                                                                           | תכונה      |
| PSDJAVA-486 | תמיכה בשכבת צורה                                                                                                                             | תכונה      |
| PSDJAVA-487 | החלפת תמונה באובייקט חכם אינה מעדכנת                                                                                                  | באג          |
| PSDJAVA-488 | לא ניתן לשמור קובץ PSD כקובץ PSD עם החרפה הבאה: מצבי Rgb ו-Lab לא יכולים להכיל פחות מ-3 ערוצים ויותר מ-4 ערוצים   | באג          |
| PSDJAVA-489 | היישור של הטקסט נמאס אם נפתח את שכבת הטקסט במצב עריכה של פוטושופ                                                                         | באג          |
| PSDJAVA-490 | חריגת התייחסות ריקה בעת שמירת קובץ PSD                                                                                                     | באג          |
| PSDJAVA-491 | חריגה בעת טעינת שכבת הצורה: נקודות לשורש המצורף לא נתמכות עדיין                                                  | באג          |
| PSDJAVA-492 | חריגה בטעינת Vogk קישור: נקודות נשמרות כמבנה Double, אנו קוראים כ-מבנה יחיד                                                                     | באג          |
| PSDJAVA-493 | סוג השכבה של שכבת צורה ריק                                                              | באג          |

## **שינויים בAPI הציבורי**

# **API חדשות:**
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
- M:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setScale(double)
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

# **API הוסרו:**

- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psdlayers.layerresources.Lr16Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLayers
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

## **דוגמאות שימוש:**

**PSDJAVA-482. תמיכה בשכבת התאמת סף**

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

**PSDJAVA-483. תמיכה בשכבת התיקון בצבעים באופן סלקטיבי**

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
        magentasCmykCorrection.setYellow((short) -14);
        magentasCmykCorrection.setBlack((short) 25);
        selectiveColorLayer.setCmykCorrection(SelectiveColorsTypes.Magentas, magentasCmykCorrection);

        image.save(outputPsdWithoutSelectiveColorLayer);
        image.save(outputPngWithoutSelectiveColorLayer, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objects are not equal.");
}
{{< /highlight >}}

**PSDJAVA-484. אפשרות לייצא זמן PSD לקובץ Gif מונפש**

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

**PSDJAVA-487. החלפת תמונה באובייקט חכם אינה מעדכנת**

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

**PSDJAVA-479. Refactor API של TimeLine**

{{< highlight java >}}
    String sourceFile = "4_animated.psd";
    String outputFile = "output_edited.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        Timeline timeline = psdImage.getTimeline();

        // Add one more frame
        List<Frame> frames = new List<Frame>(timeline.getFrames());
        frames.add(new Frame());
        timeline.setFrames(frames.toArray(new Frame[0]));

        timeline.switchActiveFrame(4);

        psdImage.save(outputFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-488. לא ניתן לשמור קובץ PSD כקובץ PSD עם החרפה הבאה: מצבי Rgb ו-Lab לא יכולים להכיל פחות מ-3 ערוצים ויותר מ-4 ערוצים**

{{< highlight java >}}
    String sourceFile = "Ex3_B1H1_Dave_Arthur.psd";
    String exportPath = "export.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // It takes default saving options from header but header has wrong number of channels.
        try {
            image.save(exportPath);
        } catch (PsdImageException ex) {
            if (ex.getMessage() != "Rgb and Lab modes can not contain less than 3 channels and more than 4 channels") {
                throw new Exception("It is wrong PsdImageException");
            }
        }

        // Without error
        image.save(exportPath, new PsdOptions());
    }
{{< /highlight >}}

**PSDJAVA-480. מהפך אפקטים בעת עיבוד של קערה**

{{< highlight java >}}
    String sourceFile = "smart_Test.psd";
    String changeFile = "newImage.png";

    String exportFile = "export.psd";
    String exportImg = "export_new.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof SmartObjectLayer)
            {
                SmartObjectLayer smartObjectLayer = (SmartObjectLayer)layer;
                smartObjectLayer.replaceContents(changeFile);
                smartObjectLayer.embedLinked();

                break;
            }
        }

        psdImage.save(exportFile, new PsdOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);

    try (PsdImage psdImage = (PsdImage) Image.load(exportFile, psdLoadOptions)) {
        psdImage.save(exportImg, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-481. אופטימיזציה של עיבוד של קערה**

{{< highlight java >}}
    String sourceFile = "Bottom_Right.psd";
    String exportFile = "output.png";

    DateTime dtStart = DateTime.getNow();

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        psdImage.save(exportFile, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }

    DateTime dtFinish = DateTime.getNow();

    double totalSeconds = TimeSpan.fromTicks(dtFinish.getTicks()).getTotalSeconds() 
            - TimeSpan.fromTicks(dtStart.getTicks()).getTotalSeconds();

    final int MaxAllowableSecunds = 5;

    // Old rendering time was about 1 minute
    if (totalSeconds > MaxAllowableSecunds)
    {
        throw new Exception("Rendering so low, and is " + totalSeconds);
    }
{{< /highlight >}}

**PSDJAVA-489. היישור של הטקסט נמאס אם נפתח את שכבת הטקסט במצב עריכה של פוטושופ**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String sourceFile = "input-test.psd";
    String outputFile = "output.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        IText textData = ((TextLayer) psdImage.getLayers()[2]).getTextData();

        ITextStyle defaultStyle = textData.getItems()[0].getStyle();
        ITextParagraph defaultParagraph = textData.getItems()[0].getParagraph();
        defaultParagraph.setJustification(JustificationMode.Center);
        textData.removePortion(0);

        addTextPortion("Lorem Ipsum", textData,