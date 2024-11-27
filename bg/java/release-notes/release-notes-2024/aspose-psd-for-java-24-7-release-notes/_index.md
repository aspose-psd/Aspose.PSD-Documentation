---
title: Aspose.PSD за Java 24.7 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-24-7-belezhki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}} 

| **Ключ**     | **Резюме**                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Изключение "Грешка при зареждане на изображението." при отваряне на AI документ               | Грешка       |
| PSDJAVA-636 | Текстът се визуализира неправилно в изходните PDF файлове                                      | Грешка       |
| PSDJAVA-637 | Оправяне на грешката ImageSaveException: Грешка при експортиране на изображението за дадения файл на Linux | Грешка       |
| PSDJAVA-638 | Оправяне на зареждането на шрифтове при използване на Aspose.Drawing                            | Грешка       |
| PSDJAVA-639 | 'Аритметичната операция доведе до препълване' при създаване на смарт обектен слой с голям JPEG | Грешка       |
| PSDJAVA-640 | Файлът AI не може да бъде конвертиран в JPG файл                                               | Грешка       |

## **Промени в обществения API**
# **Добавени API-та:**

- Няма

# **Премахнати API-та:**

- Няма 

## **Примери за използване:**

**PSDJAVA-635. Изключение "Грешка при зареждане на изображението." при отваряне на AI документ**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Текстът се визуализира неправилно в изходните PDF файлове**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Оправяне на грешката ImageSaveException: Грешка при експортиране на изображението за дадения файл на Linux**

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

**PSDJAVA-638. Оправяне на зареждането на шрифтове при използване на Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Преди актуализацията. Брой на инсталираните шрифтове: " + installedFonts.getFamilies().length);
        System.out.println("- Платформа: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Обновете кеша на шрифтовете, като опитате да получите Adobe името на шрифта 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- След актуализацията. Брой на инсталираните шрифтове: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Аритметичната операция доведе до препълване' при създаване на смарт обектен слой с голям JPEG**

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

**PSDJAVA-640. Файлът AI не може да бъде конвертиран в JPG файл**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}