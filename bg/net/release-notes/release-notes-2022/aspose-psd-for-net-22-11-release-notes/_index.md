---
title: Aspose.PSD за .NET 22.11 - Бележки към изданието
type: docs
weight: 20
url: /bg/net/aspose-psd-za-net-22-11-belejki-kam-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки към изданието на [Aspose.PSD за .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- Това издание има регресия в случая на експортиране на 16-битови изображения, затова препоръчваме внимание при използването на тази функция в това издание.
Моля, не актуализирайте Aspose.PSD до версии 22.9-22.11, ако обработката на 16-битови изображения е вашата основна функционалност.

Работим по решения на тези проблеми.

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1320|Не може да се експортират изключително големи PSB файлове|Подобрение|
|PSDNET-659|Да направи центъра на радиалния градиент подвижен|Функционалност|
|PSDNET-1330|Неподдържан метод за компресиране ZipWithoutPrediction за специфичните файлове|Функционалност|
|PSDNET-735|След използване на метод за трансформация само за слой, запазеният слой има грешно граница на блока|Проблем|
|PSDNET-1234|Изключение при зареждане на PSD изображение с шаблон|Проблем|
|PSDNET-1244|Грешка при експортиране на изображение (IndexOutOfRangeException) при запазването на PSD файл с китайски символи|Проблем|
|PSDNET-1303|TimeLine ActiveFrame прилага неправилно|Проблем|
|PSDNET-1307|Регресия 22.7: неправилно изчертаване на текст с арабски символи|Проблем|
|PSDNET-1321|Векторната маска върху слоя на групата работи неправилно. Крайното изображение има черна дупка, но не трябва|Проблем|


## **Промени в обществения API**
# **Добавени API:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **Премахнати API:**
- Нито един


## **Примери за използване:**

**PSDNET-659. Направете центъра на радиалния градиент подвижен**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // Актуализиране на точката за отместване
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. След използване на метод за трансформация само за слой, запазеният слой има грешно граница на блока**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // Задава нов размер на текстовия слой
    const int NewWidth = 250;
    const int NewHeight = 250;

    // Задава механизма за това как функцията за преоразмеряване ще преоразмери слоя (стандартна стойност)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // Нов механизъм за преоразмеряване на текстов слой, който изисква и промяна на матрицата за трансформация на текстовия слой
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // Причината за разликата е различният заместителен шрифт по подразбиране
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // Всичко е наред
    }
    else
    {
        throw new Exception("Местоположението е грешно");
    }
}
{{< /highlight >}}

**PSDNET-1234. Изключение при зареждане на PSD изображение с шаблон**

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

**PSDNET-1244. Грешка при експортиране на изображение (IndexOutOfRangeException) при запазването на PSD файл с китайски символи**

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

    // Тук не трябва да има изключение.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame прилага неправилно**

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

**PSDNET-1307. Регресия 22.7: неправилно изчертаване на текст с арабски символи**

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

**PSDNET-1320. Не може да се експортират изключително големи PSB файлове**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. Векторната маска върху слоя на групата работи неправилно. Крайното изображение има черна дупка, но не трябва**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. Неподдържан метод за компресиране ZipWithoutPrediction за специфичните файлове**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
