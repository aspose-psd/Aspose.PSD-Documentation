---
title: Aspose.PSD за Java 23.4 - Забележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-4-zabelezhki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа забележки за изданието за [Aspose.PSD за Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDJAVA-446|Пренос на пропусната функционалност от Aspose.PSD за .Net към Aspose.PSD за Java|Подобрение|
|PSDJAVA-441|Дизайн на клас RawColor за публичното API, за да се използва в PSD API вместо остарялата Color структура|Подобрение|
|PSDJAVA-418|Интегриране на модерната лицензия на Aspose за Aspose.PSD|Подобрение|
|PSDJAVA-445|Преместване на форматирането при редактиране в Photoshop|Грешка|
|PSDJAVA-443|Редактирането на текст, използвайки текстови порции, не запазва правилния резултат|Грешка|
|PSDJAVA-444|Началото и краят на стиловете или параграфите се появяват на неправилното място при редактиране на текстов слой с ITextPortion|Грешка|

# **Промени в публичното API**
# **Добавени API:**
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.VibAResource.save(com.aspose.psd.StreamContainer,int)
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
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer.getLevels
- M:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer.setLevels(short)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.#ctor(java.lang.String,com.aspose.psd.Rectangle,int,int,com.aspose.psd.fileformats.psd.layers.ChannelInformation[],com.aspose.psd.fileformats.psd.layers.ChannelInformation,com.aspose.psd.Rectangle,com.aspose.psd.fileformats.psd.layers.ChannelInformation)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getGUID
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getRectangle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getPixelsDepth
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getMaxChannels
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getChannels
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getUserMask
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getMaskRectangle
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.getSheetMask
- M:com.aspose.psd.fileformats.psd.layers.layerresources.FilterEffectMaskData.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.ShmdResource.setSubResources(com.aspose.psd.fileformats.psd.layers.LayerResource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompInfoKeyName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.ListStructure.getItemList
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.getSmartFilters
- T:com.aspose.psd.PixelsData
- M:com.aspose.psd.PixelsData.#ctor
- M:com.aspose.psd.PixelsData.#ctor(int[],com.aspose.psd.Rectangle)
- M:com.aspose.psd.PixelsData.getBounds
- M:com.aspose.psd.PixelsData.getPixels
- M:com.aspose.psd.PixelsData.setBounds(com.aspose.psd.Rectangle)
- M:com.aspose.psd.PixelsData.setPixels(int[])
- M:com.aspose.psd.fileformats.psd.layers.text.IText.getTextOrientation
- M:com.aspose.psd.fileformats.psd.layers.text.IText.setTextOrientation(int)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.get_noBreak
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.set_noBreak(boolean)
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.is_isStandardVerticalRomanAlignmentEnabled
- M:com.aspose.psd.fileformats.psd.layers.text.ITextStyle.set_isStandardVerticalRomanAlignmentEnabled(boolean)
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getAllowWarpRepaint
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setAllowWarpRepaint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.Layer.save(com.aspose.psd.system.io.Stream)
- M