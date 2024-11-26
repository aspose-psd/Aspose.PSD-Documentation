---
title: Примітки до версії Aspose.PSD для .NET 22.12
type: docs
weight: 10
url: /uk/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}

Ця сторінка містить примітки до версії [Aspose.PSD для .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="success" %}}

- У цьому випуску було виправлено регресію з експортом 16-бітного зображення.

{{% /alert %}}

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-1336|Додано властивість редагованого TextOrientation до інтерфейсу IText|Функція|
|PSDNET-725|Зміна розміру вказаного файлу PSD з маскою шару породжує неправильну маску|Помилка|
|PSDNET-1277|Додано можливість зберігати та завантажувати маску для 16 зображень|Помилка|
|PSDNET-1281|Неправильна прозорість при збереженні 16-бітного зображення на 16 або 8 біт|Помилка|
|PSDNET-1375|Виправлення CMYK в 16-бітному кольорі|Помилка|


## **Зміни у громадському API**
# **Додані API:**
- T:Aspose.PSD.FileFormats.Psd.TextOrientation
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:Aspose.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **Вилучені API:**
- Жодних


## **Приклади використання:**

**PSDNET-725. Редагування вказаного файлу PSD з маскою шару породжує неправильну маску**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// Відкриття вихідного файлу PSD
using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    const int Scale = 4;

    int newWidth = image.Width * Scale;
    int newHeight = image.Height * Scale;

    // Його змінено розміри
    image.Resize(newWidth, newHeight);
    image.Save(psdExportPath, new PsdOptions(image));
}

// Відкриття файлу PSD зі зміненими розмірами
using (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // Рендеринг у PNG
    image.Save(pngExportPath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1277. Додавання можливості зберігання та завантаження маски для 16 зображень**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

using (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // Параметри дозволяють зберігати 16-бітний колір
    PsdOptions options16 = new PsdOptions { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb};

    // Файл PSD буде збережений з прозорістю
    image.Save(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. Неправильна прозорість при збереженні 16-бітного зображення на 16 або 8 біт**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// 16-бітний колірний файл psd (з прозорістю) буде відкрито та збережено у 16-бітий колір
using (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };
    image.Save(resavedFile, options16);
}

// Збережений файл psd з 16 бітним кольором буде рендеред до png з прозорістю
using (var image = (PsdImage)Image.Load(resavedFile))
{
    image.Save(imageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. Додавання властивості редагованого TextOrientation до інтерфейсу IText**

{{< highlight csharp >}}
// Наведений нижче код демонструє можливість редагування нової властивості TextOrientation.
// На даний момент це не впливає на рендеринг, а лише дозволяє вам редагувати значення властивості.

string src = "1336test.psd";
string output = "out_1336test.psd";

using (var image = (PsdImage)Image.Load(src))
{
    var textLayer = image.Layers[1] as TextLayer;
    if (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // Правильне читання
    }
    else
    {
        throw new Exception("Неправильне читання значення властивості TextOrientation");
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
        // Правильне читання
    }
    else
    {
        throw new Exception("Неправильне читання значення властивості TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. Виправлення CMYK у 16-бітному кольорі**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// Встановлюються параметри конвертування
PsdOptions psdOptions = new PsdOptions()
{
    ColorMode = ColorModes.Cmyk,
    ChannelBitsCount = 16,
    ChannelsCount = 5,
    CompressionMethod = CompressionMethod.Raw
};

// Конвертування та збереження
using (var image = (PsdImage)Image.Load(srcFile))
{
    image.Convert(psdOptions);
    image.Save(exportPath);
}

// Відкриття конвертованого файлу та рендеринг до PNG
using (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    image.Save(pngExportPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
