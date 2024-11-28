---
title: استخدام واجهة برمجة التطبيقات الرسومية لتحرير الطبقات في ملفات PSD
weight: 100
type: docs
description: مثال على استخدام واجهة برمجة التطبيقات الرسومية في Aspose.PSD للبايثون
keywords: [تحديث الطبقة, رسم دائرة, رسم قرنفلة, رسم دائرة مليئة, رسومات, واجهة برمجة التطبيقات لـ PSD, بايثون, مثال على الشيفرة]
url: /ar/python-net/graphics-api/
---

## **نظرة عامة**
أولاً، تحتاج إلى تحميل ملف PSD باستخدام الطريقة Image.load() أو إنشاء صورة Psd من البداية. في المثال، تمثل المتغير inputFile مسار ملف PSD الخاص بك، ويمثل loadOpt خيارات التحميل (إن وجدت).

```python 
with Image.load(inputFile, loadOpt) as image:
    psdImage = cast(PsdImage, image)
```
بعد ذلك، يمكنك الوصول إلى الطبقة الأولى لصورة PSD باستخدام علامة الترقيم psdImage.layers[0]. هذا يمنحك مرجعًا لكائن الطبقة الذي يمكنك التلاعب به.

```python 
layer = psdImage.layers[0]
```
لتحرير الطبقة، تحتاج إلى إنشاء كائن Graphics عن طريق تمرير الطبقة كمعلمة. يوفر هذا الكائن طرقًا مختلفة لرسم الأشكال وتطبيق الفرش.

```python 
graphics = Graphics(layer)
```
في مثال الشيفرة، يتم إنشاء كائن Pen لتحديد لون وسمك حدود شكل القرنفلة. يمثل الثابت Color.alice_blue اللون، ويمكنك ضبط السمك حسب الحاجة.

```python 
pen = Pen(Color.alice_blue)
```
بالمثل، يتم إنشاء كائن LinearGradientBrush لتحديد لون التعبئة لشكل القرنفلة. يمثل Rectangle(250, 250, 150, 100) الموضع والحجم لشكل القرنفلة، ويمثل Color.red و Color.aquamarine الألوان البداية والنهاية للتدرج.

```python 
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
```
لرسم شكل القرنفلة على الطبقة، يمكنك استخدام طريقة graphics.draw_ellipse(). يمثل Rectangle(100, 100, 200, 200) الموضع والحجم لشكل القرنفلة.

```python 
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
```
لملء شكل القرنفلة بالفرشاة التدرجية، يمكنك استخدام طريقة graphics.fill_ellipse(). يمثل Rectangle(250, 250, 150, 100) الموضع والحجم لشكل القرنفلة.

```python 
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```
بعد إجراء التغييرات المطلوبة على الطبقة، يمكنك حفظ صورة PSD المعدلة باستخدام طريقة psdImage.save(). في المثال، يمثل المتغير psdName مسار حفظ ملف PSD المعدل.

```python 
psdImage.save(psdName)
```
بالإضافة إلى ذلك، يمكنك أيضًا حفظ الصورة المعدلة في تنسيقات أخرى، مثل PNG، باستخدام فئة PngOptions. يمثل المتغير pngName مسار حفظ ملف PNG.

```python 
psdImage.save(pngName, PngOptions())
```
هذا هو كل شيء! لقد استخدمت بنجاح واجهة برمجة التطبيقات الرسومية لـ Aspose.PSD للبايثون لتحرير الطبقات في ملف PSD. لا تتردد في استكشاف المزيد من الميزات والخصائص لمكتبة Aspose.PSD لتعزيز قدرات تحرير الصور الخاصة بك.

يرجى التحقق من المثال الكامل.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-graphics-api.py " >}}