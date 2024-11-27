---
title: Notes de version Aspose.PSD pour Java 23.7
type: docs
weight: 40
url: /fr/java/aspose-psd-pour-java-23-7-notes-de-version/
---

{{% alert color="primary" %}} Cette page contient les notes de version pour [Aspose.PSD pour Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Clé**     | **Résumé**                                                                                                                                      | **Catégorie** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-502 | Ajouter la possibilité d'exporter chaque calque du fichier PSD vers le fichier Animated Gif                                  | Fonctionnalité |
| PSDJAVA-503 | Attribuer la propriété Remplissage du calque de forme à partir de la ressource vscg                                      | Fonctionnalité |
| PSDJAVA-504 | Ajouter de nouveaux types de déformations (arc & arch)                                                                   | Fonctionnalité |
| PSDJAVA-505 | Changer l'application qui enregistre le fichier PSD en Aspose.PSD si la propriété UpdateMetadata est définie sur true     | Fonctionnalité |
| PSDJAVA-510 | Augmenter la zone de calcul de l'image déformée                                                                           | Fonctionnalité |
| PSDJAVA-511 | Le calque d'ajustement noir et blanc traite mal la semi-transparence                                                    | Problème     |
| PSDJAVA-512 | Le remplacement de contenu SmartObject (lorsque l'option AllowWarpRepaint est active) tombe après 2 minutes de calcul    | Problème     |
| PSDJAVA-513 | Ajouter la possibilité d'obtenir la véritable position gauche et supérieure du Groupe de calques                        | Problème     |
| PSDJAVA-514 | Le redimensionnement du calque ne fonctionne pas correctement lorsque le fichier PSD contient une VogkResource avec des structures en points | Problème     |
| PSDJAVA-515 | TextBound ne fonctionne pas comme prévu                                                                                   | Problème     |
| PSDJAVA-516 | Ajouter un calque créé avec le constructeur par défaut à une image PSD ne lui ajoute pas des ressources par défaut        | Problème     |
| PSDJAVA-517 | Timeline.LoopesCount est ignoré lors de l'exportation en GIF animé                                                        | Problème     |

## **Modifications de l'API publique**
# **APIs ajoutées :**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **APIs supprimées :**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Exemples d'utilisation :**

**PSDJAVA-502. Ajouter la possibilité d'exporter chaque calque du fichier PSD vers le fichier Gif animé**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Créer des images pour chaque calque.
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

        // Mettre à jour les états actuels
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Attribuer la propriété Remplissage du calque de forme à partir de la ressource vscg**

{{< highlight java >}}
        // Exemple de remplissage solide
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

            // Vérifier les changements enregistrés
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
            assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
        }
		
		// Exemple de remplissage dégradé:

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

    // Vérifier les changements enregistrés
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
    assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
}

{{< /highlight >}}

**PSDJAVA-504. Ajouter de nouveaux types de déformations (arc & arch)**

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

**PSDJAVA-505. Changer l'application qui enregistre le fichier PSD en Aspose.PSD si la propriété UpdateMetadata est définie sur true**

{{< highlight java >}}
    String path = "src/main/resources/output.psd";
    try (PsdImage image = new PsdImage(100, 100)) {
        // Si vous souhaitez modifier l'outil de création, assurez-vous que la propriété "UpdateMetadata" est définie sur true. Elle est par défaut à true.
        PsdOptions psdOptions = new PsdOptions();
        psdOptions.setUpdateMetadata(true);

        // Enregistrement de l'image.
        image.save(path, psdOptions);

        // Vérification de l'outil de création dans le code.
        XmpPacketWrapper xmpData = image.getXmpData();
        XmpPackage basicPackage = image.getXmpData().getPackage(Namespaces.XmpBasic);

        // Ici, les informations sur l'outil de création seront mises à jour.
        String currentCreatorTool = (String) basicPackage.get_Item(":CreatorTool");
{{< /highlight >}}

**PSDJAVA-510. Augmenter la zone de calcul de l'image déformée**

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

**PSDJAVA-511. Le calque d'ajustement noir et blanc traite mal la semi-transparence**

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

    // Vérifier les changements enregistrés
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        BlackWhiteAdjustmentLayer blackWhiteAdjustmentLayer = (BlackWhiteAdjustmentLayer) image.getLayers()[1];

        if (blackWhiteAdjustmentLayer == null) {
            throw new Exception("Le calque 2 devrait être BlackWhiteAdjustmentLayer");
        }

        image.save(outFile);
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

**PSDJAVA-512. Le remplacement de contenu SmartObject (lorsque l'option AllowWarpRepaint est active) tombe après 2 minutes de calcul**

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

**PSDJAVA-513. Ajouter la possibilité d'obtenir la véritable position gauche et supérieure du Groupe de calques**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/layerGroupFigures.psd";

    try (PsdImage image = (PsdImage) Image.load(sourceFile)) {
        Layer[] layers = image.getLayers();

        for (int i = 0; i < layers.length; i++) {
            Layer layer = layers[i];

            if (layer instanceof LayerGroup) {
                {
                    // Obtenir le LayerGroup.
                    LayerGroup group = (LayerGroup) layer;

                    int expectedLeft = Integer.MAX_VALUE;
                    int expectedTop = Integer.MAX_VALUE;
                    int expectedRight = 0;
                    int expectedBottom = 0;

                    // Calcul des véritables positions gauche, supérieure, droite et inférieure.
                    for (Layer innerLayer : group.getLayers()) {
                        if (innerLayer instanceof AdjustmentLayer || innerLayer.getBounds().isEmpty()) {
                            continue;
                        }

                        expectedLeft = Math.min(expectedLeft, innerLayer.getLeft());
                        expectedTop = Math.min(expectedTop, innerLayer.getTop());
                        expectedRight = Math.max((expectedLeft + group.getWidth()), (innerLayer.getLeft() + innerLayer.getWidth()));
                        expectedBottom = Math.max((expectedTop + group.getHeight()), (innerLayer.getTop() + innerLayer.getHeight()));
                    }

                    // Les positions gauche, supérieure, droite et inférieure du calque de groupe sont maintenant correctement calculées.
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
    assertAreEqual(expected, actual, "Les objets ne sont pas égaux.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-514. Le redimensionnement du calque ne fonctionne pas correctement lorsque le fichier PSD contient une VogkResource avec des structures en points**

{{< highlight java >}}
public static void main(String[] args) {
    String[] sourceFiles = new String[]
            {
                    "src/main/resources/PointsVectorOrigin.psd",
                    "src/main/resources/TopVogkResStruct