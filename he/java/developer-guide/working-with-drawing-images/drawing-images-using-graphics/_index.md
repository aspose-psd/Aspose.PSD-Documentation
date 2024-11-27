---
title: ציור תמונות באמצעות Graphics
type: docs
weight: 20
url: /he/java/drawing-images-using-graphics/
---

## **ציור תמונות באמצעות Graphics**

עם ספריית Aspose.PSD תוכל לצייר צורות פשוטות כמו קווים, מלבנים ומעגלים, כמו גם צורות מורכבות כמו מצולעים, עקופים, קשתות וצורות בזיר. ספריית Aspose.PSD יוצרת צורות כאלה באמצעות מחלקת Graphics השוכנת במרחב השמות של Aspose.PSD. עצם Graphics אחראי על ביצוע פעולות שונות של ציור על תמונה, כך שמשנים את משטח התמונה. מחלקת Graphics משתמשת בגרסאות של מופעי מחסנית שונים לשיפור הצורות:

- עטים, לצייר קווים, להיפתר בצורות או לצייר ייצוגים גיאומטריים אחרים.
- מברשות, להגדיר איך אזורים יומלאו.
- גופנים, להגדיר את צורת התוים של טקסט.
### **ציור עם מחלקת Graphics**
למטה דוגמה לקוד המדגים את שימוש במחלקת Graphics. קוד המקור של הדוגמה נחלק למספר חלקים כדי לשמור עלו פשוט ונוח למעקב אחריו. שלב אחר שלב, הדוגמאות מציגות כיצד ל:

1. ליצור תמונה.
1. ליצור ולאתחל אובייקט Graphics.
1. לנקות את המשטח.
1. לצייר אליפסה.
1. לצייר מצולע ממולא ולשמור את התמונה.
### **דוגמאות תכנות**
#### **יצירת תמונה**
התחל ביצירת תמונה בכל אחת מהשיטות הנתמכות המתוארות ביצירת קבצים.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingBezier-DrawingBezier.java" >}}
#### **יצירה ואתחול אובייקט Graphics**
לאחר מכן, צור ואתחל אובייקט Graphics על ידי מעבירת אובייקט Image לבונה.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingArc-DrawingArc.java" >}}
#### **ניקוי המשטח**
נקה את משטח ה- Graphics על ידי קריאה לשיטת הניקוי של מחלקת Graphics והעברת צבע כפרמטר. שיטה זו ממלאה את משטח ה- Graphics בצבע שהועבר כארגומנט.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
#### **ציור אליפסה**
ניתן להבחין שמחלקת Graphics חשפה כמות רבה של שיטות לצייר ולמלא צורות. תמצא את הרשימה המלאה של השיטות במדריך ה-API של Aspose.PSD ל- Java. ישנם מספר גרסאות מועמדות למחלקת DrawEllipse שמוצגות על ידי מחלקת Graphics. כל אלה מקבלות אובייקט Pen כארגומנט הראשון שלהן. הפרמטרים המאוחרים מועברים להגדרת המלבן מסביב לאליפסה. למען הדוגמה, השתמש בגרסה שמקבלת אובייקט Rectangle כפרמטר שני כדי לצייר אליפסה באמצעות אובייקט Pen בצבע הרצוי.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingEllipse-DrawingEllipse.java" >}}
#### **ציור מצולע ממולא**
באמצעות LinearGradientBrush ומערך של נקודות, ניתן לצייר מצולע. מחלקת Graphics חשפה מספר גרסאות מועמדות למחלקת FillPolygon. כל אלו מקבלות אובייקט Brush כארגומנט ראשון שלהן, המגדיר את התכונות של המילוי. הפרמטר השני הוא מערך של נקודות. יש לשים לב שכל שתי נקודות רצופות במערך מציינות צד של המצולע.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}
### **ציור תמונות באמצעות Graphics : מקור מלא**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.java" >}}

כל המחלקות שמיישמות IDisposable ומגישון משאבים שאינם מנוהלים, מופעלות בהצהרת שימוש לסימן ייבוא מסודר שנשמר על ניתוקן בצורה נכונה.
