---
title: Aspose.PSD за .NET 22.12 - Забележки за изданието
type: docs
weight: 10
url: /bg/net/aspose-psd-za-net-22-12-zabejki-za-izdanieto/
---

{{% alert color="primary" %}}

Тази страница съдържа забележки за изданието на [Aspose.PSD за .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- В това издание беше отстранен проблем с регресия при износ на 16-битови изображения.

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-1336|Добавяне на свойство за редактируем ориентация на текста към интерфейса IText|Функционалност|
|PSDNET-725|Преоразмеряването на определен файл PSD с маска на слой дава невярна маска|Грешка|
|PSDNET-1277|Добавяне на възможността за запазване и зареждане на маска за 16 изображения|Грешка|
|PSDNET-1281|Неправилна прозрачност при запазване на 16-битово изображение към 16- или 8-битово изображение|Грешка|
|PSDNET-1375|Оправяне на CMYK в 16-битов цвят|Грешка|


## **Промени в публичния API**
# **Добавени API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Премахнати API:**
- Няма


## **Примери за използване:**

**PSDNET-725. Преоразмеряването на определен файл PSD с маска на слой дава невярна маска**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Отваря се изходният PSD файл
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Промяна на размера
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Отваря се преоразмереният PSD файл
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Рендиране към PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Добавяне на възможността за запазване и зареждане на маска за 16 изображения**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Опциите позволяват запазването на 16-битов цвят
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Файлът PSD ще бъде запазен с прозрачност
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Неправилна прозрачност при запазване на 16-битово изображение към 16- или 8-битово изображение**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16-битов цветен PSD файл (с прозрачност) ще бъде отворен и запазен като 16-битов цветен
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Запазеният 16-битов цветен PSD файл ще бъде преобразуван в png файл с прозрачност
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Добавяне на свойството за редактируема ориентация на текста към интерфейса IText**

{{< highlight csharp >}}
// Следният код демонстрира способността да се редактира новото свойство за ориентация на текста.
// Това не засяга рендерирането в момента, а само позволява редакция на стойността на свойството.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Правилно четене
    }
    else
    {
        throw new Exception("Неправилно четене на стойността на свойството за ориентация на текста");
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
        // Правилно четене
    }
    else
    {
        throw new Exception("Неправилно четене на стойността на свойството за ориентация на текста");
    }
}
{{< /highlight >}}

**PSDNET-1375. Оправяне на CMYK в 16-битов цвят**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Задават се опциите за конвертиране
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Конвертира се и запазва
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Отваря се конвертираният файл и се рендира към PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
