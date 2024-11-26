---
title: Aspose.PSD для .NET 22.12 - Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-psd-для-net-22-12-примечания-к-выпуску/
---

{{% alert color="primary" %}}

Эта страница содержит примечания к выпуску для [Aspose.PSD для .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- В этом выпуске была исправлена ошибка с экспортом изображений 16 бит.

{{% /alert %}}

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-1336|Добавить свойство для редактирования текстовой ориентации в интерфейс IText|Функциональность|
|PSDNET-725|Изменение размера указанного файла PSD с маской слоя приводит к некорректной маске|Ошибка|
|PSDNET-1277|Добавление возможности сохранения и загрузки маски для 16 изображений|Ошибка|
|PSDNET-1281|Неверная прозрачность при сохранении изображения 16 бит в изображение 16 или 8 бит|Ошибка|
|PSDNET-1375|Исправление CMYK в цвете 16 бит|Ошибка|


## **Изменения в общедоступном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Удаленные API:**
- Нет


## **Примеры использования:**

**PSDNET-725. Изменение размера указанного файла PSD с маской слоя приводит к некорректной маске**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Открывает исходный файл PSD
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Изменяет размер
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Открывает измененный файл PSD
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Сохраняет в формате PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Добавление возможности сохранения и загрузки маски для 16 изображений**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Опции позволяют сохранить изображения с 16 битным цветом
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Файл PSD сохранится с прозрачностью
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Неверная прозрачность при сохранении изображения 16 бит в изображение 16 или 8 бит**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// Открывается файл PSD с цветом 16 бит (с прозрачностью) и сохраняется как 16 битный цвет
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Сохраненный файл PSD с цветом 16 бит рендерится в файл PNG с прозрачностью
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Добавить свойство для редактирования текстовой ориентации в интерфейс IText**

{{< highlight csharp >}}
// Следующий код демонстрирует возможность редактировать новое свойство TextOrientation.
// Оно не влияет на рендеринг в настоящее время, но позволяет только редактировать значение свойства.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Правильное чтение
    }
    else
    {
        throw new Exception("Неправильное чтение значения свойства TextOrientation");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    image.Save(output);
}

using (var image = (PsdImage)Image.Load(output))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // Правильное чтение
    }
    else
    {
        throw new Exception("Неправильное чтение значения свойства TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Исправление CMYK в 16 битном цвете**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Устанавливаются параметры конвертации
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Происходит конвертация и сохранение
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Открывается сконвертированный файл и рендерится в PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
