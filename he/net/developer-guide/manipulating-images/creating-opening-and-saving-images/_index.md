---
title: יצירת, פתיחה ושמירת קבצי תמונה
type: מסמכים
weight: 30
url: /he/net/יצירת-פתיחה-ושמירת-תמונות/
---

## **יצירת קבצי תמונה**
Aspose.PSD עבור .NET מאפשר למפתחים ליצור תמונות משלהם. השתמשו בשיטת Create הסטטית שנמשקת על ידי מחלקת ה-Image על מנת ליצור תמונות חדשות. כל מה שצריך לעשות הוא לספק אובייקט רלוונטי מאחת ממחלקות ה-ImageOptions שבשם מרחב השמות לפורמט תמונה המבוקש. על מנת ליצור קובץ תמונה, יש ליצור תחילה מופע של אחת המחלקות ממרחב השמות ImageOptions. מחלקות אלו קובעות את מבנה פורמט התמונה. להלן מחלקות כמה ממרחב שמות ImageOptions (שים לב כי בינתיים רק משפחת פורמטי קבצי PSD נתמכים ליצירה בלבד):

[PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) מגדיר את האפשרויות ליצירת קובץ PSD. ניתן ליצור קבצי תמונה על ידי הגדרת נתיב פלט או על ידי הגדרת זרם.
### **יצירה על ידי הגדרת נתיב**
יצרו PsdOptions ממרחב ה- [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) והגדירו את המאפיינים השונים. המאפיין החשוב ביותר להגדרה הוא המאפיין Source. מאפיין זה מציין איפה נמצאים נתוני התמונה (בקובץ או בזרם). בדוגמה הבאה, המקור הוא קובץ. לאחר הגדרת המאפיינים, העבירו את האובייקט לאחת משיטות הייצור הסטטיות [Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) יחד עם מוסף הרוחב והגובה. הרוחב והגובה מוגדרים בפיקסלים.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.cs" >}}
### **יצירה באמצעות זרם**
התהליך ליצירת תמונה באמצעות זרם דומה לתהליך של שימוש בנתיב. ההבדל הוא רק שיש ליצור מופע של [StreamSource](https://reference.aspose.com/psd/net/aspose.psd.sources/streamsource) על ידי העברת אובייקט Stream לבוניו והקצאתו למאפיין ה- Source.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.cs" >}}
## **פתיחת קבצי תמונה**
מפתחים יכולים להשתמש ב-API של Aspose.PSD עבור .NET כדי לפתוח קבצי תמונה PSD קיימים לצורכים שונים, כמו הוספת אפקטים לתמונה או להמיר קובץ קיים לפורמט אחר. למרות מטרת השימוש, Aspose.PSD מציע שני דרכים סטנדרטיות לפתיחת קבצים קיימים: מקובץ או מזרם.
### **פתיחה מתוך דיסק**
לפתוח קובץ תמונה על ידי מעבר נתיב הקובץ והשם כפרמטר לשיטת ה- Load הסטטית שנמשקת על ידי מחלקת ה- Image.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **פתיחה באמצעות זרם**
לפעמים התמונה שצריך לפתוח מאוחסנת כזרם. במקרים כאלה, השתמשו בגרסה כפולה של השיטת Load. פונקציה זו מקבלת אובייקט Stream כארגומנט על מנת לפתוח את התמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-LoadingFromStream-LoadingFromStream.cs" >}}
### **טעינת תמונה כשכבה**
מאמר זה מדגים את השימוש ב-Aspose.PSD לטעינת תמונה כשכבה. ה- APIs של Aspose.PSD חשפו שיטות יעילות וקלות לשימוש כדי להשיג מטרה זו. Aspose.PSD חשפו את השיטה AddLayer של מחלקת PsdImage כדי להוסיף תמונה לתוך קובץ PSD כשכבה.

השלבים לטעינת תמונה אל PSD כשכבה הם כפי שלמטה:

- צור מופע של תמונה על ידי המחלקה PsdImage עם רוחב וגובה מסוימים.
- טען קובץ PSD כתמונה באמצעות שיטת הייצור Load החשופה על ידי מחלקת Image.
- צור מופע של מחלקת Layer והקצה את שכבת התמונה של PSD אליה.
- הוסף את השכבה שנוצרה על ידי שימוש בשיטת AddLayer החשופה על ידי מחלקת PsdImage
- שמור את התוצאות.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.cs" >}}
### **טעינת תמונה כשכבה מזרם**
מאמר זה מדגים את השימוש ב-Aspose.PSD לטעינת תמונה כשכבה מזרמ. כדי לטעון תמונה מזרם, פשוט מעבר לאובייקט זרם הכולל תמונה לבונה של השכבה ולהקצתה למאפיין ה- Source. הוסף את השכבה שנוצרה על ידי שימוש בשיטת AddLayer החשופה על ידי מחלקת PsdImage ושמור את התוצאות.


כאן קישור לקוד לדוגמא.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **שמירת קבצי תמונה**
‏Aspose.PSD מאפשר לך ליצור קבצי תמונה מאפס. זה מספק גם את האמצעים לעריכת קבצי תמונה קיימים. פרט לעת צורה התמונה נשמרת לרוב בדיסק. Aspose.PSD נותן לך שיטות לשמירת תמונות לדיסק באמצעות ציון של נתיב או באמצעות אובייקט Stream.
### **שמירה לדיסק**
מחלקת ה-Image מייצגת אובייקט תמונה, כך שמחלקה זו מספקת את כל הכלים הדרושים ליצירה, טעינה ושמירת קובץ תמונה. השתמשו בשיטת השמירה של Image כדי לשמור תמונות. גרסה מועמתת אחת של השיטת שמירה מקבלת מיקום קובץ כמחרוזת.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoDisk-SavingtoDisk.cs" >}}
### **שמירה לזרם**
‏גרסה שניה מועמתת של השיטת שמירה מקבלת את אובייקט הזרם כארגומנט ושומרת את קובץ התמונה לזרם.

אם התמונה נוצרה על ידי ציון אחד ממחלקות ה-CreateOptions בבניית התמונה, התמונה נשמרת אוטומטית לנתיב או לזרם המסופקים במהלך אתחול מחלקת ה-Image על ידי קריאה לשיטת השמירה שאינה מקבלת שום פרמטר.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SavingtoStream-SavingtoStream.cs" >}}
### **הגדרה להחלפת גופני פונט חסרים**
מפתחים יכולים להשתמש ב-API של Aspose.PSD עבור .NET כדי לטעון קבצי תמונת PSD קיימים לצרכים שונים, לדוגמה, להגדיר שם של גופן ברירת מחדל בעת שמירת מסמכי PSD כתמונה רסטר (לתוך פורמטים PNG, JPG ו-BMP). שם של גופן ברירת מחדל זה ישמש כהחלפה לכל הגופנים החסרים (גופנים שאינם נמצאים במערכת ההפעלה הנוכחית). לאחר שהתמונה נערכה, הקובץ נשמר על דיסק.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.cs" >}}
