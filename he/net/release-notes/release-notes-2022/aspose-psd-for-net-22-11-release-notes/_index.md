---
title: Aspose.PSD עבור .NET 22.11 - הערות גרסה
type: docs
weight: 20
url: /he/net/aspose-psd-for-net-22-11-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות גרסה עבור [Aspose.PSD עבור .NET 22.11](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- הגרסה הזו כוללת שיבוש במקרה של יצוא 16 ביטים, לכן אנו ממליצים על הזהירות בשימוש בתכונה זו בגרסה זו. אנא אל תעדכנו את Aspose.PSD לגרסה 22.9-22.11 אם עיבוד תמונות ב-16 ביטים היא הפונקציונליות העיקרית שלכם.

אנו עובדים על פתרונות לבעיות אלו.

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1320|אין אפשרות לייצא קבצי PSB בגודל קיצוני מאוד|שיפור|
|PSDNET-659|שינוי מהמרכז של הצבע הרדיאלי|תכונה|
|PSDNET-1330|שיטת דחיפה ZipWithoutPrediction לא נתמכת עבור קבצים ספציפיים|תכונה|
|PSDNET-735|לאחר שימוש בשיטת טרנספורמציה רק עבור שכבה, השכבה שמורה מבחינת תיבות הגבול הנכונות|באג|
|PSDNET-1234|חריגה בעת טעינת תמונת PSD עם דפוס|באג|
|PSDNET-1244|יצוא תמונה נכשל (IndexOutOfRangeException) בעת שמירת קובץ PSD עם סמלים סיניים|באג|
|PSDNET-1303|TimeLine ActiveFrame מיישם באופן בלתי נכון|באג|
|PSDNET-1307|שיבוש 22.7: תמונה במראה לא נכון של טקסט עם תווים ערביים|באג|
|PSDNET-1321|מסיכה וקטורית על השכבה הקבוצתית פועלת באופן שגוי. התמונה הסופית מכילה את החור השחור אך לא צריך|באג|


## **שינויים ב- API ציבוריים**
# **APIs שנוספו:**
- M:Aspose.PSD.FileFormats.Psd.Layers.TextLayer.Resize(System.Int32,System.Int32,Aspose.PSD.ResizeType)


# **APIs שהוסרו:**
- אף אחד


## **דוגמאות שימוש:**

**PSDNET-659. שינוי מהמרכז של הצבע הרדיאלי**

{{< highlight csharp >}}
string sourceFile = "psdnet659.psd";
string outputFile = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    FillLayer radialLayer = (FillLayer)psdImage.Layers[5];
    GradientFillSettings settings = (GradientFillSettings)radialLayer.FillSettings;

    // עדכון נקודת הצוק
    settings.HorizontalOffset = 10;
    settings.VerticalOffset = -25;

    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-735. לאחר שימוש בשיטת טרנספורמציה רק עבור שכבה, השכבה שמורה מבחינת תיבות הגבול הנכונות**

{{< highlight csharp >}}
string sourceFileName = @"TextLayer.psd";
string outputFile = "TextLayerResized_output.psd";

using (PsdImage image = (PsdImage)Image.Load(sourceFileName, new PsdLoadOptions()))
{
    TextLayer textLayer = (TextLayer)image.Layers[1];

    // מגדיר גודל חדש של שכבת הטקסט
    const int NewWidth = 250;
    const int NewHeight = 250;

    // מגדיר את המנגנון לכיצד יבצע הפונקציה לשינוי גודל השכבה (ערך ברירת מחדל)
    ResizeType resizeType = ResizeType.NearestNeighbourResample;

    // מנגנון חדש לשינוי גודל שכבת טקסט בשימוש כאן
    // לא רק שכבה אלא גם מטריצת הטרנספורמציה של שכבת הטקסט ישתנה
    textLayer.Resize(NewWidth, NewHeight, resizeType);

    image.Save(outputFile, new PsdOptions(image));
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions()))
{
    TextLayer txtLayer = (TextLayer)image.Layers[1];

    // הסיבה לדלתא היא גופן ברירת מחדל שונה
    if (txtLayer.TransformMatrix[4] >= 65 
        && txtLayer.TransformMatrix[4] <= 67
        && txtLayer.TransformMatrix[5] >= 234
        && txtLayer.TransformMatrix[5] <= 237)
    {
        // הכל בסדר
    }
    else
    {
        throw new Exception("נקודת המיקום שגויה");
    }
}
{{< /highlight >}}

**PSDNET-1234. חריגה בעת טעינת תמונת PSD עם דפוס**

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

**PSDNET-1244. ייצוא תמונה נכשל (IndexOutOfRangeException) בעת שמירת קובץ PSD עם סמלים סיניים**

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

    // לא צריך להיות חריגה כאן.
    image.Save(outputPath, new PsdOptions() { CompressionMethod = CompressionMethod.RLE, ColorMode = ColorModes.Rgb });
}
{{< /highlight >}}

**PSDNET-1303. TimeLine ActiveFrame מיישם באופן בלתי נכון**

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

**PSDNET-1307. שיבוש 22.7: תמונה במראה לא נכון של טקסט עם תווים ערביים**

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

**PSDNET-1320. אין אפשרות לייצא קבצי PSB בגודל קיצוני מאוד**

{{< highlight csharp >}}
string sourceFile = "hf-mim-liman-han-guc-art-kuvvet.psb";
string psdExportPath = "hf-mim-liman-han-guc-art-kuvvet.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { ReadOnlyMode = true }))
{
    image.Save(psdExportPath, new PngOptions() { ColorType =  PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1321. מסיכה וקטורית על השכבה הקבוצתית פועלת באופן שגוי. התמונה הסופית מכילה את החור השחור אך לא צריך**

{{< highlight csharp >}}
string srcFile = "demo.psd";
string output = "demo_net.png";

using (PsdImage im = (PsdImage)PsdImage.Load(srcFile))
{
    PngOptions pngOptions = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };
    im.Save(output, pngOptions);
}
{{< /highlight >}}

**PSDNET-1330. שיטת דחיפה ZipWithoutPrediction אינה נתמכת עבור קבצים ספציפיים**

{{< highlight csharp >}}
string sourceFile = "20221017_220706_0000.psd";
string outputFile = "20221017_220706_0000.jpg";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    ImageOptionsBase optionsBase = new JpegOptions() { Quality = 80 };
    image.Save(outputFile, optionsBase);
}
{{< /highlight >}}
