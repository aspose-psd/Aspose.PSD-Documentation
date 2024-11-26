---
title: Aspose.PSD для .NET 24.1 - Примітки до випуску
type: docs
weight: 120
url: /uk/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до випуску для [Aspose.PSD для .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Опис**                                                                                         | **Категорія** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [Формат AI] Додавання базової обробки для багатосторінкових зображень AI                        |   Функціонал   |
| PSDNET-718  | Ефект нахилення тексту не застосовується до тексту                                               |     Помилка     |
| PSDNET-1620 | Неправильне відтворення маски у конкретному файлі                                                 |     Помилка     |
| PSDNET-1855 | NullReferenceException в Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor     |     Помилка     |
| PSDNET-1883 | [Формат AI] Виправлення використання пам'яті в AiExporterUtils                                    |     Помилка     |



## **Зміни в публічному API**
# **Додані API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Вилучені API:**
- Немає


## **Приклади використання:**

**PSDNET-718. Ефект нахилення тексту не застосовується до тексту**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. Неправильне відтворення маски у конкретному файлі**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [Формат AI] Додавання базової обробки для багатосторінкових зображень AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Завантаження зображення AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // За замовчуванням, ActivePageIndex становить 0.
    // Таким чином, якщо ви збережете зображення AI без зміни цього параметру, буде відобразиотано і збережено першу сторінку.
    image.Save(firstPageOutputPng, new PngOptions());

    // Зміна активного індексу сторінки на другу.
    image.ActivePageIndex = 1;

    // Збереження другої сторінки зображення AI як зображення PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Зміна активного індексу сторінки на третю.
    image.ActivePageIndex = 2;

    // Збереження третьої сторінки зображення AI як зображення PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException в Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [Формат AI] Виправлення використання пам'яті в AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Завантаження зображення AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Збереження першої сторінки зображення AI як зображення PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Зміна активного індексу сторінки на другу.
    image.ActivePageIndex = 1;

    // Збереження другої сторінки зображення AI як зображення PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Зміна активного індексу сторінки на третю.
    image.ActivePageIndex = 2;

    // Збереження третьої сторінки зображення AI як зображення PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Використання пам'яті занадто велике. " + memoryUsed + " замість " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
