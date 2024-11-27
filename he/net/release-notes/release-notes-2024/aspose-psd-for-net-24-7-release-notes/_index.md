---
title: התכנית Aspose.PSD עבור .NET 24.7 - הערות לשחרור
type: docs
weight: 60
url: /he/net/aspose-psd-for-net-24-7-release-notes/
---

{{% alert color="primary" %}}

עמוד זה מכיל את הערות השחרור עבור [Aspose.PSD עבור .NET 24.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**   | **תקציר**                                                                                         | **קטגוריה** |
|:------------|:-------------------------------------------------------------------------------------------------|:-------------|
| PSDNET-1029 | חריגה "טעינת תמונה נכשלה." כאשר נפתח מסמך AI                                        | באג      |
| PSDNET-2022 | טקסט מוצג באופן שגוי בקבצי PDF המוצאים                                                | באג      |
| PSDNET-2061 | תיקון ImageSaveException: ייצוא התמונה נכשל עבור הקובץ שצוין בלינוקס                  | באג      |
| PSDNET-2080 | תיקון טעינת גופנים בעת השימוש ב-Aspose.Drawing                                           | באג      |
| PSDNET-2085 | 'פעולה חשבונית גרמה להתמקמות חריגה' בעת יצירת שכבת אובייקט חכם ב-JPEG גדול        | באג      |
| PSDNET-2100 | הקובץ AI לא יכול להיות ממומר לקובץ JPG                                                | באג      |

## **שינויים בAPI הציבורי**

# **APIs המוסיפים:**
- לא

# **APIs המסרבים:**
- לא

## **דוגמאות שימוש:**

**PSDNET-1029. חריגת "טעינת תמונה נכשלה." כאשר נפתח מסמך AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "[SA]_ID_card_template.ai");
string outputFile = Path.Combine(outputFolder, "[SA]_ID_card_template.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-2022. טקסט מוצג באופן שגוי בקבצי PDF המוצאים**

{{< highlight csharp >}}
string src = Path.Combine(baseFolder, "CVFlor.psd");
string output = Path.Combine(outputFolder, "output.pdf");

using (var psdImage = (PsdImage)Image.Load(src))
{
    PdfOptions saveOptions = new PdfOptions();
    saveOptions.PdfCoreOptions = new PdfCoreOptions();

    psdImage.Save(output, saveOptions);
}
{{< /highlight >}}

**PSDNET-2061. תיקון ImageSaveException: ייצוא תמונה נכשל עבור הקובץ שצוין בלינוקס**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "Bed_Roll-Sticker4_1.psd");
string outputFile = Path.Combine(outputFolder, "output.jpg");

using (var psdImage = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions() { LoadEffectsResource = true }))
{
    var saveOptions = new JpegOptions() { Quality = 70 };
    psdImage.Save(outputFile, saveOptions);
}
{{< /highlight >}}

**PSDNET-2080. תיקון טעינת גופנים בעת השימוש ב-Aspose.Drawing**

{{< highlight csharp >}}
using (var installedFonts = new System.Drawing.Text.InstalledFontCollection())
{
    Console.WriteLine("- לפני העדכון. סופרת הפונטים המותקנים: " + installedFonts.Families.Length);
    Console.WriteLine("- פלטפורמה: " + Environment.OSVersion.Platform.ToString());
    Console.WriteLine("-ריענון מטמון הפונטים באמצעות ניסיון לקבל את השם של הפונט של Adobe עבור 'Arial': "
    FontSettings.GetAdobeFontName("Arial"));

    Console.WriteLine("- לאחר העדכון. סופרת הפונטים המותקנים: " + installedFonts.Families.Length);

    Assert.Greater(installedFonts.Families.Length, 1);
}
{{< /highlight >}}

**PSDNET-2085. 'פעולה חשבונית גרמה להתמקמות חריגה' בעת יצירת שכבת אובייקט חכם ב-JPEG גדול**

{{< highlight csharp >}}
string srcFile = Path.Combine(baseFolder, "source.psd");
string imageJpg = Path.Combine(baseFolder, "test.jpg");

using (var image = (PsdImage)Image.Load(srcFile, new PsdLoadOptions { DataRecoveryMode = DataRecoveryMode.MaximalRecover }))
{
    using (var stream = new FileStream(imageJpg, FileMode.Open))
    {
        var addedLayer = new SmartObjectLayer(stream);
        addedLayer.Name = "Test Layer";
        image.AddLayer(addedLayer);
    }
}
{{< /highlight >}}

**PSDNET-2100. הקובץ AI לא יכול להיות ממומר לקובץ JPG**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "aaa.ai");
string outputFile = Path.Combine(outputFolder, "aaa.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFile, new PngOptions());
}
{{< /highlight >}}
