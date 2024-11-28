---
title: Notatki wydania Aspose.PSD dla Java 24.7
type: docs
weight: 40
url: /pl/java/aspose-psd-dla-java-24-7-notatki-wydania/
---

{{% alert color="primary" %}} Ta strona zawiera notatki wydania dla [Aspose.PSD dla Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Klucz**    | **Podsumowanie**                                                                                | **Kategoria** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Wyjątek "Błąd ładowania obrazu." występuje podczas otwierania dokumentu AI                       | Błąd         |
| PSDJAVA-636 | Tekst jest niepoprawnie renderowany w plikach PDF wyjściowych                                    | Błąd         |
| PSDJAVA-637 | Naprawiono ImageSaveException: Błąd eksportu obrazu dla określonego pliku na systemie Linux      | Błąd         |
| PSDJAVA-638 | Naprawiono ładowanie czcionek przy użyciu Aspose.Drawing                                         | Błąd         |
| PSDJAVA-639 | 'Operacja arytmetyczna spowodowała przepełnienie' przy tworzeniu warstwy obiektu inteligentnego z dużym plikiem JPEG | Błąd |
| PSDJAVA-640 | Plik AI nie może zostać skonwertowany na plik JPG                                                | Błąd         |

## **Zmiany w API publicznym**
# **Dodane API:**

- Brak

# **Usunięte API:**

- Brak

## **Przykłady użycia:**

**PSDJAVA-635. Wyjątek "Błąd ładowania obrazu." występuje podczas otwierania dokumentu AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Tekst jest niepoprawnie renderowany w plikach PDF wyjściowych**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Naprawiono ImageSaveException: Błąd eksportu obrazu dla określonego pliku na systemie Linux**

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

**PSDJAVA-638. Naprawiono ładowanie czcionek przy użyciu Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Przed aktualizacją. Liczba zainstalowanych czcionek: " + installedFonts.getFamilies().length);
        System.out.println("- Platforma: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Odśwież pamięć podręczną czcionek, próbując uzyskać nazwę czcionki Adobe dla 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Po aktualizacji. Liczba zainstalowanych czcionek: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Operacja arytmetyczna spowodowała przepełnienie' przy tworzeniu warstwy obiektu inteligentnego z dużym plikiem JPEG**

{{< highlight java >}}

    String srcFile = "src/main/resources/source.psd";
    String imageJpg = "src/main/resources/test.jpg";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setDataRecoveryMode(DataRecoveryMode.MaximalRecover);
    
    try (var image = (PsdImage) Image.load(srcFile, psdLoadOptions)) {
        final FileStream stream = new FileStream(imageJpg, FileMode.Open);
        try {
            var addedLayer = new SmartObjectLayer(stream);
            addedLayer.setName("Nazwa warstwy testowej");
            image.addLayer(addedLayer);
        } finally {
            stream.dispose();
        }
    }

{{< /highlight >}}

**PSDJAVA-640. Plik AI nie może zostać skonwertowany na plik JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
