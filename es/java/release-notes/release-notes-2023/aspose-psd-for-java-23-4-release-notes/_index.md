---
title: Aspose.PSD for Java 23.4 - Notas de la versión
type: docs
weight: 40
url: /es/java/aspose-psd-for-java-23-4-notas-de-la-version/
---

{{% alert color="primary" %}} Esta página contiene notas de la versión de [Aspose.PSD para Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDJAVA-446|Portar funcionalidades omitidas de Aspose.PSD para .Net a Aspose.PSD para Java|Mejora|
|PSDJAVA-441|Diseñar la clase RawColor para la API pública y usarla en la API PSD en lugar de la estructura Color obsoleta|Mejora|
|PSDJAVA-418|Integrar Licencia Moderna de Aspose para Aspose.PSD|Mejora|
|PSDJAVA-445|Movimiento de formato al editar en photoshop|Error|
|PSDJAVA-443|La edición de texto usando Porciones de Texto no guarda el resultado correcto|Error|
|PSDJAVA-444|El inicio y fin de los estilos o párrafos aparece en un lugar incorrecto al editar la Capa de Texto por ITextPortion|Error|

# **Cambios en la API Pública**
# **APIs Agregadas:**
- M:com.aspose.psd.FontSettings.getFontReplacements(java.lang.String)
- M:com.aspose.psd.FontSettings.getReplacementFont(java.lang.String)
- M:com.aspose.psd.FontSettings.setAllowedFonts(java.lang.String[])
- M:com.aspose.psd.FontSettings.setFontReplacements(java.lang.String,java.lang.String[])
- M:com.aspose.psd.FontSettings.isFontAllowed(java.lang.String)
- M:com.aspose.psd.License.setLicense(java.io.File)
- M:com.aspose.psd.License.getRenewSubscriptionStartMessage
- M:com.aspose.psd.License.getErrorCodeMessages
- M:com.aspose.psd.License.removeLicense
- T:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.#ctor(int,int,com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getFilterEffectMasks
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.save(com.aspose.psd.StreamContainer,int)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FEidTypeToolKey
- F:com.aspose.psd.fileformats.psd.layers.layerresources.FXidResource.FXidTypeToolKey
- T:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getKeyName
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.getAnimatedDataSection
- M:com.aspose.psd.fileformats.psd.resources.AnimatedDataSectionResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,int,int)
- M:com.aspose.psd.fileformats.psd.layers.IGradientColorPoint.getRawColor
- M:com.aspose.psd.fileformats.psd.layers.IGradientColorPoint.getRawColor
- M:com.aspose.psd.fileformats.psd.layers.IGradientColorPoint.setRawColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.setRawColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientColorPoint.getRawColor
- T:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.#ctor(byte,java.lang.String)
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getBitDepth
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getDescription
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getFullName
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getName
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getPermittedFullNames
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.getValue
- M:com.aspose.psd.fileformats.psd.rawcolor.ColorComponent.setValue(long)
- T:com.aspose.psd.fileformats.psd.rawcolor.RawColor
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.fileformats.psd.rawcolor.ColorComponent[])
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.#ctor(com.aspose.psd.PixelDataFormat)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getAsInt
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getAsLong
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getBitDepth
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getComponents
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.getColorModeName
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setAsInt(int)
- M:com.aspose.psd.fileformats.psd.rawcolor.RawColor.setAsLong(long)
- T:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator
- M:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator.#ctor(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator.getChannelsHash
- M:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator.getBlendingHash
- M:com.aspose.psd.fileformats.psd.layers.LayerHashCalculator.getContentHash
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addOuterGlow
- M:com.aspose.psd.fileformats.psd.layers.layereffects.ILayerEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.ColorOverlayEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.InnerShadowEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.PatternOverlayEffect.getEffectType
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getEffectType
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePositionExtensions
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePositionExtensions.#ctor
- T:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getDescriptorVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getItems
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.save(com.aspose.psd.StreamContainer,int)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.MlstResource.TypeToolKey
- T:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure
- M:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure.getItems
- F:com.aspose.psd.fileformats.psd.layers.layerresources.AnimatedDataSectionStructure.StructureKey
- T:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.getVibrance
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.setVibrance(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.setSaturation(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.getSaturation
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.save(com.aspose```
.aspose.psd.StreamContainer,int)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.TypeToolKey
- T:com.aspose.psd.fileformats.psd.layers.layereffects.outerglow.OuterGlowProcessor
- M:com.aspose.psd.fileformats.psd.layers.layereffects.outerglow.OuterGlowProcessor.process(com.aspose.psd.Rectangle)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.TypeToolKey2
- F:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.TypeToolKey3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.#ctor(int,com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.getPatterns
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResource.setPatterns(com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData[])
- T:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getHeight
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getImageMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getPatternData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getPatternId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.getWidth
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.save(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.setName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.setPattern(int[],com.aspose.psd.Rectangle)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.PattResourceData.setPatternId(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.ClassID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.setPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.getPrefix
- F:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.StructureKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.getPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.setPrefix(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer.getLevels
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer.setLevels(short)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.#ctor(java.lang.String,com.aspose.psd.Rectangle,int,int,com.aspose.psd.fileformats.psd.layers.ChannelInformation[],com.aspose.
```