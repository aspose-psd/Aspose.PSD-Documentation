---
title: Aspose.PSD pro Java 23.6 - Release Notes
type: docs
weight: 40
url: /cs/aspose-psd-pro-java-23-6-release-notes/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Klíč**    | **Shrnutí**                                                                                                                                      | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Refaktorovat API s časovou osou                                                                                                                   | Vylepšení    |
| PSDJAVA-480 | Odebrat artefakty při vykreslování deformace                                                                                                      | Vylepšení    |
| PSDJAVA-481 | Optimalizace vykreslování deformace                                                                                                               | Vylepšení    |
| PSDJAVA-482 | Podpora vrstvy přizpůsobení prahu                                                                                                                 | Funkce       |
| PSDJAVA-483 | Podpora vrstvy selektivní korekce barev                                                                                                           | Funkce       |
| PSDJAVA-484 | Schopnost exportovat časovou osu PSD do souboru s animovaným gifem                                                                                | Funkce       |
| PSDJAVA-485 | Přidání podpory pro Textovou vrstvu bez obdélníkových hranic                                                                                      | Funkce       |
| PSDJAVA-486 | Podpora Vrstvy tvaru                                                                                                                             | Funkce       |
| PSDJAVA-487 | Nahrazení obrázku ve Smart objektu neaktualizuje                                                                                                 | Chyba        |
| PSDJAVA-488 | Soubor PSD nelze uložit jako PSD s následující výjimkou: Režimy Rgb a Lab nemohou obsahovat méně než 3 kanály a více než 4 kanály          | Chyba        |
| PSDJAVA-489 | Zarovnání textu se ztrácí při otevření Vrstvy s textem v editačním režimu Photoshopu                                                              | Chyba        |
| PSDJAVA-490 | Výjimka s nulovým odkazem při ukládání souboru PSD                                                                                                | Chyba        |
| PSDJAVA-491 | Výjimka při načítání Vrstvy tvaru: Body pro původní mez obrázkem nejsou podporovány                                                                        | Chyba        |
| PSDJAVA-492 | Výjimka při načítání VogkResource: Body jsou uloženy jako DoubleStructures, my čteme jako UnitStructures                                        | Chyba        |
| PSDJAVA-493 | Typ vrstvy Vrstvy tvaru je prázdný                                                                                                               | Chyba        |

## **Změny ve veřejném API**
# **Přidaná API:**

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

# **Odstraněná API:**

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

## **Příklady použití:**

