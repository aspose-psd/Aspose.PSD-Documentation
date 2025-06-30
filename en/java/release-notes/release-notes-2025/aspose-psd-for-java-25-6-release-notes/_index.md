---
title: Aspose.PSD for Java 25.6 - Release Notes
type: docs
weight: 40
url: /java/aspose-psd-for-java-25-6-release-notes/
---

{{% alert color="primary" %}} This page contains release notes
for[Aspose.PSD for Java 25.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-25.6/) {{%
/alert %}}

| **Key**     | **Summary**                                                                                                                                                                 | **Category** |
|:------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-742 | Add API to Apply Layer Mask to Layer.                                                                                                                                       | Feature      |

## **Public API Changes**

# **Added APIs:**

- M:com.aspose.psd.fileformats.psd.layers.Layer.applyLayerMask

# **Removed APIs:**

- None

## **Usage examples:**

**PSDJAVA-742. Add API to Apply Layer Mask to Layer.**

{{< highlight java >}}

    var sourceFile = "src/main/resources/example.psd";
    var outFile = "src/main/resources/export.png";

    try (var psdImage = (PsdImage) Image.load(sourceFile, new PsdLoadOptions())) {
        psdImage.getLayers()[1].applyLayerMask();

        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);
        psdImage.save(outFile, pngOptions);
    }

{{< /highlight >}}