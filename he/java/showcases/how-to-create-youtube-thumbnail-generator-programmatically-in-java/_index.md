---
title: כיצד ליצור מחולל תמונות קטעי YouTube באופן תוכנתי ב-Java
type: docs
weight: 10
url: /he/java/how-to-create-youtube-thumbnail-generator-programmatically-in-java/
---

## **הקדמה**
מטרת המסמך הזה היא להדגים את שימוש ה- API של כלי הקומפוננטות [Aspose.PSD עבור Java](https://products.aspose.com/psd/java) על דוגמה מעולם האמיתי. במאמר זה, **תוכנית Java פשוטה שיוצרת קטעי תמונה מהתצוגה של YouTube** עבור ערוץ המסמכים האחרוניים והכלים הבאים בוצעים ונסברים. במאמר זה, הופרט ערוץ זה הואשם מעולם האמיתי מאחר ותמונותיו הן די סטנדרטיות, והן ממחישות את השימוש בכלי הקומפוננטות הפופולריים של Aspose.PSD עבור Java (לדוגמה: אפקט צל [אחים](/psd/he/java/manipulating-photoshop-formats/#manipulatingphotoshopformats-supportdropshadoweffect), מילוי דרקון, שרטוט טקסט וצורות):

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_1.png)

## **איך זה עובד בקצרה**
תוכנית Java פשוטה מקבלת שני ארגומנטים: תיאור ותמונה. מסמך פוטושופ (PSD) בקפיץ **נוצר מהקלט הזה** באמצעות Aspose.PSD עבור Java. לאחר מכן, **התוכנית ממירה את המסמך מ-PSD לתבנית PNG** כדי לקבל קטעי יוטיוב בגודל של 1280x720 פיקסלים. התמונה המוצאת נראית כמו הבאה:

![todo:image_alt_text](how-to-create-youtube-thumbnail-generator-programmatically-in-java_2.png)

## **דרישות טכניות**
הטכנולוגיות הבאות נדרשות להצלחה בהרצת הקוד של מאמר זה:

- Java 6+
- [Aspose.PSD עבור Java](/psd/he/java/installation/) (האחרון)

## **התחלה**
כמו שכבר נאמר, התוכנית משתמשת ב-PSD בזיכרון פנימי כדי ליצור קטע. לכן, נתחיל **ביצירת מסמך PSD**:

```java
PsdImage psdImage = new PsdImage(1280, 720);
```

אם תביט טוב יותר בקטע היוטיוב מעלה, תוכל לשים לב ש**הוא מורכב מכמה רכיבים**:

1. תמונת רקע (מסכית מודפסת)
1. מילוי פסד רדיאלי (מדגיש את האזור בפינת מימין למעלה)
1. לוגוטיפ עם אפקט צל
1. כיתוב ושרטוט פשוט (מלבן כחול)

בוא נעזוב עמוק יותר כדי לראות איך לממש כל אחד מהרכיבים הללו באמצעות Aspose.PSD עבור Java במדורים הבאים.

## **1. הוספת תמונת רקע**
סדר השכבות חשוב. לכן, יש להוסיף תמונת רקע תחילה כדי לא לחפוף שכבות אחרות. שים לב שרק [תבניות קובץ רסטר](/psd/he/java/supported-file-formats/) נתמכות כעת.

