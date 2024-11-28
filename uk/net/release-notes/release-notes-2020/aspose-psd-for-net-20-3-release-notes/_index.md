---
title: Примітки до релізу Aspose.PSD для .NET 20.3
type: docs
weight: 100
url: /uk/net/aspose-psd-dlya-net-20-3-primіtki-do-relіzu/
---

{{% alert color="primary" %}} 

Ця сторінка містить примітки до релізу для [Aspose.PSD для .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Ключ**|**Опис**|**Категорія**|
| :- | :- | :- |
|PSDNET-188|Підтримка .Net Core|Функціонал|
|PSDNET-523|Конвертування файлів Adobe Illustrator в PDF|Функціонал|
|PSDNET-212|Додано можливість рендерингу різних стилів у одному текстовому шарі|Функціонал|
|PSDNET-144|Підтримка корекції чорно-білого рівня|Функціонал|
|PSDNET-233|Додано підтримку експорту формату AI (Версія 8) в інші формати|Функціонал|
|PSDNET-540|Підтримка обробки режиму змішування PassThrough (Використовується лише для груп шарів).|Функціонал|
|PSDNET-539|Виняток: Помилка завантаження зображення при завантаженні зображення із порожніми символьними іменами Unicode Alpha Resource|Помилка|
|PSDNET-541|Некоректний вивід після зміни видимості Групи Шарів|Помилка|
|PSDNET-516|Виняток при завантаженні зображення PSD: Секція кольору (ресурс DropShadow) повинна містити 3 компоненти кольору для RGB або 4 компоненти кольору для CMYK|Помилка|
|PSDNET-536|Виняток, якщо намагаєтесь малювати на відновленому вигляді, якщо використовується проста версія Конструктора|Помилка|

## **Зміни в публічному API**
# **Додано API:**
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
# **Вилучено API:**
- Немає

## **Приклади використання:**
**PSDNET-523. Конвертування файлів Adobe Illustrator в PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. Додавання можливості рендерингу різних стилів в один текстовий шар**

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

**PSDNET-233. Додана підтримка експорту формату AI (Версія 8) в інші формати**

{{< highlight java >}}

 // Приклад експорту AI-файлу в формати PSD та PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. Підтримка обробки режиму змішування PassThrough (Використовується лише для груп шарів).**

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

    AssertIsTrue(image.Layers.Length >= 23, "There is not 23rd layer.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "The 23rd layer is not a layer group.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "The 23rd layer name is not 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "AdjustmentGroup layer should have 'pass through' blend mode.");

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. Оновлення текстового шару в текст викидає виняток**

{{< highlight java >}}

 // Оновлення текстового шару в текст викидає виняток

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

**PSDNET-182. Збереження зображення PSD після операції RotateFlip призводить до пошкодженого файла, який не можна відкрити.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// Повинно бути виконано без винятків

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Нічого не робити

}

{{< /highlight >}}

**PSDNET-539. Виняток: Помилка завантаження зображення при завантаженні зображення із порожніми символьними іменами Unicode Alpha Resource**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // Тут ми не повинні отримати винятки

{

    // нічого не робити

}

{{< /highlight >}}

**PSDNET-541. Некоректний вивід після зміни видимості Групи Шарів**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// робимо зміни в назвах шарів та зберігаємо їх

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // Вимкнути все в середині групи

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. Виняток при завантаженні зображення PSD: Секція кольору (ресурс DropShadow) повинна містити 3 компоненти кольору для RGB або 4 компоненти кольору для CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // Тут ми не повинні отримати винятки

{

    // нічого не робити

}

{{< /highlight >}}

**PSDNET-536. Виняток, якщо намагаєтесь малювати на відновленому вигляді, якщо використовується проста версія Конструктора**

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

    // Намалювати прямокутник за допомогою інструмента Pen

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // Намалювати ще один прямокутник за допомогою Solid Brush у синьому кольорі

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}




