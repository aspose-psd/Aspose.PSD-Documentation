---
title: התקנה
type: docs
weight: 40
url: /he/java/installation/
---

## **התקנת Aspose.PSD עבור Java ממאגר Maven**
Aspose מארחת את כל ממשקי ה- Java על מאגר ה-Maven. תוכל להשתמש בקלות ב- [Aspose.PSD עבור Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) ישירות בפרויקטי Maven שלך עם הגדרות פשוטות.

### **ציין תצורת מאגר Maven**
ראשית, עליך לציין את תצורת/המיקום של מאגר Maven של Aspose בקובץ ה-pom.xml שלך כדלקת:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}

### **ציין תלות ב-API של Aspose.PSD עבור Java**
לאחר מכן, ציין תלות ב-API של Aspose.PSD עבור Java ב-pom.xml שלך כדלקת:

{{< highlight java >}}

 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-psd</artifactId>
        <version>24.2</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>

{{< /highlight >}}

לאחר ביצוע השלבים הנ"ל, התלות ב-Aspose.PSD עבור Java תהיה סופית בפרויקט Maven שלך.

## **פלטפורמות נתמכות**
Aspose.PSD עבור Java תומך בפלטפורמות הפיתוח וההפצה הפופולריות ביותר.

|**תכונה**|**תיאור**|
| :- | :- |
|יישומי שולחן העבודה|Aspose.PSD עבור Java יכולה לשמש לפיתוח של יישומי שולחן העבודה ב-Windows.|
|יישומי רשת ארגוניים|Aspose.PSD עבור Java תומכת באופן מלא באפליקציות רשת.|
|Linux/Unix|Aspose.PSD עבור Java היא API תלת-פלטפורמה ויכולה לעבוד בסביבת Linux ו-Unix.|

## **גרסאות Java נתמכות**
- JDK 1.6 או גבוהה יותר
