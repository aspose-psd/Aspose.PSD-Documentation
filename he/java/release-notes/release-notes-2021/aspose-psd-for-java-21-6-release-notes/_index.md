---
title: Aspose.PSD עבור Java 21.6 - הערות אחרי גרסה
type: מסמכים
weight: 40
url: /he/java/aspose-psd-for-java-21-6-release-notes/
---

{{% alert color="primary" %}} עמוד זה מכיל את ההערות לגרסה של [Aspose.PSD עבור Java 21.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-21.6/) {{% /alert %}}

| **מפתח** | **סיכום** | **קטגוריה** |
| :- | :- | :- |
| PSDJAVA-351 | מסכת גילוף עבור קבוצה לא מוצגת בצורה נכונה | באג |
| PSDJAVA-352 | מסכה רגילה או וקטורית לקבוצת שכבות מתעלמת בזמן התרגום | באג |
| PSDJAVA-353 | תמונת PSD עם מסכות שכבות וקטוריות מנוטרלות בעת שמירה מאפשרת מסכות וקטוריות | באג |
| PSDJAVA-354 | יוצא חרגות בעת יצירת TextLayer עם טקסט ארוך יותר מ-255 תווים | באג |

# **שינויים ציבוריים ב-API**
# **APIs חדשות:**
- אין

# **APIs שהוסרו:**
- אין

# **דוגמאות שימוש:**

**PSDJAVA-351. מסכת גילוף עבור קבוצה לא מוצגת בצורה נכונה**

{{< highlight java >}}
        String sourceFileName = "AppleClip.psd";
        String outputFileName = "result.png";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-352. מסכה רגילה או וקטורית לקבוצת שכבות מתעלמת בזמן התרגום**

{{< highlight java >}}
        String sourceFileName = "Stripes3Mask.psd";
        String outputFileName = "OutputStripes3Mask.png";

        PsdImage image = (PsdImage)Image.load(sourceFileName);
        try
        {
            image.save(outputFileName, new PngOptions());
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-353. תמונת PSD עם מסכות שכבות וקטוריות מנוטרלות בעת שמירה מאפשרת מסכות וקטוריות**

{{< highlight java >}}
        String sourceFileName = "FourWithMasksVd.psd";
        String outputFileName = "FourWithMasksVdOutput.psd";

        PsdImage image = (PsdImage) Image.load(sourceFileName);
        try
        {
            image.save(outputFileName);
        }finally {
            image.dispose();
        }
{{< /highlight >}}

**PSDJAVA-354. יוצא חרגות בעת יצירת TextLayer עם טקסט ארוך יותר מ-255 תווים**

{{< highlight java >}}
        String output = "output.psd";

        PsdImage image = new PsdImage(100, 100);
        try
        {
            char[] chars = new char[256];
            Arrays.fill(chars, '*');
            String text = new String(chars);
            image.addTextLayer(text, Rectangle.getEmpty());

            image.save(output);
        }finally {
            image.dispose();
        }
{{< /highlight >}}
