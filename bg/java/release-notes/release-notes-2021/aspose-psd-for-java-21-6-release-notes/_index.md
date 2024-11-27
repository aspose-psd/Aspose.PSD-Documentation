---
title: Aspose.PSD за Java 21.6 - Бележки за изданието
type: docs
weight: 40
url: /bg/java/aspose-psd-za-java-21-6-belejki-za-izdanieto/
---

{{% alert color="primary" %}} Тази страница съдържа бележки за изданието на [Aspose.PSD за Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDJAVA-351|Сlipping маска за група не се визуализира правилно|Проблем|
|PSDJAVA-352|Редовна или векторна маска за група от слоеве се игнорира при визуализация|Проблем|
|PSDJAVA-353|PSD изображение с деактивирани векторни слойни маски при запазване активира векторни маски|Проблем|
|PSDJAVA-354|Изключение при създаване на TextLayer с текст по-дълъг от 255 знака|Проблем|

# **Промени в Публичния API**
# **Добавени API:**
- Няма

# **Премахнати API:**
- Няма

# **Примери за използване:**

**PSDJAVA-351. Сlipping маска за група не се визуализира правилно**

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

**PSDJAVA-352. Редовна или векторна маска за група от слоеве се игнорира при визуализация**

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

**PSDJAVA-353. PSD изображение с деактивирани векторни слойни маски при запазване активира векторни маски**

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

**PSDJAVA-354. Изключение при създаване на TextLayer с текст по-дълъг от 255 знака**

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