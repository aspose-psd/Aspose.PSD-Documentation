---
title: Notas da Versão Aspose.PSD para Java 24.1
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-24-1-release-notes/
---

{{% alert color="primary" %}} Esta página contém as notas de versão para [Aspose.PSD para Java 24,1](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.1/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                                  | **Categoria** |
|:------------|:---------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-576 | [Formato AI] Adicionar manipulação básica para imagens AI multipágina.                        | Recurso      |
| PSDJAVA-579 | Efeito de Texto Diferente não se aplica ao texto.                                            | Erro         |
| PSDJAVA-580 | Renderização incorreta da máscara no arquivo específico.                                     | Erro         |
| PSDJAVA-581 | NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor. | Erro         |
| PSDJAVA-582 | [Formato AI] Correção do uso de memória em AiExporterUtils.                                  | Erro         |

## **Alterações na API Pública**

# **APIs Adicionadas:**

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

# **APIs Removidas:**

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

## **Exemplos de Uso:**

** PSDJAVA-576. [Formato AI] Adicionar manipulação básica para imagens AI multipágina**

{{< highlight java >}}

        String arquivoFonte = "src/main/resources/tresPaginas.ai";
        String primeiraPaginaOutputPng = "src/main/resources/primeiraPaginaOutput.png";
        String segundaPaginaOutputPng = "src/main/resources/segundaPaginaOutput.png";
        String terceiraPaginaOutputPng = "src/main/resources/terceiraPaginaOutput.png";

        // Carregar a imagem AI.
        try (AiImage imagem = (AiImage) Image.load(arquivoFonte)) {
            // Por padrão, o ActivePageIndex é 0.
            // Assim, se você salvar a imagem AI sem alterar essa propriedade, a primeira página será renderizada e salva.
            imagem.save(primeiraPaginaOutputPng, new PngOptions());

            // Mudar o índice da página ativa para a segunda página.
            imagem.setActivePageIndex(1);

            // Salvar a segunda página da imagem AI como uma imagem PNG.
            imagem.save(segundaPaginaOutputPng, new PngOptions());

            // Mudar o índice da página ativa para a terceira página.
            imagem.setActivePageIndex(2);

            // Salvar a terceira página da imagem AI como uma imagem PNG.
            imagem.save(terceiraPaginaOutputPng, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-579. Efeito de Texto Diferente não se aplica ao texto**

{{< highlight java >}}

        String arquivoFonte = "src/main/resources/texto_reta.psd";
        String arquivoOutput = "src/main/resources/exportar.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);
        opt.setAllowWarpRepaint(true);

        try (PsdImage img = (PsdImage) Image.load(arquivoFonte, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(arquivoOutput, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-580. Renderização incorreta da máscara no arquivo específico**

{{< highlight java >}}

        String arquivoFonte1 = "src/main/resources/problema_da_mascara.psd";
        String arquivoFonte2 = "src/main/resources/puh_softLight3_1.psd";
        String arquivoOutput1 = "src/main/resources/exportar_mascara.png";
        String arquivoOutput2 = "src/main/resources/puh_exportar.png";

        PsdLoadOptions opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (PsdImage img = (PsdImage) Image.load(arquivoFonte1, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(arquivoOutput1, pngOptions);
        }

        try (PsdImage img = (PsdImage) Image.load(arquivoFonte2, opt)) {
            PngOptions pngOptions = new PngOptions();
            pngOptions.setCompressionLevel(9);
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            img.save(arquivoOutput2, pngOptions);
        }

{{< /highlight >}}

** PSDJAVA-581. NullReferenceException em Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo.ctor**

{{< highlight java >}}

        String pastaFontes = "src/main/resources/Fontes";
        FontSettings.setFontsFolders(new String[]{pastaFontes}, true);

        String arquivoEntrada = "src/main/resources/1.psd";
        String arquivoSaida = "src/main/resources/out_1855.png";
        try (PsdImage imagemPsd = (PsdImage) Image.load(arquivoEntrada)) {
            imagemPsd.save(arquivoSaida, new PngOptions());
        }

{{< /highlight >}}

** PSDJAVA-582. [Formato AI] Correção do uso de memória em AiExporterUtils**

{{< highlight java >}}

        String arquivoFonte = "src/main/resources/tresPages.ai";
        String primeiraPaginaOutputPng = "src/main/resources/primeiraPaginaOutput.png";
        String segundaPaginaOutputPng = "src/main/resources/segundaPaginaOutput.png";
        String terceiraPaginaOutputPng = "src/main/resources/terceiraPaginaOutput.png";

        final double LimiteMemoria = 700;
        double memoriaUtilizada = Double.MAX_VALUE;

        // Carregar a imagem AI.
        try (AiImage imagem = (AiImage) Image.load(arquivoFonte)) {
            // Salvar a primeira página da imagem AI como uma imagem PNG.
            imagem.save(primeiraPaginaOutputPng, new PngOptions());

            // Mudar o índice da página ativa para a segunda página.
            imagem.setActivePageIndex(1);

            // Salvar a segunda página da imagem AI como uma imagem PNG.
            imagem.save(segundaPaginaOutputPng, new PngOptions());

            // Mudar o índice da página ativa para a terceira página.
            imagem.setActivePageIndex(2);

            // Salvar a terceira página da imagem AI como uma imagem PNG.
            imagem.save(terceiraPaginaOutputPng, new PngOptions());
        }

        System.gc();

        memoriaUtilizada = (double) (Runtime.getRuntime().totalMemory() - Runtime.getRuntime().freeMemory()) / (1024.0 * 1024.0);

        if (memoriaUtilizada > LimiteMemoria) {
            throw new RuntimeException("Uso de memória é muito grande. " + memoriaUtilizada + " ao invés de " + String.format("%.1f", LimiteMemoria));
        }

{{< /highlight >}}