---
title: כתבות אחרונות Aspose.PSD עבור .NET 24.3
type: docs
weight: 100
url: /he/net/aspose-psd-for-net-24-3-release-notes/
---

{{% alert צבע="כחול" %}}

דף זה מכיל כתבות אחרונות עבור [Aspose.PSD עבור .NET 24.3](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

| **מפתח**     | **סיכום**                                                          | **קטגוריה** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1914 | [פורמט AI] הפחתת זמן טעינה של תמונות AI מרובות עמודים גדולות         |     שיפור     |
| PSDNET-1905 | הקובץ PSD אחרי המרתו מ-8 ביט ל-16 ביט הפך לא קריא |     באג     |
| PSDNET-1906 | הקובץ PSD אחרי המרתו מ-8 ביט ל-32 ביט הפך לא קריא |     באג     |
| PSDNET-1921 | [פורמט AI] תיקון העברת העקום הקצר בקובץ AI                 |     באג     |

## **שינויים ב-API הציבוריים**
# **APIs חדשים:**
- אין

# **APIs שהוסרו:**
- אין

## **דוגמאות שימוש:**

**PSDNET-1905. הקובץ PSD אחרי המרתו מ-8 ביט ל-16 ביט הפך לא קריא**

{{< highlight csharp >}}
string קובץמקור = Path.Combine(תיקייתבסיס, "test_smart_layer.psd");
string קובץיציאה = Path.Combine(תיקייתפלט, "export.psd");

using (var תמונתPsd8 = (PsdImage)Image.Load(קובץמקור))
{
    var אפשרויותPsd16 = new PsdOptions()
    {
        ChannelBitsCount = 16
    };

    תמונתPsd8.Save(קובץיציאה, אפשרויותPsd16);
}

using (var תמונתPsd16 = (PsdImage)Image.Load(קובץיציאה))
{
    if (תמונתPsd16.GlobalLayerResources[0] is Lr16Resource)
    {
        // הכל בסדר
    }
    else
    {
        throw new Exception("משאב גלובלי שגוי, המשאב הראשון צריך להיות Lr16Resource");
    }
}
{{< /highlight >}}

**PSDNET-1906. הקובץ PSD אחרי המרתו מ-8 ביט ל-32 ביט הפך לא קריא**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "test_smart_layer.psd");
string outputFile = Path.Combine(outputFolder, "export.psd");

using (var psdImage8 = (PsdImage)Image.Load(sourceFile))
{
    var psdOptions32 = new PsdOptions()
    {
        ChannelBitsCount = 32
    };

    psdImage8.Save(outputFile, psdOptions32);
}

using (var psdImage8 = (PsdImage)Image.Load(outputFile))
{
    if (psdImage8.GlobalLayerResources[0] is Lr32Resource)
    {
        // הכל בסדר
    }
    else
    {
        throw new Exception("משאב גלובלי שגוי, המשאב הראשון צריך להיות Lr32Resource");
    }
}
{{< /highlight >}}

**PSDNET-1921. [פורמט AI] תיקון העברת העקום הקצר בקובץ AI**

{{< highlight csharp >}}
string sourceFile = Path.Combine(baseFolder, "shortCurve.ai");
string outputFilePath = Path.Combine(outputFolder, "shortCurve.png");

using (AiImage image = (AiImage)Image.Load(sourceFile))
{
    image.Save(outputFilePath, new PngOptions());
}
{{< /highlight >}}
