---
title: עבודה עם שכבות טקסט
type: docs
weight: 170
url: /he/net/working-with-text-layers/
---

## **הוספת שכבת טקסט**
Aspose.PSD עבור .NET מאפשר לך להוסיף שכבת טקסט בקובץ PSD. השלבים להוספת שכבת טקסט בקובץ PSD פשוטים כמו שמוצגים להלן:

- טען קובץ PSD כתמונה באמצעות שיטת היצרן [**Load**](https://reference.aspose.com/psd/net/aspose.psd/image/methods/load/index) החשוף על ידי [Image class](https://reference.aspose.com/js/net/aspose.psd/image)
- קרא לשיטת [**AddTextLayer**](https://reference.aspose.com/psd/net/aspose.psd/fileformats/psd/psdimage/methods/addtextlayer) שמקבלת טקסט ומופע של מחלקת [**Rectangle**](https://reference.aspose.com/psd/net/aspose.psd/rectangle)  
- שמור את התוצאות

הקטע של הקוד הנ"ל מראה לך כיצד להוסיף שכבת טקסט בקובץ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddTextLayer-AddTextLayer.cs" >}}


## **הגדרת מיקום שכבת טקסט**
Aspose.PSD עבור .NET מאפשר לך להגדיר את מיקום שכבת הטקסט בקובץ PSD. השלבים להגדרת מיקום שכבת טקסט בקובץ PSD פשוטים כמו שמוצגים להלן:

- טען קובץ PSD כתמונה באמצעות שיטת היצרן Load החשוף על ידי Image class
- קרא לשיטת ההוספה של שכבת הטקסט וציין את מיקומי השמאל והעליון של שכבת הטקסט
- שמור את התוצאות

הקטע של הקוד הנ"ל מראה לך כיצד להגדיר את מיקום שכבת הטקסט בקובץ PSD

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SetTextLayerPosition-SetTextLayerPosition.cs" >}}


## **קבלת מאפייני טקסט משכבת טקסט**
עם Aspose.PSD עבור .NET, אתה יכול לקבל ולעדכן את מאפייני הטקסט של סעיפים שונים של טקסט הזמינים בשכבת הטקסט של קובץ PSD. מאמר זה מדגים כיצד ניתן לקבל פסקות, סגנונות ומאפייני טקסט של שכבת הטקסט ולעדכן אותם.

הקטע של הקוד למטה מציג איך לבצע את הדרישה הזו.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetTextPropertiesFromTextLayer-GetTextPropertiesFromTextLayer.cs" >}}


הנה דוגמה נוספת המדגימה כיצד מפתח יכול לקבל את העיצוב של קטעי טקסט שונים מ [TextLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers/textlayer) באמצעות [Aspose.PSD עבור .NET](https://products.aspose.com/psd/net).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GetPropertiesOfInlineFormattingOfTextLayer-GetPropertiesOfInlineFormattingOfTextLayer.cs" >}}


## **עדכון שכבת טקסט בקובץ PSD**
Aspose.PSD עבור .NET מאפשר לך לנהל את הטקסט בשכבת הטקסט של קובץ PSD. אנא השתמש במחלקת Aspose.PSD.FileFormats.Psd.Layers.TextLayer כדי לעדכן את הטקסט בשכבת ה-PSD. הקטע של הקוד הבא טוען קובץ PSD, גושת הטקסט, מעדכן את הטקסט ושומר את קובץ ה-PSD בשם חדש באמצעות [Aspose.PSD.FileFormats.Psd.Layers.TextLayer.UpdateText](https://reference.aspose.com/psd/net/aspose.psd.fileformats/psd/layers/textlayer/methods/updatetext/index) method.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UpdateTextLayerInPSDFile-UpdateTextLayerInPSDFile.cs" >}}


## **תמיכה בשכבות טקסט בזמן ריצה**
מאמר זה מדגים כיצד להוסיף שכבות טקסט בזמן ריצה על תמונות PSD. הקטע של הקוד ניתן למטה.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AddEffectAtRunTime-AddEffectAtRunTime.cs" >}}
