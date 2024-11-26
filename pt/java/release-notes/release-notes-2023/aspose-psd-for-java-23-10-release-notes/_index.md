---
title: Notas de Lançamento Aspose.PSD para Java 23.10
type: documentos
weight: 40
url: /pt/java/aspose-psd-for-java-23-10-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para o [Aspose.PSD para Java 23.10](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.10/) {{% /alert %}}

| **Chave**      | **Resumo**                                                                             | **Categoria** |
|:---------------|:----------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-538    | Suporte à direção do texto vertical                                                   |    Recurso   |
| PSDJAVA-542    | Usar configurações de traço do recurso vstk em renderização de traço de forma          |    Recurso   |
| PSDJAVA-540    | Implementar renderização da área interna de formas de traço                           |    Recurso   |
| PSDJAVA-541    | Não redesenhar camada de forma se não tiver sido alterada                              |    Recurso   |
| PSDJAVA-545    | [Formato AI] Adicionar suporte para leitura de Cabeçalho de Arquivos AI baseados em PDF |    Recurso   |
| PSDJAVA-546    | Várias maneiras de definir a resolução do arquivo Psd não funcionam                    |      Bug     |
| PSDJAVA-547    | FontSettings.SetFontsFolders não funciona ou Aspose.PSD usa a fonte incorreta          |      Bug     |
| PSDJAVA-548    | Regressão. Corrigir exceção de referência nula ao salvar PsdImage quando tem camada de forma |      Bug     |

## **Mudanças na API Pública**
# **APIs Adicionadas:**

