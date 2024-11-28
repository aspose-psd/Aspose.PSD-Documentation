---
title: إنشاء صورة PSD أو PSB من البداية باستخدام Python
weight: 100
type: docs
description: مثال على كيفية يمكن لـ Aspose.PSD for Python إنشاء صورة Psd من الصفر
keywords: [إنشاء psd, إنشاء psb, إنشاء جديد, إنشاء طبقة, إنشاء طبقة نص, واجهة برمجة التطبيقات لـ psd, python, مثال على الشيفرة]
url: /ar/python-net/إنشاء-صور-psd-psb-من-البداية/
---

## **نظرة عامة**
لإنشاء ملف PSD أو PSB من البداية باستخدام Aspose.PSD لـ Python، يمكنك اتباع الخطوات التالية:

استيراد الوحدات والصفوف اللازمة من مكتبة Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

تحديد اسم ملف الإخراج والمسار:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

إنشاء صورة PSD بالأبعاد المرغوبة:

```python 
with PsdImage(500, 500) as img:
```

إضافة طبقة PSD عادية وتحديثها باستخدام واجهة برمجة التطبيقات الرسومية:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

إنشاء طبقة نص:
```python 
textLayer = img.add_text_layer("نص عينة", Rectangle(200, 200, 100, 100))
```

إضافة تأثير ظل النص إلى طبقة النص:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

حفظ ملف الـ PSD:
```python 
img.save(outputFile)
```

ينشئ هذا الكود صورة PSD بأبعاد 500x500 بكسل. يضيف طبقة عادية ويرسم إليبس عليها باستخدام قلم وفرشاة. ثم يضيف طبقة نص بالنص "نص عينة" ويطبق تأثير ظل النص عليه. وأخيرًا، يقوم بحفظ ملف الـ PSD بالاسم المحدد.

يرجى ملاحظة أنه سيتعين عليك أن تكون لديك مكتبة Aspose.PSD مثبتة ومهيأة بشكل صحيح في بيئة Python الخاصة بك لكي يعمل هذا الشيفرة. يمكنك الرجوع إلى وثائق Aspose.PSD الرسمية لمزيد من المعلومات حول كيفية تثبيت واستخدام المكتبة.

يرجى التحقق من المثال الكامل.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose.Psd-create-psd-psb-images-from-scratch.py" >}}