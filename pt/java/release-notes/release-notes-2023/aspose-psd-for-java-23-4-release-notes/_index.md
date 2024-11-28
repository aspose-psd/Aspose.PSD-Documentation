---
title: Aspose.PSD for Java 23.4 - Notas de Lançamento
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-23-4-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD for Java 23.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.4/) {{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-446|Portar funcionalidades ausentes do Aspose.PSD para .Net para o Aspose.PSD para Java|Melhoria|
|PSDJAVA-441|Projetar a classe RawColor para ser utilizada na API pública do PSD em vez da estrutura Color obsoleta|Melhoria|
|PSDJAVA-418|Integrar a Licença Moderna do Aspose para Aspose.PSD|Melhoria|
|PSDJAVA-445|Movimentação de formatação ao editar no Photoshop|Erro|
|PSDJAVA-443|A edição de texto usando Porções de Texto não salva o resultado correto|Erro|
|PSDJAVA-444|O início e o final dos estilos ou parágrafos aparecem no lugar incorreto na edição da Camada de Texto por ITextPortion|Erro|

# **Mudanças na API Pública**
# **APIs Adicionadas:**
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
- M:com.aspose.psd.fileformats.psd.layers.layerresources.typetoolinfostructures.PathStructure.setPrefix(java.lang.String)
- T:com.aspose.psd.fileformats.psd.layers.adjustmentlayers.PosterizeLayer
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
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.isOpen
- M:com.aspose.psd.fileformats.psd.layers.LayerGroup.setOpen(boolean)
- M:com.aspose.psd.fileformats.psd.layers.TextLayer.resize(int,int,int)
- M:com.aspose.psd.xmp.Namespaces.#ctor

# **APIs Removidas:**
- M:com.aspose.psd.FontSettings.addFontsFolder(java.lang.String)
- M:com.aspose.psd.FontSettings.removeFontsFolder(java.lang.String)
- M:Continuação:

# **Exemplos de Uso:**

**PSDJAVA-446. Portar funcionalidades ausentes do Aspose.PSD para .Net para o Aspose.PSD para Java**

Por favor, consulte a <a href="https://reference.aspose.com/psd/java/">Referência da API para Aspose.PSD for Java </a>. Nem todos os exemplos de uso da nova API foram copiados e testados.

{{< highlight java >}}        
        // Exemplos serão fornecidos posteriormente.
{{< /highlight >}}

**PSDJAVA-441. Projetar a classe RawColor para ser utilizada na API pública do PSD em vez da estrutura Color obsoleta**

{{< highlight java >}}
		PixelDataFormat rgb32Bpp = PixelDataFormat.getRgb32Bpp();
		RawColor color = new RawColor(rgb32Bpp);
		Color oldColor = Color.fromArgb(5, 1, 2, 3);

		int argbValue = oldColor.toArgb();
		color.setAsInt(argbValue);

		Assertions.assertEquals("ARGB", color.getColorModeName());
		Assertions.assertEquals(32, color.getBitDepth());
		Assertions.assertEquals("A Alpha", color.getComponents()[0].getFullName());
		Assertions.assertEquals(5, (int)color.getComponents()[0].getValue());
		Assertions.assertEquals("R Red", color.getComponents()[1].getFullName());
		Assertions.assertEquals(1, (int)color.getComponents()[1].getValue());
		Assertions.assertEquals("G Green", color.getComponents()[2].getFullName());
		Assertions.assertEquals(2, (int)color.getComponents()[2].getValue());
		Assertions.assertEquals("B Blue", color.getComponents()[3].getFullName());
		Assertions.assertEquals(3, (int)color.getComponents()[3].getValue());

		Assertions.assertEquals(argbValue, color.getAsInt());
{{< /highlight >}}

**PSDJAVA-445. Movimentação de formatação ao editar no Photoshop**

{{< highlight java >}}
 public static void main(String[] args) throws Exception {
    String strings1 = Directory.getCurrentDirectory() + "/input-lsaks-strings1-forTicket.txt";
    String psdInput = Directory.getCurrentDirectory() + "/input_for_ticket.psd";

    PsdImage image = (PsdImage) Image.load(psdInput);
   