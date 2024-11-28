---
title: שכבת התאמה להיפוך
type: docs
weight: 30
url: /he/java/layer-types/adjustment-layer/invert/
---

# עבודה עם שכבת התאמה להיפוך בפוטושופ ב-Java

במאמר זה אנו מציגים איך להפוך תמונה במסמך של פוטושופ לתמונת שלילה באופן תכנותי ב-Java. למטרה זו, נשתמש בספריית עיבוד מבנה קובץ PSD הנקראת Aspose.PSD for Java.

ממשק ה-API להיפוך הצבע מאפשר **להוסיף אפקט שלילי לתמונה**. כבר ראית איך ל [הפוך צבעי תמונה באמצעות שכבת קינון עקומות](/psd/he//java/layer-types/adjustment-layer/curves/). אך, היום נשקול דרך מהירה וקלה יותר לעשות את העבודה באמצעות שכבת ההתאמה להיפך.

## סקירת API

**ממשק שכבת ההתאמה להיפוך** מורכב ממחלקת השכבה עצמה שהיא [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer). מחלקה זו אינה מכילה חברים ציבוריים משלה, מאחר והיא יורשת את כל חברי הציבור מהמחלקה האב ([AdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/AdjustmentLayer)). עובדה זו מקלה על השימוש בגלל שכל מה שעליך לעשות הוא להוסיף אותה לקובץ PSD והתמונה משתנה לשלילית.

## היפוך צבעי התמונה

לכן, גם אם זה נראה מובן אבל נדגים למען בהירות **איך להחיל שכבת ההתאמה להיפוך על התמונה** של חדל תנאות (A) כדי ליצור אפקט שלילי עבור התמונה הזאת (B).

![דוגמה להשקפת שכבת ההתאמה להיפוך לפני ואחרי](invert-adjustment-layer-figure-1.png)

כדי **להיפוך את צבעי התמונה** סתם הוסף שכבת ההתאמה להיפוך לתוך ה-PSD:

    InvertAdjustmentLayer invertAdjustmentLayer = psdImage.addInvertAdjustmentLayer();

זהו! אין פרטים ספציפיים להגדרה עבור סוג זה של שכבת ההתאמה.

## מסקנה

במאמר זה למדנו על API של שכבת ההתאמה להיפוך של Aspose.PSD for Java. זהו כלי בלתי מתקשה לקבלת תמונות שליליות מאחר ו-API של שכבת ההתאמה הזו אינו מצהיר על חברי ציבור.
