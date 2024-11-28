---
title: Релизные заметки Aspose.PSD для .NET 21.6
type: docs
weight: 70
url: /ru/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит релизные заметки для [Aspose.PSD для .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Сводка**|**Категория**|
| :- | :- | :- |
|PSDNET-546|Маска обрезки для группы не отображается правильно|Ошибка|
|PSDNET-547|Обычная или векторная маска для группы слоев игнорируется при рендеринге|Ошибка|
|PSDNET-647|Изображение PSD с отключенными векторными масками слоя при сохранении включает векторные маски|Ошибка|
|PSDNET-786|Исключение при создании слоя текста с текстом длиннее 255 символов|Ошибка|
|PSDNET-900|Текст слоя текста не может быть отображен на Linux|Улучшение|

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-546. Маска обрезки для группы не отображается правильно**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. Обычная или векторная маска для группы слоев игнорируется при рендеринге**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. Изображение PSD с отключенными векторными масками слоя при сохранении включает векторные маски**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. Исключение при создании слоя текста с текстом длиннее 255 символов**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
