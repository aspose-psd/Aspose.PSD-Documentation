---
title: שימוש בשכבת התאמה לשיפורי PSD
weight: 100
type: docs
description: דוגמאות לשימוש בשכבות התאמה דרך Aspose.PSD עבור C#
keywords: [שכבת התאמה, שיפור תמונה, התאמת עקומות, הגבלת רמות, היפוך, מסנן תמונה, API של PSD, C#, סי-שארפ, קוד דוגמא]
url: he/net/adjustment-layer-enhancement/
---

## סקירה

במאמר זה, נבחן את עריכת השכבות המתאימות ב- Aspose.PSD עבור C#. שכבות ההתאמה הן תכונה חזקה בעריכת תמונות שמאפשרת לך לבצע שינויים לא הוסרים בתמונות שלך. Aspose.PSD מספק סט מקיף של שכבות התאמה שבאפשרותך להשתמש בהן כדי לשנות אפשרויות שונות בתמונות שלך.

כדי להדגים את עריכת השכבות התואמות, נשתמש במקטע קוד דוגמא בסופו של הדף שטוען תמונת PSD ומחיל שינויים שונים על שכבותיה.

במקטע הקוד למעלה, אנחנו מתחילים על ידי טעינת התמונה של PSD באמצעות השיטה `PsdImage.Load()`. לאחר מכן אנו מגדירים את האפשרויות לשמירת קבצי ה-PNG המוצרטים. מחלקת `PngOptions` מאפשרת לנו לציין את סוג הצבעים לתמונת הפלט.

הבאנו, אנו משתלבים דרך כל שכבה בתמונת ה-PSD ובודקים את סוגה באמצעות השיטה `IsAssignable()`. אם השכבה היא מסוג מסוים, אנו משנים אותה לסוג זה באמצעות השיטה `Cast()` ומחילים את הכוונה הרצויה. לדוגמה, אנו מתאימים את בהירות וניגודיות של `BrightnessContrastLayer`, משנים את רמות ה-Levels של `LevelsLayer`, מוסיפים נקודה מעקיפה לשכבת `CurvesLayer`, וכן הלאה.

תוכל להוסיף קוד נוסף כדי ליישם שינויים אחרים לשכבותיהן התואמות. Aspose.PSD מספק מגוון רחב של מחלקות שכבות ההתאמה, כמו [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer), ועוד.

לבסוף, אנו שומרים את התמונה המשוננעת באמצעות השיטה `Save()` של מחלקת `PsdImage`.

הקוד מספק סקירה בסיסית על אופן עריכת שכבות ההתאמה ב- Aspose.PSD עבור C#. תוכל להתאים את השינויים לפי דרישותיך ולסקור את האפשרויות השונות הזמינות במסמך ה- API.

## דוגמה

הנה דוגמה לקוד המדגים איך להשתמש בשכבות ההתאמה באמצעות Aspose.PSD עבור C#:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

למידע נוסף ודוגמאות מפורטות יותר, נא לבקר ב[תיעוד של Aspose.PSD עבור C#](https://docs.aspose.com/psd/net/).
