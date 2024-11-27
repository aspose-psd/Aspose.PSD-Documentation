---
title: Aspose.PSD за .NET 21.6 - Бележки за изданието
type: docs
weight: 70
url: /bg/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-546|Сlipping маската за група не се изобразява правилно|Проблем|
|PSDNET-547|Редовната или векторната маска за групата на слоеве се игнорира при изобразяване|Проблем|
|PSDNET-647|PSD изображението с изключени векторни маски за слоя при запазване активира векторни маски|Проблем|
|PSDNET-786|Изключение при създаването на TextLayer с текст по-дълъг от 255 символа|Проблем|
|PSDNET-900|Текстът на слоя Text не може да бъде изобразен на Linux|Подобрение|

## **Промени в Общественото API**
# **Добавени API:**
- Нито един

# **Премахнати API:**
- Нито един

## **Примери за използване:**

**PSDNET-546. Сlipping маската за група не се изобразява правилно**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Редовната или векторната маска за групата на слоеве се игнорира при изобразяване**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. PSD изображението с изключени векторни маски за слоя при запазване активира векторни маски**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Изключение при създаването на TextLayer с текст по-дълъг от 255 символа**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
