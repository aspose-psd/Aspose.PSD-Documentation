---
title: Aspose.PSD עבור .NET 23.8 - רשימות הוצאה לאור
type: docs
weight: 50
url: /he/net/aspose-psd-for-net-23-8-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל רשימות הוצאה לאור עבור [Aspose.PSD עבור .NET 23.8](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח** | **סיכום** | **קטגוריה** |
|:------------|:-------------------------------------------------------------------------------------------------------------|:--------|
| PSDNET-1566 | הוספת סוג חדש של סדרת השתנות (דגל) | תכונה |
| PSDNET-1621 | הוספת סוגי שינוי חדשים: קשת מעלה, קשת מטה, כדור | תכונה |
| PSDNET-1682 | הישווא שיטה חדשה PsdImage.AddPosterizeAdjustmentLayer להוספת שכבת Posterize חדשה | תכונה |
| PSDNET-913  | אובדן מידע של PSD רק בפתיחה ושמירה | באג     |
| PSDNET-1352 | נכשל בטעינת התמונה | באג     |
| PSDNET-1553 | נכשל בטעינת התמונה: לא ניתן להמיר אובייקט מסוג UnknownStructure לסוג DescriptorStructure | באג     |
| PSDNET-1631 | שינוי בקובץ בספרייה צד שלישי מכשיל את קובץ PSD אך אפשר לפתוח אותו ב-Photoshop | באג     |


## **שינויים ב- API הציבורי**
# **APIs שנוספו:**
- M:Aspose.PSD.FileFormats.Psd.PsdImage.AddPosterizeAdjustmentLayer


# **APIs שהוסרו:**
- אין


## **דוגמאות שימוש:**

**PSDNET-913. אובדן מידע של PSD רק בפתיחה ושמירה**

{{< highlight csharp >}}
string src = "קובץ מקורי.psd";
string outputPsd = "פלט_קובץ מקורי.psd";
string outputPng = "פלט_קובץ מקורי.png";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}


**PSDNET-1352. נכשל בטעינת התמונה**

{{< highlight csharp >}}
string srcFile1 = "בדיקת_טקסט.psd";
string srcFile2 = "אובייקט_חכם.psd";

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile1))
{
}

using (PsdImage psdImage = (PsdImage)Aspose.PSD.Image.Load(srcFile2))
{
}
{{< /highlight >}}


**PSDNET-1553. נכשל בטעינת התמונה: לא ניתן להמיר אובייקט מסוג UnknownStructure לסוג DescriptorStructure**

{{< highlight csharp >}}
using (PsdImage newPsd = (PsdImage)new PsdImage(10, 10))
{
    newPsd.AddLayer(FillLayer.CreateInstance(FillType.Gradient));

    using (var memStream = new MemoryStream(DescriptorStructure.StructureKey + 1000))
    {
        newPsd.Save(memStream);

        memStream.Seek(DescriptorStructure.StructureKey, System.IO.SeekOrigin.Current);
        memStream.Write(new byte[1]);
        memStream.Position = 0;

        using (PsdImage psdImage = (PsdImage)Image.Load(memStream))
        {
            // צריך לטעון בצורה תקינה
        }
    }
}
{{< /highlight >}}


**PSDNET-1631. שינוי בקובץ בספרייה צד שלישי מכשיל את קובץ PSD אך אפשר לפתוח אותו ב-Photoshop**

{{< highlight csharp >}}
string sourceFile = "קובץ_פלט.psd";
string outputFile = "ייצוא.png";

using (PsdImage img = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}


**PSDNET-1566. הוספת סוג חדש של סדרת השתנות (דגל)**

{{< highlight csharp >}}
string sourceFile = "flag_warp.psd";
string outputFile = "ייצוא_דגל.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFile, new PngOptions
    {
        ColorType = PngColorType.TruecolorWithAlpha
    });
}
{{< /highlight >}}


**PSDNET-1621. הוספת סוגי שינוי חדשים: קשת מעלה, קשת מטה, כדור**

{{< highlight csharp >}}
string sourceFileArcUpper = "קשת_מעלה_warp.psd";
string sourceFileArcLower = "קשת_מטה_warp.psd";
string sourceFileBulge =  "בליטה_warp.psd";

string outputFileArcUpper ="ייצוא_קשת_מעלה.png";
string outputFileArcLower = "ייצוא_קשת_מטה.png";
string outputFileBulge = "ייצוא_בליטה.png";

using (var psdImage = (PsdImage)Image.Load(sourceFileArcUpper, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcUpper, new PngOptions {ColorType = PngColorType.TruecolorWithAlpha});
}

using (var psdImage = (PsdImage)Image.Load(sourceFileArcLower, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileArcLower, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}

using (var psdImage = (PsdImage)Image.Load(sourceFileBulge, new PsdLoadOptions() { AllowWarpRepaint = true, LoadEffectsResource = true }))
{
    psdImage.Save(outputFileBulge, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}


**PSDNET-1682. הישווא שיטה חדשה PsdImage.AddPosterizeAdjustmentLayer להוספת שכבת Posterize חדשה**

{{< highlight csharp >}}
string srcFile = "zendeya.psd";
string outFile = "zendeya.psd.out.psd";

using (PsdImage psdImage = (PsdImage)Image.Load(srcFile))
{
    psdImage.AddPosterizeAdjustmentLayer();
    psdImage.Save(outFile);
}

// בדוק שינויים שנשמרו
using (PsdImage image = (PsdImage)Image.Load(
    outFile,
    new PsdLoadOptions { LoadEffectsResource = true }))
{
    AssertAreEqual(2, image.Layers.Length);

    PosterizeLayer posterizeLayer = (PosterizeLayer)image.Layers[1];

    AssertAreEqual(true, posterizeLayer is PosterizeLayer);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "האובייקטים אינם תואמים.");
    }
}
{{< /highlight >}}