### **1.1. הוספת תמונת רקע לשכבת פוטושופ**
כדי **להוסיף תמונה רסטר לתוך PSD**, יש להעביר זרם המידע כארגומנט במהלך בניית השכבה (ראה עוד [דוגמאות נוספות לטעינת תמונות רסטר](https://docs.aspose.com/display/psdnet/Creating%2C+Opening+and+Saving+Images)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-1.java" >}}
```

1.2. התאמת תמונת רקע לקנבס

הפעולות הבאות שתיים (שינוי גודל, תיקון מיקומים) שימושיות למקרים בהם **גודל התמונה שונה מגודל הקנבס**, אף על פי שבמאמר זה התמונה באותה גודל כמו הקנבס (נוח להניח כי זה לא תמיד יהיה כך).

ודא שהתמונה שהועלתה **מתאימה** ל**גודל הקנבס** (ראה עוד [דוגמאות לשינוי גודל](https://docs.aspose.com/display/psdnet/Crop%2C+Rotate+and+Resize+Images#Crop,RotateandResizeImages-ResizingImages)):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-2.java" >}}
```

לאחר ששינוי הגודל, המיקום של התמונה משתנה. לכן, כדי **לאפס את המיקום של התמונה**, יש להעביר את התמונה ששונתה לפינה השמאלית העליונה:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-3.java" >}}
```

## **2. הוספת בלט רדיאלי**
קיימות **שתי דרכים להוסיף בלט רדיאלי**, באמצעות:

- אפקט גרדיינט שכבה ([על הגרזן](/psd/he/java/aspose-psd-for-java-20-4-release-notes/#-~-text=psdjava-163)) על שכבה קיימת (פעולת גרזיינט שכבתית שחברה לשכבה הנוכחית ומיישמת לתוככה)
- שכבת מילוי גרדיינט חדשה ([תמיכה בשכבות מילוי](/psd/he/java/support-of-fill-layers/#supportoffilllayers-supportoffilllayerswithgradientfill)) (שכבה נפרדת ששומרת תצורת גרדיינט עצמאית)

מספיק להשתמש באפקט גרדיינט שכבה לדוגמה זו. בכדי להביא יתרה למאמר זה **שימשו כרטיס פסד גרדיינט** מאחר וכל יתרות השכבות מיישמות בדרך דומה כשתפעלנ השכבת אפקט זיהה על בסיס המידע הנוכחי של התמונה.
### **2.1. Add a radial gradient fill layer**
תהליך הוספת שכבת מילוי גרדיינט חדשה מתחיל מהשלבים הבאים 2:

1. חייבים **להצהיר על תצורת מילוי גרדיינט** מאחר ואין דברים מוגדרים מראש. הגדרת המינימום הנדרש נראית כך (תבונה שסוג הגרדיינט, הקנה, נקודות הצבע והשקפת השקיפות הן מאפיינים נדרשים):

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-4.java" >}}
```

הגדרת המינימום מעלה גרדיינט רדיאלי שהוא שקוף בקצוות וכחול כהה במרכז. המקום של הגרדיינט נמצא באמצע הקנבס כברירת מחדל.

כדי להפוך את מילוי הגרדיינט ולהזיז אותו לשני הפינה הימינית העליונה כדי להשתמש בנכסים אופציונאליים מתאימים:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-5.java" >}}
```

2. כשההגדרה הושלמה, עלינו להוסיף שכבת מילוי גרדיינט כולל הגדרות שלה לתוך ה-PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-6.java" >}}
```

## **להוסיף לוגוטיפ עם אפקט שקיפה**
ה**ציליית נפילה** היא אפקט שמאפשר להוסיף צל נתמך מותאם אישית לגבול הפריט (תמונה, טקסט וכו ').
### **3.1. הוספת לוגוטיפ לשכבת פוטושופ**
התקופה אל מוד כמו בקטע 1.1. ניתן להשתמש בהכנסת לוגוטיפ לתוך ה-PSD:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-7.java" >}}
```

### **3.2. פוזיציית הלוגוטיפ**
התמונה שהועלתה דבוקה בקצה השמאלי העליון לפי ברירת המחדל. אולם, מסבירים **נדרשים להוסיף** מרגינים **כדי שייראה כמו תמונה אורכת בערוץ היוטיוב המקורי**. לכן, יש להזיז את מיקום התמונה כדי לרחם מהקצוות של השכבה:

```java
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-YouTubeThumbnailGenerator-Snippet-8.java" >}}
```

### **3.3. הוסיפת אפקט שקיפה ללוגוטיפ**
הלוגוטיפ יכול להיות בלתי נראה במקרה שבו משתמשים בתמונת רקע בהירה. לכן, משתמש