**PSDJAVA-482. Podpora vrstvy přizpůsobení prahu**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String souborZdrojeSPrahem = "flowers_threshold_source.psd";
    String výstupníPsdSPrahem = "flowers_threshold_output.psd";
    String výstupníPngSPrahem = "flowers_threshold_output.png";

    String souborBezPrahu = "flowers_source.psd";
    String výstupníPsdBezPrahu = "flowers_output.psd";
    String výstupníPngBezPrahu = "flowers_output.png";

    // Získejte, zkontrolujte a změňte vrstvu úpravy prahu ze snímku.
    try (PsdImage image = (PsdImage) Image.load(souborZdrojeSPrahem)) {
        for (Layer vrstva : image.getLayers()) {
            if (vrstva instanceof ThresholdLayer) {
                // Získejte vrstvu úpravy prahu.
                ThresholdLayer vrstvaPrah = (ThresholdLayer) vrstva;
                short úroveň = vrstvaPrah.getLevel();

                // Ověřte parametry vrstvy.
                assertAreEqual(úroveň, (short) 115);

                // Nastavte parametry vrstvy.
                vrstvaPrah.setLevel((short) 50);

                image.save(výstupníPsdSPrahem);
                image.save(výstupníPngSPrahem, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // Přidejte a nastavte vrstvu úpravy prahu do snímku.
    try (PsdImage image = (PsdImage) Image.load(souborBezPrahu)) {
        // Přidejte vrstvu úpravy prahu.
        ThresholdLayer vrstvaPrah = image.addThresholdAdjustmentLayer();

        // Nastavte parametry vrstvy.
        vrstvaPrah.setLevel((short) 115);

        image.save(výstupníPsdBezPrahu);
        image.save(výstupníPngBezPrahu, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}
{{< /highlight >}}

**PSDJAVA-483. Podpora vrstvy selektivní korekce barev**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String souborSeSelektivníKorekcíBarev = "houses_selectiveColor_source.psd";
    String výstupníPsdSeSelektivníKorekcíBarev = "houses_selectiveColor_output.psd";
    String výstupníPngSeSelektivníKorekcíBarev = "houses_selectiveColor_output.png";

    String souborBezSelektivníKorekceBarev = "houses_source.psd";
    String výstupníPsdBezSelektivníKorekceBarev = "houses_output.psd";
    String výstupníPngBezSelektivníKorekceBarev = "houses_output.png";

    // Získejte, zkontrolujte a změňte vrstvu selektivní korekce barev ze snímku.
    try (PsdImage image = (PsdImage) Image.load(souborSeSelektivníKorekcíBarev)) {
        for (Layer vrstva : image.getLayers()) {
            if (vrstva instanceof SelectiveColorLayer) {
                // Získejte vrstvu selektivní korekce barev.
                SelectiveColorLayer vrstvaSelektivníchBarev = (SelectiveColorLayer) vrstva;
                CmykCorrection korekceČervené = vrstvaSelektivníchBarev.getCmykCorrection(SelectiveColorsTypes.Reds);
                CmykCorrection korekceŽluté = vrstvaSelektivníchBarev.getCmykCorrection(SelectiveColorsTypes.Yellows);
                CmykCorrection korekceZelené = vrstvaSelektivníchBarev.getCmykCorrection(SelectiveColorsTypes.Greens);
                CmykCorrection korekceModré = vrstvaSelektivníchBarev.getCmykCorrection(SelectiveColorsTypes.Blues);

                // Ověřte parametry vrstvy.
                assertAreEqual(CorrectionMethodTypes.Absolute, vrstvaSelektivníchBarev.getCorrectionMethod());

                assertAreEqual(korekceČervené.getCyan(), (short) -31);
                assertAreEqual(korekceČervené.getMagenta(), (short) -12);
                assertAreEqual(korekceČervené.getYellow(), (short) 27);
                assertAreEqual(korekceČervené.getBlack(), (short) 33);

                assertAreEqual(korekceŽluté.getCyan(), (short) -22);
                assertAreEqual(korekceŽluté.getMagenta(), (short) -19);
                assertAreEqual(korekceŽluté.getYellow(), (short) 8);
                assertAreEqual(korekceŽluté.getBlack(), (short) 0);

                assertAreEqual(korekceZelené.getCyan(), (short) 0);
                assertAreEqual(korekceZelené.getMagenta(), (short) 0);
                assertAreEqual(korekceZelené.getYellow(), (short) 0);
                assertAreEqual(korekceZelené.getBlack(), (short) 0);

                assertAreEqual(korekceModré.getCyan(), (short) 58);
                assertAreEqual(korekceModré.getMagenta(), (short) 18);
                assertAreEqual(korekceModré.getYellow(), (short) 1);
                assertAreEqual(korekceModré.getBlack(), (short) 7);

                // Změňte parametry vrstvy.
                vrstvaSelektivníchBarev.setCorrectionMethod(CorrectionMethodTypes.Relative);
                CmykCorrection korekceČervenéNastavené = new CmykCorrection();
                korekceČervenéNastavené.setCyan((short) 12);
                korekceČervenéNastavené.setMagenta((short) -20);
                korekceČervenéNastavené.setYellow((short) 10);
                korekceČervenéNastavené.setBlack((short) -15);
                vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Reds, korekceČervenéNastavené);

                CmykCorrection korekceBílé = new CmykCorrection();
                korekceBílé.setCyan((short) 15);
                korekceBílé.setMagenta((short) 20);
                korekceBílé.setYellow((short) -75);
                korekceBílé.setBlack((short) 42);
                vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Whites, korekceBílé);

                image.save(výstupníPsdSeSelektivníKorekcíBarev);
                image.save(výstupníPngSeSelektivníKorekcíBarev, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // Přidejte a nastavte vrstvu selektivní korekce barev do snímku.
    try (PsdImage image = (PsdImage) Image.load(souborBezSelektivníKorekceBarev)) {
        // Přidejte vrstvu selektivní korekce barev.
        SelectiveColorLayer vrstvaSelektivníchBarev = image.addSelectiveColorAdjustmentLayer();

        // Nastavte parametry vrstvy.
        vrstvaSelektivníchBarev.setCorrectionMethod(CorrectionMethodTypes.Absolute);

        CmykCorrection korekceBílé = new CmykCorrection();
        korekceBílé.setCyan((short) 100);
        korekceBílé.setMagenta((short) -100);
        korekceBílé.setYellow((short) 100);
        korekceBílé.setBlack((short) 0);
        vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Whites, korekceBílé);

        CmykCorrection korekceČerné = new CmykCorrection();
        korekceČerné.setCyan((short) 10);
        korekceČerné.setMagenta((short) 15);
        korekceČerné.setYellow((short) 17);
        korekceČerné.setBlack((short) -3);
        vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Blacks, korekceČerné);

        CmykCorrection korekceNeutrální = new CmykCorrection();
        korekceNeutrální.setCyan((short) 45);
        korekceNeutrální.setMagenta((short) 21);
        korekceNeutrální.setYellow((short) -14);
        korekceNeutrální.setBlack((short) 0);
        vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Neutrals, korekceNeutrální);
        
        CmykCorrection korekceMagenta = new CmykCorrection();
        korekceMagenta.setCyan((short) 8);
        korekceMagenta.setMagenta((short) -10);
        korekceMagenta.setYellow((short) -14);
        korekceMagenta.setBlack((short) 25);
        vrstvaSelektivníchBarev.setCmykCorrection(SelectiveColorsTypes.Magentas, korekceMagenta);

        image.save(výstupníPsdBezSelektivníKorekceBarev);
        image.save(výstupníPngBezSelektivníKorekceBarev, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}
{{< /highlight >}}

**PSDJAVA-484. Schopnost exportovat časovou osu PSD do souboru s animovaným gifem**

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

**PSDJAVA-487. Nahrazení obrázku ve Smart objektu neaktualizuje**

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

**PSDJAVA-479. Refaktorovat API s časovou osou**

{{< highlight java >}}
    String sourceFile = "4_animated.psd";
    String outputFile = "output_edited.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        Timeline timeline = psdImage.getTimeline();

        // Přidejte ještě jeden snímek
        List<Frame> snímky = new List<Frame>(timeline.getFrames());
        snímky.add(new Frame());
        timeline.setFrames(snímky.toArray(new Frame[0]));

        timeline.switchActiveFrame(4);

        psdImage.save(outputFile);
    } catch (Exception e) {
        e.printStackTrace();
    }
{{< /highlight >}}

**PSDJAVA-488. Soubor PSD nelze uložit jako PSD s následující výjimkou: Režimy Rgb a Lab nemohou obsahovat méně než 3 kanály a více než 4 kanály**

{{< highlight java >}}
    String sourceFile = "Ex3_B1H1_Dave_Arthur.psd";
    String exportPath = "export.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        // Přijímá výchozí uložení z možností hlavičky, ale hlavička má nesprávný počet kanálů.
        try {
            image.save(exportPath);
        } catch (PsdImageException ex) {
            if (!ex.getMessage().equals("Režimy Rgb a Lab nemohou obsahovat méně než 3 kanály a více než 4 kanály")) {
                throw new Exception("Je to chybná výjimka PsdImage");
            }
        }

        // Bez chyby
        image.save(exportPath, new PsdOptions());
    }
{{< /highlight >}}

**PSDJAVA-480. Odebrat artefakty při vykreslování deformace**

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

**PSDJAVA-481. Optimalizace vykreslování deformace**

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

    // Stará doba vykreslování byla asi 1 minuta
   