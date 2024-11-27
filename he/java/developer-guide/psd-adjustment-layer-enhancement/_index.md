---
title: שימוש בשכבת ההתאמה לשיפורים ב־PSD
weight: 100
type: docs
description: דוגמאות לשימוש בשכבת ההתאמה דרך Aspose.PSD עבור Java
keywords: [שכבת התאמה, שיפור תמונות, התאמת עקומות, שיפור רמות, הפיכה, סינון תמונה, API של PSD, Java, קטע קוד]
url: he/java/adjustment-layer-enhancement/
---

## **סקירה**

מאמר זה חוקר את עריכת שכבות ההתאמה ב־Aspose.PSD עבור Java. שכבות ההתאמה הן תכונה עוצמתית בעריכת תמונות שמאפשרת לך לבצע שינויים לא נפגעים בתמונות שלך. Aspose.PSD מספק סט מקיף של שכבות התאמה שבאפשרותך להשתמש בהן כדי לשנות אפקטים שונים בתמונות שלך.

כדי להדגים עריכת שכבות ההתאמה, נספק קטע קוד לדוגמה בסופו של העמוד שטוען תמונת PSD ומחליף פרטים שונים לשכבותיה.

בקטע קוד הבא, אנו מתחילים על ידי טעינת התמונה ב־PSD באמצעות השימוש בשיטת PsdImage.load(). לאחר מכן, אנו מגדירים את האפשרויות לשמירת קבצי ה־PNG המוצאים. המחלקה PngOptions מאפשרת לנו לציין את סוג הצבע לתמונת הפלט.

בהמשך, אנו עוברים בעקבות כל שכבה בתמונת ה־PSD ובודקים את סוגה באמצעות השימוש בשיטת isAssignable(). אם השכבה היא מסוג מסוים, אנו מהקסטינג לסוג זה באמצעות השימוש בשיטת cast() ומחילים את ההתאמה הרצויה. לדוגמה, אנו משנים את עוצמת האור והניגודות של BrightnessContrastLayer, משנים את רמות הצבע ב־LevelsLayer, מוסיפים נקודת עקומה ל־CurvesLayer, וכן הלאה.

בנוסף, ניתן להוסיף קטעי קוד נוספים כדי ליישם התאמות נוספות לשכבותיהן המתאימות. Aspose.PSD מספקת מגוון רחב של מחלקות שכבות ההתאמה, כגון [ExposureLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), ועוד.

לבסוף, אנו שומרים את התמונה שנערכה באמצעות שיטת השמירה של מחלקת PsdImage.

זה מספק סקירה בסיסית על אופן עריכת שכבות ההתאמה ב־Aspose.PSD עבור Java. באפשרותך להתאים אישית את ההתאמות לפי הדרישות שלך ולחקור את האפשרויות השונות הזמינות במסמך המסמך עם ה־API.

אנא בדוק את הדוגמא המלאה להלן.

## **דוגמה**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-adjustment-layer-enhancement.java" >}}
