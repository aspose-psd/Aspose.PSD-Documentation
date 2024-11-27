---
title: הופעות בהוצאת Aspose.PSD ל- CLI NLP עבור .NET 24.6 - הודעות השחרור
type: מסמכים
weight: 90
url: /he/net/cli/nlp-editor/aspose-psd-nlp-editor-cli-app-for-net-24-6-release-notes/
---
{{% alert color="primary" %}}

דף זה מכיל את ההודעות השחרור עבור [Aspose.PSD CLI NLP Editor for .NET 24.6](https://www.nuget.org/packages/Aspose.PSD.CLI.NLP.Editor/)

{{% /alert %}}

| **מפתח**    | **סיכום**                                                                                      | **קטגוריה** |
|:------------|:------------------------------------------------------------------------------------------------|:--------------|
| PSDNET-2110 | הוצאה ראשונית של אפליקציות Aspose.PSD CLI: Aspose.PSD.CLI.Export ו-Aspose.PSD.CLI.NLP.Editor | שיפור        |


## **דוגמאות שימוש:**

**PSDNET-2110. הוצאה ראשונית של אפליקצית Aspose.PSD CLI NLP Editor**

## **שימוש באמצעות שורת פקודה:**

{{% alert color="primary" %}}
ראשית, התקן את כלי ה- dotnet הזה:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

אנו ממליצים להריץ את הפקודה הבאה לפני השימוש הראשון:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
לאחר הפקודה הזו, תהיה מסוגל להריץ את האפליקציה הזו עם השם הקצר nlp.cli במקום Aspose.PSD.CLI.NLP.Editor. תוכל לציין שם קצר משלך.
{{% /alert %}}

**דוגמאות לשימוש**

1. פקודה זו תמיר את הקובץ הראשון שנמצא (שניתן לפתיחה עם aspose.psd) מתיקית הנוכחית ותשמור אותו כקובץ png עם שקיפות. גם, הרישוי יתקין. עליך לציין רישוי רק פעם אחת. הפעלות נוספות ישתמשו בה נגזרת מהנתיב שצוין. פקודה זו תציג יומן מפורט של עיבוד NLP אם הוא זמין.
{{< highlight bash >}}nlp.cli Convert file from this folder to png format with alpha --license "C:\Aspose\LicenseFile.lic --verbose "{{< /highlight >}}

2. פקודה זו תמצא את הקובץ עם השם הכי דומה ל-"smth.psd". לאחר מכן תכוין את הניגודיות ותשמור את הקובץ כ-jpeg עם האיכות הטובה ביותר. שם הקובץ המחולק יודפס. זה יהיה smth.jpg
{{< highlight bash >}}Adjust contrast on 10 of layer with name ellipse in file smth.psd and save it to output.jpg with best quality{{< /highlight >}}

3. פקודה זו תטפטף את הקובץ בנתיב המוגדר, ותהפיס את גודלו ל-25%. הקובץ המוחזק יודפס. יישמר בתיקיית הנוכחית של המסוף.
{{< highlight bash >}}Resize file C:\Users\someuser\Desktop\input.psd to 25%{{< /highlight >}}

4. פקודה זו תמצא את הקובץ input.psd ב- C:\Users\someuser\Desktop\. לאחר מכן תמצא שכבה עם מספר סידורי 3 ותשנה את הגובה שלה ל-50 פיקסלים ואת הרוחב ל-100 פיקסלים. לאחר מכן תוזן שכבה זו כ-PDF ב- C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}Resize layer with index 3 of C:\Users\someuser\Desktop\input.psd to width 50 and height 100 and save it to C:\Users\someuser\Desktop\output.pdf{{< /highlight >}}

5. פקודה זו תפתח את smth.psd בתיקיה הנוכחית, אך כל האפקטים יישבתו. ולאחר מכן קובץ זה יהפוך לתבנית BMP וישמור כ-output.bmp בתיקיית הנוכחית.
{{< highlight bash >}}Open smth.psd without effects and save it to output.bmp{{< /highlight >}}

**ברירת מחדל**

זו אפליקציה ניסיונית. אנא נסה והשאר משוב. כל משוב מוערך מאוד. רוצים להביא את האפליקציה ללא קוד לרמה הבאה. האינטגרציה הקלה אל כל צינור בנייה או תהליך עסקי היא המטרה שלנו.
