---
title: כתבות שחרור ל-Aspose.PSD עבור .NET 20.3
type: מסמכים
weight: 100
url: /he/net/aspose-psd-for-net-20-3-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל כתבות שחרור עבור [Aspose.PSD עבור .NET 20.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Key**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-188|תמיכה ב-.Net Core|תכונה|
|PSDNET-523|המרת קבצי Adobe Illustrator ל- PDF|תכונה|
|PSDNET-212|הוספת יכולת לעיצוב סגנונות שונים בשכבת טקסט אחת|תכונה|
|PSDNET-144|תמיכה בשכבת התאמת שחור ולבן|תכונה|
|PSDNET-233|הוספת תמיכה ביצוא תבנית AI (גרסה 8) לתבניות אחרות|תכונה|
|PSDNET-540|תמיכה בעיבוד מצב ערבוב חלף (שמשמש לקבוצת שכבות בלבד)|תכונה|
|PSDNET-539|חריגה: נכשלה טעינת תמונה בעת טעינת תמונה עם שמות אלפא יוניקוד ריקים|באג|
|PSDNET-541|פלט שגוי לאחר שינוי רואיות של קבוצת שכבות|באג|
|PSDNET-516|חריגה בטעינת תמונת PSD: המיכל הצבע (משאבת הצל) חייב להכיל 3 רכיבי צבע ל-RGB או 4 רכיבי צבע ל-CMYK|באג|
|PSDNET-536|חריגה אם ישנסה לצייר על שכבה שנוצרה חדשה אם נעשה שימוש בגרסת קונסטרוקטור הפשוטה|באג|

## **שינויים ב-API הציבוריים**
# **APIים שנוספו:**
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
# **APIים שהוסרו:**
- אף אחד

## **דוגמאות שימוש:**
**PSDNET-523. המרת קבצי Adobe Illustrator ל-PDF**

{{< highlight java >}}

 string sourceFile = "rect2_color.ai";

using (var aiImage = (AiImage)Image.Load(sourceFile))

{

    aiImage.Save("rect2_color.ai_output.pdf", new PdfOptions());

}

{{< /highlight >}}

**PSDNET-212. הוספת יכולת לעיצוב סגנונות שונים בשכבת טקסט אחת**

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

**PSDNET-233. הוספת תמיכה ביצוא תבנית AI (גרסה 8) לתבניות אחרות**

{{< highlight java >}}

 // דוגמא לייצוא קובץ AI לתבניות PSD ו-PNG

string sourceFileName = "form_8.ai";

string outputFileName = "form_8_export";

using (AiImage image = (AiImage)Image.Load(sourceFileName))

{

    image.Save(outputFileName + ".psd", new PsdOptions());

    image.Save(outputFileName + ".png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**PSDNET-540. תמיכה בעיבוד מצב ערבוב חלף (שמשמש לקבוצת שכבות בלבד).**

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

    AssertIsTrue(image.Layers.Length >= 23, "אין 23 שכבה.");

    var layer = image.Layers[23] as LayerGroup;

    AssertIsTrue(layer != null, "השכבה ה-23 אינה קבוצת שכבות.");

    AssertIsTrue(layer.Name == "AdjustmentGroup", "שם השכבה ה-23 הוא לא 'AdjustmentGroup'.");

    AssertIsTrue(layer.BlendModeKey == BlendMode.PassThrough, "שכבת קבוצת ההתאמה צריכה להיות בעלת מצב ערבוב 'עבור'."); 

    image.Save(outputFileName, new PsdOptions());

    image.Save("OutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

    layer.BlendModeKey = BlendMode.Normal;

    image.Save("Normal" + outputFileName, new PsdOptions());

    image.Save("NormalOutputApple.png", new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

}

{{< /highlight >}}

**SPSDNET-180. עדכון טקסט בשכבת טקסט גורם לחריגה**

{{< highlight java >}}

 // עדכון טקסט בשכבת טקסט גורם לחריגה

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

**PSDNET-182. שמירת תמונת PSD לאחר פעולת RotateFlip יוצרת קובץ פגום שלא ניתן לפתוח.**

{{< highlight java >}}

 string sourceFileName = "1.psd";

RotateFlipType flipType = RotateFlipType.Rotate270FlipXY;

string outFileNamePsd = "RotateFlipTest2617.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName))

{

    image.RotateFlip(flipType);

    image.Save(outFileNamePsd);

}

// אמור להתבצע בלי חריגות

using (PsdImage image = (PsdImage)Image.Load(outFileNamePsd)) 

{

    // Do nothing

}

{{< /highlight >}}

**PSDNET-539. חריגה: נכשלה טעינת תמונה בעת טעינת תמונה עם שמות אלפא יוניקוד ריקים**

{{< highlight java >}}

 string sourcePath = "apple.psd";

using (var psdImage = (PsdImage)Image.Load(sourcePath)) // כאן לא צריך לקבל חריגות

{

    // do nothing

}

{{< /highlight >}}

**PSDNET-541. פלט שגוי לאחר שינוי רואיות של קבוצת שכבות**

{{< highlight java >}}

 string sourceFile = "input.psd";

string outputFile = "output.psd";

// לבצע שינויים בשמות השכבות ולשמור אותן

using (var image = (PsdImage)Image.Load(sourceFile))

{

    for (int i = 0; i < image.Layers.Length; i++)

    {

        var layer = image.Layers[i];

        // לכבות הכל בתוך קבוצה

        if (layer is LayerGroup)

        {

            layer.IsVisible = false;

        }

    }

    image.Save(outputFile);

}

{{< /highlight >}}

**PSDNET-516. חריגה בטעינת תמונת PSD: המיכל הצבע (משאבת צל) חייב להכיל 3 רכיבי צבע ל-RGB או 4 רכיבי צבע ל-CMYK**

{{< highlight java >}}

 string sourceFile = "sss0136=GUID-SSS0136=1=ar-sa=Low.psd";

using (var img = (PsdImage)Image.Load(sourceFile)) // כאן לא צריך לקבל חריגות

{

    // לא לעשות כלום

}

{{< /highlight >}}

**PSDNET-536. חריגה אם ישנסה לשרטט על שכבה שנוצרה חדשה אם נעשה שימוש בגרסת קונסטרוקטור הפשוטה**

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

    // משרטט מלבן עם כלי Pen

    graphic.DrawRectangle(new Pen(Color.Red), new Rectangle(30, 10, 40, 80));

    // משרטט מלבן נוסף עם מברשת סולידית בצבע כחול

    graphic.DrawRectangle(new Pen(new SolidBrush(Color.Blue)), new Rectangle(10, 30, 80, 40));

    image.Save(outputFile);

}

{{< /highlight >}}

