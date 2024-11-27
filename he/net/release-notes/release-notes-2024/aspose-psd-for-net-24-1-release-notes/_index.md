---
title: Aspose.PSD עבור .NET 24.1 - הערות גרסה
type: docs
weight: 120
url: /he/net/aspose-psd-for-net-24-1-release-notes/
---

{{% alert color="primary" %}}

דף זה מכיל הערות גרסה עבור [Aspose.PSD עבור .NET 24.1](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                                                                      | **קטגוריה** |
|:------------|:--------------------------------------------------------------------------------------------------|:------------|
| PSDNET-1835 | [פורמט AI] הוספת טיפול בסיסי לתמונות AI מרובות עמודים                                        |   תכונה    |
| PSDNET-718  | אפקט הכוונון של טקסט אינו מיושם על הטקסט                                               |     באג      |
| PSDNET-1620 | תצורה שגויה של מסכה בקובץ ספציפי                                                        |     באג      |
| PSDNET-1855 | NullReferenceException ב- Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor |     באג      |
| PSDNET-1883 | [פורמט AI] תיקון של תפעול הזיכרון ב- AiExporterUtils                                        |     באג      |



## **שינויים ב- API הציבוריים**
# **APIs שהוספו:**
- P: Aspose.PSD.FileFormats.Ai.AiImage.ActivePageIndex

# **APIs שהוסרו:**
- לא

## **דוגמאות שימוש:**

**PSDNET-718. אפקט הכוונון של טקסט אינו מיושם על הטקסט**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "text_warp.psd");
string outputFile = Path.Combine(outputFolder, "export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
    AllowWarpRepaint = true
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile, opt))
{
    img.Save(outputFile, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha });
}
{{< /highlight >}}

**PSDNET-1620. תצורה שגויה של מסכה בקובץ ספציפי**

{{< highlight csharp >}}
string sourceFile1 = Path.Combine(baseFolder, "mask_problem.psd");
string sourceFile2 = Path.Combine(baseFolder, "puh_softLight3_1.psd");
string outputFile1 = Path.Combine(outputFolder, "mask_export.png");
string outputFile2 = Path.Combine(outputFolder, "puh_export.png");

var opt = new PsdLoadOptions()
{
    LoadEffectsResource = true,
};

using (PsdImage img = (PsdImage)Image.Load(sourceFile1, opt))
{
    img.Save(outputFile1, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;                
}

using (PsdImage img = (PsdImage)Image.Load(sourceFile2, opt))
{
    img.Save(outputFile2, new PngOptions() { CompressionLevel = 9, ColorType = PngColorType.TruecolorWithAlpha }); ;
}
{{< /highlight >}}

**PSDNET-1835. [פורמט AI] הוספת טיפול בסיסי לתמונות AI מרובות עמודים**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

// טוען את התמונה AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // כברירת מחדל, ה- ActivePageIndex הוא 0.
    // אז אם תשמור את תמונת ה- AI מבלי לשנות מאפיין זה, הדף הראשון ייתגלה ויתורגם.
    image.Save(firstPageOutputPng, new PngOptions());

    // שינוי ב- ActivePageIndex לדף השני.
    image.ActivePageIndex = 1;

    // שמור את הדף השני של התמונת AI כתמונת PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // שינוי ב- ActivePageIndex לדף השלישי.
    image.ActivePageIndex = 2;

    // שמור את הדף השלישי של התמונת AI כתמונת PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1855. NullReferenceException ב- Aspose.PSD.FontParsing.OpenType.Serialization.OpenTypeFontInfo..ctor**

{{< highlight csharp >}}
string fontsFolder = Path.Combine(baseFolder, "Fonts");
FontSettings.SetFontsFolders(new string[] { fontsFolder }, true);

string inputFile = Path.Combine(baseFolder, "1.psd");
string outputFile = Path.Combine(outputFolder, "out_1855.png");
using (var psdImage = (PsdImage)Image.Load(inputFile))
{
    psdImage.Save(outputFile, new PngOptions());
}
{{< /highlight >}}

**PSDNET-1883. [פורמט AI] תיקון של תפעול הזיכרון ב- AiExporterUtils**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "threePages.ai");
string firstPageOutputPng = Path.Combine(outputFolder, "firstPageOutput.png");
string secondPageOutputPng = Path.Combine(outputFolder, "secondPageOutput.png");
string thirdPageOutputPng = Path.Combine(outputFolder, "thirdPageOutput.png");

const double MemoryLimit = 220;
double memoryUsed = double.MaxValue;

// טוען את התמונה AI.
using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    // שמור את הדף הראשון של התמונת AI כתמונת PNG.
    image.Save(firstPageOutputPng, new PngOptions());

    // שינוי ב- ActivePageIndex לדף השני.
    image.ActivePageIndex = 1;

    // שמור את הדף השני של התמונת AI כתמונת PNG.
    image.Save(secondPageOutputPng, new PngOptions());

    // שינוי ב- ActivePageIndex לדף השלישי.
    image.ActivePageIndex = 2;

    // שמור את הדף השלישי של התמונת AI כתמונת PNG.
    image.Save(thirdPageOutputPng, new PngOptions());
}

GC.Collect();

memoryUsed = (GC.GetTotalMemory(false) / 1024.0) / 1024.0;

if (memoryUsed > MemoryLimit)
{
    throw new Exception("שימוש בזיכרון גדול מדי. " + memoryUsed + " במקום " + MemoryLimit.ToString("F1"));
}
{{< /highlight >}}
