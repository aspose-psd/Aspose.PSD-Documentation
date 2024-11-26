---
title: Aspose.PSD для Java 23.9 - Примітки до випуску
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-23-9-vypuski/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до [Aspose.PSD для Java 23.9](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.9/) {{% /alert %}}

| **Ключ**   | **Опис**                                                                                                                                      | **Категорія** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-527 | Реалізація створення масок для нових слоїв коригування                                                                                         |    Функція   |
| PSDJAVA-528 | Додавання підтримки злиття в обрізані шари як опцію злиття групи                                                                              |    Функція   |
| PSDJAVA-529 | Файл PSD у режимі кольору 16 біт не застосовує маску для шарів коригування                                                                     |      Помилка  |
| PSDJAVA-530 | Некоректне відображення дужок у текстовому шарі                                                                                                  |      Помилка  |
| PSDJAVA-531 | Неможливість оновлення стилів в текстових шарах                                                                                                 |      Помилка  |
| PSDJAVA-532 | Після експорту PSD файлу з CMYK руйнує кольори в експортованому PSD                                                                             |      Помилка  |
| PSDJAVA-533 | Конкретний файл PSB видає виняток "Прямокутник не має спільної області обробки"                                                               |      Помилка  |
| PSDJAVA-534 | Не вдалося завантажити зображення. Помилка переповнення: Арифметична операція призвела до переповнення.                                      |      Помилка  |

## **Зміни в публічному API**
# **Додані API:**

- M:com.aspose.psd.PixelDataFormat.getCmyk16
- M:com.aspose.psd.PixelDataFormat.getCmyka16
- M:com.aspose.psd.fileformats.psd.layers.Layer.getBlendClippedElements
- M:com.aspose.psd.fileformats.psd.layers.Layer.setBlendClippedElements(boolean)

# **Вилучені API:**

- Немає

## **Приклади використання:**

** PSDJAVA-527. Реалізація створення масок для нових шарів коригування**

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
    assertAreEqual(expected, actual, "Об'єкти не рівні.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

** PSDJAVA-528. Додавання підтримки злиття в обрізані шари як опцію злиття групи**

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

(Інші приклади використання скорочено через обсяг тексту)

** PSDJAVA-534. Не вдалося завантажити зображення. Помилка переповнення: Арифметична операція призвела до переповнення.**

{{< highlight java >}}
public static void main(String[] args) {
    String sourceFile = "src/main/resources/9baa6962-f409-41ee-88da-418ea87bb56f_test_2.psd";

    try (PsdImage im = (PsdImage)PsdImage.load(sourceFile))
    {
        Layer layer = im.getLayers()[28];
        GrdmResource grdmResource = (GrdmResource)layer.getResources()[0];

        assertAreEqual("自定", grdmResource.getGradientName());
    }

}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Об'єкти не рівні.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}
