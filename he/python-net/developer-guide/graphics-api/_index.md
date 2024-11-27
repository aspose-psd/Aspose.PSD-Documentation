---
title: שימוש ב- API גרפי לעריכת שכבות בקבצי PSD
weight: 100
type: docs
description: דוגמה לשימוש ב- API גרפי ב- Aspose.PSD עבור Python
keywords: [עדכון שכבה, ציור מעגל, ציור אליפסה, ציור מעגל ממולא, גרפיקה, API של psd, פייתון, קוד לדוגמה]
url: he/python-net/graphics-api/
---

## **סקירה**
לפני הכל, עליך לטעון את קובץ ה-PSD באמצעות השיטה Image.load() או ליצור תמונת Psd מאפס. בדוגמה, המשתנה inputFile מייצג את הנתיב אל קובץ ה-PSD שלך, והשיטת loadOpt מייצגת אפשרויות הטעינה (אם יש).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
לאחר מכן, ניתן לגשת לשכבה הראשונה של התמונת PSD באמצעות התחביר psdImage.layers[0]. זה נותן לך ייחוד לפריט השכבה שניתן לנהל.

```python 
layer = psdImage.layers[0]
```
כדי לערוך את השכבה, עליך ליצור אובייקט של Graphics על ידי העברת השכבה כפרמטר. אובייקט זה מספק שיטות שונות לצייר צורות ולהחיל מכחולים.

```python 
graphics = Graphics(layer)
```
בדוגמה הקודמת, נוצר אובייקט Pen כדי להגדיר את הצבע והעובי של קו מעגל האליפסה. קבוע הצבע Color.alice_blue מייצג את הצבע, וניתן להתאים את העובי כפי הצורך.

```python 
pen = Pen(Color.alice_blue)
```
באופן דומה, נוצר אובייקט LinearGradientBrush כדי להגדיר את צבע המילוי של אליפסת הצורה. ה-Rectangle(250, 250, 150, 100) מייצג את המיקום והגודל של אליפסת הצורה, והצבעים Color.red ו-Color.aquamarine מייצגים את הצבעים התחילתי והסופי של הגרדיאנט.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
כדי לצייר את אליפסת הצורה על השכבה, ניתן להשתמש בשיטה graphics.draw_ellipse(). ה-Rectangle(100, 100, 200, 200) מייצג את המיקום והגודל של אליפסת הצורה.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
כדי למלא את אליפסת הצורה במברשת הגרדיאנט, ניתן להשתמש בשיטת graphics.fill_ellipse(). ה-Rectangle(250, 250, 150, 100) מייצג את המיקום והגודל של אליפסת הצורה.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
לאחר לבצע את השינויים הרצויים על השכבה, ניתן לשמור את קובץ התמונה בפורמט PSD המשוכפל באמצעות השיטה psdImage.save(). בדוגמה, המשתנה psdName מייצג את הנתיב לשמור את קובץ ה-PSD המשופר.

```python 
psdImage.save(psdName)
```
בנוסף, ניתן גם לשמור את התמונה המשופרת בפורמטים אחרים, כגון PNG, על ידי שימוש במחלקת PngOptions. המשתנה pngName מייצג את הנתיב לשמור את קובץ ה-PNG.

```python 
psdImage.save(pngName, PngOptions())
```
!זהו, השתמשת בהצלחה ב- API גרפי של Aspose.PSD עבור Python כדי לערוך שכבות בקובץ PSD. נשמח להמשך בחקר התכונות והפונקציות הנוספות בספריית Aspose.PSD כדי לשפר את יכולות העריכה שלך לתמונות.

.V. דוגמה
{{<gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py" >}}
