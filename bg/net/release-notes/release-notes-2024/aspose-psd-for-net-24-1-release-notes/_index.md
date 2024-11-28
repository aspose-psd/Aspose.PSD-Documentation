---
title: Aspose.PSD за .NET 24.1 - Бележки за изданието
type: docs
weight: 120
url: /bg/net/aspose-psd-za-net-24-1-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **Ключ**      | **Резюме**                                                                                        | **Категория** |
|:--------------|:---------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1835   | [Формат AI] Добавяне на основно обработване за многoстранични AI изображения                           |   Характеристика   |
| PSDNET-718    | Ефектът на изкривяването на текста не се прилага към текста                                            |     Грешка     |
| PSDNET-1620   | Неправилно изобразяване на маската в конкретния файл                                                      |     Грешка     |
| PSDNET-1855   | NullReferenceException при Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor         |     Грешка     |
| PSDNET-1883   | [Формат AI] Оптимизиране на използваната памет в AiExporterUtils                                              |     Грешка     |



## **Промени в публичният API**
# **Добавени API:**
- P:Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **Премахнати API:**
- Няма


## **Примери за използване:**

**PSDNET-718. Ефектът на изкривяването на текста не се прилага към текста**

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

**PSDNET-1620. Неправилно изобразяване на маската в конкретния файл**

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

**PSDNET-1835. [Формат AI] Добавяне на основно обработване за многoстранични AI изображения**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// Заредете AI изображението.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // По подразбиране, ActivePageIndex е 0.
    // Така че, ако запазите AI изображението без да променяте това свойство, ще бъде изобразена и запазена първата страница.
    image.Save(firstPageOutputPng, new PngOptions());

    // Променете активния индекс на страницата на втората страница.
    image.ActivePageIndex = 1;

    // Запазете втората страница на AI изображението като PNG изображение.
    image.Save(secondPageOutputPng, new PngOptions());

    // Променете активния индекс на страницата на третата страница.
    image.ActivePageIndex = 2;

    // Запазете третата страница на AI изображението като PNG изображение.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException при Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

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


**PSDNET-1883. [Формат AI] Оптимизиране на използваната памет в AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// Заредете AI изображението.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // Запазете първата страница на AI изображението като PNG изображение.
    image.Save(firstPageOutputPng, new PngOptions());

    // Променете активния индекс на страницата на втората страница.
    image.ActivePageIndex = 1;

    // Запазете втората страница на AI изображението като PNG изображение.
    image.Save(secondPageOutputPng, new PngOptions());

    // Променете активния индекс на страницата на третата страница.
    image.ActivePageIndex = 2;

    // Запазете третата страница на AI изображението като PNG изображение.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("Използването на памет е твърде голямо. " + memoryUsed + " вместо " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
