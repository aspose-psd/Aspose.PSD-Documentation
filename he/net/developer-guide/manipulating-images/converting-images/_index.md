---
title: המרת תמונות
type: מסמך
weight: 20
url: /he/net/converting-images/
---

## **המרת תמונות לשחור לבן ולגווני גרייסקייל**
לפעמים עשויים להיות צורך להמיר תמונות צבעוניות לתמונות שחור לבן או גרייסקייל למטרות הדפסה או ארכיבה. מאמר זה מדגים את השימוש ב-API של Aspose.PSD ל-.NET כדי להשיג זאת באמצעות שתי שיטות כפי שמתוארות להלן.

- המרת Binarization
- Grayscaling
### **המרת Binarization**
כדי להבין את המושג של Binarization, חשוב להגדיר תמונה בינרית; זו תמונה דיגיטלית שיש לה רק שני ערכים אפשריים עבור כל פיקסל. כללית, הצבעים שנמצאים בשימוש עבור תמונת בינרית הם שחור ולבן, אך יתכן להשתמש בכל צמד צבעים. Binarization היא התהליך של המרת תמונה לרמה כפולה, המשמרת שפיקסל כלשהו מאוחסן כביט אחד (0 או 1) שכאשר 0 מציין חסרון צבע ו-1 אומר קיום צבע. באמצעות API של Aspose.PSD ל-.NET יש תמיכה נוכחית בשתי שיטות Binarization.
#### **Binarization עם אחזור קבוע**
קטע הקוד הבא מראה איך ניתן להשתמש בחיזוק האחזור הקבוע על מנת ליישם אותו על תמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **Binarization עם אחזור Otsu**
קטע הקוד הבא מראה איך ניתן להשתמש בחיזוק האחזור Otsu על מנת ליישם אותו על תמונה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **Grayscaling**
גרייסקייל (חורז) היא התהליך של המרת תמונת טון-רציפים לתמונה עם גווני אפור דיסקונטינואים. קטע הקוד הבא מראה איך ניתן להשתמש בגרייסקייל.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Garysacling-Garysacling.cs" >}}
## **המרת שכבות תמונת GIF לתמונת TIFF**
לפעמים נדרש לחלץ ולהמיר שכבות של תמונה PSD לתבנית תמונה רסטר נוספת על מנת לעמוד בצורך של אפליקציה. API של Aspose.PSD תומך ביכולת לחלץ ולהמיר שכבות של תמונה PSD לתבנית תמונה רסטר נוספת. לרשותנו תמיד ליצור מופע של תמונה ולטעון תמונת PSD מהכונן הקשיח המקומי, אז נעבור על כל שכבה בנכס השכבה. לאחר מכן נמיר את הבלוק לתמונת TIFF. קטע הקוד הבא מראה איך להמיר שכבות של תמונה PSD לתמונות TIFF.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}
## **המרת מקובץ CMYK PSD לקובץ CMYK TIFF**
באמצעות Aspose.PSD ל-.NET, מפתחים יכולים להמיר קובץ CMYK PSD לתבנית tiff בצבעים CMYK. מאמר זה מציג איך לייצא/להמיר קובץ CMYK PSD לתבנית tiff CMYK עם Aspose.PSD. באמצעות Aspose.PSD ל-.NET ניתן לטעון תמונות PSD ולהגדיר מאפיינים שונים באמצעות ה-[TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) class ולשמור או לייצא את התמונה. קטע הקוד הבא מראה איך להשיג את התכונה הזאת.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}
## **יצוא תמונות**
בנוסף למערך עשיר של רוטינות עיבוד תמונה, Aspose.PSD מספק כיתות מובחנות להמרת פורמטי קבצים PSD לפורמטים אחרים. באמצעות ספריית זו, המרת תמונות PSD היא פשוטה ואינטואיטיבית מאוד. להלן כמה כיתות מובחנות לכך ב- [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

קל לייצא תמונות PSD עם Aspose.PSD ל-.NET API. הכל מה שנדרש הוא אובייקט של המחלקה הרלוונטית מתוך [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) namespace. באמצעות המחלקות הללו, ניתן בקלות לייצא כל תמונה שנוצרה, נערכה או פשוט נטענה עם Aspose.PSD ל-.NET לכל פורמט הנתמך.
## **שילוב תמונות**
דוגמא זו משתמשת במחלקת Graphics ומראה כיצד לשלב שתי או יותר תמונות לתוך תמונה שלמה אחת. להדגים את הפעולה, הדוגמה יוצרת PsdImage חדש ומרקמת תמונות על גבי פני הקנבס באמצעות שיטת Draw Image המוצגת על ידי מחלקת Graphics. באמצעות מחלקת Graphics ניתן לשלב שתי או יותר תמונות באופן שהתמונה התוצאתית תיראה כתמונה מלאה בלי רווחים בין חלקי התמונה וללא עמודות. גודל הקנבס חייב להיות שווה לגודל התמונה התוצאתית. באילו־כדי יש המחזור המוצג שמראה כיצד להשתמש בשיטת [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) של מחלקת [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) על מנת לשלב תמונות בתמונה אחת.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}
## **הרחבה וחיתוך תמונות**
API של Aspose.PSD מאפשר רחבה או חיתוך של תמונה במהלך תהליך ההמרה של התמונה. המפתח צריך ליצור ריבוע עם ציר X ו-Y שואפים, ולציין את רוחב וגובה של תיבת המלבן. ערכי ה-X, Y ורוחב, גובה של הריבוע יתארו את הרחבה או החיתוך של התמונה שנטענת. אם נדרש להרחיב או לחתוך את התמונה במהלך ההמרה של התמונה, יש להינות מהשלבים הבאים:

1. צור מופע של מחלקת [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) וטען את התמונה הקיימת.
1. צור מופע של מחלקת ImageOption.
1. צור מופע של [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) class ואתחל את ערכי ה-X, Y ורוחב, גובה של תיבת המלבן.
1. קרא ל-[Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) method של מחלקת RasterImage בעת מעבר שם קובץ פלט, אפשרויות תמונה ואובייקט ריבוע כפרמטרים.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}
## **קריאה וכתיבת נתוני XMP לתמונות**
XMP (פלטפורמת מטא-נתונים המתרחבת) הוא תקן של ISO. XMP מסטנדרדיז את מודל הנתונים, פורמט הסידור ותכונות הליבה להגדרת ועיבוד של מטא-נתונים הניתנים להרחבה. הוא מספק כללי הנחייה להשבתת מידע XMP לתוך תמונה פופולרית כדי לא לשבר את קריאותיהן של יישומים שאינם תומכים ב-XMP. באמצעות Aspose.PSD ל-.NET API, מפתחים יכולים לקרוא או לכתוב מטא-נתוני XMP לתמונות. מאמר זה מדגים איך ניתן לקרוא מטא-נתוני XMP
