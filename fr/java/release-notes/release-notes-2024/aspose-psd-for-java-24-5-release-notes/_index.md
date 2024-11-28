---
title: Notes de publication Aspose.PSD pour Java 24.5
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-24-5-notes-de-release/
---

{{% alert color="primary" %}} Cette page contient les notes de publication pour [Aspose.PSD pour Java 24.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.5/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                             | **Catégorie**  |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-617 | [Format AI] Ajouter la prise en charge du traitement des fichiers AI avec en-tête EPSF                               | Fonctionnalité       |
| PSDJAVA-620 | La semi-transparence est mal traitée lors de l'aperçu du fichier psd                                               | Incident           |
| PSDJAVA-621 | Rendu partiellement incorrect de la couche de forme                                                                    | Incident           |
| PSDJAVA-622 | Exception lors de l'enregistrement de fichiers PSD de plus de 200 Mo et de grandes dimensions (Problème lié à l'utilisation de la mémoire) | Incident           |
| PSDJAVA-623 | Exception d'échec de sauvegarde d'image lors de la sauvegarde en PDF après la mise à jour de 23.7 à 24.3         | Incident           |
| PSDJAVA-624 | Corriger le problème dans la méthode GetFontInfoRecords pour les polices chinoises                                   | Incident           |

## **Changements d'API publics**
# **APIs ajoutées :**

- M:com.aspose.psd.fileformats.ai.AiLayerSection.getColorIndex
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setColorIndex(int)
- M:com.aspose.psd.fileformats.ai.AiLayerSection.hasMultiLayerMasks
- M:com.aspose.psd.fileformats.ai.AiLayerSection.setMultiLayerMasks(boolean)
- M:com.aspose.psd.imageoptions.PsdOptions.getBackgroundContents
- M:com.aspose.psd.imageoptions.PsdOptions.setBackgroundContents(com.aspose.psd.fileformats.psd.rawcolor.RawColor)

# **APIs supprimées :**

- Aucune

## **Exemples d'utilisation :**

**PSDJAVA-617. [Format AI] Ajouter la prise en charge du traitement des fichiers AI avec en-tête EPSF**

{{< highlight java >}}


    public static void main(String[] args) {
        String sourceFile = "src/main/resources/example.ai";
        String outputFilePath = "src/main/resources/example.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            assertAreEqual(image.getLayers().length, 2);
            assertAreEqual(image.getLayers()[0].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[0].getColorIndex(), -1);
            assertAreEqual(image.getLayers()[1].hasMultiLayerMasks(), false);
            assertAreEqual(image.getLayers()[1].getColorIndex(), -1);

            image.save(outputFilePath, new PngOptions());
        }
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-620. La semi-transparence est mal traitée lors de l'aperçu du fichier psd**

{{< highlight java >}}


        String sourceFile = "src/main/resources/frog_nosymb.psd";
        String outputFile = "src/main/resources/frog_nosymb_backgroundcontents_output.psd";

        try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
            RawColor backgroundColor = new RawColor(PixelDataFormat.getRgb32Bpp());
            int argbValue = 255 << 24 | 255 << 16 | 255 << 8 | 255;
            backgroundColor.setAsInt(argbValue); // Blanc

            PsdOptions psdOptions = new PsdOptions(psdImage);
            psdOptions.setColorMode(ColorModes.Rgb);
            psdOptions.setCompressionMethod(CompressionMethod.RLE);
            psdOptions.setChannelsCount((short) 4);
            psdOptions.setBackgroundContents(backgroundColor);

            psdImage.save(outputFile, psdOptions);
        }

{{< /highlight >}}

**PSDJAVA-621. Rendu partiellement incorrect de la couche de forme**

