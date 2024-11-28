---
title: שכבת התאמת העקומות
type: docs
weight: 30
url: /he/java/שכבת-ההתאמה/קווים/
---

# עבודה עם שכבת התאום של פוטושופ ב-Java

המטרה של מאמר זה היא להדגים את יכולות ספריית Aspose.PSD עבור Java בעת **עבודה עם שכבות התאום של קווים** במסמכי Adobe® Photoshop®. הספרייה היא לחלוטין עצמאית. לכן, היא פועלת בלעדיו של עורך התמונות של פוטושופ. תוכלו למצוא [רשימה מלאה של תכונות](https://docs.aspose.com/psd/java/features/) בבסיס הידע שלנו. אז עכשיו נחזור לשכבות התאום.

## סקירה של ה-API

כלי הקווים יכול להתייצג כקו אלכסוני (עקום) על גרף עם הנופפרויות בפינת מימין למעלה והצללים בפינת מימין למטה.

הספרייה מספקת API לעבוד עם העקום, כלומר, מחלקת [CurvesLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CurvesLayer). עם זאת, למחלקה יש **שני גישות שונות לגמרי** לעבוד עם העקום. לכן, ניתן לערוך אותו באחת משתי המצבים בכל פעם:

- מתמיד (העקום מיוצג כנתיב עם נקודות במקומות של קיפול)
- נקודות (העקום מיוצג כקו מנוקד)

לכן, לספרייה יש שתי דרכים לשנות את העקום באמצעות [מנהל מתמיד](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvescontinuousmanager) ו-(מנהל מנקודות)[https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesDiscreteManager] בהתאמה. בשלב הבא, נסביר כיצד להשתמש בכל אחת מהן בדוגמה ספציפית.

## להתאים צבע וגוון באמצעות מנהל ההמשכים המתמיד של העקומות

[מנהל ההמשכים המתמיד](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) **מגדיר נקודות קיפול של עקום מתמיד** עבור הערוץ המישורי (RGB) וגם עבור ערוצי הצבע הספציפיים. לצורך הדגמה, יתווסף כמה התאמות עקומים (a) לתמונה שחורה של אורקסטרה (b) כדי לקבל תמונה מבהיקה עם צבעים חמימים יותר (c):

![ציור שכבת ההתאמה לקווים המתמידים תמונה 1](curves-psd-adjustment-layer-figure-1.png)

מאחר וישנם שני מנהלים, חייבים לבחור אחד באופן פעיל (מנהל מתמיד במקרה זה) לפני קבלתו. לאחר מכן, נוכל להוסיף ישירות נקודות קיפול בקואורדינטות מסוימות לערוצי הצבעים הרצויים (מרכיב RGB, אדום וכחול בהתאמה) כדי לשחזר את צורת העקום:
{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setContinuousManagerUsed(true);
    CurvesContinuousManager curvesContinuousManager = (CurvesContinuousManager)curvesLayer.getCurvesManager();

    curvesContinuousManager.addCurvePoint(0, (byte)65, (byte)125);
    curvesContinuousManager.addCurvePoint(1, (byte)120, (byte)135);
    curvesContinuousManager.addCurvePoint(3, (byte)135, (byte)120);
{{< /highlight >}}

מקור הקואורדינטות הוא בפינת התחתית של היד ימית. הערך המרבי של קואורדינטה של נקודה מוגבל לסוג הנתונים (בייט) ושווה ל-255 (127 לסוג חתום). למנהל יש גם כמה [שיטות אחרות](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/CurvesContinuousManager) שתוכלו להשתמש בהן.

## התאמת גוון באמצעות מנהל העקומות הדיסקרטי

מנהל העקומות הדיסקרטי מאפשר גם למקם נקודות קיפול (שינוי צבע וגוון בפועל), אך ההבדל הוא שהם עושים זאת בדרך שונה. ראשית, העקום **מאופס מנקודות** או נקודות (ולא קו מוצק). שנית, מנהל זה **לא מניח נקודה לאיפה שהיא** על הגרף. במקום, **הוא מעביר את הנקודה למעלה או למטה** עם טווח ערכים בין 255 ו-0 בהתאמה. כברירת מחדל, ערכי נקודת העקום עולים על ידי תדר המתרומם על פי זוית של 45 מעלות.

אז, עם זה בראש, קל לשחזר את ה-Photoshop preset של "שלילי (RBG)" (a) ולהחיל אותו על תמונת גוונים של עמק (b) כדי לקבל בסופו של דבר התיצוג השלילי של העמק (c).

![תצפית מכיוון ההתאמה של העקומות תמונה 2](curves-psd-adjustment-layer-figure-2.png) לפני הכל, אל תשכחו לבחור את מנהל המתאים כדי להיות מאושרים להשתמש בו ולאחר מכן להגיע לערכי נקודת העקום בסדר יורד החל מ-255 מטה אל 0 עבור כל נקודת עקום (סה"כ 255):

{{< highlight java >}}
    CurvesLayer curvesLayer = psdImage.addCurvesAdjustmentLayer();

    curvesLayer.setDiscreteManagerUsed(true);
    CurvesDiscreteManager curvesDiscreteManager = (CurvesDiscreteManager)curvesLayer.getCurvesManager();

    for (int i = 0; i < 255; i++)
    {
        curvesDiscreteManager.setValueInPosition(0, (byte)i, (byte)-i);
    }
{{< /highlight >}}

המנהל מספק גם כמה [שיטות אחרות](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/curvesdiscretemanager) לניהול העקום.

## מסקנה

במאמר זה למדנו כיצד לעבוד עם שכבות התאמת הקווים במסמכי פוטושופ באמצעות Aspose.PSD עבור Java בשתי דרכים שונות לחלוטין (מנהלים מתמידים ודיסקרטים).
