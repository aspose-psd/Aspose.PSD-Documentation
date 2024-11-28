---
title: Aspose.PSD für Java 24.7 - Versionshinweise
type: docs
weight: 40
url: /de/java/aspose-psd-fur-java-24-7-versionshinweise/
---

{{% alert color="primary" %}} Diese Seite enthält Versionshinweise für [Aspose.PSD für Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Schlüssel** | **Zusammenfassung**                                                                                   | **Kategorie** |
|:-------------|:-----------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635  | Ausnahme "Bild konnte nicht geladen werden", wenn AI-Dokument geöffnet wird                          | Fehler       |
| PSDJAVA-636  | Text wird in Ausgabepdf-dateien falsch gerendert                                                      | Fehler       |
| PSDJAVA-637  | Beheben von ImageSaveException: Bilderexport fehlgeschlagen für die angegebene Datei unter Linux       | Fehler       |
| PSDJAVA-638  | Beheben von Schriftartenladen bei Verwendung von Aspose.Drawing                                       | Fehler       |
| PSDJAVA-639  | 'Arithmetische Operation führte zu einem Überlauf' beim Erstellen einer Smart-Objekt-Schicht mit großem JPEG | Fehler       |
| PSDJAVA-640  | Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden                                           | Fehler       |

## **Öffentliche API-Änderungen**
# **Hinzugefügte APIs:**

- Keine

# **Entfernte APIs:**

- Keine 

## **Verwendungsbeispiele:**

**PSDJAVA-635. Ausnahme "Bild konnte nicht geladen werden", wenn AI-Dokument geöffnet wird**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Text wird in Ausgabepdf-dateien falsch gerendert**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Beheben von ImageSaveException: Bilderexport fehlgeschlagen für die angegebene Datei unter Linux**

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

**PSDJAVA-638. Beheben von Schriftartenladen bei Verwendung von Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Vor dem Update. Installierte Schriftartenanzahl: " + installedFonts.getFamilies().length);
        System.out.println("- Plattform: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Aktualisieren des Schriftcaches durch Versuch, den Adobe-Schriftname für 'Arial' zu erhalten: "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Nach dem Update. Installierte Schriftartenanzahl: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Arithmetische Operation führte zu einem Überlauf' beim Erstellen einer Smart-Objekt-Schicht mit großem JPEG**

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

**PSDJAVA-640. Die AI-Datei kann nicht in eine JPG-Datei konvertiert werden**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
