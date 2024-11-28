---
title: Notas da Versão Aspose.PSD para Java 24.7
type: docs
weight: 40
url: /pt/java/aspose-psd-para-java-24-7-notas-da-versao/
---

{{% alert color="primary" %}} Esta página contém as notas da versão para [Aspose.PSD para Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                                       | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Exceção "Falha ao carregar imagem" ao abrir documento AI                                          | Bug          |
| PSDJAVA-636 | Texto renderizado incorretamente em arquivos PDF de saída                                         | Bug          |
| PSDJAVA-637 | Corrigir ImageSaveException: falha na exportação da imagem para o arquivo fornecido no Linux     | Bug          |
| PSDJAVA-638 | Corrigir carregamento de fontes ao usar Aspose.Drawing                                             | Bug          |
| PSDJAVA-639 | 'Operação aritmética resultou em um estouro' ao criar camada de objeto inteligente usando JPEG grande | Bug       |
| PSDJAVA-640 | O arquivo AI não pode ser convertido em um arquivo JPG                                           | Bug          |


## **Alterações na API pública**
# **APIs Adicionadas:**

- Nenhuma

# **APIs Removidas:**

- Nenhuma 

## **Exemplos de uso:**

**PSDJAVA-635. Exceção "Falha ao carregar imagem" ao abrir documento AI**

{{< highlight java >}}

    String arquivoOrigem = "src/main/resources/[SA]_ID_card_template.ai";
    String arquivoSaida = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(arquivoOrigem)) {
        image.save(arquivoSaida, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Texto renderizado incorretamente em arquivos PDF de saída**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Corrigir ImageSaveException: falha na exportação da imagem para o arquivo fornecido no Linux**

{{< highlight java >}}

    String arquivoOrigem = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String arquivoSaida = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(arquivoOrigem, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(arquivoSaida, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Corrigir carregamento de fontes ao usar Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Antes da atualização. Contagem de fontes instaladas: " + installedFonts.getFamilies().length);
        System.out.println("- Plataforma: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Atualizar o cache de fontes ao tentar obter o nome da fonte da Adobe para 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Após a atualização. Contagem de fontes instaladas: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Operação aritmética resultou em um estouro' ao criar camada de objeto inteligente usando JPEG grande**

{{< highlight java >}}

    String arquivoOrigem = "src/main/resources/source.psd";
    String imagemJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var imagem = (PsdImage) Image.load(arquivoOrigem, psdLoadOptions)) {
        final FileStream stream = new FileStream(imagemJpg, FileMode.Open);
        try {
            var camadaAdicionada = new SmartObjectLayer(stream);
            camadaAdicionada.setName("Camada de Teste");
            imagem.addLayer(camadaAdicionada);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. O arquivo AI não pode ser convertido em um arquivo JPG**

{{< highlight java >}}

    String arquivoOrigem = "src/main/resources/aaa.ai";
    String arquivoSaida = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(arquivoOrigem)) {
        image.save(arquivoSaida, new PngOptions());
    }

{{< /highlight >}}
