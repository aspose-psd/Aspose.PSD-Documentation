---
title: צור תמונת PSD או PSB מאפס באמצעות Python
weight: 100
type: docs
description: דוגמה לכיצד Aspose.PSD ל-Python יכול ליצור תמונת Psd מאפס
keywords: [יצירת psd, יצירת psb, צור חדש, צור שכבה, צור שכבת טקסט, psd api, python, קוד דוגמה]
url: he/python-net/create-psd-psb-images-from-scratch/
---

## **סקירה**
כדי ליצור קובץ PSD או PSB מאפס באמצעות Aspose.PSD ל-Python, ניתן לעקוב אחר השלבים הבאים:

יבא את המודולים והמחלקות הדרושים מספריית Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

ציין את שם קובץ הפלט והנתיב:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

צור תמונת PSD עם הממדים הרצויים:

```python 
with PsdImage(500, 500) as img:
```

הוסף שכבת PSD רגילה ועדכן אותה באמצעות ממשק הגרפיקה:
```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

צור שכבת טקסט:
```python 
textLayer = img.add_text_layer("Sample Text", Rectangle(200, 200, 100, 100))
```

הוסף אפקט צל לשכבת הטקסט:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

שמור את קובץ ה-PSD:
```python 
img.save(outputFile)
```

הקוד הזה יוצר תמונת PSD בממדים של 500x500 פיקסלים. הוא מוסיף שכבה רגילה ומרשימה אליה אליפסה באמצעות עט ומברשת. לאחר מכן הוא מוסיף שכבת טקסט עם הטקסט "Sample Text" ומחיל אפקט צל לו. לבסוף, הוא שומר את קובץ ה-PSD עם שם הקובץ המצוין.

יש לציין כי לצורך פעולת הקוד הזה יהיה עליך להתקין את ספריית Aspose.PSD ולהגדיר אותה בצורה תקינה בסביבת ה-Python שלך. תוכל להתייחס למסמך ההוראות הרשמי של Aspose.PSD למידע נוסף על איך להתקין ולהשתמש בספרייה.

אנא בדוק דוגמה מלאה.

## **דוגמה**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
