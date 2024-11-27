---
title: עיבוד פורמטים של אדובי פוטושופ
type: docs
weight: 20
url: /he/net/manipulating-adobe-photoshop-formats/
---

## **מיזוג שכבות PSD לשכבות אחרות**

## **ייצוא תמונה ל-PSD**
קובץ PSD, מסמך PhotoShop, הוא פורמט הקובץ המוגדר כברירת המחדל המשמש על ידי אדובי פוטושופ לעבודה עם תמונות. Aspose.PSD מאפשר לך לטעון, לערוך ולשמור קבצים לתוך PSD כך שניתן יהיה לפתוח ולערוך בפוטושופ. מאמר זה מציג איך לשמור קובץ ל-PSD עם Aspose.PSD, וכן מדבר על כמה מההגדרות שניתן להשתמש בהן כאשר משמירים לפורמט זה. [PsdOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/psdoptions) הוא מחלקה מיוחדת במרחב [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) המשמשת לייצוא תמונות ל-PSD. כדי לייצא ל-PSD, עליך ליצור מופע של המחלקה Image, שהועלה באמצעות קובץ תמונה קיים (למשל, תמונה ממוזערת) או שנוצרה מאפס. מאמר זה מסביר כיצד. בדוגמאות להלן, תמונה נוצרת מאפס. לאחר שהיא נוצרת ונתוני הפיקסלים מומלאים, יש לשמור את התמונה באמצעות השיטה Save של Image class, ולספק אובייקט PsdOptions כארגומנט שני. ניתן להגדיר מספר מאפייני המחלקה PsdOptions להמרה מתקדמת. כמה מהמאפיינים הם ColorMode, [CompressionMethod](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/compressionmethod) וגרסה. Aspose.PSD תומך בשיטות דחיסה הבאות דרך סיווג דחיסה דרך enum CompressionMethod:

- CompressionMethod.Raw
- CompressionMethod.RLE
- CompressionMethod.ZipWithoutProtection
- CompressionMethod.ZipWithProtection

המצבים הבאים הינם נתמכים דרך enum [ColorModes](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes):

- ColorModes.Bitmap
- ColorModes.Grayscale
- ColorModes.RGB


ניתן להוסיף משאבים נוספים, כמו משאבי תמונה ממוזערת עבור PSD v4.0, v5.0 ומעלה, או משאבי רשת ומדריכים עבור PSD v4.0 ומעלה. הקוד למטה יוצר קובץ תמונה מאפס, ממלא את הפיקסלים ושומר אותו ל-PSD תוך דחיסת RLE ומצב צבעים אפור. קטע הקוד הבא מציג איך לייצא תמונה ל-PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ExportImageToPSD-ExportImageToPSD.cs" >}}
## **ייבוא תמונה לשכבת PSD**
מאמר זה מדגיש את שימוש של Aspose.PSD להוספה או לייבא תמונה לשכבת PSD. ממשקי ה-API של Aspose.PSD חשפו שיטות יעילות וקלות לשיגור מטרה זו. Aspose.PSD חשף את השיטה [DrawImage](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers/layer/methods/drawimage) של המחלקה Layer להוספת/ייבוא תמונה אל תוך קובץ PSD. שיטת DrawImage דורשת מיקום וערכי תמונה כדי להוסיף/ייבא תמונה אל קובץ PSD. השלבים לייבוא תמונה לשכבת PSD הם כהלך:

- טען קובץ PSD כתמונה באמצעות השיטה Load שנחשפת על ידי Image class.
- צור מופע של מחלקת Layer מתוך זרם עם קובץ Png, Jpeg, Tiff, Gif, Bmp, Psd או j2k
- הוסף שכבה ל- Psd באמצעות השיטה AddLayer
- שמור את התוצאות.

קטע הקוד הבא מציג איך לייבא את התמונה לשכבת PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Opening-LoadingImageFromStream-LoadingImageFromStream.cs" >}}
## **החלפת צבע בשכבות של PSD**
מאמר זה מדגיש את שימוש של Aspose.PSD להוספה או לייבא תמונה לשכבת PSD. ממשקי ה-API של Aspose.PSD חשפו שיטות יעילות וקלות לשיגור מטרה זו. Aspose.PSD חשף את השיטה של DrawImage במחלקה Layer להוספת/ייבוא תמונה אל קובץ PSD. DrawImage דורשת מיקום וערכי תמונות כדי להוסיף/ייבא תמונה אל קובץ PSD. השלבים לייבוא תמונה לשכבת PSD הם כהלך:

