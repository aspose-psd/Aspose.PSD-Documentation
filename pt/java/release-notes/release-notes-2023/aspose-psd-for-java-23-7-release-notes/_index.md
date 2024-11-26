---
title: Notas de Lançamento Aspose.PSD para Java 23.7
type: docs
weight: 40
url: /pt/java/aspose-psd-for-java-23-7-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Chave**   | **Resumo**                                                                                                                                              | **Categoria** |
|:------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Adicionar capacidade de Exportar cada camada de arquivo PSD para o Arquivo Gif Animado                                     | Recurso |
| PSDJAVA-503 | Atribuir propriedade de Preenchimento da camada de forma a partir de recurso vscg                                            | Recurso |
| PSDJAVA-504 | Adicionar novos tipos de distorção (arco e arco)                                                                             | Recurso |
| PSDJAVA-505 | Alterar a aplicação que salva o arquivo PSD para Aspose.PSD se a propriedade UpdateMetadata estiver definida como true       | Recurso |
| PSDJAVA-510 | Aumentar a área de cálculo da imagem de distorção                                                                              | Recurso |
| PSDJAVA-511 | O Ajuste de Camada em Preto e Branco processa incorretamente a semitransparência                                             | Bug     |
| PSDJAVA-512 | SmartObject ReplaceContents (quando as opções AllowWarpRepaint estão ativas) falham após 2 minutos de computação             | Bug     |
| PSDJAVA-513 | Adicionar capacidade de obter a posição real Esquerda e Superior do LayerGroup                                                | Bug     |
| PSDJAVA-514 | O redimensionamento da camada funciona de forma incorreta quando o arquivo psd tem VogkResource com estruturas em pontos   | Bug     |
| PSDJAVA-515 | TextBound não está funcionando conforme o esperado                                                                           | Bug     |
| PSDJAVA-516 | Adicionar uma camada criada com construtor padrão à imagem PSD não adiciona recursos padrão a ela                           | Bug     |
| PSDJAVA-517 | Timeline.LoopesCount é ignorado ao exportar para GIF animado                                                                 | Bug     |

## **Alterações na API Pública**
# **APIs Adicionadas:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **APIs Removidas:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Exemplos de Uso:**

**PSDJAVA-502. Adicionar capacidade de Exportar cada camada de arquivo PSD para o Arquivo Gif Animado**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Criar frames para cada camada.
        int framesCount = psdImage.getLayers().length;
        Timeline timeline = psdImage.getTimeline();

        Frame[] frames = new Frame[framesCount];
        for (int i = 0; i < framesCount; i++) {
            frames[i] = new Frame();
            LayerState[] layerStates = new LayerState[framesCount];

            for (int j = 0; j < framesCount; j++) {
                layerStates[j] = new LayerState();
                layerStates[j].setEnabled(i == j);
            }

            frames[i].setLayerStates(layerStates);
        }

        timeline.setFrames(frames);

        // Atualizar estados atuais
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Atribuir propriedade de Preenchimento da camada de forma a partir de recurso vscg**

{{< highlight java >}}
        // Exemplo de preenchimento sólido
        public static void main(String[] args) {
            String srcFile = "src/main/resources/ShapeInternalSolid.psd";
            String outFile = "src/main/resources/ShapeInternalSolid.psd.out.psd";

            PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
            psdLoadOptions.setLoadEffectsResource(true);

            try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
                 ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
                  ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();
                 fillSettings.setColor(Color.getRed());

                 shapeLayer.update();

                 image.save(outFile);
            }

            // Verificar alterações salvas
            try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
            ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
            ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

            assertAreEqual(Color.getRed(), fillSettings.getColor());

            image.save(outFile);
        }

        static void assertAreEqual(Object expected, Object actual, String message) {
            if (!expected.equals(actual)) {
                throw new IllegalArgumentException(message);
            }
        }

        static void assertAreEqual(Object expected, Object actual) {
            assertAreEqual(expected, actual, "Os objetos não são iguais.");
        }
		
		// Exemplo de preenchimento gradiente:

	public static void main(String[] args) {
    String srcFile = "src/main/resources/ShapeInternalGradient.psd";
    String outFile = "src/main/resources/ShapeInternalGradient.psd.out.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();
        fillSettings.setDither(true);
        fillSettings.setReverse(true);
        fillSettings.setAlignWithLayer(false);
        fillSettings.setAngle(20);
        fillSettings.setScale(50);
        fillSettings.getColorPoints()[0].setLocation(100);
        fillSettings.getColorPoints()[1].setLocation(4000);
        fillSettings.getTransparencyPoints()[0].setLocation(200);
        fillSettings.getTransparencyPoints()[1].setLocation(3800);
        fillSettings.getTransparencyPoints()[0].setOpacity(90);
        fillSettings.getTransparencyPoints()[1].setOpacity(10);

        shapeLayer.update();

        image.save(outFile);
    }

    // Verificar alterações salvas
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        GradientFillSettings fillSettings = (GradientFillSettings) shapeLayer.getFill();

        assertAreEqual(true, fillSettings.getDither());
        assertAreEqual(true, fillSettings.getReverse());
        assertAreEqual(false, fillSettings.getAlignWithLayer());
        assertAreEqual((double) 20, fillSettings.getAngle());
        assertAreEqual(50, fillSettings.getScale());
        assertAreEqual(100, fillSettings.getColorPoints()[0].getLocation());
        assertAreEqual(4000, fillSettings.getColorPoints()[1].getLocation());
        assertAreEqual(200, fillSettings.getTransparencyPoints()[0].getLocation());
        assertAreEqual(3800, fillSettings.getTransparencyPoints()[1].getLocation());
        assertAreEqual((double) 90, fillSettings.getTransparencyPoints()[0].getOpacity());
        assertAreEqual((double) 10, fillSettings.getTransparencyPoints()[1].getOpacity());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Os objetos não são iguais.");
}

