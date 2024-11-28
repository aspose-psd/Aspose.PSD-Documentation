---
title: Aspose.PSD voor Java 23.7 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-23-7-release-notities/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 23.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.7/) {{% /alert %}}

| **Sleutel**   | **Samenvatting**                                                                                                                                         | **Categorie** |
|:--------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-502   | Voeg de mogelijkheid toe om elk laag van PSD-bestand naar het geanimeerde Gif-bestand te exporteren                                                     | Functie       |
| PSDJAVA-503   | Wijs Vul-eigenschap van Vorm laag toe van vscg resource                                                       | Functie       |
| PSDJAVA-504   | Voeg nieuwe typen kromming toe (boog & boog)                                                                           | Functie       |
| PSDJAVA-505   | Wijzig de applicatie die het PSD-bestand opslaat naar Aspose.PSD als eigenschap UpdateMetadata op true is ingesteld                                      | Functie       |
| PSDJAVA-510   | Vergroot het berekeningsgebied van de vervormingsafbeelding                                                              | Functie       |
| PSDJAVA-511   | Zwarte en witte aanpassingslaag verwerkt halftransparantie verkeerd                                           | Fout          |
| PSDJAVA-512   | SmartObject ReplaceContents (wanneer de optie AllowWarpRepaint actief is) valt na 2 minuten van berekening                                               | Fout          |
| PSDJAVA-513   | Voeg de mogelijkheid toe om de werkelijke positie van de linker- en bovenkant van LayerGroup te krijgen                                                | Fout          |
| PSDJAVA-514   | De grootte van de laag werkt verkeerd wanneer het psd-bestand een VogkResource heeft met structuren in punten                                            | Fout          |
| PSDJAVA-515   | Textbound werkt niet zoals verwacht                                                                         | Fout          |
| PSDJAVA-516   | Het toevoegen van een laag gemaakt met een standaardconstructeur aan een PSD-afbeelding voegt geen standaardbronnen eraan toe                           | Fout          |
| PSDJAVA-517   | Timeline.LoopesCount wordt genegeerd bij exporteren naar geanimeerde GIF                                           | Fout          |

## **Openbare API-wijzigingen**
# **Toegevoegde API's:**

- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf17
- F:com.aspose.psd.fileformats.ai.AiFormatVersion.Pdf16
- M:com.aspose.psd.imageoptions.PsdOptions.getUpdateMetadata
- M:com.aspose.psd.imageoptions.PsdOptions.setUpdateMetadata(boolean)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.containsKey(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.get_Item(java.lang.String)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.set_Item(java.lang.String,java.lang.Object)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setValue(java.lang.String,com.aspose.psd.xmp.IXmlValue)

# **Verwijderde API's:**

- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setCreatedDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setMetadataDate(java.util.Date)
- M:com.aspose.psd.xmp.schemas.xmpbaseschema.XmpBasicPackage.setModifyDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.getFillColor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPath.setFillColor(com.aspose.psd.Color)

## **Gebruik voorbeelden:**

**PSDJAVA-502. Voeg de mogelijkheid toe om elk laag van PSD-bestand naar het geanimeerde Gif-bestand te exporteren**

{{< highlight java >}}
    String src = "src/main/resources/EachLayerIsFrame.psd";
    String outputGif = "src/main/resources/out_EachLayerIsFrame.gif";
    String outputPsd = "src/main/resources/out_EachLayerIsFrame.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        // Creëer frames voor elke laag.
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

        // Werk huidige staten bij
        Layer[] layers = psdImage.getLayers();
        LayerState[] states = timeline.getFrames()[timeline.getActiveFrameIndex()].getLayerStates();
        for (int i = 0; i < framesCount; i++) {
            layers[i].setVisible(states[i].getEnabled());
        }

        timeline.save(outputGif, new GifOptions());
        psdImage.save(outputPsd);
    }
{{< /highlight >}}

**PSDJAVA-503. Wijs Vul-eigenschap van Vorm laag toe van vscg resource**

{{< highlight java >}}
        // Voorbeeld van volledig vullen
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

            // Controleer opgeslagen veranderingen
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
            assertAreEqual(expected, actual, "Objecten zijn niet gelijk.");
        }
		
		// Voorbeeld van kleurovergang:

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

    // Controleer opgeslagen veranderingen
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
    assertAreEqual(expected, actual, "Objecten zijn niet gelijk.");
}

{{< /highlight >}}

**PSDJAVA-504. Voeg nieuwe typen kromming toe (boog & boog)**

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

**PSDJAVA-505. Wijzig de applicatie die het PSD-bestand opslaat naar Aspose.PSD als eigenschap UpdateMetadata op true is ingesteld**

{{< highlight java >}}
    String pad = "src/main/resources/output.psd";
    try