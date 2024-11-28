---
title: Aspose.PSD для .NET 22.11 - Примечания к выпуску
type: docs
weight: 20
url: /ru/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску для [Aspose.PSD для .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

{{% alert color="warning" %}}

- В этом выпуске есть ошибка в случае экспорта 16-битных изображений, поэтому рекомендуем быть осторожными при использовании этой функции в данном выпуске.
Пожалуйста, не обновляйте Aspose.PSD до версии 22.9-22.11, если обработка изображений с 16 битами является вашей основной функциональностью.

Мы работаем над решением этих проблем.

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-1320|Невозможно экспортировать очень большие файлы PSB|Улучшение|
|PSDNET-659|Делает центр радиального градиента подвижным|Функция|
|PSDNET-1330|Неподдерживаемый метод сжатия ZipWithoutPrediction для определенных файлов|Функция|
|PSDNET-735|После применения метода трансформации только к слою, сохраненный слой имеет неправильную ограничивающую рамку|Ошибка|
|PSDNET-1234|Исключение при загрузке изображения PSD с узором|Ошибка|
|PSDNET-1244|Сбой экспорта изображения (IndexOutOfRangeException) при сохранении файла PSD с китайскими символами|Ошибка|
|PSDNET-1303|TimeLine ActiveFrame применяется некорректно|Ошибка|
|PSDNET-1307|Регрессия 22.7: неправильное отображение текста с арабскими символами|Ошибка|
|PSDNET-1321|Векторная маска на слое группы работает неправильно. Итоговое изображение имеет черную дыру, но не должно|Ошибка|


## **Изменения в открытом API**
# **Добавленные API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-659. Делает центр радиального градиента подвижным**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // Обновление точки смещения
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. После применения метода трансформации только к слою, сохраненный слой имеет неправиль...**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // Устанавливает новый размер текстового слоя
    const int NewWidth = 250;
    const int NewHeight = 250;

    // Устанавливает механизм, как функция изменения размера будет изменять слой (значение по умолчанию)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Новый механизм изменения размера для текстового слоя
    // Будут изменены как сам слой, так и матрица трансформации текстового слоя
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // Причина отличия - другой шрифт по умолчанию
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // Все в порядке
    }
    else
    {
        throw new Exception("Неправильное местоположение точки");
    }
}
{{< /highlight >}}

**PSDNET-1234. Исключение при загрузке изображения PSD с узором**

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

**PSDNET-1244. Сбой экспорта изображения (IndexOutOfRangeException) при сохранении файла PSD с китайскими символ...**

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

    // Здесь не должно быть исключения.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame применяется некорректно**

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

**PSDNET-1307. Регрессия 22.7: неправильное отображение текста с арабскими символами**

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

**PSDNET-1320. Невозможно экспортировать очень большие файлы PSB**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Векторная маска на слое группы работает неправильно. Итоговое изображение имеет черную д...**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. Неподдерживаемый метод сжатия ZipWithoutPrediction для определенных файлов**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
