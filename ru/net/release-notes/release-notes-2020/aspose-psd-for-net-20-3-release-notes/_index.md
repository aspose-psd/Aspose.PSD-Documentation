---
title: Примечания к выпуску Aspose.PSD для .NET 20.3
type: docs
weight: 100
url: /ru/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску [Aspose.PSD для .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Описание**|**Категория**|
| :- | :- | :- |
|PSDNET-188|Поддержка .Net Core|Функция|
|PSDNET-523|Преобразование файлов Adobe Illustrator в PDF|Функция|
|PSDNET-212|Добавление возможности отображения различных стилей в одном текстовом слое|Функция|
|PSDNET-144|Поддержка слоя регулировки черного и белого|Функция|
|PSDNET-233|Добавление поддержки экспорта формата AI (версия 8) в другие форматы|Функция|
|PSDNET-540|Поддержка режима смешивания PassThrough (используется только для группы слоев)|Функция|
|PSDNET-539|Исключение: Ошибка загрузки изображения при загрузке изображения с пустыми именами Unicode Alpha Names Resource|Ошибкa|
|PSDNET-541|Неверный вывод после изменения видимости LayerGroup|Ошибкa|
|PSDNET-516|Исключение при загрузке изображения PSD: Раздел цвета (DropShadow Resource) должен содержать 3 цветовых компонента для RGB или 4 цветовых компонента для CMYK|Ошибкa|
|PSDNET-536|Исключение при попытке рисования на новом созданном слое, если используется простая версия конструктора|Ошибкa|

## **Изменения в общедоступном API**
# **Добавленные API:**
- T:Aspose.PSD.FileFormats.Psd.FontBaseline
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.None
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Superscript
- F:Aspose.PSD.FileFormats.Psd.FontBaseline.Subscript
- T:Aspose.PSD.FileFormats.Psd.FontCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.None
- F:Aspose.PSD.FileFormats.Psd.FontCaps.SmallCaps
- F:Aspose.PSD.FileFormats.Psd.FontCaps.AllCaps
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddBlackWhiteAdjustmentLayer
- F:Aspose.PSD.FileFormats.Psd.Layers.BlendMode.Absent
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerGroup.BlendModeKey
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxBold
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FauxItalic
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Underline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Strikethrough
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontBaseline
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.BaselineShift
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.FontCaps
- M:Aspose.PSD.FileFormats.Psd.Layers.Text.IText.ProducePortions(System.String[],Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle,Aspose.PSD.FileFormats.Psd.Layers.Text.ITextParagraph)
# **Удаленные API:**
- Ничего

## **Примеры использования:**
**PSDNET-523. Конвертация файлов Adobe Illustrator в PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Добавление возможности отображения различных стилей в одном текстовом слое**

{{< highlight java >}}

 string sourceFile = "text212.psd";

string ethalonFile = "Ethalon_text212.psd";

string outputFile = "Output_text212.psd";

using (var img = (PsdImage)Image.Load(sourceFile))

{

    TextLayer textLayer = (TextLayer)img.Layers[1];

    IText textData = textLayer.TextData;

    ITextStyle defaultStyle = textData.ProducePortion().Style;

    ITextParagraph defaultParagraph = textData.ProducePortion().Paragraph;

    defaultStyle.FillColor = Color.DimGray;

    defaultStyle.FontSize = 51;

    textData.Items[1].Style.Strikethrough = true;

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Bold",  "Italic\r",  "Lowercasetext" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // edit text style "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // edit text style "2\r"

    newPortions[2].Style.FauxBold = true; // edit text style "Bold"

    newPortions[3].Style.FauxItalic = true; // edit text style "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // edit text style "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // edit text style "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Добавление поддержки экспорта формата AI (версия 8) в другие форматы**

{{< highlight java >}}

 // Пример экспорта файла AI в формат PSD и PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Поддержка обработки режима смешивания PassThrough (используется только для группы слоев).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Apple.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Там нет 23-го слоя.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23-й слой не является группой слоев.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Имя 23-го слоя не 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Слой группы регулировки должен иметь режим смешивания 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Обновление текста в текстовом слое вызывает исключение**

{{< highlight java >}}

 // Обновление текста в текстовом слое вызывает исключение

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Test";

using (var image = Image.Load(filePath))

{

    var psdImage = image as PsdImage;

    if (image == null)

    {

        return;

    }

    var layers = psdImage.Layers;

    for (var index = layers.Length - 1; index >= 0; index--)

    {

        var layer = layers[index] as TextLayer;

        if (layer == null)

        {

            continue;

        }

        layer.UpdateText(newText);

    }

    var imageOptions = new PsdOptions(psdImage);

    psdImage.Save(outputPath, imageOptions);

}

{{< /highlight >}}

**PSDNET-182. Сохранение изображения PSD после операции RotateFlip создает поврежденный файл, который нельзя открыть.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Должно быть выполнено без исключений

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Ничего не делать

}

{{< /highlight >}}

**PSDNET-539. Исключение: Ошибка загрузки изображения при загрузке изображения с пустыми именами Unicode Alpha Names Resource**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Здесь не должно возникать исключений

{

    // Ничего не делать

}

{{< /highlight >}}

**PSDNET-541. Неверный вывод после изменения видимости LayerGroup**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// внесение изменений в имена слоев и сохранение

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Выключить все внутри группы

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Исключение при загрузке изображения PSD: Раздел цвета (DropShadow Resource) должен содержать 3 цветовых компонента для RGB или 4 цветовых компонента для CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Здесь не должно возникать исключений

{

    // Ничего не делать

}

{{< /highlight >}}

**PSDNET-536. Исключение при попытке рисования на новом созданном слое, если используется простая версия конструктора**

{{< highlight java >}}

 string outputFile = "output.psd";

int width = 100;

int height = 100;

using (var image = new PsdImage(width, height))

{

    var layer = new Layer();

    layer.Bottom = height;

    layer.Right = width;

    image.AddLayer(layer);

    Graphics graphic = new Graphics(layer);

    graphic.Clear(Color.Yellow);

    // нарисовать прямоугольник с помощью инструмента Pen

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // нарисовать еще один прямоугольник с Solid Brush с синим цветом

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
