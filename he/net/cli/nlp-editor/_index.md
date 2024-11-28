---
title: אפליקציית Aspose.PSD CLI NLP Editor עבור .NET
type: מאמרים
weight: 10
url: /he/net/cli/nlp-editor/
is_root: false
keywords: CLI כלי פוטושופ NLP עיבוד שפה טבעית PSD קונסולה סי-שארפ API של PSD
description: אפליקציית ה-CLI של Aspose.PSD NLP Editor המבוססת על Aspose.PSD לקבצים בפורמט PSD, PSB, ו-AI. אוטומציה CI/CD ללא קוד. תומכת בעיבוד שפה טבעית לעריכת קבצי PSD. פשוט לכתוב את הבקשה בשפה טבעית כדי לבצע מגוון פעולות כמו המרה, כיוון, שינוי גודל, ועוד. אינה דורשת התקנת Adobe Photoshop או Adobe Illustrator ויכולה להפעיל מהקונסולה בלי קוד נוסף.
---

**![לוגו מוצר Aspose.PSD עבור .NET](home_1.png)**

**ברוכים הבאים לאפליקציית Aspose.PSD NLP Editor CLI עבור .NET**

אפליקציית ה-CLI של Aspose.PSD NLP Editor היא כלי נייד קל משקל לעריכת קבצי PSD באמצעות פקודות בשפה טבעית. אינטגרציה קלה לצנתני CI/CD.

**כתב ואחריות**

זוהי אפליקציה ניסיונית. נא לנסות ולהשאיר משוב. כל משוב מתקבל בברכה. אנו רוצים להביא אפליקציית ללא קוד לשלב הבא. האינטגרציה שלילה לכל צינור בניית או תהליך עסקי היא מטרתנו.

**הפונקציונליות העיקרית של אפליקציית Aspose.PSD NLP Editor CLI עבור .NET**

1. ביצוע פעולות על קבצים בפורמטים PSD, PSB, AI באמצעות פקודות בשפה טבעית.
2. תמיכה במגוון פעולות כמו המרה, כיוון, שינוי גודל, ועוד.
3. אוטומציה CI/CD ללא קוד.
4. תמיכה בכתיבת בקשות בשפה טבעית לעריכת קבצי PSD.

## **שימוש מהשורת הפקודה:**

{{% alert color="primary" %}}
תחילה, יש להתקין את כלי זה של dotnet:
{{< highlight bash >}}dotnet tool install --global Aspose.PSD.CLI.NLP.Editor --version 24.6.0{{< /highlight >}}

אנו ממליצים להפעיל את הפקודה הבאה לפני השימוש הראשון:
{{< highlight bash >}}Aspose.PSD.CLI.NLP.Editor --setup nlp.cli{{< /highlight >}}
לאחר מכן תוכלו להפעיל את היישום בשם קצר nlp.cli במקום Aspose.PSD.CLI.NLP.Editor. ניתן לציין שם קצר לבחירתכם.
{{% /alert %}}

**פרמטרים זמינים עבור אפליקציית Aspose.PSD.CLI.Crop**

| **Argument** | **Description**                         |
|:-------------|:----------------------------------------|
| טקסט כלשהו     | נדרש. הפקודה שלך בשפה טבעית לעדכון קובץ PSD או PSB      |
| רישיון      | נתיב אל הרישיון.                    |
| מפורט      | הצגת מידע נוסף על פקודה מסוימת. |
| התקנה        | יוצר קובץ bat בתיקיית הכלים לפנייה מהרה מהקונסולה. לדוגמה: --setup psd.nlp. אז תוכלו לקרא לכלי ב-pds.nlp |
 

**דוגמאות לשימוש**

1. הפקודה הזו תמיר את הקובץ הראשון (שניתן לפתוח עם aspose.psd) מהתיקיה הנוכחית ותשמור אותו בפורמט PNG עם שקיפות. כמו כן, יתחבר הרישיון. עליך להגדיר את הרישיון פעם אחת בלבד. בהפעלות הבאות, הרישיון ישמש מהנתיב שצויין. הפקודה תציג את לוג העיבוד המפורט של NLP, אם זמין. 
{{< highlight bash >}}
  nlp.cli המרת קובץ מהתיקיה לפורמט PNG עם אלפא --רישיון "C:\Aspose\LicenseFile.lic --verbose "
{{< /highlight >}}

