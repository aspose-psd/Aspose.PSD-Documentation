---
title: Опис версії Aspose.PSD для Java 23.8
type: docs
weight: 40
url: /uk/java/aspose-psd-dlya-java-23-8-oholoshennya-pro-vyhid/
---

{{% alert color="primary" %}} Ця сторінка містить оголошення про випуск [Aspose.PSD для Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Ключ**    | **Короткий опис**                                                                                                                               | **Категорія** |
|:------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Додано новий тип зігнуття (Flag)                                                                                                                 | Особливість  |
| PSDJAVA-519 | Додано нові типи зігнуття: дуга вгору, дуга вниз, куля                                                                                           | Особливість  |
| PSDJAVA-520 | Реалізовано новий метод PsdImage.AddPosterizeAdjustmentLayer для додавання нового шару з постеризацією                                        | Особливість  |
| PSDJAVA-521 | Інформація в PSD втрачається лише при відкритті та збереженні                                                                                    | Помилка      |
| PSDJAVA-522 | Помилка завантаження картинки                                                                                                                   | Помилка      |
| PSDJAVA-523 | Помилка завантаження картинки: Неможливо привести об'єкт типу UnknownStructure до типу DescriptorStructure                                       | Помилка      |
| PSDJAVA-524 | Файл, змінений у бібліотеці третьої сторони, пошкоджує файл PSD, але його можна відкрити в Photoshop                                         | Помилка      |

## **Зміни у публічному API**
# **Додані API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Вилучені API:**

- Жодний

## **Приклади використання:**

**PSDJAVA-518. Додано новий тип зігнуття (Flag)**

{{< highlight java >}}
    String sourceFile = "src/main/resources/flag_warp.psd";
    String outputFile = "src/main/resources/flag_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);
    try (PsdImage psdImage = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputFile, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-519. Додано нові типи зігнуття: дуга вгору, дуга вниз, куля**

{{< highlight java >}}
    String sourceFileArcUpper = "src/main/resources/arc_upper_warp.psd";
    String sourceFileArcLower = "src/main/resources/arc_lower_warp.psd";
    String sourceFileBulge = "src/main/resources/bulge_warp.psd";

    String outputFileArcUpper = "src/main/resources/ArcUpper_export.png";
    String outputFileArcLower = "src/main/resources/ArcLower_export.png";
    String outputFileBulge = "src/main/resources/Bulge_export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setAllowWarpRepaint(true);
    psdLoadOptions.setLoadEffectsResource(true);

    PngOptions pngOptions = new PngOptions();
    pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcUpper, psdLoadOptions)) {
        psdImage.save(outputFileArcUpper, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileArcLower, psdLoadOptions)) {
        psdImage.save(outputFileArcLower, pngOptions);
    }

    try (PsdImage psdImage = (PsdImage) Image.load(sourceFileBulge, psdLoadOptions)) {
        psdImage.save(outputFileBulge, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-520. Реалізовано новий метод PsdImage.AddPosterizeAdjustmentLayer для додавання нового шару з постеризацією**

{{< highlight java >}}
public static void main(String[] args) {
    String srcFile = "src/main/resources/zendeya.psd";
    String outFile = "src/main/resources/zendeya.psd.out.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile)) {
        psdImage.addPosterizeAdjustmentLayer();
        psdImage.save(outFile);
    }

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    // Перевірити збережені зміни
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
    }
}

static void assertAreEqual(Object expected, Object actual) {
    assertAreEqual(expected, actual, "Об'єкти не є рівними.");
}

static void assertAreEqual(Object expected, Object actual, String message) {
    if (!expected.equals(actual)) {
        throw new IllegalArgumentException(message);
    }
}
{{< /highlight >}}

**PSDJAVA-521. Інформація в PSD втрачається лише при відкритті та збереженні**

{{< highlight java >}}
    String src = "src/main/resources/Original file.psd";
    String outputPsd = "src/main/resources/out_Original file.psd";
    String outputPng = "src/main/resources/out_Original file.png";

    try (PsdImage psdImage = (PsdImage) Image.load(src)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        psdImage.save(outputPsd);
        psdImage.save(outputPng, pngOptions);
    }
{{< /highlight >}}

**PSDJAVA-522. Помилка завантаження картинки**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Помилка завантаження картинки: Неможливо привести об'єкт типу UnknownStructure до типу DescriptorStructure**

{{< highlight java >}}
   try (PsdImage newPsd = new PsdImage(10, 10)) {
        newPsd.addLayer(FillLayer.createInstance(FillType.Gradient));

        final MemoryStream memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000);
        try {
            newPsd.save(memStream.toOutputStream());

            memStream.seek(DescriptorStructure.StructureKey, SeekOrigin.Current);
            memStream.write(new byte[1], 0, 0);
            memStream.setPosition(0);

            try (PsdImage psdImage = (PsdImage) Image.load(memStream.toInputStream())) {
                // Повинно завантажитись коректно
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Файл, змінений у бібліотеці третьої сторони, пошкоджує файл PSD, але його можна відкрити в Photoshop**

{{< highlight java >}}
    String sourceFile = "src/main/resources/output.psd";
    String outputFile = "src/main/resources/export.png";

    PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
    psdLoadOptions.setLoadEffectsResource(true);

    try (PsdImage img = (PsdImage) Image.load(sourceFile, psdLoadOptions)) {
        PngOptions pngOptions = new PngOptions();
        pngOptions.setCompressionLevel(9);
        pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

        img.save(outputFile, pngOptions);
    }
{{< /highlight >}}
