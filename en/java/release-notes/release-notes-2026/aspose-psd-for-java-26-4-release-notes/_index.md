---
title: Aspose.PSD for Java 26.4 - Release Notes
type: docs
weight: 40
url: /java/aspose-psd-for-java-26-4-release-notes/
---

{{% alert color="primary" %}} This page contains release notes
for[Aspose.PSD for Java 26.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-26.4/) {{%
/alert %}}

| **Key**     | **Summary**                                                                                                             | **Category** |
|:------------|:------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-844 | Implement rendering of Gradient with Smooth method.                                                                     | Feature      |
| PSDJAVA-845 | Add support for a resource containing effects in a group layer.                                                         | Bug          |
| PSDJAVA-846 | PSD files with adjusted Hue/Saturation will throw the exception PsdImageArgumentException - Invalid Hue2 Resource data. | Bug          |

## **Public API Changes**

# **Added APIs:**

- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.getInterpolationMethod
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientFillSettings.setInterpolationMethod(long)
- T:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod 
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod.Classic 
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod.Perceptual 
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod.Linear 
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod.Smooth 
- F:com.aspose.psd.fileformats.psd.layers.fillsettings.InterpolationMethod.Stripes
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.getInterpolationMethod
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.IGradientFillSettings.setInterpolationMethod(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.getInterpolationMethod
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GdFlResource.setInterpolationMethod(long)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.IfxsResource 
- M:com.aspose.psd.fileformats.psd.layers.layerresources.IfxsResource.#ctor 
- F:com.aspose.psd.fileformats.psd.layers.layerresources.IfxsResource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.getInterpolationMethod
- M:com.aspose.psd.fileformats.psd.layers.layerresources.GrdmResource.setInterpolationMethod(long)
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientMapSettings.getInterpolationMethod
- M:com.aspose.psd.fileformats.psd.layers.fillsettings.GradientMapSettings.setInterpolationMethod(long)

# **Removed APIs:**

- None

## **Usage examples:**

**PSDJAVA-844. Implement rendering of Gradient with Smooth method.**

{{< highlight java >}}

    public static void main(String[] args) {
        String sourceFile = "src/main/resources/GradientOverlay.psd";
        String outputFile = "src/main/resources/output_GradientOverlay.psd";
        String outputFilePng = "src/main/resources/output_GradientOverlay.png";

        var srcMethod = InterpolationMethod.Linear;
        var newMethod = InterpolationMethod.Smooth;

        var opt = new PsdLoadOptions();
        opt.setLoadEffectsResource(true);

        try (var image = (PsdImage) Image.load(sourceFile, opt)) {
            // Read
            var effect = (GradientOverlayEffect) image.getLayers()[1].getBlendingOptions().getEffects()[0];
            var gradientSettings = effect.getSettings();
            assertAreEqual(srcMethod, gradientSettings.getInterpolationMethod());

            // Change
            gradientSettings.setInterpolationMethod(newMethod);

            PngOptions pngOptions = new PngOptions();
            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image.save(outputFile);
            image.save(outputFilePng, pngOptions);
        }

        // Check saved data
        try (var image = (PsdImage) Image.load(outputFile, opt)) {
            var effect = (GradientOverlayEffect) image.getLayers()[1].getBlendingOptions().getEffects()[0];
            var gradientSettings = effect.getSettings();

            assertAreEqual(newMethod, gradientSettings.getInterpolationMethod());
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

{{< /highlight >}}

**PSDJAVA-845. Add support for a resource containing effects in a group layer.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/example.psd";
    String outputFile = "src/main/resources/export.psd";

    var loadOptions = new PsdLoadOptions();
    loadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, loadOptions)) {
        // Example has 2 group layers with effects
        // Group layer with one effect
        LayerGroup layerGroupOne = (LayerGroup) psdImage.getLayers()[2];

        // Group layer with many effects
        LayerGroup layerGroupMany = (LayerGroup) psdImage.getLayers()[5];

        // Get the number of effects and verify their quantity
        int effectCountOne = layerGroupOne.getBlendingOptions().getEffects().length;
        int effectCountMany = layerGroupMany.getBlendingOptions().getEffects().length;

        // One effect in the group layer is in resource 'IfxsResource'
         IfxsResource ifxsResource = (IfxsResource) layerGroupOne.getResources()[0];

        // Two or more effects in a group layer are in resource 'ImfxResource'
        ImfxResource imfxResource = (ImfxResource) layerGroupMany.getResources()[0];

        // Add a third shadow to a group layer with multiple effects
        layerGroupMany.getBlendingOptions().addDropShadow();

        psdImage.save(outputFile);
    }

{{< /highlight >}}

**PSDJAVA-846. PSD files with adjusted Hue/Saturation will throw the exception PsdImageArgumentException - Invalid Hue2 Resource data.**

{{< highlight java >}}

    var hue2 = new Hue2Resource(new byte[136]);

{{< /highlight >}}
