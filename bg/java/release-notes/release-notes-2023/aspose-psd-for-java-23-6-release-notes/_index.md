---
title: Издание на Aspose.PSD за Java 23.6 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-6-belezhki-za-izdanieto/
---

{{< alert color="primary" >}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 23.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-za-java-23.6/) {{< /alert >}}

| **Ключ**     | **Резюме**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-479 | Преобразуване на TimeLine API                                                                                                                            | Подобрение  |
| PSDJAVA-480 | Премахнете артефактите при извършване на изкривяване                                                                                                             | Подобрение  |
| PSDJAVA-481 | Оптимизация на изкривяването на изкривяването                                                                                                                      | Подобрение  |
| PSDJAVA-482 | Поддръжка на слой за корекция на прага                                                                                                            | Функция      |
| PSDJAVA-483 | Поддръжка на слой за корекция с избирателни цветове                                                                                                      | Функция      |
| PSDJAVA-484 | Възможност за изнасяне на PSD TimeLine в файл Animated Gif                                                                                          | Функция      |
| PSDJAVA-485 | Добавяне на поддръжка за TextLayer без правоъгълни граници                                                                                            | Функция      |
| PSDJAVA-486 | Поддръжка на ShapeLayer                                                                                                                            | Функция      |
| PSDJAVA-487 | Замяна на изображение в умния обект не се актуализира                                                                                                  | Грешка          |
| PSDJAVA-488 | Файлът PSD не може да бъде запазен като PSD със следното изключение: Rgb и Lab режимите не могат да съдържат по-малко от 3 канала и повече от 4 канала   | Грешка          |
| PSDJAVA-489 | Подравняването на текста се губи при отварянето на TextLayer чрез режима за редактиране на Photoshop                                                                       | Грешка          |
| PSDJAVA-490 | Изключение за нулевата референция при запазване на PSD файл                                                                                                      | Грешка          |
| PSDJAVA-491 | Изключение при зареждане на ShapeLayer: Точките за оригиналните граници на вектора все още не се поддържат                                                   | Грешка          |
| PSDJAVA-492 | Изключение при зареждане на VogkResource: Точките се запазват като DoubleStructures, ние ги четем като UnitStructures                                            | Грешка          |
| PSDJAVA-493 | LayerType на ShapeLayer е празен                                                                                                                 | Грешка          |

## **Промени в публичното API**
# **Добавени API:**
- М:com.aspose.psd.PixelDataFormat.getRgba64Bpp
- F:com.aspose.psd.fileformats.psd.PsdImage.horizontalResolution
- М:com.aspose.psd.fileformats.psd.PsdImage.addSelectiveColorAdjustmentLayer
- М:com.aspose.psd.fileformats.psd.PsdImage.addVibranceAdjustmentLayer
- М:com.aspose.psd.fileformats.psd.PsdImage.addThresholdAdjustmentLayer
- М:com.aspose.psd.fileformats.psd.PsdImage.getTimeline
- М:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getColorMode
- М:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setColorMode(short)
- М:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.getAngle
- М:com.aspose.psd.fileformats.psd.layers.fillsettings.IPatternFillSettings.setAngle(double)
- М:com.aspose.psd.fileformats.psd.layers.fillsettings.PatternFillSettings.getAngle
- М:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat,short)
- М:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorMode
- М:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setColorMode(short)
- М:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.getSubResources
- М:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.getPointsUnitType
- М:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorShapeBoundingBox.setPointsUnitType(int)
- T:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Horizontal
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.TextOrientation.Vertical
- М:com.aspose.psd.imageoptions.PsdOptions.isColorModeSet
- T:com.aspose.psd.fileformats.psd.layers.animation.Frame
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.#ctor
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDelay
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.getDisposalMethod
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.getFrGA
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.getId
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.getLayerStates
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDelay(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.setDisposalMethod(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.setFrGA(double)
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.setId(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Frame.setLayerStates(com.aspose.psd.fileformats.psd.layers.animation.LayerState[])
- T:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Dispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.DoNotDispose
- F:com.aspose.psd.fileformats.psd.layers.animation.FrameDisposalMethod.Automatic
- T:com.aspose.psd.fileformats.psd.layers.animation.LayerState
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.#ctor
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getBlendMode
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getEnabled
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getFillOpacity
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getHorizontalFXRf
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getId
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getOpacity
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getPositionOffset
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getStateEffects
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.getVerticalFXRf
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setBlendMode(long)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setEnabled(boolean)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setFillOpacity(double)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setHorizontalFXRf(double)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setId(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setOpacity(double)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setPositionOffset(com.aspose.psd.Point)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerState.setVerticalFXRf(double)
- Т:com.aspose.psd.fileformats.psd.layers.animation.Timeline
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.#ctor
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getAFSt
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getActiveFrameIndex
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrame(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFrames
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFramesList
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getFsID
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getLoopesCount
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.getPsdImage
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(java.lang.String,com.aspose.psd.ImageOptionsBase)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.save(com.aspose.psd.system.io.Stream,com.aspose.psd.ImageOptionsBase)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setAFSt(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFrames(com.aspose.psd.fileformats.psd.layers.animation.Frame[])
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setFsID(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setLoopesCount(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.setPsdImage(com.aspose.psd.fileformats.psd.PsdImage)
- М:com.aspose.psd.fileformats.psd.layers.animation.Timeline.switchActiveFrame(int)
- Т:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addColorOverlay
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addDropShadow
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addGradientOverlay
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addInnerShadow
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOuterGlow
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addOrReplaceEffect(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addPatternOverlay
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.addStroke(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getEffects
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getLayerStyleFX
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.getScale
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setScale(double)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.setVisible(boolean)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.clearLayerStyle
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.removeEffectAt(int)
- М:com.aspose.psd.fileformats.psd.layers.animation.LayerStateEffects.isVisible
- Т:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getBlendMode
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getEffectType
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getFillColor
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getIntensity
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getJitter
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getNoise
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getOpacity
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getRange
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSpread
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.getSize
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isAntiAliasing
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isSoftBlend
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.isVisible
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setAntiAliasing(boolean)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setBlendMode(long)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setFillColor(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setIntensity(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setJitter(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setNoise(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setOpacity(byte)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setRange(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSpread(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSoftBlend(boolean)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setSize(int)
- М:com.aspose.psd.fileformats.psd.layers.layereffects.OuterGlowEffect.setVisible(boolean)
- М:com.aspose.psd.fileformats.psd.layers.layerresources.Lr32Resource.#ctor
- Т:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.#ctor
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getKey
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLayers
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getLength(int)
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getPsdVersion
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.getSignature
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.save(com.aspose.psd.StreamContainer,int)
- М:com.aspose.psd.fileformats.psd.layers.layerresources.LrXxResource.setLayers(com.aspose.psd.fileformats.psd.layers.Layer[])

# **Премахнати API:**

- М:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getKey
- М:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLayers
- М:com.aspose.psd.fileformats.psd.layers.layerresources.Lr16Resource.getLength