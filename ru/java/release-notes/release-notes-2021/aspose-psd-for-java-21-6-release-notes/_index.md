---
title: Aspose.PSD для Java 21.6 - Примечания к выпуску
type: docs
weight: 40
url: /ru/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}}This page contains release notes for [Aspose.PSD для Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/){{% /alert %}}

|**Ключ**|**Сводка**|**Категория**|
| :- | :- | :- |
|PSDJAVA-351|Маска обрезки для группы не отображается правильно|Ошибка|
|PSDJAVA-352|Обычная или векторная маска для группы слоев игнорируется при визуализации|Ошибка|
|PSDJAVA-353|Изображение PSD с отключенными векторными масками слоев при сохранении включает векторные маски|Ошибка|
|PSDJAVA-354|Исключение при создании текстового слоя с текстом длиной более 255 символов|Ошибка|

# **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

# **Примеры использования:**

**PSDJAVA-351. Маска обрезки для группы не отображается правильно**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. Обычная или векторная маска для группы слоев игнорируется при визуализации**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. Изображение PSD с отключенными векторными масками слоев при сохранении включает векторные маски**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. Исключение при создании текстового слоя с текстом длиной более 255 символов**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
