---
title: טיפול בתמונות TIFF
type: docs
weight: 40
url: /he/java/manipulating-tiff-images/
---

## **הוספת מסגרות עם הגדרות שונות**
TIFF הוא פורמט גמיש מאוד והוא מאפשר להוסיף מסגרות שונות, עם ממדים, דחיסה והגדרות אחרות שונות. ממשקי ה-Aspose.PSD מאפשרים לך להוסיף כל מסגרת TIFF שהיא ללא תלות בגודלה, וזה מסייע ביצירת מסמכים מורכבים. אם יש צורך להתאים את המסגרות במהלך התהליך כדי שכולן יהיו שוות, עליך לבצע את השלבים הבאים:

- צור מסגרת ריקה חדשה עם האפשרויות הרצויות או העתק את המסגרת מקור עם האפשרויות לפלט שצוינו באמצעות שיטת CreateFrameFrom.
- שנה את ממדי המסגרת/התמונה המקוריים לממדים הרצויים באמצעות השיטה Resize.
- הוסף את הפיקסלים של המסגרת/התמונה המקורית למסגרת החדשה.
- הוסף את המסגרת החדשה לתמונת ה-TIFF הפלט.

## **ייצוא שכבות של תמונת PSD לפורמט קובץ TIFF רב-עמוד**
לעיתים יש צורך לייצא שכבות של תמונת PSD לפורמט קובץ TIFF רב-עמוד. מאמר זה ידגיש כיצד תוכל לבצע משימה זו באמצעות-API של Aspose.PSD ל-Java. לראשונה, נטען את תמונת ה-PSD מהדיסק. לאחר מכן נעבור על שכבות התמונה ב-PSD וניצור TiffFrame מהשכבות המתאימות. לבסוף נשמור את תמונת ה-TIFF המתוצאה כקובץ יחיד בדיסק.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.java" >}}
## **תצורת TiffOptions**
מפתחי התוכנה יכולים להתאים מאפיינים שונים של מחלקת Tiffoptions כדי לקבל תוצאות הרצויות. במסמך זה, אנו נתמקד ב-4 מאפיינים עיקריים השולטים במאפייני התמונה המתוצאה.

המאפיינים המופיעים להלן.

1. ` `TiffOptions.Photometric
1. TiffOptions.Compression
1. TiffOptions.BitsPerSample
1. TiffOptions.Predictor

בכל פעם שאנו מאתחלים מבנה ריק של Tiffoptions, תכלית כל אפשרות היא לערך ברירת המחדל שלה, למשל, הדחיסה מוגדרת כלא, גודל הביטים לכל דגם מצוין כ-1 והצבע הפוטומטרי מוגדר כ-MinIsWhite. מעבר לשמירה בפורמט זה תגרום לתמונה הסופית להיות שחור לבן וזוהי התנהגות צפויה עבור אותן אפשרויות. על מנת לקבל תוצאות מודגשות יותר מומלץ להגדיר כל ארבעת המאפיינים שצוינו לערכים התואמים למרחב הצבעים הרצוי, או לאתחל את מבנת ה-Tiffoptions עם הגדרות מראש כפי שנדון במאמר. המידע המתואר מטה מציין ערכי פרמטר הצפויים שניתן להגדיר כדי להשיג את התוצאה הרצויה. יש לשים לב, עליך להגדיר את כל ארבעת העמודות דרך Tiffoptions לצורך שמירה של תמונה או ערוך שנטענת לפורמט TIFF.

