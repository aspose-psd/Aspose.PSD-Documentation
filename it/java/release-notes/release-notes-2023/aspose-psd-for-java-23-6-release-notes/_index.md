---
title: Note sulla versione di Aspose.PSD per Java 23.6
type: docs
weight: 40
url: /it/java/aspose-psd-for-java-23-6-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.6/) {{% /alert %}}

| **Chiave**     | **Sommario**                                                                                                                                      | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Refactoring dell'API TimeLine                                                                                                                    | Miglioramento  |
| PSDJAVA-480 | Rimozione degli artefatti durante il rendering della deformazione                                                                                 | Miglioramento  |
| PSDJAVA-481 | Ottimizzazione del rendering della deformazione                                                                                                  | Miglioramento  |
| PSDJAVA-482 | Supporto del livello di regolazione della soglia                                                                                                 | Funzionalità   |
| PSDJAVA-483 | Supporto del livello di regolazione del colore selettivo                                                                                         | Funzionalità   |
| PSDJAVA-484 | Possibilità di esportare la TimeLine PSD nel file Gif animato                                                                                    | Funzionalità   |
| PSDJAVA-485 | Aggiunta del supporto per il TextLayer senza bordi rettangolari                                                                                  | Funzionalità   |
| PSDJAVA-486 | Supporto del livello di forma                                                                                                                   | Funzionalità   |
| PSDJAVA-487 | La sostituzione dell'immagine in Smart object non si aggiorna                                                                                    | Errore        |
| PSDJAVA-488 | Impossibile salvare il file PSD come PSD con l'eccezione seguente: Le modalità Rgb e Lab non possono contenere meno di 3 canali e più di 4 canali   | Errore        |
| PSDJAVA-489 | La giustificazione del testo viene persa se si apre il TextLayer dalla modalità di modifica di Photoshop                                           | Errore        |
| PSDJAVA-490 | Eccezione di riferimento nullo durante il salvataggio del file PSD                                                                               | Errore        |
| PSDJAVA-491 | Eccezione durante il caricamento dello ShapeLayer: i punti per i limiti dell'origine vettoriale non sono ancora supportati                        | Errore        |
| PSDJAVA-492 | Eccezione durante il caricamento di VogkResource: i punti sono salvati come DoubleStructures, li leggiamo come UnitStructures                   | Errore        |
| PSDJAVA-493 | LayerType di ShapeLayer è vuoto                                                                                                                  | Errore        |

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- M: com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F: com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- M: com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- M: com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- M: com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- M: com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- M: com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- M: com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- M: com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- M: com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- M: com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- M: com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- M: com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- M: com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- M: com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T: com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F: com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- M: com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
- T: com.aspose.psd.fileformats.psd.layers.animation.Frame
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.#ctor
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.getDelay
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.getDisposalMethod
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.getFrGA
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.getId
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.getLayerStates
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.setDelay(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.setDisposalMethod(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.setFrGA(double)
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.setId(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Frame.setLayerStates(com.aspose.psd.fileformats.psd.layers.animation.LayerState[])
- T: com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod
- F: com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Dispose
- F: com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.DoNotDispose
- F: com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Automatic
- T: com.aspose.psd.fileformats.psd.layers.animation.LayerState
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.#ctor
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getBlendMode
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getEnabled
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getFillOpacity
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getHorizontalFXRf
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getId
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getOpacity
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getPositionOffset
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getStateEffects
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.getVerticalFXRf
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setBlendMode(long)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setEnabled(boolean)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setFillOpacity(double)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setHorizontalFXRf(double)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setId(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setOpacity(double)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setPositionOffset(com.aspose.psd.Point)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerState.setVerticalFXRf(double)
- T: com.aspose.psd.fileformats.psd.layers.animation.Timeline
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.#ctor
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getAFSt
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getActiveFrameIndex
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrame(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrames
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFramesList
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFsID
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getLoopesCount
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.getPsdImage
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(java.lang.String,com.aspose.psd.ImageOptionsBase)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(com.aspose.psd.system.io.Stream,com.aspose.psd.ImageOptionsBase)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.setAFSt(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFrames(com.aspose.psd.fileformats.psd.layers.animation.Frame[])
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFsID(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.setLoopesCount(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.setPsdImage(com.aspose.psd.fileformats.psd.PsdImage)
- M: com.aspose.psd.fileformats.psd.layers.animation.Timeline.switchActiveFrame(int)
- T: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addColorOverlay
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addDropShadow
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addGradientOverlay
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addInnerShadow
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOuterGlow
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOrReplaceEffect(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addPatternOverlay
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addStroke(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getEffects
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getLayerStyleFX
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getScale
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setScale(double)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setVisible(boolean)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.clearLayerStyle
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.removeEffectAt(int)
- M: com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.isVisible
- T: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getBlendMode
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getEffectType
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getFillColor
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getIntensity
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getJitter
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getNoise
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getOpacity
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getRange
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSpread
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSize
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isAntiAliasing
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isSoftBlend
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isVisible
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setAntiAliasing(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setBlendMode(long)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setFillColor(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setIntensity(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setJitter(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setNoise(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setOpacity(byte)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setRange(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSpread(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSoftBlend(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSize(int)
- M: com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setVisible(boolean)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor
- T: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.#ctor
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getKey
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLayers
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength(int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getPsdVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getSignature
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.save(com.aspose.psd.StreamContainer,int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

# **API Rimosse:**

- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getPsdVersion
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getSignature
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.save(com.aspose.psd.StreamContainer,int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor(int)															   
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getKey																	  
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLayers
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getLength
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getPsdVersion																			 
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.getSignature
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.save(com.aspose.psd.StreamContainer,int)
- M: com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

## **Esempi d'uso:**

**PSDJAVA-482. Supporto del livello di regolazione della soglia**

{{< highlight java >}}
public static void main(String[] args) throws Exception {
    String sourceFileWithThresholdLayer = "flowers_threshold_source.psd";
    String outputPsdWithThresholdLayer = "flowers_threshold_output.psd";
    String outputPngWithThresholdLayer = "flowers_threshold_output.png";

    String sourceFileWithoutThresholdLayer = "flowers_source.psd";
    String outputPsdWithoutThresholdLayer = "flowers_output.psd";
    String outputPngWithoutThresholdLayer = "flowers_output.png";

    // Ottenere, controllare e modificare il livello di regolazione della soglia dall'immagine.
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithThresholdLayer)) {
        for (Layer layer : image.getLayers()) {
            if (layer instanceof ThresholdLayer) {
                // Ottenere il livello di regolazione della soglia.
                ThresholdLayer thrsLayer = (ThresholdLayer) layer;
                short level = thrsLayer.getLevel();

                // Controllare i parametri dei livelli.
                assertAreEqual(level, (short) 115);

                // Impostare i parametri dei livelli.
                thrsLayer.setLevel((short) 50);

                image.save(outputPsdWithThresholdLayer);
                image.save(outputPngWithThresholdLayer, new PngOptions());
            }
        }
    } catch (Exception e) {
        e.printStackTrace();
    }

    // Aggiungere e impostare il livello di regolazione della soglia all'immagine.
    try (PsdImage image = (PsdImage) Image.load(sourceFileWithoutThresholdLayer)) {
        // Aggiungere il livello di regolazione della soglia.
        ThresholdLayer thresholdLayer = image.addThresholdAdjustmentLayer();

        // Impostare i parametri dei livelli.
        thresholdLayer.setLevel((short) 115);

        image.save(outputPsdWithoutThresholdLayer);
        image.save(outputPngWithoutThresholdLayer, new PngOptions());
    } catch (Exception e) {
        e.printStackTrace();
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
}
{{< /highlight >}}