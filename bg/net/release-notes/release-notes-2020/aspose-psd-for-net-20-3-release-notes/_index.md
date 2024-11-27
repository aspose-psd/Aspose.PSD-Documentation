---
title: Aspose.PSD за .NET 20.3 - Бележки за изданието
type: docs
weight: 100
url: /bg/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-188|Поддръжка на .Net Core|Функционалност|
|PSDNET-523|Преобразуване на файлове Adobe Illustrator в PDF формат|Функционалност|
|PSDNET-212|Добавяне на възможност за изобразяване на различни стилове в един текстов слой|Функционалност|
|PSDNET-144|Поддръжка на слой за корекция на черно и бяло|Функционалност|
|PSDNET-233|Добавяне на поддръжка за експорт AI формат (Версия 8) към други формати|Функционалност|
|PSDNET-540|Поддръжка на обработка на режим на смесване (Blending Mode) PassThrough (Използва се само за Група на слоя).|Функционалност|
|PSDNET-539|Изключение: Зареждането на изображение с празни Unicode Alpha имена на ресурс се проваля|Проблем|
|PSDNET-541|Некоректен изход след промяна на видимостта на група слоеве|Проблем|
|PSDNET-516|Изключение при зареждане на PSD изображение: Цветната секция (DropShadow Resource) трябва да съдържа 3 цветни компонента за RGB или 4 цветни компонента за CMYK|Проблем|
|PSDNET-536|Изключение, ако се опитате да рисувате върху новосъздаден слой, ако се използва простата версия на конструктора|Проблем|

## **Промени в публичното API**:
# **Добавени API:**
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
# **Премахнати API:**
- Нито едно

## **Примери за използване:**
**PSDNET-523. Преобразуване на файлове Adobe Illustrator в PDFs**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Добавяне на възможност за изобразяване на различни стилове в един текстов слой**

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

    newPortions[0].Style.Underline = true; // редакция на текстовия стил "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // редакция на текстовия стил "2\r"

    newPortions[2].Style.FauxBold = true; // редакция на текстовия стил "Bold"

    newPortions[3].Style.FauxItalic = true; // редакция на текстовия стил "Italic\r"

    newPortions[3].Style.BaselineShift = -25; // редакция на текстовия стил "Italic\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // редакция на текстовия стил "Lowercasetext"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Добавяне на поддръжка за експорт на AI формат (Версия 8) към други формати**

{{< highlight java >}}

 // Пример за експорт на файл AI към PSD и PNG формат

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Поддръжка на обработка на режим на смесване (Blending Mode) PassThrough (Използва се само за Група на слоя).**

{{< highlight java >}}

 void AssertIsTrue(bool condition, string message)

{

    if (!condition)

    {

        throw new FormatException(message);

    }

}

string sourceFileName = "Ябълка.psd";

string outputFileName = "Output" + sourceFileName;

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    AssertIsTrue(image.Layers.Length >= 23, "Липсва 23-ият слой.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23-ият слой не е група на слоеве.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Името на 23-ият слой не е 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Слоят AdjustmentGroup трябва да има режим на смесване 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputЯбълка.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputЯбълка.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Актуализирането на текстов слой предизвиква изключение**

{{< highlight java >}}

 // Актуализирането на текстов слой текст предизвиква изключение

string filePath = "FlipVertical.psd";

string outputPath = "FlipVertical_changed.psd";

var newText = "Тест";

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

**PSDNET-182. Запазване на PSD изображение след операция RotateFlip произвежда повреден файл, който не може да бъде отворен.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Трябва да се изпълни без изключения

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Нищо

}

{{< /highlight >}}

**PSDNET-539. Изключение: Зареждането на изображение с празни Unicode Alpha имена на ресурс се проваля**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Тук не бива да получим изключения

{

    // Нищо

}

{{< /highlight >}}

**PSDNET-541. Некоректен изход след промяна на видимостта на група слоеве**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// Направете промени в имената на слоевете и го запазва

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Изключване на всичко вътре в група

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Изключение при зареждане на PSD изображение: Цветната секция (DropShadow Resource) трябва да съдържа 3 цветни компонента за RGB или 4 цветни компонента за CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Тук не бива да получим изключения

{

    // Нищо

}

{{< /highlight >}}

**PSDNET-536. Изключение, ако се опитате да рисувате върху новосъздаден слой, ако се използва простата версия на конструктора**

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

    // Нарисувайте правоъгълник с инструмента Pen

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // Нарисувайте друг правоъгълник с Solid Brush в син цвят

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
