---
title: Aspose.PSD для Java 24.7 - Примітки до релізу
type: docs
weight: 40
url: /uk/java/aspose-psd-for-java-24-7-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до релізу для [Aspose.PSD для Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Ключ**     | **Опис**                                                                                      | **Категорія** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Виклик винятку "Завантаження зображення не вдалося" при відкритті документа AI                 | Помилка      |
| PSDJAVA-636 | Текст неправильно відображається у вихідних файлах PDF                                          | Помилка      |
| PSDJAVA-637 | Виправити ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux          | Помилка      |
| PSDJAVA-638 | Виправити завантаження шрифтів при використанні Aspose.Drawing                                   | Помилка      |
| PSDJAVA-639 | "Арифметична операція призвела до переповнення" при створенні шару розумного об'єкту з великим JPEG | Помилка      |
| PSDJAVA-640 | Файл AI не може бути перетворений у файл JPG                                                  | Помилка      |

## **Зміни в публічному API**
# **Додані API:**

- Жодно

# **Вилучені API:**

- Жодно 

## **Приклади використання:**

**PSDJAVA-635. Виклик винятку "Завантаження зображення не вдалося" при відкритті документа AI**

{{< highlight java >}}

    String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
    String outputFile = "src/main/resources/[SA]_ID_card_template.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}

**PSDJAVA-636. Текст неправильно відображається у вихідних файлах PDF**

{{< highlight java >}}

    String src = "src/main/resources/CVFlor.psd";
    String output = "src/main/resources/output.pdf";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PdfOptions saveOptions = new PdfOptions();
        saveOptions.setPdfCoreOptions(new PdfCoreOptions());

        psdImage.save(output, saveOptions);
    }

{{< /highlight >}}

**PSDJAVA-637. Виправити ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux**

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

**PSDJAVA-638. Виправити завантаження шрифтів при використанні Aspose.Drawing**

{{< highlight java >}}

    final var installedFonts = new InstalledFontCollection();
    try {
        System.out.println("- Перед оновленням. Кількість встановлених шрифтів: " + installedFonts.getFamilies().length);
        System.out.println("- Платформа: " + Environment.get_OSVersion().get_Platform());
        System.out.println("- Оновіть кеш шрифтів, спробувавши отримати назву шрифта Adobe для 'Arial': "
            + FontSettings.getAdobeFontName("Arial"));

        System.out.println("- Після оновлення. Кількість встановлених шрифтів: " + installedFonts.getFamilies().length);

        assertAreEqual(installedFonts.getFamilies().length, 1);
    } finally {
        installedFonts.dispose();
    }

{{< /highlight >}}

**PSDJAVA-639. 'Арифметична операція призвела до переповнення' при створенні шару розумного об'єкту з великим JPEG**

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

**PSDJAVA-640. Файл AI не може бути перетворений у файл JPG**

{{< highlight java >}}

    String sourceFile = "src/main/resources/aaa.ai";
    String outputFile = "src/main/resources/aaa.png";

    try (AiImage image = (AiImage) Image.load(sourceFile)) {
        image.save(outputFile, new PngOptions());
    }

{{< /highlight >}}
