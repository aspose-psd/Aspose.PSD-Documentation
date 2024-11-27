---
title: כימוס ביעילות בעת ציור מעל תמונות דחוסות
type: docs
weight: 10
url: /he/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **חוסן ביעילות בעת ציור מעל תמונות דחוסות**
ישנם רגעים בהם תרצה לבצע פעולות גרפיות נרחבות ביותר על תמונה דחוסה. כאשר Aspose.PSD צריך לדחוס ולפרוץ תמונות בזמן ריצה, ייתכן שתהיה ירידה בביצועים. ציור מעל תמונות דחוסות עשוי גם לגרום לעניין בביצועים.
### **פתרון**
כדי למנוע התחנפות בביצועים, אנו ממליצים להמיר את התמונה לפורמט לא דחוס, או גולם, לפני ביצוע פעולות גרפיות.
### **שימוש בנתיב קובץ**
בדוגמה שמתגלה למעלה, תמונת PSD מומרת לפורמט גולם (ללא דחיסה) ושמורה בדיסק. התמונה לא דחוסה מועלת שוב לפני ביצוע פעולות גרפיות עליה. אותה הטכניקה נוגעת גם לקבצי BMP ו-GIF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}
### **שימוש בפריט זרם**
קטע קוד הבא מראה לך איך תמונת PSD מומרת לפורמט גולם (ללא דחיסה) ושמורה בדיסק באמצעות MemoryStream.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
