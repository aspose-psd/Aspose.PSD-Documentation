---
title: Aspose.PSD для Java 21.6 - Примітки до версії
type: docs
weight: 40
url: /uk/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} Ця сторінка містить примітки до версії для [Aspose.PSD для Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDJAVA-351|Маска обрізання для групи не відображається коректно|Помилка|
|PSDJAVA-352|Звичайна або векторна маска для групи шарів не враховується при відображенні|Помилка|
|PSDJAVA-353|Зображення PSD з вимкненими векторними масками на збереження увімкнює векторні маски|Помилка|
|PSDJAVA-354|Виняток при створенні текстового шару з текстом довшим за 255 символів|Помилка|

# **Зміни у публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає

# **Приклади використання:**

**PSDJAVA-351. Маска обрізки для групи не відображається коректно**

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

**PSDJAVA-352. Звичайна або векторна маска для групи шарів не враховується при відображенні**

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

**PSDJAVA-353. Зображення PSD з вимкненими векторними масками на збереження увімкнює векторні маски**

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

**PSDJAVA-354. Виняток при створенні текстового шару з текстом довшим за 255 символів**

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
