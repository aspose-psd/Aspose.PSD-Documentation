---
title: Manipulating תמונות TIFF
type: docs
weight: 50
url: /he/net/manipulating-tiff-images/
---

## **הוספת מסגרות עם הגדרות שונות**
תמונת TIFF היא פורמט גמיש מאוד והיא מאפשרת הוספת מסגרות שונות, עם ממדים שונים, דחיסה והגדרות אחרות. ממשקי ה-Aspose.PSD מאפשרים לך להוסיף כל מסגרת TIFF של כל גודל שיש בה ליצירת מסמכים מורכבים. אם יש דרישה להתאים את המסגרות במהלך ההוספה כך שתהיינה שוות, עליך לבצע את השלבים הבאים:

- צור מסגרת חדשה ריקה עם האפשרויות הרצויות או העתק את המסגרת המקורית עם האפשרויות הייצוא המצוינות באמצעות השיטה CreateFrameFrom
- שנה את גודל המסגרת/התמונה המקורית לממדים הרצויים באמצעות השיטה Resize
- הוסף את פיקסלי המסגרת/התמונה המקורית למסגרת החדשה
- הוסף את המסגרת החדשה לתמונת ה-TIFF המחושבת

## **ייצוא שכבות של תמונת PSD לפורמט קובץ TIFF עם מספר עמודים**
לפעמים יהיה עליך לייצא שכבות של תמונת PSD לפורמט קובץ TIFF עם מספר עמודים. מאמר זה ידגים כיצד ניתן לבצע את המשימה הזו באמצעות API של Aspose.PSD עבור .NET. ראשית, נטען את תמונת PSD מהדיסק. לאחר מכן נעבור על שכבות התמונה של תמונת PSD וניצור TiffFrame מהשכבות המתאימות. לבסוף נשמור את התמונת Tiff המתקבלת לקובץ אחד על הדיסק.

## **הגדרת אפשרויות TiffOptions**
מפתחים יכולים להתאים את אפשרויות השונות של המחלקה [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) כדי לקבל תוצאות המבוקשות. במסמך זה, נתמקד ב-4 מאפיינים ראשיים ששולטים בתכונות התמונה התוצאה.

הפרופרטים הללו מופרטים להלן.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

כאשר אנו מאתחלים מבנה ריק של TiffOptions, כל אפשרות מוגדרת על פי הערך המוגדר עבורה כברירת מחדל, למשל, דחיסה מוגדרת כאין, BitsPerSample מוגדר כ-1 ו-Photometric מוגדר כ-MinIsWhite. השמירה לפורמט זה תגרום לתמונה הסופית להיות שחורה ולבנה וזו התנהגות צפויה לתצוגה עבור קיבולות אלו. כדי לקבל תוצאות צבעוניות עליך להגדיר את כל המאפיינים שנזכרו לערכים המתאימים למרחב הצבע הרצוי או שתיתחיל את מבנה ה-TiffOptions עם הגדרות מוגדרות מראש כפי שדובר מאוחר יותר במאמר זה. בטבלה הבאה מתארים את הערכים הצפויים שניתן להגדיר על מנת להשיג תוצאות המבוקשות. יש לשים לב, עליך להגדיר את כל 4 העמודות דרך TiffOptions על מנת לשמור כל תמונה שנטענה/נוצרה לפורמט TIFF.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|לוח צבעים|LZW/לא דחוס|1/4/8/16 (לוח צבעים, מצב צבע) ערוץ יחיד בלבד|אין|
|MinIsWhite/MinIsBlack|LZW/לא דחוס|1/4/8/16 (מצב לבן שחור, מוד גוונים) ערוץ יחיד בלבד|אין|
|לוח צבעים|LZW/לא דחוס|8 (לוח צבעים, מצב צבע) ערוץ יחיד בלבד|אופקי (דחיסה נוספת מושגת ל-LZW אותם תבניות)|
|MinIsWhite/MinIsBlack|LZW/לא דחוס|8 (מצב לבן שחור, מוד גוונים) ערוץ יחיד בלבד|אופקי (דחיסה נוספת מושגת ל-LZW אותם תבניות)|
|RGB|LZW/לא דחוס|[8,8,8] (3 ערוצי RGB)|אין/אופקי|
|RGB|LZW/לא דחוס|[8,8,8,8] (3 ערוצי RGB וערוץ אלפא נוסף יכול להיגדר דרך TiffOptions.AlphaStorage) למעשה כל ספירת ערוצים נוספים נתמך אך כל ערוץ חייב להיות בגודל של 8 ביט כמו [8,8,8,8,8,8]|אין/אופקי|
כל 4 המאפיינים צריכים להיות מוגדרים דרך TiffOptions על מנת לשמור תמונה בפורמט כלשהו לתצורת TIFF. כאשר משתמשים בשילובים שונים, חלק מהתצוגות (כולל מציג הצילום של Windows) יכולים לסרב לנצות את התמונה המתקבלת עקב התמיכה המוגבלת שהם מציעים. במקרה כזה, עליך לבחור מציג שונה לצורכי הבדיקה שלך.

