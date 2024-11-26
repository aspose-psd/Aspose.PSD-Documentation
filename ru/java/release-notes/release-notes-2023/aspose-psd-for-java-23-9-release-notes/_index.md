---
title: Aspose.PSD для Java 23.9 - Примечания к версии
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-23-9-release-notes/
---

{{% alert color="primary" %}} Эта страница содержит примечания к версии [Aspose.PSD для Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Ключ**    | **Сводка**                                                                                                                                        | **Категория** |
|:------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Реализация создания маски для новых слоев коррекции                                                                                                  |    Функция    |
| PSDJAVA-528 | Добавлена поддержка смешивания обрезанных слоев как вариант смешивания группы                                                                       |    Функция    |
| PSDJAVA-529 | Файл PSD с 16-битным цветовым режимом не применяет маску для слоев коррекции                                                                        |      Ошибка   |
| PSDJAVA-530 | Некорректный рендеринг скобок в текстовом слое                                                                                                      |      Ошибка   |
| PSDJAVA-531 | Невозможно обновить стили в текстовых слоях                                                                                                          |      Ошибка   |
| PSDJAVA-532 | После экспорта файла PSD с ЦМИК ломаются цвета в экспортированном PSD                                                                                |      Ошибка   |
| PSDJAVA-533 | Определенный файл PSB вызывает исключение "Прямоугольник не имеет общей области обработки"                                                          |      Ошибка   |
| PSDJAVA-534 | Ошибка загрузки изображения. OverflowException: Арифметическая операция вызвала переполнение.                                                      |      Ошибка   |

## **Изменения в общедоступном API**
# **Добавленные API:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Удаленные API:**

- Нет

## **Примеры использования:**

** PSDJAVA-527. Реализация создания маски для новых слоев коррекции**

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
    assertAreEqual(expected, actual, "Объекты не равны.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. Добавление поддержки вложенных слоев как вариант смешивания группы **

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

(и т.д.)

