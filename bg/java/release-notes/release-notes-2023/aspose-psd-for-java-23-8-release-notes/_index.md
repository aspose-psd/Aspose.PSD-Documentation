---
title: Aspose.PSD за Java 23.8 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-23-8-release-notes/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 23.8](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-za-java-23.8/) {{% /alert %}}

| **Ключ**    | **Обобщение**                                                                                                                                  | **Категория** |
|:------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|:--------------|
| PSDJAVA-518 | Добавяне на нов тип warp (Flag)                                                                                                                |    Функционал |
| PSDJAVA-519 | Добавяне на нови типове warp: arc up, arc down, sphere                                                                                         |    Функционал |
| PSDJAVA-520 | Реализиране на нов метод PsdImage.AddPosterizeAdjustmentLayer за добавяне на нов слой Posterize                                               |    Функционал |
| PSDJAVA-521 | Информацията в PSD файла се губи само при отваряне и запазване                                                                                |         Грешка |
| PSDJAVA-522 | Зареждането на изображението се провали                                                                                                        |         Грешка |
| PSDJAVA-523 | Зареждането на изображението е се провали: Неуспешно преобразуване на обект от тип НеизвестенОбект към тип ОписателенОбект                    |         Грешка |
| PSDJAVA-524 | Промяна на файла във вредна библиотека поврежда PSD файла, но той може да бъде отворен във Photoshop                                           |         Грешка |

## **Промени в публичния API**
# **Добавени APIs:**

- M:com.aspose.psd.fileformats.psd.PsdImage.addPosterizeAdjustmentLayer

# **Премахнати APIs:**

- Няма

## **Примери за използване:**

**PSDJAVA-518. Добавяне на нов тип warp (Flag)**

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

**PSDJAVA-519. Добавяне на нови типове warp: arc up, arc down, sphere**

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

**PSDJAVA-520. Реализиране на нов метод PsdImage.AddPosterizeAdjustmentLayer за добавяне на нов слой Posterize**

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

    // Проверка на запазените промени
    try (PsdImage image = (PsdImage) Image.load(outFile, psdLoadOptions)) {
        assertAreEqual(2, image.getLayers().length);

        PosterizeLayer posterizeLayer = (PosterizeLayer) image.getLayers()[1];

        assertAreEqual(true, posterizeLayer instanceof PosterizeLayer);
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

**PSDJAVA-521. Информацията в PSD файла се губи само при отваряне и запазване**

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

**PSDJAVA-522. Зареждането на изображението се провали**

{{< highlight java >}}
    String srcFile1 = "src/main/resources/test_text.psd";
    String srcFile2 = "src/main/resources/test_smart_object.psd";

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile1)) {
    }

    try (PsdImage psdImage = (PsdImage) Image.load(srcFile2)) {
    }
{{< /highlight >}}

**PSDJAVA-523. Зареждането на изображението се провали: Неуспешно преобразуване на обект от тип НеизвестенОбект към тип ОписателенОбект**

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
                // Трябва да зареди коректно
            }
        } finally {
            memStream.close();
        }
    }
{{< /highlight >}}

**PSDJAVA-524. Промяна на файла във вредна библиотека поврежда PSD файла, но той може да бъде отворен във Photoshop**

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