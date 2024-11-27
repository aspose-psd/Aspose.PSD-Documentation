---
title: הערות הוצאה לאור ל- Aspose.PSD עבור .NET 22.12
type: docs
weight: 10
url: /he/net/aspose-psd-for-net-22-12-release-notes/
---

{{% alert color="primary" %}}
דף זה מכיל את הערות הוצאה לאור עבור [Aspose.PSD עבור .NET 22.12](https://www.nuget.org/packages/Aspose.PSD/)
{{% /alert %}}

{{% alert color="success" %}}
- בהוצאה לאור זו נתוקן חריג עם ייצוא 16 ביט.
{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1336|הוספת נכס עריכה של פתוח טקסט לממשק ה- IText|תכונה|
|PSDNET-725|הקטנת הקובץ PSD המצויין עם מסכת שכבה גורמת למסכה לא תקינה|תקלה|
|PSDNET-1277|הוספת יכולת לשמור ולטעון מסכה עבור 16 תמונות|תקלה|
|PSDNET-1281|שקיפות לא נכונה בשמירה של תמונת 16 ביט לתמונת 16 או 8 ביט|תקלה|
|PSDNET-1375|תיקון CMYK בצבע 16 ביט|תקלה|


## **שינויים ב- API הציבורי**
# **APIs הנוספים:**
- T:אספוז.PSD.FileFormats.Psd.TextOrientation
- F:אספוז.PSD.FileFormats.Psd.TextOrientation.Horizontal
- F:אספוז.PSD.FileFormats.Psd.TextOrientation.Vertical
- P:אספוז.PSD.FileFormats.Psd.Layers.Text.IText.TextOrientation


# **APIs שהוסרו:**
- אף אחד


## **דוגמאות שימוש:**

**PSDNET-725. הקטנת הקובץ PSD המצויין עם מסכת שכבה גורמת למסכה לא תקינה**

{{< highlight csharp >}}
string sourceFile = "source.psd";
string psdExportPath = "output.psd";
string pngExportPath = "output.png";

// פותח את קובץ ה-PSD מקור
דרך עם (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    למעלה נניח = 4;

    רוחב חדש = תמונה.רוחב * Scale;
    גובה חדש = תמונה.קוטן * Scale;

    // יצירת הקטנה
    תמונה.לשנות_גודל(רוחב חדש, גובה חדש);
    תמונה.שומר(psdExportPath, אפשרויות חדשות.הנפרדויות(תמונה));
}

// פותח קובץ PSD ממוזג
דרך עם (PsdImage image = (PsdImage)Image.Load(psdExportPath))
{
    // משנה ל-PNG
    תמונה.שומר(pngExportPath, אפשרויות PNG());
}
{{< /highlight >}}

**PSDNET-1277. הוספת יכולת לשמור ולטעון מסכה עבור 16 תמונות**

{{< highlight csharp >}}
string source8bitPsdFile = @"input_8bitColor.psd";
string output16bitPsdFile = @"output_16bitColor.psd";

עם (var image = (PsdImage)Image.Load(source8bitPsdFile))
{
    // הגדרות מאפשרות לשמור צבע 16 ביט
    PsdOptions options16 = חדש PsdOptions { מספר בתים ב-Channel = 16, מצב צבע = מצבי.צבע};
    
    // קובץ PSD ישמר עם שקיפות
    תמונה.שומר(output16bitPsdFile, options16);
}
{{< /highlight >}}

**PSDNET-1281. שקיפות לא נכונה בשמירה של תמונת 16 ביט לתמונת 16 או 8 ביט**

{{< highlight csharp >}}
string sourceFile = @"Example_16bit.psd";
string resavedFile = @"Resave_16bit.psd";
string imageFile = @"TotalImage_16bit.png";

// קובץ PSD צבע 16 ביט (עם שקיפות) יפתח וישמר כצבע 16 ביט
עם (var image = (PsdImage)Image.Load(sourceFile))
{
    PsdOptions options16 = חדש PsdOptions() { ChannelBitsCount = 16, מצב צבע = מצבי.צבע רגוע};
    תמונה.שומר(resavedFile, options16);
}

// צבע ופסק לקובץ PSD צבע 16 ביט שנשמר יציג לקובץ PNG עם שקיפות
עם (var image = (PsdImage)Image.Load(resavedFile))
{
    תמונה.שומר(imageFile, חדש PngOptions() { סוג צבע = אספאז.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1336. הוספת נכס עריכה של פתוח טקסט לממשק ה- IText**

{{< highlight csharp >}}
// הקוד הבא מדגים את היכולת לערוך את נכס ה- TextOrientation החדש.
// זה לא משפיע על הצגה כרגע, רק מאפשר לערוך את ערך הנכס.

string src = "1336test.psd";
string output = "out_1336test.psd";

עם (var image = (PsdImage)Image.Load(src))
{
    var textLayer = תמונה.Layers[1] כ- שכבת מלל;
    אם (textLayer.TextData.TextOrientation == TextOrientation.Vertical)
    {
        // קריאה נכונה
    }
    אחרת
    {
        לזרוק חריגה("קריאה שגויה של ערך המאפיין TextOrientation");
    }

    textLayer.TextData.TextOrientation = TextOrientation.Horizontal;
    textLayer.TextData.UpdateLayerData();

    תמונה.שומר(output);
}

עם (var image = (PsdImage)Image.Load(output))
{
    var textLayer = תמונה.Layers[1] כ- שכבת מלל;
    אם (textLayer.TextData.TextOrientation == TextOrientation.Horizontal)
    {
        // קריאה נכונה
    }
    אחרת
    {
        לזרוק חריגה("קריאה שגויה של ערך המאפיין TextOrientation");
    }
}
{{< /highlight >}}

**PSDNET-1375. תיקון CMYK בצבע 16 ביט**

{{< highlight csharp >}}
string srcFile = @"ClippingMaskRegular.psd";
string exportPath = @"export.psd";
string pngExportPath = @"export.png";

// מגדיר אפשרויות המרה
PsdOptions psdOptions = חדש PsdOptions()
{
    מצב צבע = מצבי.Cmyk,
    מספר בתים ב-Channel = 16,
    מספר ערוצים = 5,
    שיטת דחיסה = שיטת דחיסה ציטור
};

// ממיר ושומר
עם (var image = (PsdImage)Image.Load(srcFile))
{
    תמונה.ממיר(psdOptions);
    תמונה.שומר(exportPath);
}

// פותח קובץ המרה ומציג ל-PNG
עם (PsdImage image = (PsdImage)Image.Load(exportPath))
{
    תמונה.שומר(pngExportPath, חדש PngOptions() { סוג צבע = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}
