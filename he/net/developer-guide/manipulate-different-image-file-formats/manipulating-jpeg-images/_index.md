---
title: Manipulating JPEG Images
type: docs
weight: 30
url: /he/net/manipulating-jpeg-images/
---

## **שימוש במחלקת ExifData לקריאה ושינוי תגי EXIF של Jpeg**
רוב מצלמות הדיגיטל (כולל סמארטפונים), סורקים ומערכות אחרות שמטפלות בתמונות שומרות תמונות עם מידע EXIF (קובץ תמונה המתוחלף). הגדרות המצלמה ומידע על הסצנה נרשמים על ידי המצלמה בקובץ התמונה. מידע EXIF כולל גם מהירות שערוך, תאריך ושעה בה צולמה התמונה, אורך מוקד, פיצוי חשיפה, דפוס מדידת חשיפה והאם נעשה שימוש בפלאש. ממשקי Aspose.Imaging APIs הפכו את תהליך חליצת מידע ה-EXIF מתמונה נתונה לתהליך קל ופשוט מאוד. מפתחים יכולים גם לכתוב נתוני EXIF לתמונות או לשנות את המידע הקיים כפי שנדרש. Aspose.PSD סיפקה מחלקת **[ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata)** לקריאה, כתיבה ושינוי של מידע ה-EXIF, בעוד שתחום ה- [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) מכיל את הרשימות הרלוונטיות המשמשות בתהליך.
### **קריאת מידע EXIF**
ממשקי ה-Aspose.PSD מאפשרים לקרוא את מידע ה-EXIF מתמונה נתונה. השלבים הבאים ממחישים את השימוש במחלקת ExifData לקריאת המידע ה-EXIF מתמונה.

- טעינת תמונת PSD באמצעות שיטת ה-factory Load.
- מציאת תמונת Jpeg ממתוך משאבי PSD.
- חילוץ מופע של מחלקת ExifData.

קח את המידע הדרוש וכתוב אותו לקונסולה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}


בנוסף, מפתחים יכולים גם לקבל את המידע הספציפי באמצעות הקטע הקוד הבא.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **כתיבה ושינוי מידע EXIF**
בעזרת ממשקי Aspose.PSD, מפתחים יכולים לכתוב מידע EXIF חדש ולשנות מידע EXIF קיים בתמונה. שני הבתהליכים (כתיבה ושינוי) דורשים טעינת תמונה והבאת נתוני EXIF לתוך מופע ממחלקת ExifData. לאחר מכן ניתן לגשת לתכונות שגשר עליהן ממחלקת ExifData כדי להגדיר אותן בהתאם. נא לשים לב שתמונות לצורך עיבוד שולפות להיות תמונות Jpeg או Tiff עליהן קנאפים בדרך כלל. הקוד לדוגמה להרצת השיטה נמצא להלהלן:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **חילוץ של תמונת-תצלום ממשאבי PSD**
תמונות-תצלומות הן גרסאות ממוזערות של תמונות, משמשות לתצוגה של חלק חשוב מהתמונה במקום המסגרת המלאה. קבצי תמונה מסוימים (במיוחד הנצולדים במצלמה דיגיטלית) מכילים תמונה-תצלום מוטבעת בקובץ. ממשק ה-Aspose.PSD מאפשר לך לחלוץ תמונות-תצלום ממשאבי PSD ולשמור אותן בנפרד על הדיסק. משאבי-תמונת-תצלום מכילים פרופרטי **[תמונת-תצלום](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail)** שמכילים את נתוני התמונת-תצלום. הטקסט הקודי שמופיע להלן מדגים איך ניתן להשתמש בו.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

השתמש בשיטה המבוססת שנדוססה לשמירת תצוגת-תמונה בפורמטי קובץ אחרים. אם ברצונך לייצא נתוני תמונת-תצלום לפורמטים תמונה אחרים כגון BMP ו-PNG, אנא עשה שימוש באפשרויות ייצוא תמונה אחרות.
### **חליץ תמונה-תרשימה ממשאבי JFIF**
כן אפשר גם לחלץ תמונת-תרשימה מהמחלקת ExifData או מהרכיב JFIF של משאבי תמונת-תרשימה של PSD. הקוד הבא מוצג כיצד לבצע את פעולת חילוץ מידע התמונה-תרשימה מהרכיב JFIF או ExifData:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}

השתמש בשיטה המבוססת על דמוי לשמירת תצוגת-תמונה בפורמטי קובץ אחרים. אם ברצונך לייצא נתוני תמונת-תרשימה לפורמטים תמונה אחרים כגון BMP ו-PNG, נא להשתמש באפשרויות ייצוא תמונה אחרות.
### **הוספת תמונת-תרשימה לרכיב JFIF**
הקטע הקודי למטה מדגים כיצד להשתמש בפרופרטי התמונה-תרשימה של JFIF כדי להוסיף תמונת-תרשימה לרכיב JFIF של תמונת PSD שנטענת.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}

תמונות-תרשימה יחד עם נתוני רכיב אחר לא יכולות להוריד יותר מ-65,545 בתים בשל תקנות פורמט ה-JPEG. במקרים בהם נדרש להגדיר תמונות גדולות כעתמתים, יכולה להופיע יוצאת דופן.
### **הוספת תמונת-תרשימה לרכיב EXIF**
הקטע הקודי למטה מדגים כיצד להשתמש בפרופרטי התמונה-תרשימה של ExifData על מנת להוסיף תמונת-תרשימה לרכיב ה-EXIF של תמונת PSD שנטענת.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}

במקרה זה, ממשק ה-Aspose.PSD לא יכול לאפס את גודל התמונת-תרשימה, אך הוא יכול לבדוק את גודל רכיב הנתוני EXIF כולו. לא יכול להיות רכיב זה יותר מ-65,535 בתים.
## **שימוש במחלקת JpegExifData לקריאה ושינוי תגי EXIF של תמונות Jpeg**
ממשקי Aspose.PSD מספקים מחלקת [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) שמיועדת בלעדית לתבניות תמונה Jpeg לחדור ולעדכן את מידע ה-EXIF. מאמר זה מדגים את שימוש במחלקת JpegExifData להשגת התוצאה הנדרשת. מחלקת Aspose.PSD.Exif.JpegExifData משמשת כמחזיק נתוני EXIF עבור תמונות Jpeg, ומספקת דרכים לאחזרת תגי Jpeg EXIF תקניים כפי שמוצג למטה:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-C-AsposingAndXJPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **רשימה מלאה של תגי EXIF**
הקוד הבא קורא מעט תגי EXIF באמצעות הפרופריות שמציעה מחלקת Aspose.PSD.Exif.JpegExifData. רשימה מלאה של פרופרטיים אלו זמינה כאן. הקוד להלן יקרא את כל התגי EXIF באמצעות [מחלקת System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0).

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-C-AsposingAndXJPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **תיקון אוטומטי של כיוון התמונה בתמונות Jpeg**


יתכן שתמונות תופסות במצלמה שהוסבה ב-90°, 180°, 270° או שאינה הוסבה כלל (כיוון רגיל).
