---
title: הערות לגרסה Aspose.PSD for Java 20.5 - Release Notes
type: docs
weight: 40
url: /he/java/aspose-psd-for-java-20-5-release-notes/
---

{{% alert color="primary" %}} דף זה מכיל את ההערות לגרסה של [Aspose.PSD for Java 20.5](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.5/) {{% /alert %}} 

|**מפתח**|**סיכום**|**קטגוריה**|
| :- | :- | :- |
|PSDJAVA-188|תמיכה בהתקדמות המרת המסמך|תכונה|
|PSDJAVA-197|תמיכה בשמירת תמונת PSD במצב צבע גרייסקייל עם 16 ביט לערוץ|תכונה|
|PSDJAVA-198|תמיכה במשאב Nvrt (משאב שכבת תיקון מלהובן)|תכונה|
|PSDJAVA-200|` `תמיכה במסיכות שכבה עבור קבוצות שכבות|תכונה|
|PSDJAVA-195|תיקון שמירת תמונת PSD במצב צבע גרייסקייל עם 16 ביט לערוץ לפורמט PSD RGB ב-16 ביט לערוץ|תקלה|
|PSDJAVA-196|תיקון שמירת תמונת PSD במצב צבע גרייסקייל עם 16 ביט לערוץ לפורמט PSD גרייסקייל ב-8 ביט לערוץ|תקלה|
|PSDJAVA-199|יישור טקסט דרך ITextPortion לא עובד עבור שפות מימין לשמאל. הקובץ המוצג נפגם.|תקלה|
|PSDJAVA-201|שגיאה בעת ניסיון לפתוח קובץ Psd מסוים עם צבע Lab ו-8 ביט לערוץ|תקלה|
# **שינויים ב- API הציבוריים**
# **API שנוספו:**
- אין
## **API שהוסרו:**
- אין
# **דוגמאות שימוש:**

**PSDJAVA-188. תמיכה בהתקדמות המרת המסמך**

{{< highlight java >}}
 // דוגמה לשימוש במטפל בהתקדמות עבור פעולות טעינה ושמירה.

// התוכנית משתמשת באפשרויות שמירה שונות כדי להשתיק אירועי התקדמות.

String sourceFilePath = "Apple.psd";

ByteArrayOutputStream outputStream = new ByteArrayOutputStream();

// יצירת מטפל התקדמות שמכתב את נתוני ההתקדמות לקונסולה

ProgressEventHandler localProgressEventHandler = new ProgressEventHandler()

{

    @Override

    public void invoke(ProgressEventHandlerInfo progressInfo)

    {

        String message = String.format(

                "%s %s: %s מתוך %s",

                progressInfo.getDescription(),

                Enum.getName(EventType.class, progressInfo.getEventType()),

                progressInfo.getValue(),

                progressInfo.getMaxValue());

        System.out.println(message);

    }

}; // קשר בין מטפל התקדמות להצגת התקדמות

loadOptions.setProgressEventHandler(localProgressEventHandler);

// טוען PSD באמצעות אפשרויות טעינה ספציפיות

PsdImage image = (PsdImage)Image.load(sourceFilePath, loadOptions);

try

{

    System.out.println("---------- שומר Apple.psd ל