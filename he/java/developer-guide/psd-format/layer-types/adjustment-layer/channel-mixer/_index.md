---
title: רכיב סידור הערות במערכת התמונות
type: docs
weight: 30
url: /he/java/שכבת-התאמת-ערוצים/צימוד-לורחב/
---

# עבודה עם שכבת התאמת ערוצים בפוטושופ ב-Java

היום נבחן כיצד לערבב צבעי ערוץ במסמכי פוטושופ בצורה תכנותית ב-Java. מאחר ועורך הפוטושופ לא תומך בכתיבת קודי Java, נשתמש בספרייה מיוחדת לטיפול בפורמט קובץ PSD בשם Aspose.PSD עבור Java.

הספרייה מכילה **API לעבודה עם ערוצי צבע**. ישנן מספר דרכים לערבב צבעים, אך במאמר זה נתמקד בשכבת התאמת ערוצים של צימוד לורחב.

ה-API של שכבת התאמת ערוצים מאפשר **שחקות עם ערוצי צבע** כדי ליצור תמונות צינור, ליצור אפקטי צבע יצירתיים שונים או אף להמיר את התמונה לתמונה שחור לבן. נדון כיצד להחיל שכבת התאמת מערבב למסמך פוטושופ קיים באמצעות Aspose.PSD עבור Java, אך תחילה יש לדבר על תכונות ה-API בכללי.

## סקירת ה-API

קיים מאוד כלום מיוחד ביצירת שכבת התאמת ערוצים. ניתן להוסיף אותו דרך [שיטת הפעלת המפעיל המוגדרת כברירת מחדל](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#addChannelMixerAdjustmentLayer--) שמחזירה מופע של מחלקת ChannelMixerLayer. מחלקה זו מכילה פונקציות כלליות כגון אפשרות מונוכרום ושיטה לקבלת ערוץ פלט. ערוץ פלט ספציפי יכול להיות אחד משני סוגים: [CmykMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/CmykMixerChannel) או [RgbMixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/RgbMixerChannel). הסוג של [MixerChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/mixerchannel) תלוי [במצב הצבע](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/PsdImage#getColorMode--) של התמונה.

## שינוי התמונה למונוכרומטי

כעת, נבחין בדוגמא להחלת שכבת התאמת ערוצים למסמך פוטושופ קיים. מאחר וכזה סוג של שכבת התאמה אינה תומכת בפריסטים עדיין, עלינו לבנות מחדש את פריסט ה-Fotorחבש הלבן האינפרא אדום (RGB) בפוטושופ (א). הפריסט יוחל על תמונת עץ פורח (ב). כתוצאה, ברצוננו להשיג הפקט של צילום אינפרא אדום (ח).

![דוגמת שכבת התאמת ערוצים לתמונת PS](channel-mixer-adjustment-psd-layer-figure-1.png) תחילה, לבנית מחדש של הפריסט ה-Fotorחבש הלבן האינפרא אדום בפוטושופ נדרש לאפשר את הדגל על מונוכרום ולהגדיר ערכי גולם מתאימים לכל צבע (אדום, ירוק וכחול) לערוץ פלט אפור:

    ChannelMixerLayer channelMixerLayer = psdImage.addChannelMixerAdjustmentLayer();
    channelMixerLayer.setMonochrome( **true** );
    RgbMixerChannel grayOutputChannel = (RgbMixerChannel)channelMixerLayer.getChannelByIndex(0);
    grayOutputChannel.setRed(( **short** )-70);
    grayOutputChannel.setGreen(( **short** )200);
    grayOutputChannel.setBlue(( **short** )-30);

על התמונה להיות במצב צבע RGB כדי להפעיל את הקוד (בגלל ההמרה למחלקת RgbMixerChannel). מצב צבע CMYK גם נתמך אך רק לתמונות עם מצב צבע תואם.

חשוב לזכור שערך של כל צבע כמו גם המאפיין הקבוע חייבים להימצא בטווח של -200 עד 200.

## מסקנה

במאמר זה חקרנו כיצד לעבוד עם סידור הערוצים של ה-API של Aspose.PSD עבור Java על מנת לכוון צבעים בערוצי הצבע ולהמיר את התמונה לגוונים שחור לבן.