### **הגדרות מוגדרות מראש עבור מחלקת TiffOptions**
כדי להנגיש למשתמשים ולמנוע טעויות בהגדרת מופע של TiffOptions, ה- API של Aspose.PSD עבור .NET חשף בנאי נוסף המקבל פרמטר מסוג [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat). על פי הערך שנבחר מהרשימה של TiffExpectedFormat, הAPI מגדיר באופן אוטומטי את כל המאפיינים החובה עבור מופע TiffOptions על מנת להפיק את התוצאות המבוקשות. לפני שנמשיך לקטע הקוד הדוגמא, הנה רשימת שדותי TiffExpectedFormat והפרטים שלהם למהירות הבנה טובה יותר של השימוש.

- TiffExpectedFormat.Default: שינוי השדה ל- Default פועל באופן דומה לבנאי ברירת המחדל של מחלקת TiffOptions עם אין דחיסה מוגדרת ו-BitsPerPixel מוגדר ל-1 כדי להפיק תוצאה שחורה ולבנה. מאוד מומלץ להשתמש בשדה זה כאשר יש להגדיר מאפייני פרמט מסוימים לפי התוצאות הרצויות.
- TiffExpectedFormat.TiffCcitRle: ספציפי לקידוד RLE בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן) של TIFF.
- TiffExpectedFormat.TiffCcittFax3: ספציפי לקידוד CCITT Fax3 בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן) של TIFF.
- TiffExpectedFormat.TiffCcittFax4: ספציפי לקידוד CCITT Fax4 בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן) של TIFF.
- TiffExpectedFormat.TiffDeflateBW: ספציפי לדחיסת Deflate בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן) של TIFF.
- TiffExpectedFormat.TiffDeflateRGB: ספציפי לדחיסת Deflate בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffJpegRGB: ספציפי לדחיסת JPEG בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffJpegYCBCR: ספציפי לדחיסת JPEG בעת שמירת התוצאה בפורמט YCBCR (צבע) של TIFF.
- TiffExpectedFormat.TiffLzwBW: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן) של TIFF.
- TiffExpectedFormat.TiffLzwRGB: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט RGB (צבע) של TIFF.
- TiffExpectedFormat.TiffLzwRGBA: ספציפי לדחיסת LZW בעת שמירת התוצאה בפורמט RGBA (צבע עם שקיפות) של TIFF.
- TiffExpectedFormat.TiffNoCompressionBW: ספציפי לפורמט TIFF ללא דחיסה בעת שמירת התוצאה בפורמט אחד ביט לפיקסל (שחור ולבן).
- TiffExpectedFormat.TiffNoCompressionRGB: ספצ