{{< /highlight >}}

**PSDJAVA-504. Adicionar novos tipos de distorção (arco e arco)**

{{< highlight java >}}
    String sourceArcFile = "src/main/resources/arc_warp.psd";
    String outputArcFile = "src/main/resources/arc_export.png";

    String sourceArchFile = "src/main/resources/arch_warp.psd";
    String outputArchFile = "src/main/resources/arch_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceArcFile, psdLoadOptions)) {
        psdImage.save(outputArcFile, pngOptions);
    }


    try (PsdImage psdImage = (PsdImage) Image.load(sourceArchFile, psdLoadOptions)) {
        psdImage.save(outputArchFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-505. Alterar a aplicação que salva o arquivo PSD para Aspose.PSD se a propriedade UpdateMetadata estiver definida como true**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Se deseja alterar a ferramenta criadora, certifique-se de que a propriedade "UpdateMetadata" esteja definida como true. Por padrão, está definida como true.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // Salvando a imagem.
        image.save(path, psdOptions);

        // Verificando a ferramenta criadora no código.
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // Aqui será atualizada a informação da ferramenta criadora.
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. Aumentar a área de cálculo da imagem de distorção**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug4_warp.psd";
    String outputFile = "src/main/resources/mug4_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-511. O Ajuste de Camada em Preto e Branco processa a semitransparência de forma errada**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/frog_nosymb.psd";
    String outFile = "src/main/resources/frog_nosymb.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addBlackWhiteAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Verificar alterações salvas
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("Layer 2 should be BlackWhiteAdjustmentLayer");
        }

        image.save(outFile);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Os objetos não são iguais.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
       throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (quando as opções AllowWarpRepaint estão ativas) falham após 2 minutos de computação**

{{< highlight java >}}
    String sourceFile = "src/main/resources/mug 4.psd";
    String changeFile = "src/main/resources/artwork for replace.png";
    String outputFile = "src/main/resources/export.png";

    int newHeight = 300;

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        SmartObjectLayer smartObjectLayer = (SmartObjectLayer) psdImage.getLayers()[3];

        double scale = (double) newHeight / smartObjectLayer.getHeight();
        int newWidth = (int) Math.round(smartObjectLayer.getWidth() * scale);

        PsdImage innerImage = new PsdImage(newWidth, newHeight);
        innerImage.setResolution(72, 72);

        Stream innerStream = new FileStream(changeFile, FileMode.Open);
        Layer layer = new Layer(innerStream.toInputStream());
        layer.setHorizontalResolution(72);
        layer.setVerticalResolution(72);

        try {
            innerImage.addLayer(layer);

            smartObjectLayer.replaceContents(innerImage);
            smartObjectLayer.updateModifiedContent();

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            psdImage.save(outputFile, pngOptions);
        } finally {
            innerImage.dispose();
            innerStream.dispose();
            layer.dispose();
        }
    }
{{< /highlight >}}

**PSDJAVA-513. Adicionar capacidade de obter a posição real Esquerda e Superior do LayerGroup**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/layerGroupFigures.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer[] layers = image.getLayers();

        for (int i = 0; i < layers.length; i++) {
            Layer layer = layers[i];

            if (layer instanceof LayerGroup) {
                // Obter LayerGroup.
                LayerGroup group = (LayerGroup) layer;

                int expectedLeft = Integer.MAX_VALUE;
                int expectedTop = Integer.MAX_VALUE;
                int expectedRight = 0;
                int expectedBottom = 0;

                // Calcular posições reais da Esquerda, Superior, Direita e Inferior.
                for (Layer innerLayer : group.getLayers()) {
                    if (innerLayer instanceof AdjustmentLayer || innerLayer.getBounds().isEmpty()) {
                        continue;
                    }

                    expectedLeft = Math.min(expectedLeft, innerLayer.getLeft());
                    expectedTop = Math.min(expectedTop, innerLayer.getTop());
                    expectedRight = Math.max((expectedLeft + group.getWidth()), (innerLayer.getLeft() + innerLayer.getWidth()));
                    expectedBottom = Math.max((expectedTop + group.getHeight()), (innerLayer.getTop() + innerLayer.getHeight()));
                }

                // As posições de Esquerda, Superior, Direita e Inferior do LayerGroup são calculadas corretamente agora.
                assertAreEqual(group.getLeft(), expectedLeft);
                assertAreEqual(group.getTop(), expectedTop);
                assertAreEqual(group.getRight(), expectedRight);
                assertAreEqual(group.getBottom(), expectedBottom);
            }
        }
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Os objetos não são iguais.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-514. O redimensionamento da camada funciona de forma incorreta quando o arquivo psd tem VogkResource com estruturas em pontos**

{{< highlight java >}}
public static void main(String[] args) {
    String[] sourceFiles = new String[]
            {
                    "src/main/resources/PointsVectorOrigin.psd",
                    "src/main/resources/TopVogkResStruct.psd"
            };

    for (String sourceFile : sourceFiles) {
        try (PsdImage image = (PsdImage)Image.load(sourceFile))
        {
            Layer layer = image.getLayers()[0];

            layer.resize(50, 50);

            assertAreEqual(layer.getHeight(), 50);
