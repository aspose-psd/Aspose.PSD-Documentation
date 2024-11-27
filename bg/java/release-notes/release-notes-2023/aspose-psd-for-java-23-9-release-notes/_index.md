---
title: Aspose.PSD за Java 23.9 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-9-belezki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието за [Aspose.PSD за Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-za-java-23.9/) {{% /alert %}}

| **Ключ**     | **Резюме**                                                                                                                                      | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Реализиране на създаване на маска за новите слоеве за корекции                                                                                             |    Функционалност   |
| PSDJAVA-528 | Добавяне на поддръжка на смесени слоеве като опция за групово смесване                                                                                     |    Функционалност     |
| PSDJAVA-529 | Файлът PSD с 16-битов цветов режим не прилага маска за слоевете за корекции                                                                  |      Грешка     |
| PSDJAVA-530 | Неправилно изобразяване на скоби в текстовия слой                                                                                                |      Грешка     |
| PSDJAVA-531 | Не може да се актуализират стиловете в текстовите слоеве                                                                                                         |      Грешка     |
| PSDJAVA-532 | След изнасянето на файл PSD с CMYK цветове се нарушават цветовете в изведения PSD файл                                                                             |      Грешка     |
| PSDJAVA-533 | Конкретният PSB файл генерира грешка "Правоъгълника няма общо обработване"                                                                 |      Грешка     |
| PSDJAVA-534 | Грешка при зареждане на изображението. OverflowException: Аритметичната операция доведе до препълване.                                                           |      Грешка     |

## **Промени в публичния API**
# **Добавени API-и:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Премахнати API-и:**

- Няма

## **Примери за използване:**

**PSDJAVA-527. Реализиране на създаване на маска за новите слоеве за корекции**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya_BW.psd";
    String dstFile = "src/main/resources/zendeya_BW_out.psd";

    try (PsdImage im = (PsdImage) Image.load(srcFile)) {
        im.addBlackWhiteAdjustmentLayer();

        im.save(dstFile);
    }

    try (PsdImage im = (PsdImage) Image.load(dstFile)) {
        Layer layer = im.getLayers()[1];

        assertAreEqual(5, layer.getChannelsCount());
        assertAreEqual((short) -2, layer.getChannelInformation()[4].getChannelID());
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Обектите не са равни.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-528. Добавяне на поддръжка на смесени слоеве като опция за групово смесване**

{{< highlight java >}}
    String sourceFile = "src/main/resources/example_source.psd";
    String outputPsd = "src/main/resources/example_output.psd";
    String outputPng = "src/main/resources/example_output.png";

    try (PsdImage image = (PsdImage)Image.load(sourceFile)) {
        image.getLayers()[1].setBlendClippedElements(false);
        image.save(outputPsd);
        image.save(outputPng, new PngOptions());
    }
{{< /highlight >}}

(Повече текст следва...)