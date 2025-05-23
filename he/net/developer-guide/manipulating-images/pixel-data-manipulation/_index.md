---
title: עיבוד נתוני פיקסלים באמצעות Aspose.PSD עבור C#
weight: 100
type: docs
description: דוגמה כיצד לעדכן במהירות נתוני פיקסלים גולמיים באמצעות ממשק ה-PSD C# API
keywords: [עריכת פיקסלים, עריכת PSD, עריכת שכבה, עיבוד נתונים גולמיים, עריכת נתוני PSD, API של PSD, C#, csharp, דוגמת קוד]
url: he/net/pixel-data-manipulation/
---

## היכרות

Aspose.PSD הינה ספרייה עצומה שמאפשרת לך לעבוד עם קבצי אדובי פוטושופ (PSD) ב-C#. במאמר זה, נשקול כיצד להשתמש בהספרייה כדי לערוך נתוני פיקסלים בקובץ PSD באמצעות Aspose.PSD עבור C#.

## סקירה

הקוד המסופק מדגים כיצד ליצור קובץ PSD, להוסיף שכבה חדשה, לערוך את נתוני הפיקסלים ישירות ולשמור את התמונה שעברה שינויים.

### שלבים לפעול בעיבוד נתוני פיקסלים

1. **יבוא מודולים נדרשים**:
   ייבא את המודולים הנדרשים. עליך לייבא את המחלקות `PsdImage` ו-`Layer` מהספרייה של Aspose.PSD.

2. **הגדרת נתיבי קובץ הקלט והקלט שלך**:
   ציין נתיבי קובץ הקלט והקלט שלך.

3. **פתח את קובץ הקלט כזרם**:
   פתח את קובץ הקלט כזרם באמצעות המחלקה `FileStream` במצב קריאה. צור אובייקט `PsdImage` על ידי טעינת הזרם.

4. **צרו תמונת PSD חדשה**:
   צרו תמונת PSD חדשה באמצעות בנאי ה- `PsdImage` וספקו את רוחב וגובה השכבה כארגומנטים.

5. **הקצאת השכבה לתמונת ה- PSD**:
   הקצה את השכבה למאפיית `Layers` של תמונת ה- PSD.

6. **עריכת נתוני הפיקסלים**:
   טען את הפיקסלים מהשכבה באמצעות השיטה `LoadArgb32Pixels`. הגדר טווח אינדקסים על פי אורך מערך הפיקסלים ושנה את ערכי הפיקסלים כפי שנדרש.

7. **שמירת נתוני הפיקסלים שעברו שינוי**:
   שמור את נתוני הפיקסלים שעברו שינוי חזרה לשכבה באמצעות השיטה `SaveArgb32Pixels`.

8. **שמירת תמונת ה- PSD**:
   שמור את תמונת ה- PSD לקובץ הפלט באמצעות השיטה `Save`.

### דוגמה

הנה קוד מציג שבתיה שמדגים כיצד לערוך נתוני פיקסלים באמצעות Aspose.PSD עבור C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "PixelDataManipulation-PixelDataManipulation.cs" >}}

### סיכום

Aspose.PSD עבור C# מספק סט חזק של יכולות לעיבוד נתוני פיקסלים בקבצי PSD. בין אם יידרש לך לשנות פיקסלים בהתבסס על תנאים ספציפיים או ליצור דפוסים מורכבים, Aspose.PSD הופך את משימות אלו לפשוטות ויעילות.

למידע נוסף ולדוגמאות מפורטות יותר, נא לבקר ב-[תיעוד Aspose.PSD עבור C#](https://docs.aspose.com/psd/net/).
