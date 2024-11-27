---
title: יצירת, פתיחה ושמירת קבצי תמונה
type: docs
weight: 30
url: /he/java/creating-opening-and-saving-images/
---

## **יצירת קבצי תמונה**
Aspose.PSD עבור Java מאפשר למפתחים ליצור תמונות בעצמם. השתמשו בשיטת היצירה הסטטית החשופה על ידי המחלקה Image כדי ליצור תמונות חדשות. כל מה שעליכם לעשות הוא לספק אובייקט המתאים מאחד המחלקות מ־ImageOptions לפורמט התמונה המבוקש. כדי ליצור קובץ תמונה, תחילה עליכם ליצור אינסטנס של אחת מהמחלקות מ־ImageOptions. מהמחלקות הנ"ל מצויות במרחב השמות ImageOptions (שימו לב שרק משפחת פורמטי קבצים PSD נתמכים כרגע ליצירה):

PsdOptions מגדיר את האפשרויות ליצירת קובץ PSD. ניתן ליצור קבצי תמונה על ידי הגדרת נתיב פלט או באמצעות זרם.
### **יצירה על ידי הגדרת נתיב**
יצרו PsdOptions מתוך מרחב השמות ImageOptions והגדירו את המאפיינים השונים. המאפיין החשוב ביותר להגדרה הוא המאפיין Source. מאפיין זה מציין איפה הנתונים של התמונה ממוקמים (בקובץ או בזרם). בדוגמה למטה, המקור הוא קובץ. לאחר שהגדרתם את המאפיינים, העבירו את האובייקט לאחת משיטות היצירה הסטטיות יחד עם פרמטרי הרוחב והגובה. הרוחב והגובה מוגדרים בפיקסלים.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingbySettingPath-CreatingbySettingPath.java" >}}
### **יצירה באמצעות זרם**
תהליך יצירת תמונה באמצעות זרם דומה לתהליך של שימוש בנתיב. ההבדל היחיד הוא שעליכם ליצור אינסטנס של StreamSource על ידי העברת אובייקט זרם לבונה שלו ולהקצות אותו למאפיין Source.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreatingUsingStream-CreatingUsingStream.java" >}}
## **פתיחת קבצי תמונה**
מפתחים יכולים להשתמש ב־API של Aspose.PSD עבור Java כדי לפתוח קבצי תמונה PSD קיימים למטרות שונות, כגון הוספת אפקטים לתמונה או להמיר קובץ קיים לפורמט אחר. למרות המטרה, Aspose.PSD מספק שני דרכים סטנדרטיות לפתיחת קובצים קיימים: מקובץ או מזרם.
### **פתיחה מדיסק**
פתחו קובץ תמונה על ידי העברת הנתיב ושם הקובץ כפרמטר לשיטת הסטטית Load החשופה על ידי המחלקה Image.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **פתיחה באמצעות זרם**
לפעמים התמונה שצריך לפתוח מאוחסנת כזרם. במקרים כאלה, השתמשו בגרסה שחורת העומק של שיטת Load. שיטה זו מקבלת אובייקט זרם כארגומנט כדי לפתוח את התמונה.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-LoadingFromStream-LoadingFromStream.java" >}}
### **טעינת תמונה כשכבה**
מאמר זה מדגים את שימושה של Aspose.PSD לטעינת תמונה כשכבה. API של Aspose.PSD חשף שיטות יעילות וקלות לשימוש להשגת מטרה זו. Aspose.PSD חשף את שיטת ההוספה של המחלקה PsdImage להוספת תמונה לקובץ PSD כשכבה.

השלבים לטעינת תמונה לתוך PSD כשכבה הם כהלך:

- צרו אינסטנס של image באמצעות המחלקה PsdImage עם רוחב וגובה מסוימים.
- טענו קובץ PSD כתמונה באמצעות שיטת הפאקטוריה Load שחשפה על ידי מחלקת Image.
- צרו אינסטנס של המחלקה Layer והקצו לה את שכבת התמונה PSD.
- הוסיפו את השכבה שנוצרה באמצעות שיטת ההוספה AddLayer שחשפה על ידי מחלקת PsdImage.
- שמרו את התוצאות.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-LoadImageToPSD-LoadImageToPSD.java" >}}

## **שמירת קבצי תמונה**
Aspose.PSD מאפשר לך ליצור קבצי תמונה מאפס. הוא מספק גם את האמצעים לעריכת קבצי תמונה קיימים. לאחר שהתמונה נוצרה או נערכה, הקובץ נשמר כללית בדרך כלל לדיסק. Aspose.PSD מספק לך שיטות לשמירת תמונות לדיסק על ידי ציון נתיב או באמצעות אובייקט זרם.
### **שמירה לדיסק**
מחלקת התמונה מייצגת אובייקט תמונה, לכן מחלקה זו מספקת את כל הכלים הדרושים ליצירה, טעינה ושמירת קובץ תמונה. עליכם להשתמש בשיטת השמירה Save של המחלקה Image כדי לשמור תמונות. גרסת השמירה שמקבלת את מיקום הקובץ כמחרוזת.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoDisk-SavingtoDisk.java" >}}
### **שמירה לזרם**
גרסת נטענת כבר של השמירה מקבלת את עצם הזרם כארגומנט ושומרת את קובץ התמונה לזרם.

אם התמונה נוצרה על ידי הציון של אחת מהאפשרויות של היצירה בבונה Image, התמונה נשמרת אוטומטית לנתיב או לזרם שניתן במהלך אתחול מחלקת Image על ידי קריאה לשיטת השמירה שאינה מקבלת אף פרמטר.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SavingtoStream-SavingtoStream.java" >}}
### **הגדרה להחלפת גופנים חסרים**
מפתחים יכולים להשתמש באפיון של Aspose.PSD עבור API של Java כדי לטעון קבצי תמונה PSD קיימים למטרות שונות, לדוגמה להגדיר שם גופן ברירת מחדל כאשר נשמרים מסמכי PSD כתמונת רסטר (לפורמטים PNG, JPG ו־BMP). גופן ברירת מחדל זה צריך לשמש כהחלפה לכל הגופנים החסרים (כלומר, גופנים שאינם נמצאים במערכת ההפעלה הנוכחית). לאחר שהתמונה השתנתה, הקובץ יישמר לדיסק.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-SettingforReplacingMissingFonts-SettingforReplacingMissingFonts.java" >}}
