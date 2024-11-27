---
title: תמיכה בשכבות מילוי
type: docs
weight: 90
url: /he/net/support-of-fill-layers/
---


## **שכבות מילוי עם מילוי תבנית**
מאמר זה מדגים איך למלא את שכבת ה- [PSD](https://wiki.fileformat.com/image/psd/)עם מילוי תבנית. תבנית היא תמונה, צבע, צל או קו שמשמש למילוי שטח של תמונה. נא להשתמש ב- Aspose.PSD.FileFormats.Psd.Layers.FillLayer כדי להוסיף תבנית בשכבת ה- PSD. קטעי הקוד הבאים טוענים קובץ PSD, גושי הגישה למחלקת [Filllayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) ומגדירים את התבנית באמצעות נכסי ה-[PatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/patternfillsettings).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-PatternFillLayer-PatternFillLayer.cs" >}}



להלן דוגמה נוספת המדגימה כיצד [Aspose.PSD](https://products.aspose.com/psd/net) מציג את התבנית באמצעות [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) ו-[IPatternFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/ipatternfillsettings).



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ImplementPatternFillLayer-ImplementPatternFillLayer.cs" >}}
## **שכבות מילוי עם מילוי גרסיאלי**
מאמר זה מדגים את השימוש במילוי גרסיאלי כדי למלא את שכבת ה- PSD. ממשקי ה- Aspose.PSD חשפו שיטות יעילות וקלות לשים את המטרה הזו לגבי. ה- Aspose.PSD חשף את המחלקות [GradientColorPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientcolorpoint) ו-[GradientTransparencyPoint](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradienttransparencypoint) כדי להוסיף אפקט גרסיאלי לשכבה.

`השלבים כדי למלא [את שכבת ה- PSD](https://wiki.fileformat.com/image/psd/) במילוי עם גרסיאלי הם כל כך פשוטים כפי שמוצג למטה:

- טוען קובץ PSD כתמונה באמצעות שיטת המפעיל [Load](https://reference.aspose.com/net/psd/aspose.psd/image/methods/load/index) שנחשפה על ידי המחלקה [Image](https://reference.aspose.com/net/psd/aspose.psd/image).
- מגדיר נכסי הגדרות של אובייקט [FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer).
- יוצר רשימת [ColorPoints](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/colorpoints) עם צבעים נדרשים ועמדות של צבע.
- יוצר רשימת נקודות שקיפות עם שקיפות נדרשת ועמדת נקודת השקיפות.
- קורא לשיטת [FillLayer.Update](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer/methods/update)
- שומר את התוצאות.



הקטע הבא מראה איך להוסיף מילוי גרסיאלי למילוי שכבת PSD.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.cs" >}}



**להלן דוגמה נוספת המשתמשת ב-[** GradientFillSettings.GradientType **](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/gradientfillsettings/properties/gradienttype)** כדי למלא את שכבת ה- PSD במילוי גרסיאלי. ה- Aspose.PSD תומך בסוגי הגרסיאל הבאים דרך תיאור הסוג הגרסיאלי:

- **GradientType.Linear:** מהגרסיאל הלינארי, ההעברות של הצבע מהגוון התחילתי לסופי בקו ישר.
- **GradientType.Radial:** בגרסיאל מעגלי, הצבעים מתפשטים מנקודת ההתחלה בתבנית מעגלית.
- **GradientType.Angle:** בגרסיאל זוויתית, הגרסיאל נסבב נגד כיוון השעון סביב נקודת ההתחלה.
- **GradientType.Reflected:** בגרסיאל שהתקשר, הצבע משתקף שני צידי נקודת ההתחלה.
- **GradientType.Diamond:** הגרסיאל יוצר צורה מעויינת מנקד ההתחלה.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-GradientFillLayers-GradientFillLayers.cs" >}}
## **תמיכה במאפיין הקניית שכבות עבור שכבת מילוי גרסיאלית**
מאמר זה מדגים כיצד לקנות את שכבת המילוי עם מילוי גרסיאלי באמצעות Aspose.PSD עבור .NET. לצורך זה, נוסף מאפיין חדש [Scale](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings/properties/scale) נוסף ב-[IGradientFillSettings](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.fillsettings/igradientfillsettings).

להלן הדגמה לקוד שמדגים כיצד להשתמש במאפיין **Scale**.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfScaleProperty-SupportOfScaleProperty.cs" >}}
## **שכבות מילוי עם מילוי צבע**
מאמר זה מדגים איך למלא את שכבת ה- [PSD](https://wiki.fileformat.com/image/psd/) עם צבע. נא להשתמש במחלקת [Psd.Layers.FillLayer](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd.layers.filllayers/filllayer) כדי להוסיף צבע בשכבת PSD. הקטע הבא מראה טעינת קובץ PSD, גישה למחלקת שכבת המילוי והגדרת הצבע באמצעות נכסי השכבה המלאים FillLayer.FillSettings.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.cs" >}}


