---
title: Aspose.PSD voor Java 24.3 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-24-3-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 24.3](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.3/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                           | **Categorie** |
|:------------|:---------------------------------------------------------------------------|:-------------|
| PSDJAVA-601 | [AI-indeling] Verkort laadtijd van grote multipage AI-afbeeldingen.        | Verbetering  |
| PSDJAVA-604 | PSD-bestand nadat het converteren van 8-bits naar 16-bits onleesbaar werd. | Bug          |
| PSDJAVA-605 | PSD-bestand nadat het converteren van 8-bits naar 32-bits onleesbaar werd. | Bug          |
| PSDJAVA-606 | [AI-indeling] Repareer de weergave van Short Curve in AI-bestand.          | Bug          |

## **Wijzigingen in openbare API**
# **Toegevoegde API's:**

- T:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.getFilters
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isEnabled
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskEnabled
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskExtendWithWhite
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isMaskLinked
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.isValidAtPosition
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.setFilters(com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter[])
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.SmartFilters.updateResourceValues
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.#ctor
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.apply(com.aspose.psd.RasterImage)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.applyToMask(com.aspose.psd.fileformats.psd.layers.Layer)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.deepClone
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getBlendMode
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getFilterId
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getName
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getOpacity
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.getSourceDescriptor
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setBlendMode(long)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setEnabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.setOpacity(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.SmartFilter.isEnabled
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.#ctor
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.FilterType
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getAmountNoise
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getDistribution
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getFilterId
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.getName
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setAmountNoise(double)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setDistribution(int)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.setMonochromatic(boolean)
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.AddNoiseSmartFilter.isMonochromatic
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer.render(com.aspose.psd.PixelsData)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.#ctor
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.FilterType
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getFilterId
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getName
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.getRadius
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.GaussianBlurSmartFilter.setRadius(double)
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.rendering.ISmartFilterRenderer
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Gaussian
- F:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.NoiseDistribution.Uniform
- T:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getFilterId
- M:com.aspose.psd.fileformats.psd.layers.smartfilters.filters.UnknownSmartFilter.getName

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-604. PSD-bestand nadat het converteren van 8-bits naar 16-bits onleesbaar werd**

{{< highlight java >}}

        String sourceFile = "src/main/resources/test_smart_layer.psd";
        String outputFile = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(sourceFile)) {
            PsdOptions psdOptions16 = new PsdOptions();
            psdOptions16.setChannelBitsCount((short) 16);

            psdImage8.save(outputFile, psdOptions16);
        }

        try (PsdImage psdImage16 = (PsdImage) Image.load(outputFile)) {
            if (psdImage16.getGlobalLayerResources()[0] instanceof Lr16Resource) {
                // is ok
            } else {
                throw new Exception("Verkeerde globale bron, de eerste bron zou Lr16Resource moeten zijn");
            }
        }

{{< /highlight >}}

**PSDJAVA-605. PSD-bestand nadat het converteren van 8-bits naar 32-bits onleesbaar werd**

{{< highlight java >}}

        String sourceFile = "src/main/resources/test_smart_layer.psd";
        String outputFile = "src/main/resources/export.psd";

        try (PsdImage psdImage8 = (PsdImage) Image.load(sourceFile)) {
            PsdOptions psdOptions32 = new PsdOptions();
            psdOptions32.setChannelBitsCount((short) 32);

            psdImage8.save(outputFile, psdOptions32);
        }

        try (PsdImage psdImage8 = (PsdImage) Image.load(outputFile)) {
            if (psdImage8.getGlobalLayerResources()[0] instanceof Lr32Resource) {
                // is ok
            } else {
                throw new Exception("Verkeerde globale bron, de eerste bron zou Lr16Resource moeten zijn");
            }
        }

{{< /highlight >}}

**PSDJAVA-606. [AI-indeling] Repareer de weergave van Short Curve in AI-bestand**

{{< highlight java >}}

        String sourceFile = "src/main/resources/shortCurve.ai";
        String outputFilePath = "src/main/resources/shortCurve.png";

        try (AiImage image = (AiImage) Image.load(sourceFile)) {
            image.save(outputFilePath, new PngOptions());
        }

{{< /highlight >}}
