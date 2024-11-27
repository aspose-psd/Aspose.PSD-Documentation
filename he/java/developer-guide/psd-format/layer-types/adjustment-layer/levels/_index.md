---
title: שכבת התאמת שחור לבן
type: docs
weight: 30
url: /he/java/layer-types/adjustment-layer/levels/
---

## עבודה עם שכבת התאמת רמקולים בפוטושופ בשפת Java

במאמר זה נלמד כיצד להתאים את טווח הגוונים ואת איזון הצבעים של תמונה בפורמט קובץ [PSD](/he/psd/java/psd-format/) באופן תכנותי בשפת Java. אנו לא משתמשים בעורך התמונות Adobe® Photoshop® עצמו. במקום זאת, אנו משתמשים בספריית Aspose.PSD עבור Java שעובדת לבדה כדי לערוך את המסמך של פוטושופ.

אמנם, Aspose.PSD עבור Java תומך בכלים מספיקים יותר [לעריכת התמונה](/he/psd/java/manipulating-images/) כפי שרוצים, אך נעשה **שימוש ב-API של שכבת התאמת רמקולים Levels** שהוא אחד מהדרכים הפשוטות והמהירות ביותר לבצע את המשימה.

## סקירת API

המימוש הנוכחי (20.6 ברגע כתיבת הטקסט) של API שכבת שינוי רמקולים **תומך בכל תכונות הבסיס של רמקולי Photoshop** , כלומר, התאמת רמקולי קלט ופלט עבור הערוץ הקומפוזיטי (RGB) כמו גם עבור כל ערוץ צבע ראשי (אדום, ירוק וכחול).

ה-API של שכבת התאמת רמקולים הוא ישיר. המחלקה [LevelsLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/LevelsLayer) היא נקודת הכניסה להתאמת רמקולים Levels. היא מכילה מספר שיטות לגישה לערוצי צבע: getMasterChannel ו-getChannel(int). שתי השיטות מחזירות [LevelChannel](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.layerresources/LevelChannel) שיש להן תכונות מתאימות לכלים של כניסה ויציאה. ההבדל הוא ש-getMasterChannel משמשת להתאמת ערוץ צבע קומפוזיטי (RGB) בעוד getChannel גוששת ערוץ צבע מסוים (אדום, ירוק או כחול) על פי האינדקס שלו.

## תיאומיות עם מצבי צבע

שווה לציין שכבת התאמת רמקולים **תואמת לרוב רב ערכי מצבי הצבע** על פי רמקולי Photoshop. לכן, ניתן להתאים את הרמקולים לתמונות במצבי צבע Grayscale (ערוץ אפור), RGB (RGB, אדום, ירוק וכחול), CMYK (CMYK, ציאן, מגנטה, צהוב ושחור), Duotone (ערוץ מונוטון) ו-LAB (בהירות, a ו-b ערוצים).

## התאמת טווח גוונים

פשוט מדברים, התיקון הגונאי מתייחס לתמונה על מנת לשונן את הצללים והקיקורים על מנת לחלק את הטונאליות האמצעית. כללית, **הוא הופך את התמונה להירה יותר** , אם נעשה בצורה נכונה. לדוגמה, נקח תמונה של כלב (ב) ונכוון את טווח הגוונים שלה (א – התקן צולם מחלון רמקולים של פוטושופ למען בהירות) כדי להשיג כיוון יותר ברור (ג).

![](RackMultipart20200821-4-1x13l6z_html_8fc7fa6738d8d302.png)

|![Levels Layer תמונה 1](levels-adjustment-figure-1.png)|

ל**התאמת טוות הגוונים הכוללית** של תמונה, יש להגדיר רמקולי קלט של הערוץ הראשי:

    LevelsLayer levelsLayer = psdImage.addLevelsAdjustmentLayer();

    LevelChannel masterChannel = levelsLayer.getMasterChannel();
    masterChannel.setInputShadowLevel(( **short** )21);
    masterChannel.setInputMidtoneLevel(( **float** )1.19);
    masterChannel.setInputHighlightLevel(( **short** )229);

חשוב לשים לב שרמקולי הקלט צריכים להיות בטווח של 0 עד 253 עבור צללים, מ-9.99 עד 0.01 עבור צבעים אמצעיים ומ-2 עד 255 עבור קיקורים. טווח רמקולי הפלט חייב להיות בין 0 ל-255.

רוצה עוד דוגמאות? תוכל למצוא אותן ב-[Github](https://github.com/aspose-psd/Aspose.PSD-for-Java) וב-[מאגר ידע](https://docs.aspose.com/display/psdjava/Manipulating+Photoshop+Formats#ManipulatingPhotoshopFormats-AddLevelAdjustmentLayers).

## מסקנה

כדי לסכם, Aspose.PSD עבור Java מציע API נוח ופשוט לשינוי טווח הגוונים ואיזון איזון צבעים של תמונה שתואם עם רוב מצבי הצבע. עם API של שכבת התאמת רמקולים בספרייה נראה כמו רמקולי Photoshop, לכן, קל להתחיל גם אם לא עבדת עם הספרייה לפני כן.