- טען קובץ PSD כתמונה באמצעות השיטה המפעילה Load שנחשפת על ידי Image class.
- צור מופע של מחלקת Layer והקצה לה את שכבת התמונה מכונת הריצה.
- טען את התמונה שיש צורך להוסיף או ליצור אחת מאפס.
- קרא לשיטת Layer.DrawImage בזמן הציון של המיקום והמופע של התמונה.
- שמור את התוצאות.

קטע הקוד הבא מציג איך לייבא תמונה לשכבת PSD.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorReplacementInPSD-ColorReplacementInPSD.cs" >}}
## **יצירת תמונות ממוזערות מקבצי PSD**
- תוקפי JPG
- תפיסת מסך בעזרת הקוד
- ניהול תקן
- סדרות תמונות
- מומלץ לאירגון.

הנה קוד:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateThumbnailsFromPSDFiles-CreateThumbnailsFromPSDFiles.cs" >}}
## **יצירת קבצי PSD מאינדקס**
- צור מופע של PsdOptions והגדר את מקורו
- הגדר את מאפיין ColorMode של PsdOptions ל-ColorModes.Indexed
- צור לוח צבעים חדש מהמרחב RGB והגדר אותו כמאפיין הלוח של PsdOptions
- הגדר את מאפיין CompressionMethod לאלגוריתם דחיסה נדרש
- צור תמונת PSD חדשה באמצעות קריאה ל PsdImage.[Create](https://reference.aspose.com/psd/net/aspose.psd/image/methods/create) method
- שרטט גרפיקה או בצע פעולות אחרות כפי הצורך
- קרא ל PsdImage.Save method כדי לממש את כל השינויים.

הנה קוד:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateIndexedPSDFiles-CreateIndexedPSDFiles.cs" >}}
## **ייצוא שכבת PSD לתמונת רסטר**
- שימוש בשכבות בקובץ PSD פורמט תמונות רסטריות 
- שימוש במשאב עבור PSD
- PNG
- צילום תמונה

ראה קוד:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-ModifyConvert-PSD-ExportPSDlayerToRasterImage-ExportPSDlayerToRasterImage.cs" >}}
## **עדכון שכבת טקסט בקובץ PSD**
- ניהול קובץ עם סיומת PSD
- אפשרות צילום תמונה
- PSD
- הגדרת Code
- טקסט מבנה

ראה קוד:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-ModifyConvert-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}
## **איתור שכבת PSD מטושנת**
- ניהול קובץ עם מיקוד תמונה
- PSD
- כימיה
- ליבה
- בדיקת תקן

ראה קוד:

{{< gist "aspose-com-gists" "8a4d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-DetectFlattenedPSD-DetectFlattenedPSD.cs" >}}
## **מיזוג שכבות PSD**
- ריכוז כרגעה
- קריאת קובץ CMD
- JPG
- צילום תמונה
- PSD של קובץ

ראה קוד:

{{< gist "aspose-com-gists" "8a4d56d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-MergePSDlayers-MergePSDlayers.cs" >}}
## **תמיכה בצבע גרייסקייל עם אלפא לקובץ PSD**
- המחלקה הפופולרית
- גלריית תמונות
- JPG עם JS
- איכות גבוהה
- קוד גון

ראה קוד:

{{< gist "aspose-com-gists" "8a4d56d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GrayScaleSupportForAlpha-GrayScaleSupportForAlpha.cs" >}}
## **תמיכה באפקטי שכבה עבור PSD**
- טיפול מרחיב
- האפקט הפנימי
- אובתר הבזק
- אפקט [בזוי](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/colormodes) עבור יישום

ראה קוד:

{{< gist "aspose-com-gists" "8a4d56d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportLayerForPSD-SupportLayerForPSD.cs" >}}