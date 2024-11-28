---
title: Aspose.PSD dla Java 24.1 - Notatki dotyczące wersji
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-24-1-notatki-dotyczace-wersji/
---

{{% alert color="primary" %}} Ta strona zawiera notatki dotyczące wersji [Aspose.PSD dla Java 24.1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) {{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                              | **Kategoria** |
|:------------|:-----------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [Format AI] Dodano podstawową obsługę obrazów AI wielostronicowych.                              | Funkcja     |
| PSDJAVA-579 | Efekt zniekształcenia tekstu nie jest stosowany do tekstu.                                       | Błąd         |
| PSDJAVA-580 | Błędne renderowanie maski w określonym pliku.                                                    | Błąd         |
| PSDJAVA-581 | NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor.  | Błąd         |
| PSDJAVA-582 | [Format AI] Naprawienie zużycia pamięci w AiExporterUtils.                                       | Błąd         |

## **Zmiany w publicznym API**
# **Dodane API:**

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

# **Usunięte API:**

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

## **Przykłady użycia:**

** PSDJAVA-576. [Format AI] Dodanie podstawowej obsługi obrazów AI wielostronicowych**

{{< highlight java >}}


        String plikWejsciowy = "src/main/resources/trzyStrony.ai";
        String pierwszaStronaOutputPng = "src/main/resources/pierwszaStronaOutput.png";
        String drugaStronaOutputPng = "src/main/resources/drugaStronaOutput.png";
        String trzeciaStronaOutputPng = "src/main/resources/trzeciaStronaOutput.png";

        // Wczytaj obraz AI.
        try (AiImage obraz = (AiImage) Image.load(plikWejsciowy)) {
            // Domyślnie ActivePageIndex wynosi 0.
            // Jeśli zapiszesz obraz AI bez zmiany tej właściwości, pierwsza strona zostanie wyrenderowana i zapisana.
            obraz.save(pierwszaStronaOutputPng, new PngOptions());

            // Zmień indeks aktywnej strony na drugą stronę.
            obraz.setActivePageIndex(1);

            // Zapisz drugą stronę obrazu AI jako obraz PNG.
            obraz.save(drugaStronaOutputPng, new PngOptions());

            // Zmień indeks aktywnej strony na trzecią stronę.
            obraz.setActivePageIndex(2);

            // Zapisz trzecią stronę obrazu AI jako obraz PNG.
            obraz.save(trzeciaStronaOutputPng, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. Efekt zniekształcenia tekstu nie jest stosowany do tekstu**

{{< highlight java >}}


        String plikWejsciowy = "src/main/resources/tekst_znieksztalcenie.psd";
        String plikWyjsciowy = "src/main/resources/eksport.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(plikWejsciowy, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(plikWyjsciowy, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-580. Błędne renderowanie maski w określonym pliku**

{{< highlight java >}}


        String plikWejsciowy1 = "src/main/resources/problem_maski.psd";
        String plikWejsciowy2 = "src/main/resources/puh_softLight3_1.psd";
        String plikWyjsciowy1 = "src/main/resources/eksport_maski.png";
        String plikWyjsciowy2 = "src/main/resources/puh_eksport.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(plikWejsciowy1, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(plikWyjsciowy1, pngOptions);
        }

        try (PsdImage img = (PsdImage) Image.load(plikWejsciowy2, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(plikWyjsciowy2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-581. NullReferenceException w Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor**

{{< highlight java >}}


        String katalogCzcionek = "src/main/resources/Czcionki";
        FontSettings.setFontsFolders(new String[]{katalogCzcionek}, true);

        String plikWejsciowy = "src/main/resources/1.psd";
        String plikWyjsciowy = "src/main/resources/wy_1855.png";
        try (PsdImage psdImage = (PsdImage) Image.load(plikWejsciowy)) {
            psdImage.save(plikWyjsciowy, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [Format AI] Naprawienie zużycia pamięci w AiExporterUtils**

{{< highlight java >}}


        String plikWejsciowy = "src/main/resources/trzyStrony.ai";
        String pierwszaStronaOutputPng = "src/main/resources/pierwszaStronaOutput.png";
        String drugaStronaOutputPng = "src/main/resources/drugaStronaOutput.png";
        String trzeciaStronaOutputPng = "src/main/resources/trzeciaStronaOutput.png";

        final double LimitPamieci = 700;
        double uzyciePamieci = Double.MAX_VALUE;

        // Wczytaj obraz AI.
        try (AiImage obraz = (AiImage) Image.load(plikWejsciowy)) {
            // Zapisz pierwszą stronę obrazu AI jako obraz PNG.
            obraz.save(pierwszaStronaOutputPng, new PngOptions());

            // Zmień indeks aktywnej strony na drugą stronę.
            obraz.setActivePageIndex(1);

            // Zapisz drugą stronę obrazu AI jako obraz PNG.
            obraz.save(drugaStronaOutputPng, new PngOptions());

            // Z