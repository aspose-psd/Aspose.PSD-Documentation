---
title: המרת תמונות
type: docs
weight: 20
url: /he/java/converting-images/
---

## **המרת תמונות לשחור לבן וגווני אפור**
לפעמים עשויים להיות נדרשים להמיר תמונות מצבעוניות לשחור לבן או גווני אפור לצורך הדפסה או ארכובת. מאמר זה מדגים את השימוש ב-Aspose.PSD עבור API Java כדי להשיג זאת באמצעות שימוש בשני שיטות כפי שמצוין להלן.

- הבינריזציה
- יישוא

### **הבינריזציה**
על מנת להבין את המושג של הבינריזציה, חשוב להגדיר תמונת בינארית; תמונת דיגיטלית שיש לה שני ערכים אפשריים רק לכל פיקסל. בדרך כלל, שתי הצבעים המשמשים בתמונת בינארית הם שחור ולבן אך אפשר להשתמש בכל שתי צבעים. הבינריזציה היא תהליך של המרת תמונה לרמה אחת המשמרת שמירה אחת (0 או 1) שבה 0 מציין חיסור צבע ו-1 אומר שקיימת צבע. Aspose.PSD עבור API Java תומך כיום בשתי שיטות הבינריזציה.

#### **הבינריזציה עם סף קבוע**
הקטע קוד הבא מראה כיצד להשתמש בהבינריזציה עם סף קבוע שיכולה להיות מיושמת לתמונה.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.java" >}}

#### **הבינריזציה עם סף Otsu**
הקטע קוד הבא מראה כיצד ניתן ליישם הבינריזציה עם סף Otsu לתמונה.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.java" >}}

### **יבוא**
הגווניות היא תהליך של המרת תמונת טונים רציפים לתמונה עם גוונים אפורים מנותקים. הקטע קוד הבא מראה כיצד להשתמש בגווניות.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GrayScaling-GrayScaling.java" >}}

## **המרת שכבות תמונת GIF לתמונת TIFF**
לפעמים יש צורך לחלץ ולהמיר שכבות של תמונת PSD לתוך פורמט תמונה רסטר נוסף להתאמה לצורך יישום. API של Aspose.PSD תומך ביכולת לחלץ ולהמיר שכבות של תמונת PSD לתוך פורמט תמונה רסטר אחר. לפני כן ניצור מופע של תמונה ונטען את תמונת PSD מתוך התיקייה המקומית, ואז נעבור על כל שכבה במאפיין השכבה. לאחר מכן נמיר את הבלוק לתמונת TIFF. הקטע קוד הבא מראה כיצד להמיר שכבות תמונת PSD לתמונות TIFF.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.java" >}}

## **המרת CMYK PSD ל- CMYK TIFF**
באמצעות Aspose.PSD עבור ג'אווה, מפתחים יכולים להמיר קובץ CMYK PSD לפורמט CMYK tiff. מאמר זה מציג איך לייצא / להמיר קובץ CMYK PSD לפורמט TIFF CMYK באמצעות Aspose.PSD. באמצעות Aspose.PSD עבור ג'אווה ניתן לטעון תמונות PSD ואז ניתן להגדיר שכבות שונות באמצעות מחלקת TiffOptions ולשמור או לייצא את התמונה. הקטע קוד הבא מראה כיצד להשיג מאפיין זה.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.java" >}}

## **ייצוא תמונות**
בנוסף לסט עשיר של פעולות עיבוד תמונות, Aspose.PSD מספק כיתות מיוחדות ליצירת ממשק עבור פורמטי קובץ PSD לפורמטים אחרים. בשימוש בספרייה זו, ייצוא תמונות PSD הוא פשוט ואינטואיטיבי. להלן מספר כיתות מיוחדות לצורך זה במרחב השמות ImageOptions.

- BmpOptions
- GifOptions
- JpegOptions
- Jpeg2000Options
- TiffOptions
- PngOptions

פשוט לייצא תמונות PSD עם Aspose.PSD עבור API Java. כל מה שנדרש הוא אובייקט של המחלקה המתאימה במרחב השמות ImageOptions. באמצעות שימוש במחלקות אלה, ניתן בקלות לייצא כל תמונה שנוצרה, נערכה או פשוט נטענה עם Aspose.PSD עבור Java לכל פורמט נתמך.

## **שילוב תמונות**
דוגמה זו משתמשת במחלקת Graphics ומראה כיצד לשלב שתי או יותר תמונות לתוך תמונה שלמה אחת. כדי להדגיש את הפעולה, הדוגמה יוצרת PsdImage חדש ומשתמשת בשיטת Draw Image המוצגת על ידי המחלקה Graphics. באמצעות מחלקת Graphics ניתן לשלב שתי או יותר תמונות בדרך שהתמונה הנובעת תיראה כתמונה שלמה ללא רווחים בין חלקי התמונה וללא עמודות. גודל הקנבס חייב להיות שווה לגודל התמונה הנוצרת. הנה דמיון קוד המדגים איך להשתמש בשיטת Draw Image של מחלקת Graphics כדי לשלב תמונות בתמונה אחת.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CombiningImages-CombiningImages.java" >}}

## **הרחבה וחיתוך תמונות**
API של Aspose.PSD מאפשר להרחיב או לחתוך תמונה במהלך תהליך ההמרה של התמונה. מפתח צריכה ליצור מלבן עם צירים X ו-Y ולציין את רוחב וגובה של תיבת המלבן. הווט X,Y ו-Width, Height של המלבן יתארו את ההרחבה או החיתוך של התמונה שנטענת. אם נדרש להרחיב או לחתוך את התמונה במהלך ההמרה של התמונה, יש לבצע את השלבים הבאים:

1. ליצור מופע של מחלקת RasterImage ולטעון את התמונה הקיימת.
1. ליצור מופע של ImageOption class.
1. ליצור מופע של מחלקת Rectangle ולאתחל את צירי ה-X וה-Y ואת רוחב וגובה של תיבת המלבן.
1. לקרוא לשיטת Save של מחלקת RasterImage תוך העברת שם קובץ פלט, אפשרויות תמונה ואובייקט המלבן כפרמטרים.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-ExpandAndCropImages-ExpandAndCropImages.java" >}}

## **קריאה וכתיבה של נתוני XMP לתמונות**
XMP (מיתגר נתונים מורחב) הוא תקן של תותח ופלת נתונים מורחבים. XMP מסתקרן מודל נתונים, פורמט סידור ומאפיינים יסודיים להגדרת ועיבוד של נתוני מטא נרחבים. הוא גם נותן הנחיות להטמעת מידע XMP בתמונות פופולריות כגון JPEG, מבלי לפגוע בקריאות שלהן על ידי היישומים שאינם תומכים ב-XMP. באמצעות Aspose.PSD עבור API Java מפתחים יכולים לקרוא או לכתוב מטא נתונים XMP לתמונות. מאמר זה מדגים כיצד ניתן לקרוא מטה נתוני XMP מתוך תמונה ולכתוב מטה נתוני XMP לתמונות.

### **יצירת מטה נתוני XMP, כתיבתם וקריאה מתוך קובץ**
עם עזרת המרחב שמות XMP, מפתח יכול ליצור אובייקט מטה נתונים XMP ולכתוב אותו לתמונה. הקטע קוד הבא מראה כיצד להשתמש בחביבי XmpHeaderPi, XmpTrailerPi, XmpMeta, XmpPacketWrapper, PhotoshopPackage ו-DublinCorePackage הכלולים במרחב שמות XMP.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-DrawingAndFormattingImages-CreateXMPMetadata-CreateXMPMetadata.java" >}}

##
