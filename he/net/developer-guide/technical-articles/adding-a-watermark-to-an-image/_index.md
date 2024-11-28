---
title: הוספת סימן מים לתמונה
type: מסמך
weight: 30
url: /he/net/הוספת-סימן-מים-לתמונה/
---

## **הוספת סימן מים לתמונה**
מסמך זה מסביר איך להוסיף סימן מים לתמונה באמצעות Aspose.PSD. הוספת סימן מים לתמונה היא דרישה נפוצה ביישומי עיבוד תמונה. בדוגמה זו אנו משתמשים במחלקת ה-Graphics כדי לשרטט מחרוזת על פני התמונה.
### **הוספת סימן מים**
כדי להדגים את הפעולה, נטען תמונת BMP מהדיסק ונשרטט מחרוזת כסימן מים על פני התמונה באמצעות שיטת DrawString של מחלקת ה-Graphics. נשמור את התמונה בפורמט PNG באמצעות מחלקת ה-PngOptions. להלן דוגמה לקוד שמדגים איך להוסיף סימן מים לתמונה. קוד הדוגמה פוצל לחלקים כדי להקל על המעקב. שלב אחר שלב, הדוגמאות מציגות כיצד:

1. [נטען](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) תמונה.
1. ניצור ונאתחל אובייקט [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).
1. ניצור ונאתחל אובייקטי Font ו-[SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush).
1. נשרטט מחרוזת כסימן מים באמצעות שיטת [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) של מחלקת ה-Graphics.
1. נשמור את התמונה בפורמט PNG.

קטע הקוד הבא מציג איך להוסיף סימן מים לתמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}
### **הוספת סימן מים אלכסוני**
הוספת סימן מים אלכסוני לתמונה דומה להוספת סימן מים אופקי כפי שנדון לעיל, עם מספר שינויים. כדי להדגים את הפעולה, נטען תמונת JPG מהדיסק, נוסיף המרות באמצעות אובייקט של מחלקת [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) ונשרטט מחרוזת כסימן מים באמצעות שיטת DrawString של מחלקת ה-Graphics. להלן דוגמה לקוד שמדגים איך להוסיף סימן מים אלכסוני לתמונה. קוד הדוגמה פוצל לחלקים כדי להקל על המעקב. שלב אחר שלב, הדוגמאות מציגות כיצד:

1. נטען תמונה.
1. ניצור ונאתחל אובייקט Graphics.
1. ניצור ונאתחל אובייקטי [Font](https://reference.aspose.com/psd/net/aspose.psd/font) ו-SolidBrush.
1. נקבל גודל של התמונה ב-[SizeF](https://reference.aspose.com/psd/net/aspose.psd/sizef).
1. ניצור אינסטנס של מחלקת Matrix ונבצע שינוי משולב.
1. נקצוב את השינוי על אובייקט Graphics.
1. ניצור ונאתחל אובייקט [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat).
1. נשרטט מחרוזת כסימן מים באמצעות שיטת DrawString של מחלקת ה-Graphics.
1. נשמור את התמונה התוצאה.

קטע הקוד הבא מציג איך להוסיף סימן מים אלכסוני.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
