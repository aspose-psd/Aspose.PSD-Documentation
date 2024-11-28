---
title: Aspose.PSD за .NET 20.3 - Бележки към Изданието
type: docs
weight: 100
url: /bg/net/aspose-psd-za-net-20-3-release-notes/
---

{{% alert color="primary" %}}

Тази страница съдържа бележки за изданието на [Aspose.PSD за .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Ключ**|**Резюме**|**Категория**|
| :- | :- | :- |
|PSDNET-188|Поддръжка на .Net Core|Функционалност|
|PSDNET-523|Конвертиране на файлове от Adobe Illustrator в PDF|Функционалност|
|PSDNET-212|Добавяне на възможност за изобразяване на различни стилове в един текстов слой|Функционалност|
|PSDNET-144|Поддръжка на регулиране на черното и бялото в слой за коригиране|Функционалност|
|PSDNET-233|Добавяне на поддръжка на експорт на AI формат (Версия 8) към други формати|Функционалност|
|PSDNET-540|Поддръжка на обработка на режим на смесване PassThrough (Използва се само за Група на слоевете)|Функционалност|
|PSDNET-539|Грешка: Зареждането на изображение е неуспешно при зареждане на изображение с празни Unicode Alpha Names Resource|Проблем|
|PSDNET-541|Некоректен изход след промяна на видимостта на Група на слоевете|Проблем|
|PSDNET-516|Грешка при зареждане на PSD изображение: Секцията за цвят (DropShadow Resource) трябва да съдържа 3 цветови компонента за RGB или 4 цветови компонента за CMYK|Проблем|
|PSDNET-536|Грешка, ако се опитате да рисувате върху вново създаден слой, ако се използва простата версия на конструктора|Проблем|

## **Промени в Общественото API**
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
- Няма

## **Примери за Използване:**
**PSDNET-523. Конвертиране на файлове от Adobe Illustrator в PDF**

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

    ITextPortion[] newPortions = textData.ProducePortions(new string[] { "E=mc",  "2\r",  "Наситен",  "Курсив\r",  "Малкибукви" }, defaultStyle, defaultParagraph);

    newPortions[0].Style.Underline = true; // редакция на стила на текста "E=mc"

    newPortions[1].Style.FontBaseline = FontBaseline.Superscript; // редакция на стила на текста "2\r"

    newPortions[2].Style.FauxBold = true; // редакция на стила на текста "Наситен"

    newPortions[3].Style.FauxItalic = true; // редакция на стила на текста "Курсив\r"

    newPortions[3].Style.BaselineShift = -25; // редакция на стила на текста "Курсив\r"

    newPortions[4].Style.FontCaps = FontCaps.SmallCaps; // редакция на стила на текста "Малкибукви"

    foreach (var newPortion in newPortions)

    {

        textData.AddPortion(newPortion);

    }

    textData.UpdateLayerData();

    img.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-233. Добавяне на поддръжка на експорт на AI формат (Версия 8) към други формати**

{{< highlight java >}}

 // Пример за експортиране на AI файл към PSD и PNG формат

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Поддръжка на обработка на режим на смесване PassThrough (Използва се само за Група на слоевете).**

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

    AssertIsTrue(image.Layers.Length >= 23, "Липсва 23-тият слой.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "23-тият слой не е група на слоевете.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "Името на 23-тият слой не е 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "Слоят на групата за коригиране трябва да има режим на смесване 'pass through'.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Обновяването на текстов слой предизвиква изключение**

{{< highlight java >}}

 // Обновяването на текстов слой предизвиква изключение

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

**PSDNET-182. Запазването на PSD изображение след операцията RotateFlip произвежда повреден файл, който не може да бъде отворен.**

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

**PSDNET-539. Грешка: Зареждането на изображение е неуспешно при зареждане на изображение с празни Unicode Alpha Names Resource**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Тук не бива да получим изключения

{

    // нищо

}

{{< /highlight >}}

**PSDNET-541. Некоректен изход след промяна на видимостта на Група на слоевете**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// направете промени в имената на слоевете и го запазете

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Изключете всичко вътре в група

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Изключение при зареждане на PSD изображение: Секцията за цвят (DropShadow Resource) трябва да съдържа 3 цветови компонента за RGB или 4 цветови компонента за CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Тук не бива да получим изключения

{

    // нищо

}

{{< /highlight >}}

**PSDNET-536. Изключение при опит да се нарисува върху вново създаден слой, ако използвате простата версия на конструктора**

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

    // нарисувайте правоъгълник с инструмента за писалка

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // нарисувайте друг правоъгълник с пълен четка в син цвят

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}
