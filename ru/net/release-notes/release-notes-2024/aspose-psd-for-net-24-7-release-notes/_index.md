---
title: Aspose.PSD для .NET 24.7 - Примечания к выпуску
type: docs
weight: 60
url: /ru/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

На этой странице содержатся примечания к [Aspose.PSD для .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**     | **Краткое описание**                                                                              | **Категория** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Исключение "Не удалось загрузить изображение" при открытии документа AI                         | Ошибка      |
| PSDNET-2022 | Текст отображается неправильно в выходных файлах PDF                                           | Ошибка      |
| PSDNET-2061 | Исправление ImageSaveException: Ошибка экспорта изображения для указанного файла на Linux       | Ошибка      |
| PSDNET-2080 | Исправление загрузки шрифтов при использовании Aspose.Drawing                                     | Ошибка      |
| PSDNET-2085 | "Арифметическая операция привела к переполнению" при создании умного объектного слоя с использованием большого JPEG     | Ошибка      |
| PSDNET-2100 | Файл AI не может быть преобразован в файл JPG                                                   | Ошибка      |

## **Изменения в общедоступном API**
# **Добавленные API:**
- Нет

# **Удаленные API:**
- Нет

## **Примеры использования:**

**PSDNET-1029. Исключение "Не удалось загрузить изображение" при открытии документа AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Текст отображается неправильно в выходных файлах PDF**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. Исправление ImageSaveException: Ошибка экспорта изображения для указанного файла на Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Исправление загрузки шрифтов при использовании Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Перед обновлением. Количество установленных шрифтов: " + installedFonts.Families.Length);
    Console.WriteLine("- Платформа: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Обновите кэш шрифтов, попытавшись получить название шрифта Adobe для 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- После обновления. Количество установленных шрифтов: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. "Арифметическая операция привела к переполнению" при создании умного объектного слоя с использованием большого JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Тестовый слой";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. Файл AI не может быть преобразован в файл JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
