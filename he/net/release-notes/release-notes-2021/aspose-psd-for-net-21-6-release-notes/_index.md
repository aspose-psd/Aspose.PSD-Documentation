---
title: Aspose.PSD עבור .NET 21.6 - יומן השחרורים
type: מדריכים
weight: 70
url: /he/net/aspose-psd-for-net-21-6-release-notes/
---

{{% alert color="primary" %}} 

דף זה מכיל את יומן השחרורים עבור [Aspose.PSD עבור .NET 21.6](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDNET-546|מסכת קיצור עבור קבוצה לא נצפית כראוי|באג|
|PSDNET-547|מסכת רגילה או וקטורית עבור קבוצת שכבות מתעלמת בתהליכי עיבוד|באג|
|PSDNET-647|תמונת PSD עם מסכות שכבה וקטוריות מנוטרלות בעת שמירה מאפשרת מסכות וקטוריות|באג|
|PSDNET-786|חריגה בעת יצירת שכבת טקסט עם טקסט ארוך יותר מ-255 תווים|באג|
|PSDNET-900|טקסט של שכבת טקסט לא ניתן להצגה ב-Linux|שדרוג|

## **שינויים ב-API הציבוריים**
# **APIs שנוספו:**
- ללא

# **APIs שהוסרו:**
- ללא

## **דוגמאות שימוש:**

**PSDNET-546. מסכת קיצור עבור קבוצה לא נצפית כראוי**

{{< highlight csharp >}}
            string sourceFileName = "AppleClip.psd";
            string outputFileName = "result.png";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName, new PngOptions());
            }
{{< /highlight >}}

**PSDNET-547. מסכת רגילה או מסכת וקטורית עבור קבוצת שכבות מתעלמת בתהליכי עיבוד**

{{< highlight csharp >}}
        string sourceFileName = "Stripes3Mask.psd";
        string outputFileName = "OutputStripes3Mask.png";
        using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
        {
            image.Save(outputFileName, new PngOptions());
        }
{{< /highlight >}}

**PSDNET-647. תמונת PSD עם מסכות שכבה וקטוריות מנוטרלות בעת שמירה מאפשרת מסכות וקטוריות**

{{< highlight csharp >}}
            string sourceFileName = "FourWithMasksVd.psd";
            string outputFileName = "FourWithMasksVdOutput.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFileName))
            {
                image.Save(outputFileName);
            }
{{< /highlight >}}

**PSDNET-786. חריגה בעת יצירת שכבת טקסט עם טקסט ארוך יותר מ-255 תווים**

{{< highlight csharp >}}
            string output = "output.psd";

            using (var image = new PsdImage(100, 100))
            {
                string text = new string('a', 256);
                image.AddTextLayer(text, Rectangle.Empty);

                image.Save(output);
            }
{{< /highlight >}}
