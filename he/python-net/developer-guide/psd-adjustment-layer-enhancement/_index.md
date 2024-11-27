---
title: שימוש בשכבת התאמה עבור שיפורים ב-PSD
weight: 100
type: docs
description: דוגמאות לשימוש בשכבת ההתאמה דרך Aspose.PSD עבור פייתון
keywords: [שכבת הכווץ, שיפור תמונה, התאמת עקומות, שיפור רמות, היפוך, מסנן תמונות,  ממשק תכנות ל-PSD, פייתון, קוד דוגמה]
url: he/python-net/adjustment-layer-enhancement/
---

## **סקירה**

במאמר זה, נבחן את עריכת שכבות ההתאמה ב-Aspose.PSD עבור פייתון. שכבות ההתאמה הם תכונה חזקה בעריכת תמונות שמאפשרת לך לבצע שינויים ללא השחתה בתמונות שלך. Aspose.PSD מספק סט מקיף של מחלקות שכבות ההתאמה שאפשר להשתמש בהן כדי לשנות אספקטים שונים של התמונות שלך.

כדי להדגים את עריכת שכבות ההתאמה, נשתמש בקטע קוד דוגמה בסוף העמוד שטוען תמונת PSD ומיישם התאמות שונות לשכבות שלה.

בקטע הקוד למטה, אנו מתחילים על ידי טעינת תמונת ה-PSD באמצעות שיטת `PsdImage.load()`. לאחר מכן, אנו מגדירים את האפשרויות לשמירת קבצי ה-PNG המוצאים. המחלקה `PngOptions` מאפשרת לנו לציין את סוג הצבע לתמונת הפלט.

לאחר מכן, אנו עוברים על כל שכבה בתמונת ה-PSD ובודקים את סוגה באמצעות השיטה `is_assignable()`. אם השכבה היא מסוג מסוים, אנו משנים אותה לסוג זה באמצעות השיטה `cast()` ומיישמים את ההתאמה הרצויה. לדוגמה, אנו מכווננים את עוצמת האור והניגודיות של BrightnessContrastLayer, משנים את רמות הצבע של LevelsLayer, מוסיפים נקודת עקיף ל- CurvesLayer, וכן הלאה.

ניתן להוסיף קוד נוסף כדי ליישם התאמות אחרות לשכבות המתאימות שלהן. Aspose.PSD מספק מגוון רחב של מחלקות שכבות ההתאמה, כגון [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer), [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer), [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer), [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer), [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer), [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer), ועוד.

לבסוף, אנו שומרים את התמונה ששונתה באמצעות שיטת `save()` של מחלקת PsdImage.

קטע הקוד הזה מספק סקירה בסיסית על איך לערוך שכבות ההתאמה ב-Aspose.PSD עבור פייתון. ניתן להתאים אישית את ההתאמות לפי דרישותיך ולחקור את האפשרויות השונות הזמינות במסמך ה- API.

נא לבדוק דוגמה מלאה.

## **דוגמה**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
