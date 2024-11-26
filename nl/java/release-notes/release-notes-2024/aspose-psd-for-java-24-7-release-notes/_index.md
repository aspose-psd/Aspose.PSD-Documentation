---
title: Aspose.PSD voor Java 24.7 - Release-opmerkingen
type: docs
weight: 40
url: /nl/java/aspose-psd-voor-java-24-7-release-opmerkingen/
---

{{% alert color="primary" %}} Deze pagina bevat release-opmerkingen voor [Aspose.PSD voor Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-voor-java-24.7/) {{% /alert %}}

| **Sleutel**  | **Samenvatting**                                                                                 | **Categorie** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Uitzondering "Afbeelding laden mislukt." wanneer AI-document wordt geopend                        | Bug          |
| PSDJAVA-636 | Tekst incorrect weergegeven in uitvoer-PDF-bestanden                                              | Bug          |
| PSDJAVA-637 | Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het gegeven bestand op Linux     | Bug          |
| PSDJAVA-638 | Oplossing voor laden van lettertypen bij gebruik van Aspose.Drawing                               | Bug          |
| PSDJAVA-639 | 'Arithmetic operation resulted in an overflow' bij het maken van een slimme objectlaag met grote JPEG | Bug          |
| PSDJAVA-640 | Het AI-bestand kan niet worden geconverteerd naar een JPG-bestand                                  | Bug          |

## **Wijzigingen in de openbare API**
# **Toegevoegde API's:**

- Geen

# **Verwijderde API's:**

- Geen

## **Gebruik voorbeelden:**

**PSDJAVA-635. Uitzondering "Afbeelding laden mislukt." wanneer AI-document wordt geopend**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Tekst incorrect weergegeven in uitvoer-PDF-bestanden**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Oplossing voor ImageSaveException: Afbeeldingsexport mislukt voor het gegeven bestand op Linux**

{{< highlight java >}}

    String sourceFile = "src/main/resources/Bed_Roll-Sticker4_1.psd";
    String outputFile = "src/main/resources/output.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (var psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        JpegOptions saveOptions = new JpegOptions();
        saveOptions.setQuality(70);
        psdImage.save(outputFile, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-638. Oplossing voor laden van lettertypen bij gebruik van Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Voor update. Geïnstalleerde lettertypen tellen: " + installedFonts.getFamilies().length);
        System.out.println("- Platform: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Vernieuw de lettertypen cache door te proberen de Adobe-lettertypenaam voor 'Arial' te krijgen: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Na de update. Geïnstalleerde lettertypen tellen: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Arithmetic operation resulted in an overflow' bij het maken van een slimme objectlaag met grote JPEG**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Test Layer");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. Het AI-bestand kan niet worden geconverteerd naar een JPG-bestand**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
