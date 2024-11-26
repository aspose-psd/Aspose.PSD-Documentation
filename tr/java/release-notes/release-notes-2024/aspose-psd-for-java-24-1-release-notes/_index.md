---
title: Aspose.PSD for Java 24.1 - Sürüm Notları
type: docs
weight: 40
url: /tr/java/aspose-psd-for-java-24-1-release-notes/
---

{{% alert color="primary" %}} Bu sayfa, [Aspose.PSD for Java 24.1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) için sürüm notlarını içermektedir. {{% /alert %}}

| **Anahtar**  | **Özet**                                                                                       | **Kategori** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [AI Format] Çoklu sayfalı AI resimleri için temel işlemler ekleme.                               | Özellik      |
| PSDJAVA-579 | Eğik Metin Efekti metne uygulanmıyor.                                                          | Hata         |
| PSDJAVA-580 | Belirli bir dosyadaki maske renderının yanlış olması.                                            | Hata         |
| PSDJAVA-581 | Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor'da NullReferenceException. | Hata         |
| PSDJAVA-582 | [AI Format] AiExporterUtils'taki bellek kullanımını düzeltme.                                     | Hata         |

## **Genel API Değişiklikleri**
# **Eklenen API'ler:**

- M:com.aspose.psd.fileformats.ai.AiImage.getActivePageIndex
- M:com.aspose.psd.fileformats.ai.AiImage.setActivePageIndex(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolation
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolation(short)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getColorModel
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMaximumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getMinimumColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRndNumberSeed
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getRoughness
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getShowTransparency
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getUseVectorColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setColorModel(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setGradientMode(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMaximumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setMinimumColor(com.aspose.psd.fileformats.psd.rawcolor.RawColor)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRndNumberSeed(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setRoughness(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setShowTransparency(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setUseVectorColor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartobjects.SmartObjectLayer.#ctor(com.aspose.psd.system.io.Stream)
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
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientMode
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getGradientType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getHorizontalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getReverse
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getScale
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.getVerticalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientMode(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.BaseGradientFillSettings.setVerticalOffset(double)

# **Kaldırılan API'ler:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAlignWithLayer
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getAngle
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getDither 
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getFillType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getGradientType
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getHorizontalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getReverse
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getScale
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getVerticalOffset
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAlignWithLayer(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setAngle(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setDither(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setGradientType(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setHorizontalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setReverse(boolean)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setScale(int)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setVerticalOffset(double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColor
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getColorPoints
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getGradientName
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getTransparencyPoints
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setColorPoints(com.aspose.psd.fileformats.psd.layers.IGradientColorPoint[])
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setGradientName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setTransparencyPoints(com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientTransparencyPoint[])
- F:com.aspose.psd.fileformats.psd.resources.enums_.ColorSpace.RGB

## **Kullanım Örnekleri:**

** PSDJAVA-576. [AI Format] Çoklu sayfalı AI resimleri için temel işlemler ekleme**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/threePages.ai";
        String ilkSayfaCiktiPng = "src/main/resources/firstPageOutput.png";
        String ikinciSayfaCiktiPng = "src/main/resources/secondPageOutput.png";
        String ucuncuSayfaCiktiPng = "src/main/resources/thirdPageOutput.png";

        // AI resmi yükleyin.
        try (AiImage resim = (AiImage) Image.load(kaynakDosya)) {
            // Varsayılan olarak, ActivePageIndex 0'dır.
            // Bu özelliği değiştirmeden AI resmini kaydederseniz, ilk sayfa işlenecek ve kaydedilecektir.
            resim.save(ilkSayfaCiktiPng, new PngOptions());

            // ActivePageIndex'i ikinci sayfaya değiştirin.
            resim.setActivePageIndex(1);

            // AI resminin ikinci sayfasını PNG resmi olarak kaydedin.
            resim.save(ikinciSayfaCiktiPng, new PngOptions());

            // ActivePageIndex'i üçüncü sayfaya değiştirin.
            resim.setActivePageIndex(2);

            // AI resminin üçüncü sayfasını PNG resmi olarak kaydedin.
            resim.save(ucuncuSayfaCiktiPng, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. Eğik Metin Efekti metne uygulanmıyor**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/text_warp.psd";
        String ciktiDosyasi = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(kaynakDosya, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(ciktiDosyasi, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-580. Belirli bir dosyadaki maske renderının yanlış olması**

{{< highlight java >}}

        String kaynakDosya1 = "src/main/resources/mask_problem.psd";
        String kaynakDosya2 = "src/main/resources/puh_softLight3_1.psd";
        String ciktiDosyasi1 = "src/main/resources/mask_export.png";
        String ciktiDosyasi2 = "src/main/resources/puh_export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(kaynakDosya1, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(ciktiDosyasi1, pngOptions);
        }

        try (PsdImage img = (PsdImage) Image.load(kaynakDosya2, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(ciktiDosyasi2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-581. Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor'da NullReferenceException**

{{< highlight java >}}

        String fontlarKlasoru = "src/main/resources/Fonts";
        FontSettings.setFontsFolders(new String[]{fontlarKlasoru}, true);

        String girisDosyasi = "src/main/resources/1.psd";
        String ciktiDosyasi = "src/main/resources/out_1855.png";
        try (PsdImage psdResim = (PsdImage) Image.load(girisDosyasi)) {
            psdResim.save(ciktiDosyasi, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [AI Format] AiExporterUtils'taki bellek kullanımını düzeltme**

{{< highlight java >}}

        String kaynakDosya = "src/main/resources/threePages.ai";
        String ilkSayfaCiktiPng = "src/main/resources/firstPageOutput.png";
        String ikinciSayfaCiktiPng = "src/main/resources/secondPageOutput.png";
        String ucuncuSayfaCiktiPng = "src/main/resources/thirdPageOutput.png";

        final double BellekSiniri = 700;
        double kullanilanBellek = Double.MAX_VALUE;

        // AI resmi yükleyin.
        try (AiImage resim = (AiImage) Image.load(kaynakDosya)) {
            // AI resminin ilk sayfasını PNG resmi olarak kaydedin.
            resim.save(ilkSayfaCiktiPng, new PngOptions());

            // ActivePageIndex'i ikinci sayfaya değiştirin.
            resim.setActivePageIndex(1);

            // AI resminin ikinci sayfasını PNG resmi olarak kaydedin.
            resim.save(ikinciSayfaCiktiPng, new PngOptions());

            // ActivePageIndex'i üçüncü sayfaya değiştirin.
            resim.setActivePageIndex(2);

            // AI resminin üçüncü sayfasını PNG resmi olarak