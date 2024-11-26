---
title: Notas da Versão Aspose.PSD for Java 23.9
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} Esta página contém as notas de lançamento para [Aspose.PSD for Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                            | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Implementar a criação de máscara para novas camadas de ajuste                                                                          |    Recurso   |
| PSDJAVA-528 | Adicionar suporte para Camadas Recortadas como opção de mesclagem de Grupo                                                            |    Recurso   |
| PSDJAVA-529 | O arquivo PSD com modo de cor de 16 bits não aplica máscara para camadas de ajuste                                                    |      Erro    |
| PSDJAVA-530 | Renderização incorreta de colchetes na camada de texto                                                                                 |      Erro    |
| PSDJAVA-531 | Não é possível atualizar os estilos nas camadas de texto                                                                               |      Erro    |
| PSDJAVA-532 | Após exportar o arquivo PSD com CMYK, as cores no arquivo PSD exportado são alteradas                                                 |      Erro    |
| PSDJAVA-533 | Um arquivo PSB específico gera a exceção "O retângulo não possui uma área de processamento comum"                                       |      Erro    |
| PSDJAVA-534 | Falha no carregamento da imagem. OverflowException: A operação aritmética resultou em um estouro.                                      |      Erro    |

## **Alterações na API Pública**
# **APIs Adicionadas:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **APIs Removidas:**

- Nenhuma

## **Exemplos de Uso:**

** PSDJAVA-527. Implementar a criação de máscara para novas camadas de ajuste**

{{< highlight java >}}
public static void main(String[] args) {
    String arquivoSrc = "src/main/resources/zendeya_BW.psd";
    String arquivoDst = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(arquivoSrc)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(arquivoDst);
    }

    try (PsdImage im = (PsdImage) Image.load(arquivoDst)) {
        Layer camada = im.getLayers()[1];

        assertAreEqual(5, camada.getChannelsCount());
        assertAreEqual((short) -2, camada.getChannelInformation()[4].getChannelID());
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

** PSDJAVA-528. Adicionar suporte para Camadas Recortadas como opção de mesclagem de Grupo**

{{< highlight java >}}
    String arquivoFonte = "src/main/resources/arquivo_fonte_exemplo.psd";
    String outputPsd = "src/main/resources/saida_exemplo.psd";
    String outputPng = "src/main/resources/saida_exemplo.png";

    try (PsdImage imagem = (PsdImage)Image.load(arquivoFonte)) {
        imagem.getLayers()[1].setBlendClippedElements(false);
        imagem.save(outputPsd);
        imagem.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-529. O arquivo PSD com modo de cor de 16 bits não aplica máscara para camadas de ajuste**

{{< highlight java >}}
	String arquivoFonte = "src/main/resources/arquivo_fonte.psd";
    String outputPng = "src/main/resources/atual.png";

    try (PsdImage imagem = (PsdImage) Image.load(arquivoFonte)) {
        imagem.save(outputPng, new PngOptions());
    }
{{< /highlight >}}


** PSDJAVA-530. Renderização incorreta de colchetes na camada de texto**

{{< highlight java >}}
    String arquivo = "src/main/resources/arquivo1.psd";
    String output = "src/main/resources/saida_1235.png";

    try (PsdImage imagemPsd = (PsdImage) Image.load(arquivo)) {
        for (Layer camada : imagemPsd.getLayers()) {
            if (camada instanceof TextLayer) {
                TextLayer camadaTexto = (TextLayer) camada;
                camadaTexto.getTextData().updateLayerData();

                PsdOptions opcoesImagem = new PsdOptions(imagemPsd);
                imagemPsd.save(output, opcoesImagem);
            }
        }
    }
{{< /highlight >}}


** PSDJAVA-531. Não é possível atualizar os estilos nas camadas de texto**

{{< highlight java >}}
    String arquivoFonte = "src/main/resources/Exemplo_TamanhoFonte.psd";
    String outputFile = "src/main/resources/saida_Exemplo_TamanhoFonte.psd";

    PsdLoadOptions opcoesCarregamentoPsd = new PsdLoadOptions();
    opcoesCarregamentoPsd.setLoadEffectsResource(true);

    try (PsdImage imagemPsd = (PsdImage) Image.load(arquivoFonte, opcoesCarregamentoPsd)) {
        TextLayer l1 = (TextLayer) imagemPsd.getLayers()[4];
        TextLayer l2 = (TextLayer) imagemPsd.getLayers()[5];

        ITextPortion[] itensTexto1 = l1.getTextData().producePortions(new String[]{"texto1", "texto2"},
                l1.getTextData().getItems()[0].getStyle(), l1.getTextData().getItems()[0].getParagraph());

        l1.getTextData().removePortion(0);
        for (ITextPortion item : itensTexto1) {
            l1.getTextData().addPortion(item);
        }

        ITextPortion[] itensTexto2 = l2.getTextData().producePortions(new String[]{"camada de texto 1", "camada de texto 22"},
                l2.getTextData().getItems()[0].getStyle(), l2.getTextData().getItems()[0].getParagraph());

        for (ITextPortion item : itensTexto2) {
            l2.getTextData().addPortion(item);
        }

        l1.getTextData().updateLayerData();
        l2.getTextData().updateLayerData();

        imagemPsd.save(outputFile);
    }
{{< /highlight >}}


** PSDJAVA-532. Após exportar o arquivo PSD com CMYK, as cores no arquivo PSD exportado são alteradas**

{{< highlight java >}}
    String arquivoFonte = "src/main/resources/canyon.psd";
    String outputFilePng = "src/main/resources/saida_canyon.png";

    MemoryStream outputStream = new MemoryStream();

    try (PsdImage imagemPsd = (PsdImage) Image.load(arquivoFonte)) {
        imagemPsd.save(outputStream.toOutputStream());
    }

    outputStream.setPosition(0);
    try (PsdImage imagemPsd = (PsdImage) Image.load(outputStream.toInputStream())) {
        imagemPsd.save(outputFilePng, new PngOptions());
    }

    outputStream.close();
{{< /highlight >}}


** PSDJAVA-533. Um arquivo PSB específico gera a exceção "O retângulo não possui uma área de processamento comum"**

{{< highlight java >}}
    String entrada = "src/main/resources/1619_source.psb";
    String saida = "src/main/resources/1619_output.png";

    PsdLoadOptions opcoesCarregamentoPsd = new PsdLoadOptions();
    opcoesCarregamentoPsd.setLoadEffectsResource(true);
    try (PsdImage imagem = (PsdImage) Image.load(entrada, opcoesCarregamentoPsd)) {
        PngOptions opcoesPng = new PngOptions();
        opcoesPng.setCompressionLevel(9);
        opcoesPng.setColorType(PngColorType.TruecolorWithAlpha);
        imagem.save(saida, opcoesPng);
    }
{{< /highlight >}}


** PSDJAVA-534. Falha no carregamento da imagem. OverflowException: A operação aritmética resultou em um estouro.**

{{< highlight java >}}
public static void main(String[] args) {
    String arquivoFonte = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage imagem = (PsdImage)PsdImage.load(arquivoFonte))
    {
        Layer camada = imagem.getLayers()[28];
        GrdmResource recursoGrdm = (GrdmResource)camada.getResources()[0];

        assertAreEqual("自定", recursoGrdm.getGradientName());
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
