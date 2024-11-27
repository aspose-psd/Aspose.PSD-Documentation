---
title: תמיכה בשכבות מילוי
type: docs
weight: 50
url: /he/java/support-of-fill-layers/
---


## **תמיכה בשכבות מילוי עם מילוי צבע**
מאמר זה מדגים איך למלא שכבת PSD בצבע. נא להשתמש במחלקת Aspose.PSD.FileFormats.Psd.Layers.FillLayer כדי להוסיף צבע לשכבת PSD. קטעי הקוד הבאים טוענים קובץ PSD, גישה למחלקת FillLayer ומגדירים את הצבע באמצעות מאפיין FillLayer.FillSettings.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **תמיכה בשכבות מילוי עם מילוי התעמעום**
מאמר זה מדגים את השימוש במילוי התעמעום כדי למלא שכבת PSD. ממשקי ה-Aspose.PSD חשפו שיטות יעילות וקלות לשימוש כדי להגיע למטרה זו. ב-Aspose.PSD חשפו מחלקות GradientColorPoint ו-GradientTransparencyPoint כדי להוסיף אפקט תעמעום לשכבה.

השלבים למילוי שכבת PSD עם מילוי התעמעום הם פשוטים כמטה:

- טען קובץ PSD כתמונה באמצעות שיטת הפעלה Load החשופה על ידי Image class.
- הגדר מאפייני הגדרות של אובייקט FillLayer.
- צור רשימת ColorPoints עם צבעים נדרשים ומיקום של הצבע.
- צור רשימת transparencyPoints עם שקיפות נדרשת ומיקום של נקודת השקיפות.
- קרא לשיטת FillLayer.Update
- שמור את התוצאות.

הקטע הבא מראה לך איך להוסיף מילוי התעמעעם למילוי שכבת PSD.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **אפקט הקווים עם מילוי צבע**
מאמר זה מדגים איך ליצור אפקט קווים עם מילוי צבע. אפקט הקווים משמש להוספת קווים וגבולות לשכבות וצורות. ניתן להשתמש בו כדי ליצור קווים בצבע מוצלח, גרדיאנטים צבעוניים, וגם גבולות משופצים.

השלבים ליצירת אפקט קווים עם מילוי צבע הם פשוטים כמטה:

- הגדר את המאפיין **LoadEffectsResource**.
- טען קובץ PSD כתמונה באמצעות שיטת הפעלה Load החשופה על ידי Image class והגדר **PsdLoadOptions**.
- הגדר מאפייני הגדרות של **ColorFillSetting**.
- שמור את התוצאות.

הקטע הבא מראה לך איך ליצור אפקט קווים עם מילוי צבע.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}



