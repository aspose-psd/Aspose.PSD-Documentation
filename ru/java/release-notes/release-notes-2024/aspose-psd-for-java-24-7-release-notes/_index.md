---
title: Aspose.PSD для Java 24,7 - Примечания к выпуску
type: docs
weight: 40
url: /ru/java/aspose-psd-dlya-java-24-7-primechaniya-k-vypusku/
---

{{% alert color="primary" %}} Эта страница содержит примечания к выпуску для [Aspose.PSD для Java 24.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-24.7/) {{% /alert %}}

| **Ключ**     | **Описание**                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-635 | Исключение "Ошибка загрузки изображения." при открытии документа AI                                 | Ошибка        |
| PSDJAVA-636 | Неправильное отображение текста в выходных файлах PDF                                             | Ошибка        |
| PSDJAVA-637 | Исправлена ошибка ImageSaveException: сбой экспорта изображения для указанного файла на Linux      | Ошибка        |
| PSDJAVA-638 | Исправлена загрузка шрифтов при использовании Aspose.Drawing                                        | Ошибка        |
| PSDJAVA-639 | 'Арифметическая операция привела к переполнению' при создании умного объектного слоя с большим JPEG | Ошибка        |
| PSDJAVA-640 | Файл AI не может быть преобразован в файл JPG                                                    | Ошибка        |

## **Изменения в общедоступном API**
# **Добавленные API:**

- Нет

# **Удаленные API:**

- Нет 

## **Примеры использования:**

**PSDJAVA-635. Исключение "Ошибка загрузки изображения." при открытии документа AI**

{{< highlight java >}}

String sourceFile = "src/main/resources/[SA]_ID_card_template.ai";
String outputFile = "src/main/resources/[SA]_ID_card_template.png";

try (AiImage image = (AiImage) Image.load(sourceFile)) {
    image.save(outputFile, new PngOptions());
}

{{< /highlight >}}

**PSDJAVA-636. Неправильное отображение текста в выходных файлах PDF**

{{< highlight java >}}

String src = "src/main/resources/CVFlor.psd";
String output = "src/main/resources/output.pdf";

try (PsdImage psdImage = (PsdImage) Image.load(src)) {
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.setPdfCoreOptions(new PdfCoreOptions());

    psdImage.save(output, saveOptions);
}

{{< /highlight >}}

**PSDJAVA-637. Исправлена ошибка ImageSaveException: сбой экспорта изображения для указанного файла на Linux**

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

**PSDJAVA-638. Исправлена загрузка шрифтов при использовании Aspose.Drawing**

{{< highlight java >}}

final var installedFonts = new InstalledFontCollection();
try {
    System.out.println("- Перед обновлением. Количество установленных шрифтов: " + installedFonts.getFamilies().length);
    System.out.println("- Платформа: " + Environment.get_OSVersion().get_Platform());
    System.out.println("- Обновление кеша шрифтов путем попытки получения имени шрифта Adobe для 'Arial': "
        + FontSettings.getAdobeFontName("Arial"));

    System.out.println("- После обновления. Количество установленных шрифтов: " + installedFonts.getFamilies().length);

    assertAreEqual(installedFonts.getFamilies().length, 1);
} finally {
    installedFonts.dispose();
}

{{< /highlight >}}

**PSDJAVA-639. 'Арифметическая операция привела к переполнению' при создании умного объектного слоя с большим JPEG**

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

**PSDJAVA-640. Файл AI не может быть преобразован в файл JPG**

{{< highlight java >}}

String sourceFile = "src/main/resources/aaa.ai";
String outputFile = "src/main/resources/aaa.png";

try (AiImage image = (AiImage) Image.load(sourceFile)) {
    image.save(outputFile, new PngOptions());
}

{{< /highlight >}}
