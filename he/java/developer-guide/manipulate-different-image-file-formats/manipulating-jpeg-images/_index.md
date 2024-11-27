---
title: עיבוד של תמונות JPEG
type: תיעוד
weight: 20
url: /he/java/manipulating-jpeg-images/
---

## **שימוש במחלקת ExifData כדי לקרוא ולשנות תגי EXIF של JPEG**

כמעט כל המצלמות הדיגיטליות (כולל סמארטפונים), סורקים ומערכות אחרות המתעסקות בתמונות שומרות תמונות עם מידע EXIF (החלפת קובץ תמונה). הגדרות המצלמה ומידע על הסצינה מתוודגים על ידי המצלמה לקובץ התמונה. נתוני ה-EXIF כוללים גם את מהירות הסגירה, תאריך ושעה בה נלקחה התמונה, אורך עדשה, פיצוי לחשיקה, תבנית מדידה והאם נעשה שימוש בפנס. ממשקי Aspose.Imaging הפכו אפשרי לחלץ את המידע ה-EXIF מתמונה נתונה בצורה קלה ופשוטה מאוד. מפתחים יכולים גם לכתוב נתוני EXIF לתמונות או לשנות את המידע הקיים כפי שמתאים להם. Aspose.Imaging סיפקה מחלקת ExifData לקריאה, כתיבה ושינוי נתוני ה-EXIF, כאשר מרחב התיבות Aspose.PSD.Exif.Enums מכיל את התיבות המתאימות המשמשות בתהליך.
### **קריאת נתוני EXIF**
ממשקי Aspose.PSD מספקים דרכים לקרוא נתוני EXIF מתמונה נתונה. בשלבים שניתן לראות למטה מתאר השימוש בכיתת ExifData לקריאת המידע EXIF מתמונה.

- טען תמונת PSD באמצעות שיטת הפעלה Load.
- מצא תמונת תצוגה של JPEG בתוך המשאבים של PSD.
- חלץ מופע של מחלקת ExifData.

לקחת מהמידע הנדרש ולכתוב אותו לקונסולה.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}




בנוסף, מפתחים יכולים גם לקבל את המידע המסוים באמצעות קטע הקוד הבא.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **כתיבה ושינוי נתוני EXIF**
באמצעות ממשקי Aspose.PSD, מפתחים יכולים לכתוב מידע EXIF חדש ולשנות את הנתונים הקיימים של ה-EXIF בתמונה. שני התהליכים (כתיבה ושינוי) מחייבים טעינת תמונה וקבלת נתוני ה-EXIF לתוך מופע של ExifData. לאחר מכן ניתן לגשת לנכסים שנפתחו על ידי מחלקת ExifData כדי להגדיר אותם בהתאם. יש לשים לב כי תמונות לטיפול צריכות להיות תמונות JPEG או TIFF הנמצאות כמעט תמיד בתמונות ממוזערות של PSD. הקוד המדגים את השימוש אחראי הוא כדלהלן:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **חילוץ תמונות ממשאבי PSD**
תמונות ממוזערות הן גרסאות ממוזערות של תמונות, המשמשות כדי להציג חלק חשוב מהתמונה במקום מסגרת מלאה. קבצי תמונה מסוימים (במיוחד אלה שצולמו באמצעות מצלמה דיגיטלית) מכילים תמונת ממוזערת מוטבעת בקובץ. ממשק ה-Aspose.PSD מאפשר לחלץ תמונות ממוזערות שבמשאבי PSD ולשמור אותן בנפרד על דיסק. משאבי הממוזערות מכילים את הנכס ExifData.Thumbnail שיכול לחזור על הנתונים הממוזערים. קטע הקוד המסופק למטה מדגים כיצד להשתמש בזה.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



השתמשו בשיטה המדוברת לשמור את התמונה הממוזערת לפורמטי קבצים נתמכים אחרים. אם אתם רוצים לייצא נתוני ממוזערת לפורמטי קבצים אחרים כגון BMP & PNG, השתמשו באפשרויות ייצוא תמונה אחרות.
### **חילוץ תמונות מחלקי JFIF**
כמה.roمתיק לחלץ תמונות מחלקי ExifData או JFIF של משאבי תמונות ממוזערות של PSD. הקוד הבא מראה איך לבצע את החילוץ של נתונים מממוזערת מחלק JFIF או ExifData:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



השתמשו בגישה שדובר עליו לשמור את התמונה הממוזערת לפורמטי קבצים נתמכים אחרים. אם ברצונכם לייצא את נתוני התמונה הממוזערת לפורמטי קובץ אחרים כגון BMP & PNG, השתמשו באפשרויות ייצוא תמונות אחרות.
### **הוספת ממוזערת לחלק JFIF**
קטע הקוד למטה מדגים כיצד להשתמש בנכס JFIF.Thumbnail כדי להוסיף תמונת ממוזערת לחלק ה-JFIF של תמונת PSD שנטענת.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}


תמונות ממוזערות עם נתונים ממזגי נתונים אחרים לא יכולות לצפות יותר מ-121,545 בתים עקב המפרטים של תבניות ה-JPEG. במקרים שבהם רוצים להגדיר תמונות גדולות כממוזערות, עשוי לצאת חריגה.
### **הוספת ממוזערת לחלק EXIF**
הקטע הבא מדגים כיצד להשתמש בנכס ExifData.Thumbnail כדי להוסיף תמונת ממוזערת לחלק ה-EXIF של תמונת PSD שנטענת.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-as-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}


במקרה זה, ממשקי Aspose.PSD לא יכולים לשער את גודל התמונה הממוזערת, אך הם יכולים לבדוק את גודל כל החלק של נתוני ה-EXIF. החלק הזה לא יכול להיות גדול מ-65,535 בתים.
## **שימוש במחלקת JpegExifData כדי לקרוא ולשנות תגי EXIF של JPEG**
ממשקי Aspose.PSD מספקים מחלקת JpegExifData הבלעדית לפורמטי תמונה JPEG לחזרה ועדכון של מידע EXIF. המאמר הזה מדגים את השימוש במחלקת JpegExifData כדי להשיג את התוצאה הזו. מחלקת Aspose.PSD.Exif.JpegExifData משמשת כמכולת נתוני EXIF עבור תמונות JPEG, ומספקת דרכים לחליטת תגי EXIF סטנדרטיים של JPEG כפי שמודגם מטה:



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **רשימה מלאה של תגי EXIF**
קטע הקוד לעיל קורא כמה תגי EXIF באמצעות הנכסים שמציעה מחלקת Aspose.PSD.Exif.JpegExifData. רשימה מלאה של הנכסים הללו זמינה כאן. הקוד הבא יקרא את כל תגי ה-EXIF באמצעות מחלקת System.Reflection.PropertyInfo.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **תיקון אוטומטי של כיוון התמונות בפורמט JPEG**
תמונות ניתן לצלם עם מצלמה שסובבת ב-90°, 180°, 270° או בלי (כיוון הרגיל). רוב המצלמות הדיגיטליות שומרות מידע על הכיוון יחד עם נתוני התמונה כתגי EXIF בתמונות ה-JPEG. מידע זה ניתן לשימוש כדי לב