{{< highlight java >}}


    private static final int ImgToPsdRatio = 256 * 65535;

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/ShapeLayerTest.psd";
        String outputFile = "src/main/resources/ShapeLayerTest_output.psd";
        
        try (PsdImage im = (PsdImage) Image.load(sourceFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                Collections.addAll(knotsList, knots);
            }

            // Modifier les propriétés de la couche
            PathShape newShape = new PathShape();

            BezierKnotRecord firstBezierKnotRecord = new BezierKnotRecord();
            firstBezierKnotRecord.setLinked(true);
            firstBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 100),
                            shapeLayer.getContainer().getSize())});

            BezierKnotRecord secondBezierKnotRecord = new BezierKnotRecord();
            secondBezierKnotRecord.setLinked(true);
            secondBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(50, 490),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(100, 490),
                            shapeLayer.getContainer().getSize()), // Point d'ancrage
                    pointFToResourcePoint(
                            new PointF(150, 490),
                            shapeLayer.getContainer().getSize())
            });

            BezierKnotRecord thirdBezierKnotRecord = new BezierKnotRecord();
            thirdBezierKnotRecord.setLinked(true);
            thirdBezierKnotRecord.setPoints(new Point[]{
                    pointFToResourcePoint(
                            new PointF(490, 150),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 50),
                            shapeLayer.getContainer().getSize()),
                    pointFToResourcePoint(
                            new PointF(490, 20),
                            shapeLayer.getContainer().getSize()),
            });

            BezierKnotRecord[] bezierKnots = new BezierKnotRecord[]
                    {firstBezierKnotRecord, secondBezierKnotRecord, thirdBezierKnotRecord};

            newShape.setItems(bezierKnots);

            List<IPathShape> newShapes = new ArrayList<>(Arrays.asList(pathShapes));
            newShapes.add(newShape);

            IPathShape[] pathShapeNew = newShapes.toArray(new IPathShape[0]);
            path.setItems(pathShapeNew);

            shapeLayer.update();

            im.save(outputFile, new PsdOptions());
        }

        try (PsdImage im = (PsdImage) Image.load(outputFile)) {
            ShapeLayer shapeLayer = (ShapeLayer) im.getLayers()[2];
            IPath path = shapeLayer.getPath();
            IPathShape[] pathShapes = path.getItems();
            List<BezierKnotRecord> knotsList = new ArrayList<>();
            for (IPathShape pathShape : pathShapes) {
                BezierKnotRecord[] knots = pathShape.getItems();
                knotsList.addAll(Arrays.asList(knots));
            }

            assertAreEqual(3, pathShapes.length);
            assertAreEqual(42, shapeLayer.getLeft());
            assertAreEqual(14, shapeLayer.getTop());
            assertAreEqual(1600, shapeLayer.getBounds().getWidth());
            assertAreEqual(1086, shapeLayer.getBounds().getHeight());
        }
    }

    static Point pointFToResourcePoint(PointF point, Size imageSize) {
        return new Point(
                (int) Math.round(point.getY() * (ImgToPsdRatio / imageSize.getHeight())),
                (int) Math.round(point.getX() * (ImgToPsdRatio / imageSize.getWidth())));
    }

    static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
    }

    static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-622. Exception lors de l'enregistrement de fichiers PSD de plus de 200 Mo et de grandes dimensions (Il y a un problème lié à l'utilisation de la mémoire)**

{{< highlight java >}}


    String sourceFile = "src/main/resources/bigfile.psd";
    String outputFile = "src/main/resources/output_raw.psd";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setUseDiskForLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setCompressionMethod(CompressionMethod.RLE);

        // Il ne devrait pas y avoir d'erreur ici
        psdImage.save(outputFile, psdOptions);
    }

{{< /highlight >}}

**PSDJAVA-623. Exception d'échec de sauvegarde d'image lors de la sauvegarde en PDF après la mise à jour de 23.7 à 24.3**

{{< highlight java >}}


    String sourceFile = "src/main/resources/CVFlor.psd";
    String outputFile = "src/main/resources/_export.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-624. Corriger le problème dans la méthode GetFontInfoRecords pour les polices chinoises**

{{< highlight java >}}


    String fontFolder = "src/main/resources/Font";
    String sourceFile = "src/main/resources/bd-worlds-best-pink.psd";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    psdLoadOptions.setAllowWarpRepaint(true);

    try {
        FontSettings.setFontsFolders(new String[]{fontFolder}, true);

        try (PsdImage image = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
            for (Layer layer : image.getLayers()) {
                if (layer instanceof TextLayer) {
                    TextLayer textLayer = (TextLayer) layer;

                    if ("best".equals(textLayer.getText())) {
                        // Sans cette correction, il y aura une exception en raison de la police chinoise.
                        textLayer.updateText("SUCCÈS");
                    }
                }
            }
        }
    } finally {
        FontSettings.reset();
    }

{{< /highlight >}}