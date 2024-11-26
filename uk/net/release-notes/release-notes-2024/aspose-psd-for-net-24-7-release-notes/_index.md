---
title: Опис версії Aspose.PSD для .NET 24.7
type: docs
weight: 60
url: /uk/net/aspose-psd-dlya-net-24-7-opys-versiyi/
---

{{% alert color="primary" %}}

Ця сторінка містить опис версії для [Aspose.PSD для .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**     | **Опис**                                                                                      | **Категорія** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | Виняток "Помилка завантаження зображення." при відкритті документа AI                                 | Помилка      |
| PSDNET-2022 | Текст неправильно відображається в вихідних PDF-файлах                                                    | Помилка      |
| PSDNET-2061 | Виправлено виняток ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux      | Помилка      |
| PSDNET-2080 | Виправлено завантаження шрифтів при використанні Aspose.Drawing                                           | Помилка      |
| PSDNET-2085 | 'Арифметична операція призвела до переповнення' при створенні шару розумного об'єкта за великим JPEG | Помилка      |
| PSDNET-2100 | Файл AI не може бути перетворений в файл JPG                                                            | Помилка      |

## **Зміни у публічному API**
# **Додано API:**
- Жодного

# **Видалено API:**
- Жодного

## **Приклади використання:**

**PSDNET-1029. Виняток "Помилка завантаження зображення." при відкритті документа AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. Текст неправильно відображається в вихідних PDF-файлах**

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

**PSDNET-2061. Виправлено виняток ImageSaveException: Помилка експорту зображення для вказаного файлу на Linux**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. Виправлено завантаження шрифтів при використанні Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- Перед оновленням. Кількість встановлених шрифтів: " + installedFonts.Families.Length);
    Console.WriteLine("- Платформа: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("- Оновлення кешу шрифтів шляхом спроби отримання назви шрифта Adobe для 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- Після оновлення. Кількість встановлених шрифтів: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'Арифметична операція призвела до переповнення' при створенні шару розумного об'єкта за великим JPEG**

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

**PSDNET-2100. Файл AI не може бути перетворений в файл JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
