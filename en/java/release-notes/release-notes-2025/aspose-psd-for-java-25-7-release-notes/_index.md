---
title: Aspose.PSD for Java 25.7 - Release Notes
type: docs
weight: 40
url: /java/aspose-psd-for-java-25-7-release-notes/
---

{{% alert color="primary" %}} This page contains release notes
for[Aspose.PSD for Java 25.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-25.7/) {{%
/alert %}}

| **Key**     | **Summary**                                                                       | **Category** |
|:------------|:----------------------------------------------------------------------------------|:-------------|
| PSDJAVA-743 | Make TextLayer rendering not automatic to save original pixels before changes     | Feature      |
| PSDJAVA-750 | Add support for exporting Layers with Layer Effects to raster formats             | Feature      |
| PSDJAVA-751 | Add a property to toggle all layer effects visibility                             | Feature      |
| PSDJAVA-754 | Update the structure of Gradient classes. Create base class for Gradeint specific | Enhancement  |
| PSDJAVA-757 | Make correct initializing of Layers with Linked Layers Registry                   | Bug          |
| PSDJAVA-758 | Inaccurate rendering of Smart Object Layer                                        | Bug          |
| PSDJAVA-759 | Error when applying deformation due to invalid ‘Processing Area’ value is 2       | Bug          |

## **Public API Changes**

# **Added APIs:**

- 

# **Removed APIs:**

- None

## **Usage examples:**

**PSDJAVA-743. Make TextLayer rendering not automatic to save original pixels before changes.**

