---
title: Poznámky k vydání Aspose.PSD pro Javu 23.12
type: docs
weight: 40
url: /cs/aspose-psd-pro-javu-23-12-poznamky-k-vydani/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Javu 23.12](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.12/) {{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                         | **Kategorie** |
|:------------|:----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-565 | [Formát AI] Přidání podpory pro vykreslování rastrového obrázku ve nové verzi AI.                  | Funkce      |
| PSDJAVA-566 | Řešení typu šumu Gradient v GdflResrourci.                                                        | Funkce      |
| PSDJAVA-567 | Chyba "Odkaz na objekt není nastaven na instanci objektu." při ukládání textové vrstvy po aktualizaci. | Chyba        |
| PSDJAVA-568 | Oprava ručního načítání písem na MacOS pomocí System.Drawing.Common a Aspose.Drawing.            | Chyba          |
| PSDJAVA-569 | AllowWarpRepaint v možnostech PsdLoadOptions vede k výjimce.                                      | Chyba          |
| PSDJAVA-570 | [Formát AI] Implementace zpracování křížových referenčních proudů.                                        | Vylepšení  |
| PSDJAVA-571 | Řízení licence pro VectorPathDataResource nefunguje správně.                                       | Vylepšení   |
| PSDJAVA-574 | Otevření libovolného obrázkového souboru jako vložený chytrý objekt v obrazu PSD.                                   | Vylepšení  |

## **Změny v veřejném API**
# **Přidaná API:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolace
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolace(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getRežimGradientu
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setRežimGradientu(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRežimGradientu
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRežimGradientu(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent1
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent2
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent3
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorComponent4 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getColorSpace 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getFlag 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getKey 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getLength 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getOpacity 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getPsdVersion 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.getSignature 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent1(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent2(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent3(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorComponent4(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setColorSpace(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.setOpacity(short)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.LmskResource.TypeToolKey 
- T:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.CMYK 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.GrayScale 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.HSB 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.Lab 
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getColorModel 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMaximumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getMinimumColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRndNumberSeed 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getRoughness 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getShowTransparency 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.getUseVectorColor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setColorModel(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.NoiseGradientFillSettings.setUseVectorColor(boolean)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.gradientKindToStr(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.noiseColorModelToStr(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToGradientKind(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.strToNoiseColorModel(java.lang.String)
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientNoise 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrGradientSolid 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelHSB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelLAB 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.GdflResourceHelper.StrModelRGB 
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAlignWithLayer 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getAngle 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getFillType 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getRežimGradientu 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getTypGradientu 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getHorizontálníOfset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getReverse 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getMěřítko 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getVertikálníOfset 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setRežimGradientu(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setTypGradientu(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setHorizontálníOfset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setMěřítko(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setVertikálníOfset(double)

# **Odstraněná API:**

- M:com.aspose.psd.fileformats.psd.layers.fill