2. הפקודה תמצא את הקובץ בשם הכי דומה ל-"smth.psd". לאחר מכן, תרכז ניגוד ותשמור אותו בפורמט JPEG באיכות הגבוהה ביותר. שמו של הקובץ הפלט יודפס. זה יהיה smth.jpg
{{< highlight bash >}}
  להתאים ניגוד על שכבה בשם ellipse בקובץ smth.psd ולשמור ב-output.jpg באיכות הטובה ביותר
{{< /highlight >}}

3. הפקודה הזו תגרום שהקובץ בנתיב שצוין יעטוף את עצמו ויוקטן ב-25%. הקובץ הפלט יודפס ו יישמר בתיקייה הנוכחית של הקונסולה.
{{< highlight bash >}}
  שינוי גודל לקובץ C:\Users\someuser\Desktop\input.psd ל-25%
{{< /highlight >}}

4. הפקודה הזו תמצא את הקובץ input.psd ב- C:\Users\someuser\Desktop\. לאחר מכן, תמצא את השכבה עם אינדקס 3 ותקטינו לרוחב 50px ולגובה 100px. לאחר מכן, השכבה הזאת תיודפת כקובץ PDF ב- C:\Users\someuser\Desktop\output.pdf
{{< highlight bash >}}
  שינוי שכבה עם אינדקס 3 של C:\Users\someuser\Desktop\input.psd לרוחב 50 ולגובה 100 ושמירתה ל- C:\Users\someuser\Desktop\output.pdf
 {{< /highlight >}}

5. הפקודה הזו תפתח את smth.psd בתיקייה הנוכחית, אך כל האפקטים יושבתו. לאחר מכן, קובץ זה יהפוך לפורמט BMP וישמר ב-output.bmp בתיקיית הנוכחית.
{{< highlight bash >}}
  פתח את smth.psd ללא אפקטים ושמור אותו ל-output.bmp
  {{< /highlight >}}

**נא לבדוק [יישומי CLI של Aspose.PSD](https://docs.aspose.com/psd/net/cli) ל-.NET אם תרצו להוסיף תמיכה לפורמטים PSD, PSB ו-AI לתהליך העבודה שלכם**

1. [Aspose.PSD CLI המרה](/psd/he/net/cli/convert)
2. [Aspose.PSD CLI חיתוך](/psd/he/net/cli/crop)
3. [Aspose.PSD CLI שינוי גודל](/psd/he/net/cli/resize)
4. [Aspose.PSD CLI ייצוא](/psd/he/net/cli/export)
5. [Aspose.PSD CLI עורך NLP](/psd/he/net/cli/nlp-editor)

**נא לבדוק את Aspose.PSD עבור .NET או [פלטפורמות אחרות]**

יישומי CLI של Aspose.PSD הם פתרון מוכן לשימוש עבור פעולות פופולריות. אם תרצו פתרון גמיש, נא לבדוק את הגרסה המלאה של Aspose.PSD

1. [Aspose.PSD עבור .NET](https://releases.aspose.com/psd/net/)
2. [Aspose.PSD עבור Java](https://releases.aspose.com/psd/java/) 
3. [Aspose.PSD עבור Python via .NET](https://releases.aspose.com/psd/python-net/)

## **משאבים ל-Aspose.PSD עבור .NET**

להלן קישורים למשאבים שיעזרו לכם להשלים את המשימות שלכם.

- [Aspose.PSD CLI Applications ל- .NET מדריך מקוון](/psd/he/net/cli/conversion)
- [Aspose.PSD ל CLI Applications של .NET הערות שחרור](/psd/he/net/cli/conversion/release-notes/)
- [Aspose.PSD ל CLI Applications .NET דף המוצר](https://products.aspose.com/psd/net/cli)
- [מדריך ה API של Aspose.PSD ל-.NET](https://reference.aspose.com/net/psd)
- [הורדת דוגמאות במאגר הקוד של GitHub](https://github.com/aspose-psd/CLI-Applications)
- [פורום עזרה חינמי ל-Aspose.PSD עבור .NET](https://forum.aspose.com/c/psd)
- [משדרג תמיכה לתשלום ל-Aspose.PSD עבור .NET](https://helpdesk.aspose.com/)
