---
title: עריכת מסכות שכבה רסטר בקובץ PSD דרך API
type: docs
weight: 20
url: /he/net/editing-raster-layer-masks-in-psd-file-via-api/
---

## **סקירה**
**כדי לאוטומטזציה של עריכת פורמט PSD ושינוי קובץ PSD ללא צורך ב- Adobe® Photoshop® ניתן להשתמש ב-API של Aspose.PSD המצוי למטה. ישנם קטעי קוד של C# ו.NET שיכולים לעזור לך לשנות קבצי PSD.**

בעזרת מסכי שכבה רסטר ווקטורים אנו מסוגלים להסתיר ולהציג פיקסלי שכבה בלי למחוק אותם לצמיתות. מסכות רסטר נקראים גם מסיכת שכבה או מסיכת משתמש. גישה לשתי המסכות, הרסטרית והוקטורית, ב-Aspose.PSD ניתנת דרך התכונה [LayerMaskData](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/properties/layermaskdata) וניתן ליישרה כמופע של '[LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort)' ו-'[LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull)' שהם מחלקות ילד של מחלקת מעבר 'LayerMaskData' המופשטת. אם לשכבה יש מסכות רסטר ווקטור אז מסופקת המחלקה [LayerMaskDataFull](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatafull). אם לשכבה יש רק מסך רסטר או וקטור אז מסופקת המחלקה [LayerMaskDataShort](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layermaskdatashort). אם התכונת LayerMaskData היא ריקה, אז לשכבה אין מסכות או רק מסכת וקטור מבוטלת.

|![todo:image_alt_text](editing-raster-layer-masks-in-psd-file-via-api_1.png)|<p>מסכת רסטר ומסכת וקטור מבוטלת - LayerMaskDataShort</p><p>מסכת רסטר מושבתת - LayerMaskDataShort</p><p>מסכת רסטר ומסכת וקטור - LayerMaskDataFull</p><p>מסכת רסטר - LayerMaskDataShort</p><p>מסכת וקטור - LayerMaskDataShort</p><p>מסכת וקטור מבוטלת (אך המשאב של הווקטור נמצא)</p>|
| :- | :- |

## **כיצד לקבל מסכת שכבת רסטר בקובץ PSD?**
לפני הכל, עלינו לגלות אם לשכבה יש מסכת ווקטור ומסכות שכבה:

בקוד הדוגמא המצורף מתואר איך לקבל מסכת רסטר בשכבה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-1.cs" >}}

אחרת, סוג השכבת תכונת השכבת LayerMaskData היא LayerMaskDataShort. במקרה זה, נבדוק האם לשכבה יש רק מסך רסטר על ידי בדיקת המאפיין של הדגלים. הוא לא צריך להכיל את הדגל UserMaskFromRenderingOtherData, אחרת המסך הוא מטמש וקטורי.

קטע הקוד לקבלת המסך:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-2.cs" >}}

אם תרצה ל**חלץ מסך רסטר** כ-LayerMaskDataShort (לצורך עיבוד נוסף) גם כאשר שתי המסכות נמצאות, עליך לחלץ את LayerMaskDataFull ולהמיר אותו ל-LayerMaskDataShort. הקוד הבא יכול לשמש לשני המקרים:

חילוץ של מסך רסטר מ-PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-11.cs" >}}
## **כיצד לבדוק אם לשכבה בקובץ PSD יש מסכת רסטר?**
הקוד הבא ב- C# עשוי לעזור לך לבדוק אם לשכבה יש מסכת רסטר:

כיצד לדעת אם מסך רסטר מוחל על שכבת [PSD](/psd/he/net/psd-layer/)

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-6.cs" >}}
## **כיצד להסיר / להוסיף / לעדכן מסכת שכבת רסטר בקובץ PSD?**
רק להסיר / להוסיף / לעדכן את LayerMaskData אינו מספיק לשמירה תקינה מאחר שהערוצים אינם מעודכנים; אף על פי שזה עשוי לספק עיבוד נכון. זה לא משנה את הערוצים של המסך:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-3.cs" >}}

עלינו להשתמש בשיטת הוספת שכבת מסך להסרה / הוספה / עדכון.

זה מוסיף / מעדכן שני המסכות והערוצים:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-4.cs" >}}

זה מוריד את שני המסכים והערוצים:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-5.cs" >}}
## **הסרת מסכת שכבת רסטר בתמונת ה-PSD**
לפני הכל, נבדוק אם המסך נמצא בפורמט קצר ואם אינו מסך וקטורי ניתן פשוט לקרוא לשיטה AddLayerMask עם ערך null כדי למחוק את המסך הרסטר. אם המסך נמצא בפורמט מלא, עלינו להמיר אותו לפורמט קצר ולהשאיר רק את המסך הוקטורי. למחיקת מסכה בעזרת קטע קוד ב-C# .NET ניתן להשתמש בקטע הבא:

קטע קוד איך להסיר מסך שכבה מקובץ PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}
## **עדכון מסכת שכבת רסטר בתמונת ה-PSD**
זה יחודי: אם המסך נמצא בפורמט קצר עלינו לשנות את ImageData ואת MaskRectangle כראוי, אחרת צריך לשנות את UserMaskData ואת UserMaskRectangle. קטע הקוד הבא ב-C# .NET יכול לשמש לעדכון של מסך שכבה:

עדכון מסך שכבה ב-PSD באמצעות C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-7.cs" >}}

נה דוגמה לפעולות אפשריות שמשנות מסך רסטר. זו הפוכה של מסך משתמש בשכבה:

עדכון מסך שכבה ב-PSD באמצעות C#

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-12.cs" >}}
## **עדכון מסכת וקטור בקובץ PSD כאשר נמצאת מסך שכבת רסטר**
נניח שמשתמש כבר שינה משאב וקטורי. לאחר מכן, הוא יכול לעדכן את מסך הוקטור פשוט על ידי קריאה לשיטת [AddLayerMask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/addlayermask):

עדכון [מסך הוקטור של שכבת PSD](/psd/he/net/layer-vector-mask/) עם C#

{{< gist "aspose-com-gists" "8a4d6b34ce856d1642fc7c0ce984195c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-9.cs" >}}
## **הוספת מסך שכבת רסטר בקובץ PSD**
אם לשכבה יש ללא מסך, ניתן להוסיף את המסך הרסטר הנתון בקלות על ידי קריאה לשיטת AddLayerMask.

אם המסך אינו מעיני [UserMaskFromRenderingOtherData](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers/LayerMaskFlags) כבר יש לו מסך רסטר ועלינו לעדכנו כפי שנתון למעלה. אם כן, אם המסך הזה נמצא בפורמט קצר נמיר אותו לפורמט מלא. אם לא, אנו משתמשים בו כמוצא. לאחר מכן עלינו לעדכן את UserMaskData, UserMaskRectangle ותכונות אחרות עם תכונות המסך הנתונות. קטע הקוד הבא ב-C# .NET יכול לשמש להוספה (עדכון) מסך שכבה:

הוספת מסך שכבה חדש ל-PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithRasterMasks-Snippet-10.cs" >}}

## **כיצד לבדוק אם מסך שכבה מופעל?**
כד
