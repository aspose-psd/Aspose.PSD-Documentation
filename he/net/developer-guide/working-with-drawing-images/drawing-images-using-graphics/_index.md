---
title: ציור תמונות באמצעות גרפיקה
type: docs
weight: 20
url: /he/net/drawing-images-using-graphics/
---

## **ציור תמונות באמצעות גרפיקה**
עם ספריית Aspose.PSD ניתן לצייר צורות פשוטות כמו קווים, מלבנים ומעגלים, וגם צורות מורכבות כמו מצולות, עקומות, קשתות וצורות Bezier. ספריית Aspose.PSD יוצרת צורות כאלו באמצעות מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) השוכנת במרחב השמות Aspose.PSD. אובייקטי גרפיקה אחראים לביצוע פעולות שונות של שרטוט על תמונה, משנים את משטח התמונה. מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) משתמשת במגוון אובייקטים עזר כדי לשפר את הצורות:

·         עטים, לשרטוט קווים, להדגיש צורות או לעשות ייצוגים גיאומטריים אחרים.

·         מכחול עם, להגדיר איך אזורים מתמלאים.

·         גופנים, להגדיר את הצורה של תווים בטקסט.
### **ציור עם מחלקת הגרפיקה**
להלן דוגמה לקוד המדגים את שימוש במחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics). קוד המקור המופיע מחולק לחלקים מספרים כדי לשמר אותו פשוט וקל לעקוב אחריו. שלב אחר שלב, הדוגמאות מראות כיצד לבצע:

1. יצירת תמונה.
1. יצירה ואיתחול של אובייקט Graphics.
1. ניקוי השטח.
1. שרטוט אליפסה.
1. שרטוט מצולה ממולאת ושמירת התמונה.
### **דוגמאות תכנות**
#### **יצירת תמונה**
התחל על ידי יצירת תמונה באמצעות אחת מהשיטות המתוארות ביצירת קבצים.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **יצירה ואיתחול אובייקט Graphics**
לאחר מכן יצור ואיתחול של אובייקט Graphics על ידי מעבירה של התמונה לאובייקט הבונה שלו.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}
#### **ניקוי השטח**
נקה את שטח הגרפיקה על ידי קריאה לפעולת ניקוי של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) והעברת צבע כפרמטר. פעולה זו ממלאה את שטח הגרפיקה עם הצבע הנתון כארגומנט.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
#### **שרטוט אליפסה**
תוכל ללמוד כי למחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) חשפה רשימה ארוכה של שיטות לשרטוט ולמילוי צורות. תמצא את רשימת השיטות המלאה בתיעוד ה- API של Aspose.PSD for .NET. קיימות גרסאות רבות של השיטה DrawEllipse שנחשפות על ידי מחלקת Graphics. כל השיטות אלו מקבלות אובייקט Pen כארגומנט הראשון שלהן. הפרמטרים הבאים מאותגרים להגדיר את המלבן הגומי סביב האליפסה. בשם דוגמת זאת, השתמש בגרסה המקבלת אובייקט Rectangle כמקביל שני כדי לצייר אליפסה באמצעות אובייקט Pen בצבע שנבחר על ידך.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}
#### **שרטוט מצולה ממולאת**
לאחר מכן, צייר מצולה באמצעות ה- LinearGradientBrush ומערך של נקודות. למחלקת Graphics חשפה כמה גרסאות עמודות של שיטת המילוי (FillPolygon). כל אחת מהן מקבלת אובייקט Brush כארגומנט הראשון, שמגדיר את המאפיינים של מילוי. הפרמטר השני הוא מערך של נקודות. נא לשים לב כי לכל שתי נקודות רצופות במערך נקבעת צד של המצולה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}
### **ציור תמונות באמצעות גרפיקה: מקור מלא**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

כל המחלקות שמממשות IDisposable וגושים שאינם מנוהלים נפתחים בפקודת Using כדי לוודא שהם יתפשטו בצורה נכונה.
