---
title: Note sulla versione di Aspose.PSD per Java 23.7
type: docs
weight: 40
url: /it/java/aspose-psd-per-java-23-7-note-sulla-versione/
---

{{% alert color="primary" %}} Questa pagina contiene le note sulla versione di [Aspose.PSD per Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Chiave**   | **Sommario**                                                                                                                                   | **Categoria** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Aggiungi la capacità di esportare ogni layer del file PSD nel file Animated Gif                               | Caratteristica |
| PSDJAVA-503 | Assegna la proprietà di riempimento dello strato di forma dalla risorsa vscg                                     | Caratteristica |
| PSDJAVA-504 | Aggiungi nuovi tipi di distorsione (arco e arco)                                                             | Caratteristica |
| PSDJAVA-505 | Cambia l'applicazione che salva il file PSD in Aspose.PSD se la proprietà UpdateMetadata è impostata su true      | Caratteristica |
| PSDJAVA-510 | Aumenta l'area di calcolo dell'immagine distorta                                                               | Caratteristica |
| PSDJAVA-511 | Il Livello di regolazione Bianco e nero elabora erroneamente la semitrasparenza                                  | Errore     |
| PSDJAVA-512 | SmartObject ReplaceContents (quando l'opzione AllowWarpRepaint è attiva) fallisce dopo 2 minuti di calcolo | Errore     |
| PSDJAVA-513 | Aggiungi la capacità di ottenere la vera posizione Sinistra e Superiore del LayerGroup                         | Errore     |
| PSDJAVA-514 | Il ridimensionamento dello strato funziona male quando il file psd ha la risorsa Vogk con strutture in punti  | Errore     |
| PSDJAVA-515 | TextBound non funziona come previsto                                                                       | Errore     |
| PSDJAVA-516 | Aggiungere uno strato creato con il costruttore predefinito all'immagine PSD non aggiunge risorse predefinite ad esso | Errore     |
| PSDJAVA-517 | Timeline.LoopesCount viene ignorato durante l'esportazione in GIF animato                                  | Errore     |

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **API Rimosse:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Esempi d'uso:**

**PSDJAVA-502. Aggiungi la capacità di esportare ogni layer del file PSD nel file Animated Gif**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Crea frames per ogni layer.
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

        // Aggiorna gli stati correnti
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Assegna la proprietà di riempimento dello strato di forma dalla risorsa vscg**

{{< highlight java >}}
      // Esempio di riempimento solido
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

        // Verifica le modifiche salvate
        try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        ShapeLayer shapeLayer = (ShapeLayer) image.getLayers()[1];
        ColorFillSettings fillSettings = (ColorFillSettings) shapeLayer.getFill();

        assertAreEqual(Color.getRed(), fillSettings.getColor());

        image.save(outFile);
    }

    // Esempio di riempimento a gradiente

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

        // Verifica le modifiche salvate
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
}

{{< /highlight >}}

**PSDJAVA-504. Aggiungi nuovi tipi di distorsione (arco e arco)**

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

**PSDJAVA-505. Cambia l'applicazione che salva il file PSD in Aspose.PSD se la proprietà UpdateMetadata è impostata su true**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Se vuoi cambiare lo strumento creatore, assicurati che la proprietà "UpdateMetadata" sia impostata su true. Di default è impostata su true.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // Salvataggio dell'immagine.
        image.save(path, psdOptions);

        // Verifica strumento creatore nel codice.
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // Qui verrà aggiornata l'informazione sullo strumento creatore.
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. Aumenta l'area di calcolo dell'immagine distorta**

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

**PSDJAVA-511. Il Livello di regolazione Bianco e nero elabora erroneamente la semitrasparenza**

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

    // Verifica le modifiche salvate
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("Il Livello 2 dovrebbe essere un Livello di regolazione Bianco e nero");
        }

        image.save(outFile);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
       throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (quando l'opzione AllowWarpRepaint è attiva) fallisce dopo 2 minuti di calcolo**

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

**PSDJAVA-513. Aggiungi la capacità di ottenere la vera posizione Sinistra e Superiore del LayerGroup**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/layerGroupFigures.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer[] layers = image.getLayers();

        for (int i = 0; i < layers.length; i++) {
            Layer layer = layers[i];

            if (layer instanceof LayerGroup) {
                {
                    // Ottieni il LayerGroup.
                    LayerGroup group = (LayerGroup) layer;

                    int expectedLeft = Integer.MAX_VALUE;
                    int expectedTop = Integer.MAX_VALUE;
                    int expectedRight = 0;
                    int expectedBottom = 0;

                    // Calcola le vere posizioni Sinistra, Superiore, Destra e Inferiore.
                    for (Layer innerLayer : group.getLayers()) {
                        if (innerLayer instanceof AdjustmentLayer || innerLayer.getBounds().isEmpty()) {
                            continue;
                        }

                        expectedLeft = Math.min(expectedLeft, innerLayer.getLeft());
                        expectedTop = Math.min(expectedTop, innerLayer.getTop());
                        expectedRight = Math.max((expectedLeft + group.getWidth()), (innerLayer.getLeft() + innerLayer.getWidth()));
                        expectedBottom = Math.max((expectedTop + group.getHeight()), (innerLayer.getTop() + innerLayer.getHeight()));
                    }

                    // Le posizioni Sinistra, Superiore, Destra e Inferiore del LayerGroup sono calcolate correttamente ora.
                    assertAreEqual(group.getLeft(), expectedLeft);
                    assertAreEqual(group.getTop(), expectedTop);
                    assertAreEqual(group.getRight(), expectedRight);
                    assertAreEqual(group.getBottom(), expectedBottom);
                }
            }
        }
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Gli oggetti non sono uguali.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-514. Il ridimensionamento dello strato funziona male quando il file psd ha la risorsa Vogk con strutture in punti**

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
            assertAreEqual(layer.getWidth(), 50);
        }
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assert