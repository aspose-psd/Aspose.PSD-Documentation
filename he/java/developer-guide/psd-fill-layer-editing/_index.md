---
title: עדכון שכבת מילוי PSD באמצעות Java
weight: 100
type: docs
description: דוגמאות לשימוש בכל סוגי שכבות ההתאמה כולל שכבת מילוי בצבע, שכבת מילוי בעברית ושכבת מילוי בתבנית
keywords: [fill layer, Color Fill, Gradient Fill, Pattern Fill, psd api, java, code sample]
url: he/java/psd-fill-layer-editing/
---

## **סקירה**

יצירת שכבה רגילה משתמשת בפונקציית createRegularLayer, שמחייבת פרמטרים להגדרת מיקום וגודל השכבה. פונקציה זו יוצרת שכבה חדשה, מגדירה את גבולותיה, וממלאה בצבע מוגדר.

לשכבות מילוי בצבע, אתה משתמש בשיטת FillLayer.createInstance עם הפרמטר FillType.Color. לאחר יצירת השכבת מילוי, ניתן לגשת להגדרות המילוי דרך הקרקעות fill_settings ולהגדיר את הצבע הרצוי באמצעות השדה color של מחלקת ColorFillSettings. בהקשר זה, הצבע מוגדר לצבע Coral. בנוסף, משתנה ה-clipping של השכבת המילוי מוגדר ל־1, ומופעל כמסכת חיתוך.

שכבות מילוי בגרדיאנט נוצרות באותה דרך על ידי שימוש בשיטת FillLayer.create_instance, אך עם הפרמטר FillType.Gradient. כמו בשכבות מילוי בצבע, אתה נגש להגדרות המילוי דרך fill_settings ומגדיר נקודות צבע בגרדיאנט ונקודות שקיפות. בדוגמא זו, נקודות הצבע בגרדיאנט מוגדרות עם מחלקת GradientColorPoint, והנקודות שקיפות עם מחלקת GradientTransparencyPoint. משתנה ה-clipping של השכבת מילוי מוגדר גם כן ל־1.

שכבות מילוי בתבנית נוצרות באמצעות FillLayer.createInstance עם הפרמטר FillType.Pattern. שוב, נגש להגדרות המילוי דרך fill_settings ומגדיר נתוני התבנית ומאפיינים נוספים. בקוד זה, נתוני התבנית מוגדרים באמצעות מחלקת PatternFillSettings, ומשתנה ה-clipping מוגדר ל־1.

לאחר יצירת שכבות המילוי, יש להוסיף אותן לתמונת ה־PSD באמצעות השיטה addLayer, ולהגדיר את שם התצוגה ומאפיינים נוספים עבור כל שכבת מילוי.

לבסוף, יש לשמור את תמונת ה־PSD ואת תמונת ה־PNG המתאימה שלה באמצעות הקוד שניתן. אפשרויות ה־PNG מוגדרות לשימוש בצבע אמיתי עם אלפא לשקיפות.

מומלץ לעיין בדוגמה מלאה לפרטים נוספים.

## **דוגמה**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
