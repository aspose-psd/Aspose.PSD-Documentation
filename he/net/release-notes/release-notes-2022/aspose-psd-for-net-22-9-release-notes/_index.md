---
title: Aspose.PSD עבור .NET 22.9 - הערות לגרסה
type: docs
weight: 40
url: /he/net/aspose-psd-for-net-22-9-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל את ההערות לגרסה של [Aspose.PSD עבור .NET 22.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

{{% alert color="warning" %}}

- הגרסה הזאת כוללת חריגות במקרה של ייצואי 16 ביטים, לכן אנו ממליצים על זהי להשתמש בתופס זה בזהירות בגרסה זו.
בבקשה אל תעדכנו את Aspose.PSD לגרסה 22.9 אם עיבוד תמונת 16 ביטים הוא הפונקציה העיקרית שלכם.
- למספר גרסאות של Photoshop, המשתמשים עשויים לנתק חלון עם שגיאה קוראת לשכבת קריאה, מה שלא ישפיע על העבודה עם קובץ ה-PSD.

אנו עובדים על פתרונות לבעיות אלו.

{{% /alert %}}

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-1237|יצירת המודל הפנימי של ליירסטיילFX אשר יכיל אפקטים ונתונים קשורים לשימוש במודל בודד במשאבי אפקטים Lfx2, lmfx, וmlst|שדרוג|
|PSDNET-1227|הוספת קריאה וכתיבה של מבנים 'Lefx' עם מידע על אפקטים למצבי שכבות במודלי ציר הזמן|תכונה|
|PSDNET-1230|החלת מצב שכבה של ציר זמן לשכבת PsdImage|תכונה|
|PSDNET-1072|שקיפות שגויה בשמירת קובץ PSD (RGB/16 ביט) ביצוא ל-8 ביט|באג|
|PSDNET-1140|חריגה בשלב הטעינה של משאבי שכבה גלובליים בפתיחת מסמך PSB|באג|
|PSDNET-1266|שפיכת זיכרון בעיבוד של קבצים ספציפיים|באג|


## **שינויים ב- API הציבוריים**
# **APIs שנוספו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.PositionOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.StateEffects
- T:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.IsVisible
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.Effects
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddDropShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddInnerShadow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddOuterGlow
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddStroke(Aspose.PSD.FileFormats.Psd.Layers.FillSettings.FillType)
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddColorOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddGradientOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.AddPatternOverlay
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.ClearLayerStyle
- M:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerStateEffects.RemoveEffectAt(System.Int32)


# **APIs שהוסרו:**
- P:Aspose.PSD.FileFormats.Psd.Layers.Animation.LayerState.Offset


## **דוגמאות לשימוש:**

**PSDNET-1072. שקיפות שגויה בשמירת קובץ PSD (RGB/16 ביט) ביצוא ל-8 ביט**

{{< highlight csharp >}}
string inputPsdFile    = "8bitWithTransparency.psd";
string outputPsdFile   = "16bitWithTransparency.psd";
string outputImageFile = "OutputWithTransparency.png";

using (var img = Image.Load(inputPsdFile))
{
    // 16 bit save options
    PsdOptions p16 = new PsdOptions() { ChannelBitsCount = 16, ColorMode = ColorModes.Rgb };

    img.Save(outputPsdFile, p16);
}
using (var img = Image.Load(outputPsdFile))
{
    // Save picture with 16 bit colors
    img.Save(outputImageFile, new PngOptions() { ColorType = Aspose.PSD.FileFormats.Png.PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1140. חריגה בשלב הטעינה של משאבי שכבה גלובליים בפתיחת מסמך PSB**

{{< highlight csharp >}}
string sourcePsdFile = "input.psb";
string outputImageFile = "output.png";

using (var image = (PsdImage)Image.Load(sourcePsdFile))
{
    // לא יתרחש חריגה כאן.
    image.Save(outputImageFile, new PngOptions() { ColorType = PngColorType.GrayscaleWithAlpha });
}
{{< /highlight >}}

**PSDNET-1227. הוספת קריאה וכתיבה של מבנים 'Lefx' עם מידע על אפקטים למצבי שכבות במודלי ציר הזמן**

{{< highlight csharp >}}
string sourceFile = "4_animated.psd";
string outputFile = "output.psd";

using (var psdImage = (PsdImage)Image.Load(sourceFile))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    int[] layerIds = timeLine.LayerIds;

    var layerStateEffects11 = timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects;

    layerStateEffects11.AddDropShadow();
    layerStateEffects11.AddGradientOverlay();

    var layerStateEffects21 = timeLine.Frames[2].LayerStates[layerIds[1]].StateEffects;
    layerStateEffects21.AddStroke(FillType.Color);
    layerStateEffects21.IsVisible = false;

    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputFile);
}
{{< /highlight >}}

**PSDNET-1230. החלת מצב שכבה של ציר זמן לשכבת PsdImage**

{{< highlight csharp >}}
string sourceFile = "3_animated.psd";
string outputPsd = "output.psd";
string outputPng = "output.png";

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    TimeLine timeLine = TimeLine.InitializeFrom(psdImage);
    var layerIds = timeLine.LayerIds;

    var layerState11 = timeLine.Frames[1].LayerStates[layerIds[1]];

    timeLine.Frames[1].LayerStates[layerIds[1]].StateEffects.AddPatternOverlay();
    layerState11.BlendMode = BlendMode.Multiply;

    // שינוי מסגרת פעילה מ-0 ל-1 כדי להפעיל את החלקת LayerState לשכבה
    timeLine.ActiveFrame = 1;

    // להחיל את השינויים על PsdImage
    timeLine.ApplyTo(psdImage);

    psdImage.Save(outputPsd);
    psdImage.Save(outputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1266. שפיכת זיכרון בעיבוד של קבצים ספציפיים**

{{< highlight csharp >}}
string[] filesToLoad = new string[] { "testPsd0.psd", "testPsd1.psd", "testPsd2.psd" };
int inputNumber = GC.MaxGeneration;

#if NETCOREAPP
GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
GC.Collect(inputNumber, GCCollectionMode.Forced);
GC.WaitForFullGCComplete();

double memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("סה\"כ בתים שנמצאו לפני הבדיקה: {0:N2} MiB", memCount);

double max = memCount;

for (int i = 0; i < 50; i++)
{
    int fileIndex = i % inputNumber;
    string sourceFile = Path.Combine(baseFolder, filesToLoad[fileIndex]);

    // בדיקת פתיחה ושמירה
    using (MemoryStream outputStream = new MemoryStream())
    {
        using (PsdImage psd = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
        {
            psd.Save(outputStream, new JpegOptions() { Quality = 100 });
        }
    }

#if NETCOREAPP
    GCSettings.LargeObjectHeapCompactionMode = GCLargeObjectHeapCompactionMode.CompactOnce;
#endif
    GC.Collect(inputNumber, GCCollectionMode.Forced);
    GC.WaitForFullGCComplete();

    memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
    max = Math.Max(max, memCount);
}

memCount = (double)Process.GetCurrentProcess().PrivateMemorySize64 / 1024 / 1024;
Console.WriteLine("סה\"כ בתים שנמצאו אחרי הבדיקה: {0:N2} MiB", memCount);
Assert.IsTrue(Math.Abs(memCount - max) < 20, "זיכרון שווה בפונקציות בסיסיות מצוין!");
{{< /highlight >}}
