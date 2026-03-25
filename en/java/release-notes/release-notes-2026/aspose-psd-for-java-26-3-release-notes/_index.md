---
title: Aspose.PSD for Java 26.3 - Release Notes
type: docs
weight: 40
url: /java/aspose-psd-for-java-26-3-release-notes/
---

{{% alert color="primary" %}} This page contains release notes
for[Aspose.PSD for Java 26.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-26.3/) {{%
/alert %}}

| **Key**     | **Summary**                                                                        | **Category** |
|:------------|:-----------------------------------------------------------------------------------|:-------------|
| PSDJAVA-839 | Update processing of parameter Technique-Softer of Outer glow effect on rendering. | Feature      |
| PSDJAVA-840 | Warp transformation grid is incorrect for specific cases.                          | Bug          |
| PSDJAVA-841 | Rendering of outer glow differs from the original PS rendering noticeable.         | Bug          |
| PSDJAVA-842 | The warp arc algorithm must be changed.                                            | Bug          |

## **Public API Changes**

# **Added APIs:**

- None

# **Removed APIs:**

- None

## **Usage examples:**

**PSDJAVA-839. Update processing of parameter Technique-Softer of Outer glow effect on rendering.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/OuterGlow_Softer.psd";
    String outputFile = "src/main/resources/output_OuterGlow_Softer.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var img = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(outputFile, pngOptions);
    }

{{< /highlight >}}

**PSDJAVA-840. Warp transformation grid is incorrect for specific cases.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/input.psd";
    String outputFile = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }

{{< /highlight >}}

**PSDJAVA-841. Rendering of outer glow differs from the original PS rendering noticeable.**

{{< highlight java >}}

    String sourceFile = "src/main/resources/OuterGlow.psd";
    String outputFile = "src/main/resources/output_OuterGlow.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var img = (PsdImage) PsdImage.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(outputFile, pngOptions);
    }

{{< /highlight >}}

**PSDJAVA-842. The warp arc algorithm must be changed.**

{{< highlight java >}}

    String arcSourceFile = "src/main/resources/arc_warp.psd";
    String arcOutputFile = "src/main/resources/arc_export.png";

    PsdLoadOptions arcLoadOptions = new PsdLoadOptions();
    arcLoadOptions.setAllowWarpRepaint(true);
    arcLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(arcSourceFile, arcLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(arcOutputFile, pngOptions);
    }

    String arcvSourceFile = "src/main/resources/arc_v_warp.psd";
    String arcvOutputFile = "src/main/resources/arc_v_export.png";

    PsdLoadOptions arcvLoadOptions = new PsdLoadOptions();
    arcvLoadOptions.setAllowWarpRepaint(true);
    arcvLoadOptions.setLoadEffectsResource(true);

    try (PsdImage psdImage = (PsdImage) Image.load(arcvSourceFile, arcvLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(arcvOutputFile, pngOptions);
    }

{{< /highlight >}}