- M:com.aspose.psd.FontSettings.getGetSystemAlternativeFont
- M:com.aspose.psd.FontSettings.setGetSystemAlternativeFont(boolean)
- M:com.aspose.psd.Graphics.getPaintableImageOptions
- M:com.aspose.psd.Graphics.setPaintableImageOptions(com.aspose.psd.ImageOptionsBase)
- M:com.aspose.psd.Image.getAutoAdjustPalette
- M:com.aspose.psd.Image.getFileFormat(com.aspose.psd.system.io.Stream)
- M:com.aspose.psd.extensions.RegionExtensions.#ctor
- M:com.aspose.psd.fileformats.psd.PsdImage.setResolution(double,double)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings.setColor(com.aspose.psd.Color)
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.getStroke
- M:com.aspose.psd.fileformats.psd.layers.ShapeLayer.setStroke(com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.getFillSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.VstkResource.setFillSettings(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.IStrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getEnabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getFill
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineAlignment
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setFill(com.aspose.psd.fileformats.psd.layers.fillsettings.IFillSettings)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineDashSet(double[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineCap
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineDashSet
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getLineJoin
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.getSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineAlignment(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineCap(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setLineJoin(short)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.strokeresources.StrokeSettings.setSize(double)
- T:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String)
- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

# **APIs Removidas:**

- M:com.aspose.psd.Image.isAutoAdjustPalette
- M:com.aspose.psd.ImageOptionsBase.memberwiseClone
- M:com.aspose.psd.imageoptions.BmpOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.CmxRasterizationOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.GifOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.Jpeg2000Options.memberwiseClone
- M:com.aspose.psd.imageoptions.JpegOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PdfOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PngOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.PsdOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.TiffOptions.memberwiseClone
- M:com.aspose.psd.imageoptions.VectorRasterizationOptions.memberwiseClone
- F:com.aspose.psd.fileformats.psd.layers.text.rendering.JustificationMode.Center

## **Exemplos de Uso:**

** PSDJAVA-538. Suporte à direção do texto vertical**

{{< highlight java >}}
    
    String arquivoFonte = "src/main/resources/692_lt1.psd";
    String arquivoSaida = "src/main/resources/692_output.png";
    String pastaFontes = "src/main/resources/692_Fonts";

        List<String> pastasFonte = new List<>(FontSettings.getFontsFolders());
        pastasFonte.add(pastaFontes);
        FontSettings.setFontsFolders(pastasFonte.toArray(new String[0]), true);

        try(PsdImage psdImage = (PsdImage)Image.load(arquivoFonte)) {
            PngOptions opcoesPng = new PngOptions();
            opcoesPng.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(arquivoSaida, opcoesPng);
        }

{{< /highlight >}}

** PSDJAVA-542. Usar configurações de traço do recurso vstk em renderização de traço de forma**

{{< highlight java >}}

    public static void main(String[] args) {
        String arquivoFonte = "src/main/resources/StrokeShapeTest.psd";
        String arquivoSaidaPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String arquivoSaidaPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage imagem = (PsdImage) Image.load(arquivoFonte)) {
            Layer camada = imagem.getLayers()[1];
            ShapeLayer camadaForma = (ShapeLayer) imagem.getLayers()[1];
            ColorFillSettings configuracoesPreenchimento = (ColorFillSettings) camadaForma.getFill();
            configuracoesPreenchimento.setColor(Color.getGreenYellow());
            camadaForma.update();

            ShapeLayer camadaForma2 = (ShapeLayer) imagem.getLayers()[3];
            GradientFillSettings configuracoesGradiente = (GradientFillSettings) camadaForma2.getFill();
            configuracoesGradiente.setDither(true);
            configuracoesGradiente.setReverse(true);
            configuracoesGradiente.setAlignWithLayer(false);
            configuracoesGradiente.setAngle(20);
            configuracoesGradiente.setScale(50);
            configuracoesGradiente.getColorPoints()[0].setLocation(100);
            configuracoesGradiente.getColorPoints()[1].setLocation(4000);
            configuracoesGradiente.getTransparencyPoints()[0].setLocation(200);
            configuracoesGradiente.getTransparencyPoints()[1].setLocation(3800);
            configuracoesGradiente.getTransparencyPoints()[0].setOpacity(90);
            configuracoesGradiente.getTransparencyPoints()[1].setOpacity(10);
            camadaForma2.update();

            ShapeLayer camadaForma3 = (ShapeLayer) imagem.getLayers()[5];
            StrokeSettings configuracoesTraço = (StrokeSettings) camadaForma3.getStroke();
            configuracoesTraço.setSize(15);
            ColorFillSettings configuracoesPreenchimentoT = (ColorFillSettings) configuracoesTraço.getFill();
            configuracoesPreenchimentoT.setColor(Color.getGreenYellow());
            camadaForma3.update();

            imagem.save(arquivoSaidaPsd);
            imagem.save(arquivoSaidaPng, new PngOptions());
        }

        // Verificar dados alterados.
        try (PsdImage imagem = (PsdImage) Image.load(arquivoSaidaPsd)) {
            ShapeLayer camadaForma = (ShapeLayer) imagem.getLayers()[1];
            ColorFillSettings configuracoesPreenchimento = (ColorFillSettings) camadaForma.getFill();
            assertAreEqual(Color.getGreenYellow(), configuracoesPreenchimento.getColor());

            ShapeLayer camadaForma2 = (ShapeLayer) imagem.getLayers()[3];
            GradientFillSettings configuracoesGradiente = (GradientFillSettings) camadaForma2.getFill();
            assertAreEqual(true, configuracoesGradiente.getDither());
            assertAreEqual(true, configuracoesGradiente.getReverse());
            assertAreEqual(false, configuracoesGradiente.getAlignWithLayer());
            assertAreEqual(20.0, configuracoesGradiente.getAngle());
            assertAreEqual(50, configuracoesGradiente.getScale());
            assertAreEqual(100, configuracoesGradiente.getColorPoints()[0].getLocation());
            assertAreEqual(4000, configuracoesGradiente.getColorPoints()[1].getLocation());
            assertAreEqual(200, configuracoesGradiente.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, configuracoesGradiente.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, configuracoesGradiente.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, configuracoesGradiente.getTransparencyPoints()[1].getOpacity());

            ShapeLayer camadaForma3 = (ShapeLayer) imagem.getLayers()[5];
            StrokeSettings configuracoesTraço = (StrokeSettings) camadaForma3.getStroke();
            ColorFillSettings configuracoesPreenchimentoT = (ColorFillSettings) configuracoesTraço.getFill();
            assertAreEqual(15.0, configuracoesTraço.getSize());
            assertAreEqual(Color.getGreenYellow(), configuracoesPreenchimentoT.getColor());
        }
    }

    static void assertAreEqual(Object esperado, Object atual) {
        assertAreEqual(esperado, atual, "Os objetos não são iguais.");
    }

    static void assertAreEqual(Object esperado, Object atual, String mensagem) {
        if (!esperado.equals(atual)) {
            throw new IllegalArgumentException(mensagem);
        }
    }

{{< /highlight >}}

** PSDJAVA-540. Implementar renderização da área interna de formas de traço**

{{< highlight java >}}

    public static void main(String[] args) {
        String arquivoFonte = "src/main/resources/StrokeShapeTest.psd";
        String arquivoSaidaPsd = "src/main/resources/StrokeShapeTest.out.psd";
        String arquivoSaidaPng = "src/main/resources/StrokeShapeTest.out.png";

        try (PsdImage imagem = (PsdImage) Image.load(arquivoFonte)) {
            Layer camada = imagem.getLayers()[1];
            ShapeLayer camadaForma = (ShapeLayer) imagem.getLayers()[1];
            ColorFillSettings configuracoesPreenchimento = (ColorFillSettings) camadaForma.getFill();
            configuracoesPreenchimento.setColor(Color.getGreenYellow());
            camadaForma.update();

            ShapeLayer camadaForma2 = (ShapeLayer) imagem.getLayers()[3];
            GradientFillSettings configuracoesGradiente = (GradientFillSettings) camadaForma2.getFill();
            configuracoesGradiente.setDither(true);
            configuracoesGradiente.setReverse(true);
            configuracoesGradiente.setAlignWithLayer(false);
            configuracoesGradiente.setAngle(20);
            configuracoesGradiente.setScale(50);
            configuracoesGradiente.getColorPoints()[0].setLocation(100);
            configuracoesGradiente.getColorPoints()[1].setLocation(4000);
            configuracoesGradiente.getTransparencyPoints()[0].setLocation(200);
            configuracoesGradiente.getTransparencyPoints()[1].setLocation(3800);
            configuracoesGradiente.getTransparencyPoints()[0].setOpacity(90);
            configuracoesGradiente.getTransparencyPoints()[1].setOpacity(10);
            camadaForma2.update();

            ShapeLayer camadaForma3 = (ShapeLayer) imagem.getLayers()[5];
            StrokeSettings configuracoesTraço = (StrokeSettings) camadaForma3.getStroke();
            configuracoesTraço.setSize(15);
            ColorFillSettings configuracoesPreenchimentoT = (ColorFillSettings) configuracoesTraço.getFill();
            configuracoesPreenchimentoT.setColor(Color.getGreenYellow());
            camadaForma3.update();

            imagem.save(arquivoSaidaPsd);
            imagem.save(arquivoSaidaPng, new PngOptions());
        }

        // Verificar dados alterados.
        try (PsdImage imagem = (PsdImage) Image.load(arquivoSaidaPsd)) {
            ShapeLayer camadaForma = (ShapeLayer) imagem.getLayers()[1];
            ColorFillSettings configuracoesPreenchimento = (ColorFillSettings) camadaForma.getFill();
            assertAreEqual(Color.getGreenYellow(), configuracoesPreenchimento.getColor());

            ShapeLayer camadaForma2 = (ShapeLayer) imagem.getLayers()[3];
            GradientFillSettings configuracoesGradiente = (GradientFillSettings) camadaForma2.getFill();
            assertAreEqual(true, configuracoesGradiente.getDither());
            assertAreEqual(true, configuracoesGradiente.getReverse());
            assertAreEqual(false, configuracoesGradiente.getAlignWithLayer());
            assertAreEqual(20.0, configuracoesGradiente.getAngle());
            assertAreEqual(50, configuracoesGradiente.getScale());
            assertAreEqual(100, configuracoesGradiente.getColorPoints()[0].getLocation());
            assertAreEqual(4000, configuracoesGradiente.getColorPoints()[1].getLocation());
            assertAreEqual(200, configuracoesGradiente.getTransparencyPoints()[0].getLocation());
            assertAreEqual(3800, configuracoesGradiente.getTransparencyPoints()[1].getLocation());
            assertAreEqual(90.0, configuracoesGradiente.getTransparencyPoints()[0].getOpacity());
            assertAreEqual(10.0, configuracoesGradiente.getTransparencyPoints()[1].getOpacity());

            ShapeLayer camadaForma3 = (ShapeLayer) imagem.getLayers()[5];
            StrokeSettings configuracoesTraço = (StrokeSettings) camadaForma3.getStroke();
            ColorFillSettings configuracoesPreenchimentoT = (ColorFillSettings) configuracoesTraço.getFill();
            assertAreEqual(15.0, configuracoesTraço.getSize());
            assertAreEqual(Color.getGreenYellow(), configuracoesPreenchimentoT.getColor());
        }
    }

    static void assertAreEqual(Object esperado, Object atual) {
        assertAreEqual(esperado, atual, "Os objetos não são iguais.");
    }

    static void assertAreEqual(Object esperado, Object atual, String mensagem) {
        if (!esperado.equals(atual)) {
            throw new IllegalArgumentException(mensagem);
        }
    }

{{< /highlight >}}

** PSDJAVA-541. Não redesenhar camada de forma se não tiver sido alterada**

{{< highlight java >}}

   