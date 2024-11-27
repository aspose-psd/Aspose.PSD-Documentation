---
title: כיצד להשתמש ב- Warp ב- Aspose.PSD
type: מסמכים
weight: 40
url: /he/net/how-to-use-warp-in-aspose-psd/
---

## **חלק 1 - עיבוד קובץ PSD עם אפקט ה-Warp**

פוטושופ שומרת את התמונה שעוברת עיבוד לאחר החלת האפקט Warp. ספרייתנו יכולה לשחזר או לעיבד מחדש את התמונה עם אפקט ה-Warp. על מנת להפעיל אפשרות זו, יש להגדיר דגל AllowWarpRepaint בהגדרות בעת פתיחת קובץ ה-PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 1](warp1.png)

בנוסף לעיבוד של האפקט Warp לשכבות חכמות, ספרייתנו תומכת גם ב-Warp עבור שכבות טקסט. קוד המימוש נשאר זהה, עם ההבדל היחיד בשם הקובץ.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 2](warp2.png)

**! הערה: ** כרגע, ספרייתנו תומכת בעיבוד של Custom Warp* (שבו המשתמשים מניעים נקודות משתייג) ובכל סוגי ה-Warp הסטנדרטיים.
* - כרגע, ספרייתנו תומכת ב-Custom Warp עם המשתייג הסטנדרטי, ואנו פועלים בצורה פעילה על הרחבת התמיכה שלנו על מנת לכלול את כל סוגי המשתייג בקרוב.

## **חלק 2 - שינוי האפקט Warp**

הספרייה שלנו מאפשרת לך לא רק לעשות עיבוד אלא גם לשנות (להוסיף) את אפקט ה-Warp.
השינויים האלו נתמכים דרך יכולות ה-**WarpParams** class.

| **יכולת**    | **תיאור**                                                               | 
|:-------------|:----------------------------------------------------------------------------|
| גבולות       | מחזיר את הגבולות של התמונה המשובטת.                                       |
| נקודות משתייג | מערך של נקודות, עם כל נקודה מייצגת פינת משתייג ה-Warp.                 |
| ערך           | ערך האפקט ה-Warp לאפקטים שאינם עתידיים.                                    |
| סיבובי Warp | תיאור מוגדר באיזור הכיוון של אפקטי ה-Warp שאינם עתידיים.                 |
| סיגנונות Warp | תיאור המזהה את סוג אפקט ה-Warp.                                          |

דוגמת הקוד למטה מדגימה איך לקבוע את סוג אפקט ה-Warp עבור שכבת חכמה ולהתאים את סוג האפקט ואינטנסיביות העיוות עבור האפקט.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 3](warp3.png)

## **חלק 3 - הוספת האפקט Warp**

דוגמת הקוד למטה מדגימה איך להוסיף אפקט Warp סטנדרטי לשכבת חכמה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 4](warp4.png)

דוגמת הקוד למטה מדגימה איך להוסיף אפקט Warp מותאם אישית לשכבת חכמה.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 5](warp5.png)

דוגמת הקוד למטה מדגימה איך להוסיף אפקט Warp לשכבת טקסט. 
**! ערה:** לפי תקני פוטושופ, אפקט ה-Warp עבור שכבות טקסט נמצא בדרך כלל בהגבלה לסוג הסטנדרטי. עם זאת, הספרייה שלנו תומכת בשימוש של שני סוגי אפקטי Warp. יש לשים לב כי קבצים כאלו עשויים לא להיות תואמים באופן מלא עם פוטושופ.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

תוצאה:
![Aspose.PSD for .NET Warp Result 6](warp6.png)

אנו ממשיכים לשפר ולהרחיב את היכולות של האפקט שלנו, במהירות, איכות ופונקציונליות נתמכות. הישאר מעודכן עם הוצאות חודשיות שלנו לפיתוחים האחרונים. 
צוות Aspose.PSD שלך
