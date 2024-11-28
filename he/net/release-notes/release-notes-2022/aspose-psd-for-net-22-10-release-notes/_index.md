---
title: הערות שחרור Aspose.PSD עבור .NET 22.10
type: מסמכים
weight: 30
url: /he/net/aspose-psd-for-net-22-10-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לשחרור עבור [Aspose.PSD עבור .NET 22.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- בשחרור זה קיימת חוסר ביצוב במקרה של יצוא ב-16 ביטים, לכן אנו ממליצים להקפיד בשימוש בתכונה זו בשחרור זה.
אנא אל תעדכן את Aspose.PSD לגרסה 22.9-22.10 אם עיבוד תמונות ב-16 ביטים הוא הפונקציונליות העיקרית שלך.

אנו עובדים על פתרון לבעיות אלו.

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1287|הסרת מאפיינים מיושנים ב-Lfx2Resource|שיפור|
|PSDNET-1071|Aspose.PSD לא יכולה לפתוח קובץ PSD (RGB/16 ביט) עם דחיפה בלתי צפויה של Zip|שגיאה|
|PSDNET-1257|אפקטים בציר הזמן נעלמים ומוצגים בדרך מוזרה. (בפוטושופ)|שגיאה|
|PSDNET-1278|שקיפות לא עובדת עבור אפקט הקו עם מיקום בתוך|שגיאה|
|PSDNET-1279|חיזוק: שגיאה בפתיחת קובץ PSD|שגיאה|
|PSDNET-1284|עדכון הטקסט נכשל עם סמלים אסיאטיים מסוימים. שגיאה בפענוח סמל מסוים|שגיאה|
|PSDNET-1291|עדכון הטקסט נכשל עם סמלים אסיאטיים מסוימים. שגיאה בעיבוד סמל מסוים|שגיאה|
|PSDNET-1292|שגיאה בפתיחת הקובץ שיצא ב-Photoshop לאחר שמירת סמלים אסיאטיים מסוימים|שגיאה|


## **שינויים ב-API הציבורי**
# **API שנוספו:**
- אין

# **API שהוסרו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Data
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.BlendMode
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.EffectColor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resource.Opacity


## **דוגמאות לשימוש:**

**PSDNET-1071. Aspose.PSD לא יכולה לפתוח קובץ PSD (RGB/16 ביט) עם דחיפה בלתי צפויה של Zip**

{{< highlight csharp >}}
string src = "237708.psd";
string output = "out_237708.psd";

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1257. אפקטים בציר הזמן נעלמים ומוצגים בדרך מוזרה. (בפוטושופ)**

{{< highlight csharp >}}
string sourceFile = "clearFile.psd";
string outputFile = "output_not_clearFile.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    // יצירת ציר זמן עם מספר מסגרות.
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    List<Frame> frames = new List<Frame>(timeLine.Frames);
    for (int i = 0; i < 3; i++)
    {
        frames.Add(new Frame(timeLine));
    }
    timeLine.Frames = frames.ToArray();

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddColorOverlay();

    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.AddGradientOverlay();
    timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1278. שקיפות לא עובדת עבור אפקט הקו עם מיקום בתוך**

{{< highlight csharp >}}
string sourceFile = "psdnet1278.psd";
string output = "out_1278.png";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    image.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1279. חיזוק: שגיאה בפתיחת קובץ PSD**

{{< highlight csharp >}}
string sourceFile = "AllTypesLayerPsd.psd";
string outputPsd = "out_1279.psd";

using (var image = (PsdImage) Image.Load(sourceFile))
{
    image.Save(outputPsd);
}
{{< /highlight >}}

**PSDNET-1284. עדכון הטקסט נכשל עם סימנים אסיאטיים מסוימים. שגיאה בפענוח סמל מסוים**

{{< highlight csharp >}}
string testData = @"尐少尒尓尔ן‬ה‫רם‬ד‫וד‫ק‬‫‪‬כ‬‬ י‬‬ פףק‫‬‪‫א‬‬בםם";

testData = testData.Substring(25, 1); // בחירת הסמל הבעייתי

string srcFile = "TestFileForAsianCharsBig.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1287. הסרת מאפיינים מיושנים ב-Lfx2Resource**

{{< highlight csharp >}}
string src = "fileWithEffects.psd";
string output = "output.psd";

using (var psdImage = (PsdImage)Image.Load(src, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var layer = psdImage.Layers[1];
    var effect = layer.BlendingOptions.Effects[0];

    // עדכון בחירת מצב מעבדה ביצורי אפקט
    effect.BlendMode = BlendMode.Darken;

    // עדכון בחירת שקפיות באפקט הקו
    effect.Opacity = 128; // 50%

    // עדכון בחירת צבע מילוי לאפקט הקו
    var strokeSettings = (IColorFillSettings)((StrokeEffect)effect).FillSettings;
    strokeSettings.Color = Color.DarkRed;

    psdImage.Save(output);
}
{{< /highlight >}}

**PSDNET-1291. עדכון הטקסט נכשל עם סימנים אסיאטיים מסוימים. שגיאה בעיבוד סימן מסוים**

{{< highlight csharp >}}
string testData = @"דרכהזעהתויוכובובאכל";

testData = testData.Substring(40, 25); // בחירת הסמלים הבעייתיים

string srcFile = "TestFileForAsianCharsBig 2.psd";
string output = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);
    image.Save(output);
}
{{< /highlight >}}

**PSDNET-1292. שגיאה בפתיחת הקובץ שיצא ב-Photoshop לאחר שמירת סמנים אסיאטיים מסוימים**

{{< highlight csharp >}}
string testData = @"9593י דבילרואבן‬ה‬‫רא‪‬בללנםכ‫וכל‬‫אח‬‮‬ו‪אכללפ‪רלחן‪ראללאלל‮‬י אלל‫פלדלחטרצרני‮ל‪לר‮דנלרפכ לנת‫הנחפרארלמאדפןפ‮דמ‫ףנחל‮מ‫ראך־‏ל‬‪הארז‏ל‬ךׂ‏ל";

string srcFile = "TestFileForAsianCharsBig 2.psd";
string outFile = "output.psd";

using (var image = (PsdImage)Image.Load(srcFile))
{
    var layer = (TextLayer)image.Layers[0];
    layer.UpdateText(testData);

    image.Save(outFile);
}
{{< /highlight >}}
