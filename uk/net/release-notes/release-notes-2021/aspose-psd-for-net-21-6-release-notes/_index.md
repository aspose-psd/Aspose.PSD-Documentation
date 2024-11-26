---
title: Особливості версії Aspose.PSD для .NET 21.6
type: docs
weight: 70
url: /uk/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

Ця сторінка містить інформацію про версію [Aspose.PSD для .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Зміст**|**Категорія**|
| :- | :- | :- |
|PSDNET-546|Сlipping mask для групи рендериться некоректно|Помилка|
|PSDNET-547|Звичайний або векторний масив для групи шарів ігнорується при рендерингу|Помилка|
|PSDNET-647|Зображення PSD з вимкненими векторними масками шарів при збереженні увімкнює векторні маски|Помилка|
|PSDNET-786|Виняток при створенні TextLayer з текстом довшим за 255 символів|Помилка|
|PSDNET-900|Текст шару Text не може бути відтворений на Linux|Покращення|

## **Зміни у Публічному API**
# **Додані API:**
- Немає

# **Вилучені API:**
- Немає

## **Приклади використання:**

**PSDNET-546. Сlipping mask для групи рендериться некоректно**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Звичайний або векторний масив для групи шарів ігнорується при рендерингу**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Зображення PSD з вимкненими векторними масками шарів при збереженні увімкнює векторні маски**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Виняток при створенні TextLayer з текстом довшим за 255 символів**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
