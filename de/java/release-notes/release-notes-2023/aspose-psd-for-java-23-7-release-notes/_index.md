---
title: Aspose.PSD für Java 23.7 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-23-7-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                                                                   | **Kategorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Fügen Sie die Möglichkeit hinzu, jeden Layer der PSD-Datei in eine animierte GIF-Datei zu exportieren                       | Feature |
| PSDJAVA-503 | Weisen Sie die Füllungseigenschaft der Formebene aus Ressource vscg zu                                                        | Feature |
| PSDJAVA-504 | Neue Arten von Verkrümmungen hinzufügen (Bogen & Bogen)                                                                      | Feature |
| PSDJAVA-505 | Ändern Sie die Anwendung, die die PSD-Datei speichert, auf Aspose.PSD, wenn die Eigenschaft UpdateMetadata auf true gesetzt ist | Feature |
| PSDJAVA-510 | Erhöhen Sie den Berechnungsbereich des Verkrümmungsbildes                                                                     | Feature |
| PSDJAVA-511 | Schwarz-Weiß-Anpassungsebene verarbeitet Halbtransparenz falsch                                                              | Fehler     |
| PSDJAVA-512 | SmartObject ReplaceContents (bei aktiver Option AllowWarpRepaint) stürzt nach 2 Minuten Berechnung ab                        | Fehler     |
| PSDJAVA-513 | Fügen Sie die Möglichkeit hinzu, die tatsächliche Position des LayerGroups-Links und der oberen Position zu erhalten       | Fehler     |
| PSDJAVA-514 | Die Größenänderung des Layers funktioniert falsch, wenn die PSD-Datei VogkResource mit Strukturen in Punkten enthält           | Fehler     |
| PSDJAVA-515 | TextBound funktioniert nicht wie erwartet                                                                                    | Fehler     |
| PSDJAVA-516 | Das Hinzufügen einer Ebene, die mit dem Standardkonstruktor erstellt wurde, zu einem PSD-Bild fügt keine Standardressourcen hinzu | Fehler     |
| PSDJAVA-517 | Die Timeline.LoopesCount wird beim Exportieren in ein animiertes GIF ignoriert                                               | Fehler     |

## **Änderungen in der öffentlichen API**
# **Hinzugefügte APIs:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Entfernte APIs:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Beispiele für die Verwendung:**

**PSDJAVA-502. Fügen Sie die Möglichkeit hinzu, jeden Layer der PSD-Datei in eine animierte GIF-Datei zu exportieren**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Rahmen für jeden Layer erstellen.
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

        // Aktuelle Zustände aktualisieren
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Weisen Sie die Füllungseigenschaft der Formebene aus der vscg-Ressource zu**

{{< highlight java >}}
        // Beispiel für eine feste Füllung
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

            // Überprüfen der gespeicherten Änderungen
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
            assertAreEqual(expected, actual, "Objects are not equal.");
        }
		
		// Beispiel für einen Farbverlauf
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

        // Überprüfen der gespeicherten Änderungen
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

**PSDJAVA-504. Erweitern Sie die Anwendung um neue Arten von Verkrümmungen (Bogen & Bogen)**

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

**PSDJAVA-505. Ändern Sie die Anwendung, die die PSD-Datei speichert, auf Aspose.PSD, wenn die Eigenschaft UpdateMetadata auf true gesetzt ist**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Wenn Sie möchten, dass das Ersteller-Tool geändert wird, stellen Sie sicher, dass die Eigenschaft "UpdateMetadata" auf true gesetzt ist. Sie ist standardmäßig auf true gesetzt.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // Bild speichern.
        image.save(path, psdOptions);

        // Überprüfen des Ersteller-Tools im Code.
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // Hier wird die aktualisierte Ersteller-Tool-Info sein.
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. Erhöhen Sie den Berechnungsbereich des Verkrümmungsbildes**

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

**PSDJAVA-511. Schwarz-Weiß-Anpassungsebene verarbeitet Halbtransparenz falsch**

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

    // Überprüfen der gespeicherten Änderungen
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("Ebene 2 sollte eine Schwarz-Weiß-Anpassungsebene sein");
        }

        image.save(outFile);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Objekte sind nicht gleich.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
       throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-512. SmartObject ReplaceContents (bei aktiver Option AllowWarpRepaint) stürzt nach 2 Minuten Berechnung ab**

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

**PSDJAVA-513. Fügen Sie die Möglichkeit hinzu, die tatsächliche Position des LayerGroups-Links und der oberen Position zu erhalten**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/layerGroupFigures.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer[] layers = image.getLayers();

        for (int i = 0; i < layers.length; i++) {
            Layer layer = layers[i];

            if (layer instanceof LayerGroup) {
                {
                    // LayerGroup abrufen.
                    LayerGroup group = (LayerGroup) layer;

                    int expectedLeft = Integer.MAX_VALUE;
                    int expectedTop = Integer.MAX_VALUE;
                    int expectedRight = 0;
                    int expectedBottom = 0;

                    // Echte links, obere, rechte und untere Positionen berechnen.
                    for (Layer innerLayer : group.getLayers()) {
                        if (innerLayer instanceof AdjustmentLayer || innerLayer.getBounds().isEmpty()) {
                            continue;
                        }

                        expectedLeft = Math.min(expectedLeft, innerLayer.getLeft());
                        expectedTop = Math.min(expectedTop, innerLayer.getTop());
                        expectedRight = Math.max((expectedLeft + group.getWidth()), (innerLayer.getLeft() + innerLayer.getWidth()));
                        expectedBottom = Math.max((expectedTop + group.getHeight()), (innerLayer.getTop() + innerLayer.getHeight()));
                    }

                    // Die Positionen links, oben, rechts und unten des LayerGroups sind jetzt korrekt berechnet.
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
    assertAreEqual(expected, actual, "Objekte sind nicht gleich.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-514. Die Größenänderung des Layers funktioniert falsch, wenn die PSD-Datei VogkResource mit Strukturen in Punkten enthält**

{{< highlight java >}}
public static void main(String[] args) {
    String[] sourceFiles = new String[]
            {
                    "src/main/resources/PointsVectorOrigin.psd",
                    "src/main/resources/TopVogkResStruct.psd"
            };

   