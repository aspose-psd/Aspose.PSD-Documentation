---
title: מכביר שכבת כיוון צבע
type: docs
weight: 30
url: /he/java/layer-types/adjustment-layer/color-balance/
---

# עבודה עם שכבת כיוון צבע בפוטושופ בשפת Java

במאמר זה אנו מתכוונים **לכוון את יחסי הצבע של התמונה** בפורמט קובץ PSD בשפת Java. אנו נשתמש בספריה מיוחדת בשם Aspose.PSD עבור Java שהיא אוצר הכלים לניהול מסמכי פוטושופ.

מאחר והספריה עובדת עם פורמט קובץ PSD, היא מכילה כמעט [כל התכונות](https://docs.aspose.com/psd/java/features/) הזמינות בעורך פוטושופ ו**שכבת כיוון צבע**, שמתאימה למשימה זו בדיוק, אינה חרוץ.

שכבת הכיוון צבע מאפשרת לשנות את היחס בין צבעי הראשיים (RGB) וצבעים סובקטיביים (CMY) עבור צלליות, טונים אמצעים והדגשות בדרך פשוטה ומהירה.

## כיוון צבע

כפי שצוין למעלה, שכבת כיוון צבע ב- Aspose.PSD עבור Java היא בעצם **מתיק שלישי בין צבעי הראשיים והסובקטיביים**. זה אומר שיש שלושה קני שכל עבור כל זוג צבעים (ציאן/אדום, מג'נטה/ירוק, צהוב/כחול). העוצמה של צבע מסוים בזוג יגדל אם הערך משתקף אליו ולהפך. ולמעלה מזה, השלושה זוגות הנ"ל ירושים לכל אזור בטווח הטונאלי (צלליות, טונים אמצעים והדגשות) ומרבים את הגמישות של סוג זה של כיוון.

לכן, נחליט לשמוש בידע זה בפועל. לדוגמה, נבחר תמונת פנים של אישה בגוון אדום (ב). הפנים כל כך בגווני ורוד ואנו מתכוונים לתקן את זה על ידי **הוספת שכבת כיוון צבע** כדי להפחית את האדום ולהגדיל את הצפון בסופו של דבר (א) כדי לקבל פנים שנראות טבעיות יותר (ג). שוב, יש המון עבודה לבצע עם תמונה זו אך בתוך מאמר זה זהו כל מה שנעשה.

![דוגמת שכבת כיוון צבע](color-balance-adjustment-layer-example-figure-1.png) ממשק ה- API של שכבת כיוון צבע כולל עיצוב שטוח. לכן, ה- [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer) כיתה היא כל מה שאתה צריך. לפני הכל, שמור על עוצמת האור מאחר והיא מנוטרלת כברירת מחדל. לאחר מכן, הוסף קצת ירוק ועוד קצת צהוב לצלליות באמצעות השיטות הרלוונטיות (שמותיהן מורכבים משם אזור טווח הטונאלי המסוים ושמות הצבע בזוג הצבעים), לאחר מכן הוסף יותר ציאן ומעט כחול לטונים אמצעיים, ולסיום הוסף עוד ציאן מלבד מעט מג'נטה וכחול:

    ColorBalanceAdjustmentLayer colorBalanceAdjustmentLayer = psdImage.addColorBalanceAdjustmentLayer();
    colorBalanceAdjustmentLayer.setPreserveLuminosity(true);
    colorBalanceAdjustmentLayer.setShadowsMagentaGreenBalance((short)5);
    colorBalanceAdjustmentLayer.setShadowsYellowBlueBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setMidtonesYellowBlueBalance((short)10);
    colorBalanceAdjustmentLayer.setHighlightsCyanRedBalance((short)-20);
    colorBalanceAdjustmentLayer.setHighlightsMagentaGreenBalance((short)-5);
    colorBalanceAdjustmentLayer.setHighlightsYellowBlueBalance((short)5);

עכשיו, יש לנו את התמונה שרצינו! פשוט מאוד, איננו?

לחשוב על _ערך כל זוג צבע חייב להיות בטווח מ-100 ל-100_ כולל ערכים שליליים לצבעי סובקטיביים וחיוביים לצבעי ראשיים בהתאמה, בדיוק כמו בעורך הפוטושופ.

כדי לקבל מידע טכני נוסף על [שכבת כיוון צבע](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), מומלץ להתייחס למדריך ה- API שלנו.

## מסקנה

במאמר זה בדקנו כיצד לכוון את יחסי הצבע של התמונה באופן תכנותי בשפת Java באמצעות ספריית Aspose.PSD עבור Java. הספריה מכילה ממשק API מלא שמאפשר לעבוד עם שכבות כיוון צבע במסמכי פוטושופ.
