---
title: Aspose.PSD para Java 23.11 - Notas de Lançamento
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-23-11-release-notes/
---

{{% alert color="primary" %}}Esta página contém as notas de lançamento para [Aspose.PSD para Java 23.11](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.11/){{% /alert %}}

| **Chave**       | **Resumo**                                                                                                 | **Categoria** |
|:---------------|:-----------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-551    | Suporte para LMskResource                                                                                 |    Recurso   |
| PSDJAVA-552    | [Formato AI] Adicionada capacidade de renderizar arquivo AI baseado em PDF com Aspose.PSD                   |    Recurso   |
| PSDJAVA-553    | [Formato AI] Adicionado suporte para o operador PostScript “cm”                                             |    Recurso   |
| PSDJAVA-554    | Adicionados novos tipos de distorção: Onda, concha para cima, concha para baixo                              |    Recurso   |
| PSDJAVA-555    | Adicionado suporte para distorção vertical                                                                 |    Recurso   |
| PSDJAVA-556    | System.ArgumentNullException: ‘Valor não pode ser nulo. (Parâmetro ‘chave’)’ ao chamar TextLayer.GetFonts()  |      Erro     |

## **Mudanças na API Pública**
# **APIs Adicionadas:**

- M:com.aspose.psd.FontSettings.removeFontCacheFile
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

# **APIs Removidas:**

- M:com.aspose.psd.fileformats.psd.coreexceptions.LicenseException.#ctor(java.lang.String,java.lang.Throwable)

## **Exemplos de Uso:**

**PSDJAVA-551. Suporte para LMskResource**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/sourceFile.psd";
        String outputPsd = "src/main/resources/sourceFile_output.psd";

        // Carregar imagem de 16 bits.
        try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
            // Encontrar LmskResource.
            LmskResource lmskResource = new LmskResource();
            for (LayerResource res : image.getGlobalLayerResources()) {
                if (res instanceof LmskResource) {
                    lmskResource = (LmskResource) res;
                    break;
                }
            }

            // Verificar propriedades do LmskResource.
            assertAreEqual(lmskResource.getColorSpace(), ColorSpace.RGB);
            assertAreEqual(lmskResource.getColorComponent1(), 65535);
            assertAreEqual(lmskResource.getColorComponent2(), 0);
            assertAreEqual(lmskResource.getColorComponent3(), 0);
            assertAreEqual(lmskResource.getColorComponent4(), 0);
            assertAreEqual(lmskResource.getOpacity(), (short) 45);
            assertAreEqual(lmskResource.getFlag(), (byte) 128);

            // Alterar propriedades do LmskResource.
            lmskResource.setColorSpace(ColorSpace.HSB);
            lmskResource.setColorComponent1(7854);
            lmskResource.setColorComponent2(10);
            lmskResource.setColorComponent3(15484);
            lmskResource.setOpacity((short) 85);

            // Salvar a imagem.
            image.save(outputPsd);
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objetos não são iguais.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-552. [Formato AI] Adicionada capacidade de renderizar arquivo AI baseado em PDF com Aspose.PSD**

{{< highlight java >}}

    String sourceFile = "src/main/resources/ai_one.ai";
    String outputPng = "src/main/resources/ai_one_output.psd";

    // Carregar a imagem AI baseada em PDF.
    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        // Salvar a imagem AI como uma imagem PNG.
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-553. [Formato AI] Adicionado suporte para o operador PostScript “cm”**

{{< highlight java >}}

    String sourceFile = "src/main/resources/ai_two.ai";
    String outputPng = "src/main/resources/ai_two_output.png";

    // Carregar a imagem AI.
    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        // Salvar a imagem AI como uma imagem PNG.
        image.save(outputPng, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-554. Adicionar novos tipos de distorção: Onda, concha para cima, concha para baixo**

{{< highlight java >}}

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setAllowWarpRepaint(true);
    loadOptions.setLoadEffectsResource(true);

    PngOptions saveOptions = new PngOptions();
    saveOptions.setColorType(PngColorType.TruecolorWithAlpha);

    String sourceFileFish = "src/main/resources/1752_warp_fish.psd";
    String sourceFileRise = "src/main/resources/1752_warp_rise.psd";
    String sourceFileWave = "src/main/resources/1752_warp_wave.psd";

    String outputFileFish = "src/main/resources/1752_output_fish.png";
    String outputFileRise = "src/main/resources/1752_output_rise.png";
    String outputFileWave = "src/main/resources/1752_output_wave.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileFish, loadOptions)) {
        psdImage.save(outputFileFish, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileRise, loadOptions)) {
        psdImage.save(outputFileRise, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileWave, loadOptions)) {
        psdImage.save(outputFileWave, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-555. Adicionar suporte para distorção vertical**

{{< highlight java >}}

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setAllowWarpRepaint(true);
    loadOptions.setLoadEffectsResource(true);

    PngOptions saveOptions = new PngOptions();
    saveOptions.setColorType(PngColorType.TruecolorWithAlpha);

    String sourceFileArcLower = "src/main/resources/1797_warp_arc_lower_v.psd";
    String sourceFileArcUpper = "src/main/resources/1797_warp_arc_upper_v.psd";
    String sourceFileArch = "src/main/resources/1797_warp_arch_v.psd";
    String sourceFileBulge = "src/main/resources/1797_warp_bulge_v.psd";
    String sourceFileFlag = "src/main/resources/1797_warp_flag_v.psd";
    String sourceFileFish = "src/main/resources/1797_warp_fish_v.psd";
    String sourceFileRise = "src/main/resources/1797_warp_rise_v.psd";
    String sourceFileWave = "src/main/resources/1797_warp_wave_v.psd";

    String outputFileArcLower = "src/main/resources/1797_warp_arc_lower_v.png";
    String outputFileArcUpper = "src/main/resources/1797_warp_arc_upper_v.png";
    String outputFileArch = "src/main/resources/1797_warp_arch_v.png";
    String outputFileBulge = "src/main/resources/1797_warp_bulge_v.png";
    String outputFileFlag = "src/main/resources/1797_warp_flag_v.png";
    String outputFileFish = "src/main/resources/1797_output_fish_v.png";
    String outputFileRise = "src/main/resources/1797_output_rise_v.png";
    String outputFileWave = "src/main/resources/1797_output_wave_v.png";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcLower, loadOptions)) {
        psdImage.save(outputFileArcLower, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcUpper, loadOptions)) {
        psdImage.save(outputFileArcUpper, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArch, loadOptions)) {
        psdImage.save(outputFileArch, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileBulge, loadOptions)) {
        psdImage.save(outputFileBulge, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileFlag, loadOptions)) {
        psdImage.save(outputFileFlag, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileFish, loadOptions)) {
        psdImage.save(outputFileFish, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileRise, loadOptions)) {
        psdImage.save(outputFileRise, saveOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileWave, loadOptions)) {
        psdImage.save(outputFileWave, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-556. System.ArgumentNullException: 'Valor não pode ser nulo. (Parâmetro 'chave')' ao chamar TextLayer.GetFonts()**

{{< highlight java >}}

    String src = "src/main/resources/SimpleText.psd";

    FontSettings.removeFontCacheFile();

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        for (Layer layer : psdImage.getLayers()) {
            if (layer instanceof TextLayer) {
                TextLayer textLayer = (TextLayer) layer;
                textLayer.getFonts();
            }
        }
    }

{{< /highlight >}}