{{< highlight java >}}

    String srcFile = "src/main/resources/psdnet2400.psd";
    String output1 = "src/main/resources/unchanged-2400.png";
    String output2 = "src/main/resources/updated-2400.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowNonChangedLayerRepaint(false);
    try (var psdImage = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        psdImage.save(output1, new PngOptions());
        
        ((TextLayer) psdImage.getLayers()[1]).getTextData().updateLayerData();

        psdImage.save(output2, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-750. Add support for exporting Layers with Layer Effects to raster formats.**

{{< highlight java >}}

    String srcFile = "src/main/resources/1958.psd";
    String outputFile = "src/main/resources/out_1958.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        var layer1 = psdImage.getLayers()[1];

        var layerBoudns = layer1.getBounds();
        for (var effect : layer1.getBlendingOptions().getEffects()) {
            layerBoudns = Rectangle.union(
                layerBoudns,
                effect.getEffectBounds(layer1.getBounds(), psdImage.getGlobalAngle()));
        }

        Rectangle boundsToExport = Rectangle.getEmpty(); // The default value is to save only the layer with effects.
        // boundsToExport = psdImage.Bounds; // To save within the PsdImage bounds at the original layer location
        
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        layer1.save(
            outputFile,
            pngOptions,
            boundsToExport);
        final var imgStream = new FileStream(outputFile, FileMode.Open);
        try {
            var loadedLayer = new Layer(imgStream.toInputStream());
            if (loadedLayer.getSize() == layerBoudns.getSize()) {
                System.out.println("The size is calculated correctly.");
            }
        } finally {
            imgStream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-751. Add a property to toggle all layer effects visibility.**

{{< highlight java >}}

    String srcFile = "src/main/resources/2485.psd";
    String outputOnFile = "src/main/resources/on_2485.png";
    String outputOffFile = "src/main/resources/off_2485.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);
    try (var psdImage = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        psdImage.save(outputOnFile);

        psdImage.getLayers()[1].getBlendingOptions().setAreEffectsEnabled(false);

        psdImage.save(outputOffFile);
    }

{{< /highlight >}}

**PSDJAVA-754. Update the structure of Gradient classes. Create base class for Gradeint specific.**

{{< highlight java >}}

    public static void main(String[] args) {
        String inputFile = "src/main/resources/StrokeNoise.psd";
        String outputFile = "src/main/resources/output.psd";

        PsdLoadOptions loadOptions = new PsdLoadOptions();
        loadOptions.setLoadEffectsResource(true);

        try (PsdImage image = (PsdImage) Image.load(inputFile, loadOptions)) {
            var gradientStroke = (StrokeEffect) image.getLayers()[0].getBlendingOptions().getEffects()[0];
            GradientFillSettings gradientFillSettings = (GradientFillSettings) gradientStroke.getFillSettings();

            // Check common gradient fill settings properties
            assertIsNotNull(gradientFillSettings);
            assertAreEqual(true, gradientFillSettings.getAlignWithLayer());
            assertAreEqual(true, gradientFillSettings.getDither());
            assertAreEqual(true, gradientFillSettings.getReverse());
            assertAreEqual(116.0, gradientFillSettings.getAngle());
            assertAreEqual(122, gradientFillSettings.getScale());
            assertAreEqual(GradientType.Angle, gradientFillSettings.getGradientType());

            // Check Noise gradient properties
            NoiseGradient noiseGradient = (NoiseGradient) gradientFillSettings.getGradient();
            assertIsNotNull(noiseGradient);
            assertAreEqual(GradientKind.Noise, noiseGradient.getGradientMode());
            assertAreEqual(2107422935, noiseGradient.getRndNumberSeed());
            assertAreEqual(false, noiseGradient.getShowTransparency());
            assertAreEqual(false, noiseGradient.getUseVectorColor());
            assertAreEqual(2048, noiseGradient.getRoughness());
            assertAreEqual(NoiseColorModel.RGB, noiseGradient.getColorModel());
            assertAreEqual((long) 0, noiseGradient.getMinimumColor().getAsLong());
            assertAreEqual(28147819798528050L, noiseGradient.getMaximumColor().getAsLong());

            // Change gradient settings
            gradientFillSettings.setAlignWithLayer(false);
            gradientFillSettings.setDither(false);
            gradientFillSettings.setReverse(false);
            ;
            gradientFillSettings.setAngle(30);
            gradientFillSettings.setScale(80);
            gradientFillSettings.setGradientType(GradientType.Linear);

            var solidGradient = new SolidGradient();
            solidGradient.setInterpolation((short) 2048);
            solidGradient.getColorPoints()[0].getRawColor().getComponents()[0].setValue(255); // A
            solidGradient.getColorPoints()[0].getRawColor().getComponents()[1].setValue(255); // R
            solidGradient.getColorPoints()[0].getRawColor().getComponents()[2].setValue(0);   // G
            solidGradient.getColorPoints()[0].getRawColor().getComponents()[3].setValue(0);   // B
            solidGradient.getTransparencyPoints()[1].setOpacity(50);
            gradientFillSettings.setGradient(solidGradient);

            image.save(outputFile);
        }

        // Check saved changes
        try (PsdImage image = (PsdImage) Image.load(outputFile)) {
            var gradientStroke = (StrokeEffect) image.getLayers()[0].getBlendingOptions().getEffects()[0];
            GradientFillSettings gradientFillSettings = (GradientFillSettings) gradientStroke.getFillSettings();

            // Check common gradient fill settings properties
            assertIsNotNull(gradientFillSettings);
            assertAreEqual(false, gradientFillSettings.getAlignWithLayer());
            assertAreEqual(false, gradientFillSettings.getDither());
            assertAreEqual(false, gradientFillSettings.getReverse());
            assertAreEqual(30.0, gradientFillSettings.getAngle());
            assertAreEqual(80, gradientFillSettings.getScale());
            assertAreEqual(GradientType.Linear, gradientFillSettings.getGradientType());

            SolidGradient solidGradient = (SolidGradient) gradientFillSettings.getGradient();
            assertIsNotNull(solidGradient);
            assertAreEqual((short) 2048, solidGradient.getInterpolation());
            assertAreEqual(255L, solidGradient.getColorPoints()[0].getRawColor().getComponents()[0].getValue());
            assertAreEqual(255L, solidGradient.getColorPoints()[0].getRawColor().getComponents()[1].getValue());
            assertAreEqual(0L, solidGradient.getColorPoints()[0].getRawColor().getComponents()[2].getValue());
            assertAreEqual(0L, solidGradient.getColorPoints()[0].getRawColor().getComponents()[3].getValue());
            assertAreEqual(50.0, solidGradient.getTransparencyPoints()[1].getOpacity());
        }
    }

    private static void assertAreEqual(Object expected, Object actual) {
        assertAreEqual(expected, actual, "Objects are not equal.");
    }

    private static void assertAreEqual(Object expected, Object actual, String message) {
        if (!expected.equals(actual)) {
            throw new IllegalArgumentException(message);
        }
    }

    private static void assertIsNotNull(Object testObject) {
        if (testObject == null) {
            throw new RuntimeException("Test object are null.");
        }
    }

{{< /highlight >}}

**PSDJAVA-757. Make correct initializing of Layers with Linked Layers Registry.**

{{< highlight java >}}

    public static void main(String[] args) throws Exception {
        String[] files = {"add.jpg", "add.psd"};

        for (String file : files) {
            String sourceFile = "src/main/resources/input.psd";
            String addFile = Paths.get("src/main/resources/", file).toString();

            try (PsdImage psdImage = (PsdImage) Image.load(sourceFile)) {
                final Stream stream = new FileStream(addFile, FileMode.Open);
                try {
                    try (SmartObjectLayer smartLayer = new SmartObjectLayer(stream)) {
                        psdImage.addLayer(smartLayer);

                        var layer1 = psdImage.getLayers()[1];
                        var layer2 = psdImage.getLayers()[2];

                        var size1Before = layer1.getSize();
                        var size2Before = layer2.getSize();

                        psdImage.getLinkedLayersManager().linkLayers(new Layer[]{layer1, layer2});

                        layer1.resize(100, 100);

                        var size1After = layer1.getSize();
                        var size2After = layer2.getSize();

                        areNotEqual(size1Before, size1After, "The original layer size must be changed, because resize was applied");
                        areNotEqual(size2Before, size2After, "The linked layer's size must be changed, because it linked with 'original layer'.");
                    }
                } finally {
                    stream.dispose();
                }
            }
        }
    }

    private static <T> void areNotEqual(T expected, T actual, String message) throws Exception {
        if (expected != null && expected.equals(actual)) {
            throw new Exception(message);
        }
    }

{{< /highlight >}}

**PSDJAVA-758. Inaccurate rendering of Smart Object Layer.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/test.psd";
    String newContent = "src/main/resources/newImage.png";
    String export = "src/main/resources/export.png";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setAllowWarpRepaint(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        try (var replaceImage = Image.load(newContent)) {
            var layers = psdImage.getLayers();
            for (Layer layer : layers) {
                if (layer instanceof SmartObjectLayer smartObjectLayer) {
                    smartObjectLayer.replaceContents(replaceImage);
                    smartObjectLayer.updateModifiedContent();
                    break;
                }
            }

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
            psdImage.save(export, pngOptions);
        }
    }

{{< /highlight >}}

**PSDJAVA-759. Error when applying deformation due to invalid ‘Processing Area’ value is 2.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Warping.psd";
    String outputFile = "src/main/resources/export" + 2 + ".png";

    PsdLoadOptions loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);
    loadOptions.setAllowWarpRepaint(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        // It gets WarpSettings from Smart Layer
        WarpSettings warpSettings = ((SmartObjectLayer) psdImage.getLayers()[1]).getWarpSettings();

        // It sets size of warp processing area
        warpSettings.setProcessingArea(2);
        ((SmartObjectLayer) psdImage.getLayers()[1]).setWarpSettings(warpSettings);

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        // There should no error here
        psdImage.save(outputFile, pngOptions);
    }

{{< /highlight >}}