|` `**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|פלטה|LZW/לא דחוס|1/4/8/16 (פלטה, מצב צבע) ערוץ יחיד בלבד|ללא|
|MinIsWhite/MinIsBlack|LZW/לא דחוס|1/4/8/16 (מצב גוונים) ערוץ יחיד בלבד|ללא|
|פלטה|LZW/לא דחוס|8 (פלטה, מצב צבע) ערוץ יחיד בלבד|אופקי (דחיסה נוספת מושגת עבור LZW תבניות זהות)|
|MinIsWhite/MinIsBlack|LZW/לא דחוס|8 (מצב גוונים) ערוץ יחיד בלבד|אופקי (דחיסה נוספת מושגת עבור LZW תבניות זהות)|
|RGB|LZW/לא דחוס|[8,8,8] (3 ערוצי RGB)|ללא/אופקי|
|RGB|LZW/לא דחוס|[8,8,8,8] (3 ערוצי RGB, שכבת אלפא נוספת יכולה לצוין דרך TiffOptions.AlphaStorage) בפועל תמוך כל ספירת ערוצים נוספים אך כל ערוץ חייב להכיל ערך 8 ביט כמו [8,8,8,8,8,8]|ללא/אופקי|
כל ארבעת המאפיינים צריכים להיות מוגדרים על ידי תצורת TiffOptions על מנת לשמור כל תמונה לפורמט TIFF. כאשר משתמשים בשילובים שונים, חלק מהצפייה (כולל Windows Photo Viewer) עשויים לסרב להצגת התמונה הסופית עקב התמיכה המוגבלת שהם מציעים. במקרה כזה, נא לבחור בצפיין שונה לצורך בדיקה.
### **הגדרות מוגדרות מראש עבור מחלקת TiffOptions**
כדי לעזור למשתמשים ולמנוע טעויות בהגדרת מופע של Tiffoptions, ה-API של Aspose.PSD עבור Java חשפה קונסטרקטור נוסף שמקבל פרמטר מסוג TiffExpectedFormat. בהתאם לערך הנבחר מתוך מכלול ה-TiffExpectedFormat, ה-API מגדיר באופן אוטומטי את כל המאפיינים החובה עבור Tiffoptions על מנת לייצר את התוצאה הרצויה. לפני שנמשיך לקטע הקוד הדוגמא, הנה רשימת שדות ערך ה-TiffExpectedFormat ופרטיהם להבנה טובה יותר של השימוש.


- TiffExpectedFormat.Default: הגדרת השדה ל-Default פועלת באופן דומה לבונה ברירת המחדל של מחלקת Tiffoptions עם דחיסה לא מוגדרת וביטים לכל ביט לוחצים המוגדרים כ-1 על מנת לייצר תוצאה שחור לבן. מומלץ להשתמש בשדה זה כאשר נדרשים פרטי פורמט מסוימים להתקבל באופן ידני על פי התוצאות הרצויות.
- TiffExpectedFormat.TiffCcitRle: ספציפי לקידוד RLE בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן) של TIFF.
- TiffExpectedFormat.TiffCcittFax3: ספציפי לקידוד CCITT Fax3 בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן) של TIFF.
- TiffExpectedFormat.TiffCcittFax4: ספציפי לקידוד CCITT Fax4 בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן) של TIFF.
- TiffExpectedFormat.TiffDeflateBW: ספציפי לדחיסת Deflate בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן) של TIFF.
- TiffExpectedFormat.TiffDeflateRGB: ספציפי לדחיסת Deflate בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffJpegRGB: ספציפי לדחיסת Jpeg בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffJpegYCBCR: ספציפי לדחיסת Deflate בעת שמירת התוצאה בפורמט YCBCR (צבע) של TIFF.
- TiffExpectedFormat.TiffLzwBW: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן) של TIFF.
- TiffExpectedFormat.TiffLzwRGB: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffLzwRGBA: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט RGBA (צבע עם שקיפות) של TIFF.
- TiffExpectedFormat.TiffNoCompressionBW: ספציפי לפורמט TIFF ללא דחיסה בעת שמירת התוצאה בפורמט 1 BitsPerPixel (שחור לבן).
- TiffExpectedFormat.TiffNoCompressionRGB: ספציפי לפורמט TIFF ללא דחיסה בעת שמירת התוצאה בפורמט RGB (צבע).
- TiffExpectedFormat.TiffNoCompressionRGBA: ספציפי לפורמט TIFF ללא דחיסה בעת שמירת התוצאה בפורמט RGBA (צבע עם שקיפות).



קטע הקוד הנ"ל מסביר את השימוש בשד
