---
title: נמנע התנדנדות בביצועים בעת ציור מעל תמונות מדוחסות
type: docs
weight: 40
url: /he/java/נמנע-התנדנדות-בביצועים-עת-ציור-מעל-תמונות-מדוחסות/
---

## **נמנע התנדנדות בביצועים בעת ציור מעל תמונות מדוחסות**
ישנם רגעים שבהם ברצונך לבצע פעולות גרפיות נרחבות ביותר על תמונה מדוחסת. כאשר Aspose.PSD צריך לדחוס ולפשוט תמונות במהלך הפעלתם, עשוי להתמוטט ביכולת הביצועים. ציור מעל תמונות מדוחסות עשוי גם לגרום לעונש בביצועים.

### **פתרון**
כדי למנוע התנדנדות בביצועים, אנו ממליצים להמיר את התמונה לפורמט שאינו מדוחס, או פורמט גולמי, לפני ביצוע פעולות גרפיות.

### **שימוש בנתיב קובץ**
בדוגמה שלהלן, תמונת PSD מתמרמזת לפורמט גולמי (ללא דחיפות) ומתבצעת שמירה על דיסק. לאחר מכן התמונה לא מדוחסת נטענת מחדש לפני ביצוע פעולות גרפיות עליה. טכניקה זו תקפה גם עבור קבצי BMP ו-GIF.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}
### **שימוש באובייקט זרם**
קטע הקוד הבא מציג כיצד תמונת PSD מתמרמזת לפורמט גולמי (ללא דחיפות) ומתבצעת שמירה על דיסק באמצעות זרם.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
