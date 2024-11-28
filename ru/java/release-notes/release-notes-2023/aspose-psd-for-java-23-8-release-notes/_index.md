---
title: Aspose.PSD для Java 23.8 - Примечания к выпуску
type: docs
weight: 40
url: /ru/java/aspose-psd-dlya-java-23-8-proshchie-zametki/
---

{{% alert color="primary" %}} Эта страница содержит примечания к выпуску [Aspose.PSD для Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-23.8/) {{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                                                                    | **Категория** |
|:-----------|:---------------------------------------------------------------------------------------------------------------------------------------------|:-------------|
| PSDJAVA-518 | Добавлен новый тип искажения (Flag)                                                                                                            |    Функция    |
| PSDJAVA-519 | Добавлены новые типы искажения: дуга вверх, дуга вниз, сфера                                                                                |    Функция    |
| PSDJAVA-520 | Реализован новый метод PsdImage.AddPosterizeAdjustmentLayer для добавления нового слоя постеризации                                   |    Функция    |
| PSDJAVA-521 | Информация PSD теряется только при открытии и сохранении                                                                                     |      Ошибка   |
| PSDJAVA-522 | Ошибка загрузки изображения                                                                                                                   |      Ошибка   |
| PSDJAVA-523 | Ошибка загрузки изображения: Невозможно привести объект типа UnknownStructure к типу DescriptorStructure                               |      Ошибка   |
| PSDJAVA-524 | Изменение файла в сторонней библиотеке повреждает файл PSD, но его можно открыть в Photoshop                                              |      Ошибка   |

## **Изменения в общедоступном API**
# **Добавленные API:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Удаленные API:**

- Нет

## **Примеры использования:**

**PSDJAVA-518. Добавлен новый тип искажения (Flag)**

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

**PSDJAVA-519. Добавлены новые типы искажения: дуга вверх, дуга вниз, сфера**

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

**PSDJAVA-520. Реализован новый метод PsdImage.AddPosterizeAdjustmentLayer для добавления нового слоя постеризации**

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

    // Check saved changes
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
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

**PSDJAVA-521. Информация PSD теряется только при открытии и сохранении**

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

**PSDJAVA-522. Ошибка загрузки изображения**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Ошибка загрузки изображения: Невозможно привести объект типа UnknownStructure к типу DescriptorStructure**

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
                // Должно быть загружено правильно
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Изменение файла в сторонней библиотеке повреждает файл PSD, но его можно открыть в Photoshop**

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
