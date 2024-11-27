---
title: הופקדות Aspose.PSD עבור .NET 24.2 - הערות שחרור
type: docs
weight: 110
url: /he/net/aspose-psd-for-net-24-2-release-notes/
---

{{% התראה צבע="ראשי" %}}

עמוד זה מכיל את ההערות לגרסה של [Aspose.PSD עבור .NET 24.2](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                                  | **קטגוריה** |
|:------------|:-----------------------------------------------------------------------------|:------------|
| PSDNET-1503 | טיפול בפרטי זווית עבור PatternFillSettings                                |   תכונה   |
| PSDNET-1719 | תמיכה בהתאמה אנכית ואופקית לשכבת טקסט                         |     תכונה     |
| PSDNET-1783 | [פורמט AI] מימוש תצוגה תקנית של רקע בפורמט AI מבוסס PDF |     תכונה     |
| PSDNET-1611 | שינוי בפרקן המעקב בשיקוף                                             |     שיפור     |
| PSDNET-1802 | האצת שיקוף                                                                |     שיפור     |
| PSDNET-995  | חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך                         |     תקלה     |
| PSDNET-1491 | תיקון שמירת קבצי psd מכילים דלת לקו                           |     תקלה     |
| PSDNET-1642 | סגנון הטקסט אינו נכון באובייקט חכם כאשר אנו משתמשים ב ReplaceContents    |     תקלה     |
| PSDNET-1884 | [פורמט AI] תיקון תצוגת Cubic Bezier בקובץ AI                        |     תקלה     |

## **שינויי API ציבוריים**
# **APIs נוספים:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs שהוסרו:**
- אין

## **דוגמאות שימוש:**

**PSDNET-1503. טיפול בפרטי זווית עבור PatternFillSettings**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "PatternFillLayerWide_0.psd");
string outputFile = Path.Combine(outputFolder, "PatternFillLayerWide_0_output.psd");

using (PsdImage image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;
    fillSettings.Angle = 70;
    fillLayer.Update();
    image.Save(outputFile, new PsdOptions());
}

using (PsdImage image = (PsdImage)Image.Load(outputFile, new PsdLoadOptions { LoadEffectsResource = true }))
{
    FillLayer fillLayer = (FillLayer)image.Layers[1];
    PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

    Assert.AreEqual(70, fillSettings.Angle);
}
{{< /highlight >}}

**PSDNET-1719. תמיכה בהתאמה אנכית ואופקית לשכבת טקסט**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "1719_src.psd");
string output = Path.Combine(outputFolder, "out_1719.png");

using (var psdImage = (PsdImage)Image.Load(src))
{
    psdImage.Save(output, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1783. [פורמט AI] מימוש תצוגה תקנית של רקע בפורמט AI מבוסס PDF**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "pineapples.ai");
string outputFilePath = Path.Combine(outputFolder, "pineapples.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}

**PSDNET-995. חריגת "טעינת תמונה נכשלה" כאשר נפתח מסמך**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "PRODUCT.ai");
string outputFile1 = Path.Combine(outputFolder, "PRODUCT.png");

using (AiImage image = (AiImage)Image.Load(sourceFile1))
{
    image.Save(outputFile1, new PngOptions());
}

...

using (AiImage image = (AiImage)Image.Load(sourceFile5))
{
    image.Save(outputFile5, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1491. תיקון שמירת קבצי psd מכילים דלת לקו**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "StrokeShapePattern.psd");
string outputFile = Path.Combine(outputFolder, "StrokeShapePattern_output.psd");

Rectangle newPatternBounds = new Rectangle(0, 0, 4, 4);
Guid guid = Guid.NewGuid();
string newPatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";
int[] newPattern = new int[]
{
    Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),
    ...
};

using (PsdImage image = (PsdImage)Image.Load(sourceFile))
{
    ...
}

// בדיקת מידע ששונה.
using (PsdImage image = (PsdImage)Image.Load(outputFile))
{
    ...
}
{{< /highlight >}}

...

