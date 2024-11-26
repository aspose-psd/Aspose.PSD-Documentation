---
title: Aspose.PSD voor Java 24.1 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-24-1-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 24.1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                               | **Categorie** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [AI-formaat] Basisafhandeling toevoegen voor multipage AI-afbeeldingen.                        | Functie      |
| PSDJAVA-579 | Warp Teksteffect wordt niet toegepast op tekst.                                                | Probleem     |
| PSDJAVA-580 | Onjuiste weergave van masker in het specifieke bestand.                                        | Probleem     |
| PSDJAVA-581 | NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor. | Probleem     |
| PSDJAVA-582 | [AI-formaat] Het geheugengebruik in AiExporterUtils corrigeren.                                 | Probleem     |

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**

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

# **Verwijderde API's:**

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

## **Voorbeelden van gebruik:**

** PSDJAVA-576. [AI-formaat] Basisafhandeling toevoegen voor multipage AI-afbeeldingen**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        String firstPageOutputPng = "src/main/resources/firstPageOutput.png";
        String secondPageOutputPng = "src/main/resources/secondPageOutput.png";
        String thirdPageOutputPng = "src/main/resources/thirdPageOutput.png";

        // Laad de AI-afbeelding.
        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // Standaard is de ActivePageIndex 0.
            // Als u de AI-afbeelding opslaat zonder deze eigenschap te wijzigen, wordt de eerste pagina weergegeven en opgeslagen.
            image.save(firstPageOutputPng, new PngOptions());

            // Wijzig de actieve paginaindex naar de tweede pagina.
            image.setActivePageIndex(1);

            // Sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(secondPageOutputPng, new PngOptions());

            // Wijzig de actieve paginaindex naar de derde pagina.
            image.setActivePageIndex(2);

            // Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(thirdPageOutputPng, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. Warp Teksteffect wordt niet toegepast op tekst**

{{< highlight java >}}

        String sourceFile = "src/main/resources/text_warp.psd";
        String outputFile = "src/main/resources/export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-580. Onjuiste weergave van masker in het specifieke bestand**

{{< highlight java >}}

        String sourceFile1 = "src/main/resources/mask_problem.psd";
        String sourceFile2 = "src/main/resources/puh_softLight3_1.psd";
        String outputFile1 = "src/main/resources/mask_export.png";
        String outputFile2 = "src/main/resources/puh_export.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(sourceFile1, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile1, pngOptions);
        }

        try (PsdImage img = (PsdImage) Image.load(sourceFile2, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(outputFile2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-581. NullReferenceException bij Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor**

{{< highlight java >}}

        String fontsFolder = "src/main/resources/Fonts";
        FontSettings.setFontsFolders(new String[]{fontsFolder}, true);

        String inputFile = "src/main/resources/1.psd";
        String outputFile = "src/main/resources/out_1855.png";
        try (PsdImage psdImage = (PsdImage) Image.load(inputFile)) {
            psdImage.save(outputFile, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [AI-formaat] Het geheugengebruik in AiExporterUtils corrigeren**

{{< highlight java >}}

        String sourceFile = "src/main/resources/threePages.ai";
        String firstPageOutputPng = "src/main/resources/firstPageOutput.png";
        String secondPageOutputPng = "src/main/resources/secondPageOutput.png";
        String thirdPageOutputPng = "src/main/resources/thirdPageOutput.png";

        final double MemoryLimit = 700;
        double memoryUsed = Double.MAX_VALUE;

        // Laad de AI-afbeelding.
        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            // Sla de eerste pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(firstPageOutputPng, new PngOptions());

            // Wijzig de actieve paginaindex naar de tweede pagina.
            image.setActivePageIndex(1);

            // Sla de tweede pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(secondPageOutputPng, new PngOptions());

            // Wijzig de actieve paginaindex naar de derde pagina.
            image.setActivePageIndex(2);

            // Sla de derde pagina van de AI-afbeelding op als een PNG-afbeelding.
            image.save(thirdPageOutputPng, new PngOptions());
        }

        System.gc();

        memoryUsed = (double) (Runtime.getRuntime().totalMemory() - Runtime.getRuntime().freeMemory()) / (1024.0 * 1024.0);

        if (memoryUsed > MemoryLimit) {
            throw new RuntimeException("Gebruik van geheugen is te hoog. " + memoryUsed + " in plaats van " + String.format("%.1f", MemoryLimit));
        }

{{< /highlight >}}