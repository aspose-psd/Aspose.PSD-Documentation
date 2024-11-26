---
title: Aspose.PSD для .NET 24.1 - Примечания к выпуску
type: docs
weight: 120
url: /ru/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**    | **Краткое описание**                                                                               | **Категория** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | Добавление базовой обработки для многостраничных изображений AI                                   |   Функция    |
| PSDNET-718  | Эффект «Искажение текста» не применяется к тексту                                                   |     Ошибка    |
| PSDNET-1620 | Некорректная отрисовка маски в определенном файле                                                   |     Ошибка    |
| PSDNET-1855 | NullReferenceException в Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor        |     Ошибка    |
| PSDNET-1883 | Исправление использования памяти в AiExporterUtils                                                  |     Ошибка    |



## **Изменения в общедоступном API**
# **Добавленные API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-718. Эффект искажения текста не применяется к тексту**

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

**PSDNET-1620. Некорректная отрисовка маски в определенном файле**

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

**PSDNET-1835. Добавление базовой обработки для многостраничных изображений AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Загрузка изображения AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // По умолчанию ActivePageIndex равен 0.
    // Поэтому, если вы сохраните изображение AI, не изменив это свойство, будет сохранена и отрисована первая страница.
    image.Save(firstPageOutputPng, new PngOptions());

    // Измените индекс активной страницы на вторую страницу.
    image.ActivePageIndex = 1;

    // Сохраните вторую страницу изображения AI как изображение PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Измените индекс активной страницы на третью страницу.
    image.ActivePageIndex = 2;

    // Сохраните третью страницу изображения AI как изображение PNG.
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

**PSDNET-1883. Исправление использования памяти в AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Загрузка изображения AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Сохранение первой страницы изображения AI как изображение PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // Измените индекс активной страницы на вторую страницу.
    image.ActivePageIndex = 1;

    // Сохраните вторую страницу изображения AI как изображение PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // Измените индекс активной страницы на третью страницу.
    image.ActivePageIndex = 2;

    // Сохраните третью страницу изображения AI как изображение PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Использование памяти слишком велико. " + memoryUsed + " вместо " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
