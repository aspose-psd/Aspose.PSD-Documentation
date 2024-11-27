---
title: ציור תמונות
type: docs
weight: 10
url: /he/net/drawing-images/
---

## **ציור קווים**
דוגמה זו משתמשת במחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי לצייר צורות של קווים על פני התמונה. כדי להדגים את הפעולה, הדוגמה יוצרת תמונה חדשה ומציירת קווים על פני התמונה באמצעות השיטה [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) המוצגת על ידי מחלקת Graphics. ראשית, נייצר PsdImage ונציין את גובהו ורוחבו.

לאחר שהתמונה נוצרה, נשתמש בשיטת Clear שניתנת על ידי מחלקת Graphics כדי להגדיר את צבע הרקע שלה. ה[DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משמש לציור קו על תמונה המחברת בין שתי מבני נקודות. למתודה זו יש מספר גרסאות המקבלות את מופע ממחלקת Pen וזוגות נקודות או מבני Point/PointF כארגומנטים. מחלקת הקיסם מגדירה אובייקט המשמש לציור קווים, מסילות וצורות. למחלקת הקיסם יש מספר בנאי מופעים לצייר קווים בצבע, רוחב ומברשת מוגדרים. מחלקת ה SolidBrush משמשת לציור ברציפות בצבע מסוים. לבסוף, התמונה מיוצאת לתקני קובץ BMP. קטע הקוד הבא מציג איך לצייר צורות של קווים על פני התמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}
## **ציור אליפסה**
דוגמה זו היא המאמר השני בסדרת ציור צורות. נשתמש במחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי לצייר את צורת האליפסה על פני התמונה. כדי להדגים את הפעולה, הדוגמה יוצרת תמונה חדשה ומציירת את צורת האליפסה על פני התמונה באמצעות השיטה DrawEllipse המוצגת על ידי מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). ראשית, נייצר PsdImage ונציין את גובהו ורוחבו.

לאחר יצירת התמונה, ניצור ונאתחל אובייקט מחלקת Graphics ונגדיר את צבע הרקע של התמונה באמצעות שימוש בשיטת Clear של מחלקת Graphics. השיטה DrawEllipse של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משמשת לצייר את צורת האליפסה על פני תמונה על ידי מרבית המלבנית בריבוע. לשיטה זו יש מספר אפשרויות עמודות המקבלות את מופעי מחלקת פֶּן ומבני מלבן/מלבןF או זוג נקודות, גובה ורוחב כארגומנטים. מחלקת Pen מגדירה אובייקט המשמש לציור קווים, מסילות וצורות. למחלקת Pen יש מספר בנאי מופעים לצייר קווים בצבע מסוים, רוחב ומברשת. המחלקה Rectangle מאחסנת סט של ארבעה מספרים שמייצגים את המיקום וגודלו של מלבן. למחלקה Rectangle יש מספר בנאי מופעים לצייר את מבנה המלבן עם גודל ומיקום ספציפיים. מחלקת SolidBrush משמשת לציור ברציפות בצבע מסוים. לבסוף, התמונה מיוצאת לתקני קובץ bmp. הקוד הבא מציג איך לצייר צורת אליפסה על פני התמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}
## **ציור מלבן**
בדוגמה זו נצייר את צורת המלבן על פני התמונה. כדי להדגים את הפעולה, הדוגמה תיצור תמונה חדשה ותצייר צורת מלבן על פני התמונה באמצעות השיטה DrawRectangle המוצגת על ידי מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). ראשית, נייצר PsdImage ונציין את גובהו ורוחבו. לאחר מכן, נגדיר את צבע הרקע של התמונה על ידי שימוש בשיטת Clear של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics).

שיטת DrawRectangle של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משמשת לציור צורת מלבן על פני תמונה שנקבעת על ידי מבנה המלבן. שיטה זו כוללת מספר אפשרויות עמודות המקבלות את מופעי הפֶּן ומבני מלבן/מלבןF או זוג נקודות, רוחב וגובה כארגומנטים. מחלקת Rectangle מאחסנת סט של ארבעה מספרים שמייצגים את המיקום וגודלו של מלבן. למחלקת Rectangle יש מספר בנאי מופעים שמאפשרים לצייר את מבנה המלבן עם גודל ומיקום ספציפיים. לבסוף, התמונה מיוצאת לתקני קובץ bmp. הקוד הבא מציג איך לצייר צורת מלבן על פני התמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}
## **ציור קשת**
בסדרת הסט לציור צורות, נצייר את צורת הקשת על פני התמונה. נשתמש בשיטת DrawArc של [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי להדגים את הפעולה על תמונת BMP. ראשית, נייצר PsdImage ונציין את גובהו ורוחבו. לאחר שהתמונה נוצרה, נשתמש בשיטת Clear הנחשפת על ידי מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי להגדיר את צבע הרקע שלה.

שיטת DrawArc של [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משמשת לצייר את צורת הקשת על פני התמונה. השיטה DrawArc מייצגת חלק מאליפסה כלשהי שמוגדרת על ידי מבנה מלבן או זוג הנקודות. שיטה זו יש לה מספר אפשרויות עמודות שמקבלות אפשרויות סבירות של מופעי העט האשרטיים ומבני הריבוע/מלבןF או זוג הנקודות, רוחב וגובה כארגומנטים. לבסוף, התמונה מיוצאת לתקני קובץ BMP. הקטע הבא מציג איך לצייר צורת קשת על פני התמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
## **ציור בזיר**
דוגמה זו משתמשת במחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי לצייר את צורת הבזייה על פני התמונה. כדי להדגים את הפעולה, הדוגמה תיצור תמונה חדשה ותצייר את צורת הבזייה על פני התמונה באמצעות השיטה DrawBezier המוצגת על ידי מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). ראשית, נייצר PsdImage ונציין את גובהו ורוחבו. לאחר הנצירה של התמונה, נשתמש בשיטת Clear שניתנת על ידי מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) כדי להגדיר את צבע הרקע שלה.

שיטת DrawBezier של [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משמשת לצייר את צורת Bezier spline על פני תמונה המוגדרת על ידי ארבע מבני נקודה. לשיטה יש מספר אפשרויות עמודות המקבלות אפשרויות סבירות של מופעי העט האשרטיים ומבני Point/PointF או מערך של מבני Point/PointF. מחלקת Pen מגדירה אובייקט המשמש לצייר קווים, מסילות וצורות. למחלקת Pen יש מספר בנאי מופעים
