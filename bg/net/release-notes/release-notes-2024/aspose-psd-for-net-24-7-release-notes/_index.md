---
title: Aspose.PSD за .NET 24.7 - Бележки за изданието
type: docs
weight: 60
url: /bg/aspose-psd-za-net-24-7-belejki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Обобщение**                                                                                   | **Категория** |
|:-----------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Изключение "Грешка при зареждане на изображение.", когато се отвори AI документ              | Грешка      |
| PSDNET-2022 | Текстът се рендира неправилно в изходните PDF файлове                                        | Грешка      |
| PSDNET-2061 | Оправление на ImageSaveException: Изображението не може да бъде експортирано за дадения файл на Linux | Грешка      |
| PSDNET-2080 | Оправление на зареждането на шрифтове при използването на Aspose.Drawing                     | Грешка      |
| PSDNET-2085 | 'Аритметична операция доведе до препълване' при създаване на слой на умно обект, използвайки голям JPEG | Грешка      |
| PSDNET-2100 | AI файла не може да бъде преобразуван в JPG файл                                             | Грешка      |

## **Промени в публичното API**
# **Добавени API:**
- Няма

# **Премахнати API:**
- Няма

## **Примери за използване:**

**PSDNET-1029. "Грешка при зареждане на изображение.", когато се отвори AI документ**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Текстът се рендира неправилно в изходните PDF файлове**

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

**PSDNET-2061. Оправление на ImageSaveException: Изображението не може да бъде експортирано за дадения файл на Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Оправление на зареждането на шрифтове при използването на Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Преди обновяване. Брой инсталирани шрифтове: " + installedFonts.Families.Length);
    Console.WriteLine("- Платформа: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Актуализиране на кеша на шрифтовете, като се опита да се получи името на шрифта на Adobe за 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- След обновяване. Брой инсталирани шрифтове: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Аритметична операция доведе до препълване' при създаване на слой на умно обект, използвайки голям JPEG**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. AI файла не може да бъде преобразуван в JPG файл**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
