---
title: Оновлення Aspose.PSD для .NET 22.11
type: docs
weight: 20
url: /uk/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить оновлення для [Aspose.PSD для .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- У цій версії є помилка в експорті 16-бітних файлів, тому ми радимо бути обережними при використанні цієї функції в даному випуску.
Будь ласка, не оновлюйте Aspose.PSD до версій 22.9-22.11, якщо опрацювання зображень 16-біт є вашою основною функціональністю.

Ми працюємо над вирішенням цих проблем.

{{% /alert %}}

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-1320|Не вдається експортувати дуже великі файли PSB|Покращення|
|PSDNET-659|Зробити центр радіального градієнта рухомим|Функція|
|PSDNET-1330|Непідтримуваний метод стиснення ZipWithoutPrediction для конкретних файлів|Функція|
|PSDNET-735|Після використання методу трансформації лише для шару, збережений шар має неправильну межу|Помилка|
|PSDNET-1234|Виняток при завантаженні зображення PSD з малюнком|Помилка|
|PSDNET-1244|Помилка експорту зображення (IndexOutOfRangeException) під час збереження файлу PSD з китайськими символами|Помилка|
|PSDNET-1303|Часова лінія ActiveFrame застосовується неправильно|Помилка|
|PSDNET-1307|Регресія 22.7: неправильне рендеринг тексту з арабськими символами|Помилка|
|PSDNET-1321|Векторна маска на шарі групи працює некоректно. Кінцеве зображення має чорну дірку, але не повинно|Помилка|


## **Зміни в публічному API**
# **Додані API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Вилучені API:**
- Немає


## **Приклади використання**

**PSDNET-659. Зробити центр радіального градієнта рухомим**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // Оновити точку зміщення
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. Після використання методу трансформації лише для шару, збережений шар має неправильну межу**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // Встановити новий розмір текстового шару
    const int NewWidth = 250;
    const int NewHeight = 250;

    // Встановити механізм, за межею якого функція зміни розміру буде змінювати шар (значення за замовчуванням)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Новий механізм зміни розміру для текстового шару
    // Зміниться не лише шар, але й матриця трансформації текстового шару
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // Причина дельти полягає в різних шрифтах за замовчуванням
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // Все в порядку
    }
    else
    {
        throw new Exception("Точка розташування неправильна");
    }
}
{{< /highlight >}}

**PSDNET-1234. Виняток при завантаженні зображення PSD з малюнком**

{{< highlight csharp >}}
string srcFile = "test.psd";
string output = "output1234.png";

using (PsdImage psdImage = (PsdImage)PsdImage.Load(srcFile,
new PsdLoadOptions() { LoadEffectsResource = true }))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    psdImage.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1244. Помилка експорту зображення (IndexOutOfRangeException) під час збереження файлу PSD з китайськими символами**

{{< highlight csharp >}}
string sourceFile = "input.psd";
string outputPath = "output.psd";

var loadOptions = new PsdLoadOptions
{
    LoadEffectsResource = true,
    UseDiskForLoadEffectsResource = true
};

using (var image = (PsdImage)Image.Load(sourceFile, loadOptions))
{
    foreach (var layer in image.Layers)
    {
        if (layer.Name == "1")
        {
            var txtLayer = (TextLayer)layer;

            txtLayer.UpdateText("测试测试");
        }
    }

    // Тут не повинно бути винятків.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. Часова лінія ActiveFrame застосовується неправильно**

{{< highlight csharp >}}
string src = "timeline1303.psd";
string output = "out_timeline.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);

    timeLine.ActiveFrame = 2;
    timeLine.ApplyTo(psdImage);

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1307. Регресія 22.7: неправильне рендеринг тексту з арабськими символами**

{{< highlight csharp >}}
string testFontsFolder = "Fonts";
FontSettings.SetFontsFolder(testFontsFolder);
FontSettings.UpdateFonts();

string sourceFilePath = "sarbarg.fin12.psd";
string outputFilePath = "result.tiff";

using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
{
    psdImage.Save(outputFilePath, new Aspose.PSD.ImageOptions.TiffOptions(TiffExpectedFormat.TiffLzwRgb));
}
{{< /highlight >}}

**PSDNET-1320. Не вдається експортувати дуже великі файли PSB**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Векторна маска на шарі групи працює некоректно. Кінцеве зображення має чорну дірку, але не повинно**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. Непідтримуваний метод стиснення ZipWithoutPrediction для конкретних файлів**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
