---
title: עבודה עם שכבות
type: docs
weight: 150
url: /he/net/working-with-layers/
---

## **יצירת קבוצת שכבות**
קבוצת שכבות מורכבת משכבה אחת או יותר ועוזרת לארגן שכבות דומות או קשורות. באמצעות Aspose.PSD עבור .NET תוכל ליצור קבוצת שכבות. למטרה זו, נוסף שיט חדש [**AddLayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage/methods/addlayergroup) במחלקת **[PsdImage](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/psdimage)** כדי להוסיף את קבוצת השכבות.

השלבים ליצירת קבוצות שכבות פשוטים כמו שלמטה:

- צור מופע של תמונה באמצעות מחלקת PsdImage עם רוחב, גובה ואפשרויות תמונה מסוימות.
- צור [**LayerGroup**](https://reference.aspose.com/net/psd/aspose.psd.fileformats.psd/layers/layergroup) עם השם והאינדקס שצוינו.
- צור מופע של מחלקת השכבה והקצה לה תמונת PSD.
- הוסף את השכבה שנוצרה לקבוצת השכבות באמצעות השיטה AddLayer שניתנה על ידי מחלקת LayerGroup.
- שמור את התוצאות.

קטע הקוד הבא מראה כיצד ליצור קבוצת שכבות.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-CreateLayerGroups-CreateLayerGroups.cs" >}}


## **שינוי שם שכבה**
באפשרותך להשתמש בשם כלשהו שתרצה, אך נהל טיפול נפוץ הוא להשתמש בתיאור כללי של האובייקט או אלמנט שנמצא בשכבה זו. מאמר זה מדגיש כיצד ניתן לשנות את שם השכבה באמצעות Aspose.PSD עבור .NET. למטרה זו, נוסף מאפיין חדש [**DisplayName**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/layers/layer/properties/displayname) במחלקת Layer כדי להציג שם שכבה בצורה תקינה. נמצא כי כאשר פוטושופ שומר על שם שכבה באמצעות המאפיין **Name**, אז תווים קוריאים מאוחסנים כ-63 בערך ASCII. זאת אומרת, אם ברצונך להציג שם שכבה בצורה תקינה, כדאי להשתמש במאפיין **DisplayName** מאחר שהמאפיין **Name** אינו תומך בתווים קוריאים.

שטח הקוד הבא מראה כיצד ניתן לשנות את שם השכבה.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-RenameLayer-RenameLayer.cs" >}}
## **תמיכה בשכבות מקושרות**
קישור שכבות הוא כלול לשכבות. אם אתה מקשר שתי או יותר שכבות, אז תוכל לבצע שינויים מסוימים לשתי השכבות שמחוברות. לדוגמה, אם אתה מחיל המרה לשכבה אחת, אז זה ייחוד לכל השכבות המקושרות אחרות. מאמר זה מדגיש כיצד ניתן לקבל ולבטל קישור שכבות משתמש ב [Aspose.PSD](https://products.aspose.com/psd).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-SupportOfLinkedLayer-SupportOfLinkedLayer.cs" >}}
