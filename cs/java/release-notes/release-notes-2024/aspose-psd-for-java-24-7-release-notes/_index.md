---
title: Aspose.PSD pro Java 24.7 - Poznámky k vydání
type: docs
weight: 40
url: /cs/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} Tato stránka obsahuje poznámky k vydání pro [Aspose.PSD pro Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Klíč**     | **Souhrn**                                                                                        | **Kategorie** |
|:------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Výjimka "Chyba při načítání obrázku." při otevírání dokumentu AI                                   | Chyba        |
| PSDJAVA-636 | Text je špatně vykreslen v výstupních souborech PDF                                                 | Chyba        |
| PSDJAVA-637 | Oprava výjimky ImageSaveException: Selhání exportu obrázku pro daný soubor na Linuxu               | Chyba        |
| PSDJAVA-638 | Oprava načítání písem při použití Aspose.Drawing                                                   | Chyba        |
| PSDJAVA-639 | 'Aritmetická operace způsobila přetečení' při vytváření vrstvy inteligentního objektu pomocí velkého JPEG | Chyba        |
| PSDJAVA-640 | Soubor AI nelze převést na soubor JPG                                                             | Chyba        |

## **Změny ve veřejném API**
# **Přidaná API:**

- žádné

# **Odebraná API:**

- žádné

## **Příklady použití:**

**PSDJAVA-635. Výjimka "Chyba při načítání obrázku." při otevírání dokumentu AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Text je špatně vykreslen v výstupních souborech PDF**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Oprava výjimky ImageSaveException: Selhání exportu obrázku pro daný soubor na Linuxu**

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

**PSDJAVA-638. Oprava načítání písem při použití Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Před aktualizací. Počet nainstalovaných písem: " + installedFonts.getFamilies().length);
        System.out.println("- Platforma: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Obnovení mezipaměti písem pokusem získat název písma Adobe pro 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Po aktualizaci. Počet nainstalovaných písem: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Aritmetická operace způsobila přetečení' při vytváření vrstvy inteligentního objektu pomocí velkého JPEG**

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

**PSDJAVA-640. Soubor AI nelze převést na soubor JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
