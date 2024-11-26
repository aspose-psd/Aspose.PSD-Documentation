---
title: Notas da Versão do Aspose.PSD para Java 23.8
type: docs
weight: 40
url: /pt/java/aspose-psd-para-java-23-8-notas-de-lancamento/
---

{{% alert color="primary" %}} Esta página contém as notas da versão do [Aspose.PSD para Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                                    | **Categoria** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Adicionar novo tipo de deformação (Flag)                                                                                                       |    Recurso   |
| PSDJAVA-519 | Adicionar novos tipos de deformação: arco para cima, arco para baixo, esfera                                                                   |    Recurso   |
| PSDJAVA-520 | Implementar novo método PsdImage.AddPosterizeAdjustmentLayer para adicionar nova camada Posterize                                             |    Recurso   |
| PSDJAVA-521 | Informações do PSD perdidas apenas ao abrir e salvar                                                                                            |      Bug     |
| PSDJAVA-522 | Falha no carregamento da imagem                                                                                                                |      Bug     |
| PSDJAVA-523 | Falha no carregamento da imagem: Não é possível converter um objeto do tipo UnknownStructure para o tipo DescriptorStructure                |      Bug     |
| PSDJAVA-524 | Arquivo alterado na biblioteca de terceiros corrompe o arquivo PSD, mas pode ser aberto no Photoshop                                           |      Bug     |

## **Alterações na API Pública**
# **APIs Adicionadas:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **APIs Removidas:**

- Nenhuma

## **Exemplos de Uso:**

**PSDJAVA-518. Adicionar novo tipo de deformação (Flag)**

{{< highlight java >}}
    String arquivoFonte = "src/main/resources/flag_warp.psd";
    String arquivoSaida = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(arquivoFonte, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(arquivoSaida, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Adicionar novos tipos de deformação: arco para cima, arco para baixo, esfera**

{{< highlight java >}}
    String arquivoArcoSuperior = "src/main/resources/arc_upper_warp.psd";
    String arquivoArcoInferior = "src/main/resources/arc_lower_warp.psd";
    String arquivoSaliente = "src/main/resources/bulge_warp.psd";

    String arquivoSaidaArcoSuperior = "src/main/resources/ArcUpper_export.png";
    String arquivoSaidaArcoInferior = "src/main/resources/ArcLower_export.png";
    String arquivoSaidaSaliente = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoArcoSuperior, psdLoadOptions)) {
        psdImage.save(arquivoSaidaArcoSuperior, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoArcoInferior, psdLoadOptions)) {
        psdImage.save(arquivoSaidaArcoInferior, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoSaliente, psdLoadOptions)) {
        psdImage.save(arquivoSaidaSaliente, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Implementar novo método PsdImage.AddPosterizeAdjustmentLayer para adicionar nova camada Posterize**

{{< highlight java >}}
public static void main(String[] args) {
    String arquivoSrc = "src/main/resources/zendeya.psd";
    String arquivoOut = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoSrc)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(arquivoOut);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Verificar alterações salvas
    try (PsdImage imagem = (PsdImage) Image.load(arquivoOut, psdLoadOptions)) {
        assertAreEqual(2, imagem.getLayers().length);

        PosterizeLayer camadaPosterize = (PosterizeLayer) imagem.getLayers()[1];

        assertAreEqual(true, camadaPosterize instanceof PosterizeLayer);
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

**PSDJAVA-521. Informações PSD perdidas apenas ao abrir e salvar**

{{< highlight java >}}
    String src = "src/main/resources/Arquivo_original.psd";
    String outputPsd = "src/main/resources/out_Arquivo_original.psd";
    String outputPng = "src/main/resources/out_Arquivo_original.png";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Falha no carregamento da imagem**

{{< highlight java >}}
    String arquivoFonte1 = "src/main/resources/test_text.psd";
    String arquivoFonte2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoFonte1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(arquivoFonte2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Falha no carregamento da imagem: Não é possível converter um objeto do tipo UnknownStructure para o tipo DescriptorStructure**

{{< highlight java >}}
   try (PsdImage novoPsd = new PsdImage(10, 10)) {
        novoPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            novoPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // Deve carregar corretamente
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Arquivo alterado na biblioteca de terceiros corrompe o arquivo PSD, mas pode ser aberto no Photoshop**

{{< highlight java >}}
    String arquivoFonte = "src/main/resources/saida.psd";
    String arquivoSaida = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(arquivoFonte, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(arquivoSaida, pngOptions);
    }
{{< /highlight >}}
