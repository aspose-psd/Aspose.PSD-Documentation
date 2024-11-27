---
title: ایجاد تصویر PSD یا PSB از ابتدا با استفاده از پایتون
weight: 100
type: docs
description: نمونه از نحوه‌ی ایجاد تصویر Psd از ابتدا با استفاده از Aspose.PSD برای پایتون
keywords: [ایجاد psd, ایجاد psb, ایجاد جدید, ایجاد لایه, ایجاد لایه متن, رابط برنامه نویسی psd, پایتون, نمونه کد]
url: fa/python-net/ایجاد-psd-psb-images-from-scratch/
---

## **مرور**
برای ایجاد یک فایل PSD یا PSB از ابتدا با استفاده از Aspose.PSD برای پایتون، می‌توانید مراحل زیر را دنبال کنید:

وارد کردن ماژول‌ها و کلاس‌های لازم از کتابخانه Aspose.PSD:
```python 
from aspose.psd import Graphics, Pen, Color, Rectangle
from aspose.psd.brushes import LinearGradientBrush
from aspose.psd.fileformats.psd import PsdImage
```

مشخص کردن نام و مسیر فایل خروجی:

```python 
outputFile = "CreateFileFromScratchExample.psd"
```

ایجاد تصویر PSD با ابعاد مورد نظر:

```python 
with PsdImage(500, 500) as img:
```

اضافه کردن یک لایه PSD معمولی و به‌روزرسانی آن با استفاده از رابط گرافیکی:

```python 
regularLayer = img.add_regular_layer()
graphics = Graphics(regularLayer)
pen = Pen(Color.alice_blue)
brush = LinearGradientBrush(Rectangle(250, 250, 150, 100), Color.red, Color.aquamarine, 45)
graphics.draw_ellipse(pen, Rectangle(100, 100, 200, 200))
graphics.fill_ellipse(brush, Rectangle(250, 250, 150, 100))
```

ایجاد یک لایه متن:
```python 
textLayer = img.add_text_layer("متن نمونه", Rectangle(200, 200, 100, 100))
```

اضافه کردن اثر سایه به لایه متن:
```python 
dropShadowEffect = textLayer.blending_options.add_drop_shadow()
dropShadowEffect.distance = 0
dropShadowEffect.size = 8
dropShadowEffect.color = Color.blue
```

ذخیره کردن فایل PSD:
```python 
img.save(outputFile)
```

این کد یک تصویر PSD با ابعاد 500x500 پیکسل ایجاد می‌کند. یک لایه معمولی اضافه کرده و یک بیضوی بر روی آن رسم می‌کند با استفاده از یک خودکار و یک مداد. سپس یک لایه متن با متن "متن نمونه" اضافه می‌کند و یک اثر سایه به آن اعمال می‌کند. در نهایت، فایل PSD را با نام فایل خروجی مشخص شده ذخیره می‌کند.

لطفاً توجه داشته باشید که برای کارکردن این کد، باید کتابخانه Aspose.PSD را نصب و به‌درستی در محیط پایتون خود تنظیم کرده باشید. می‌توانید به مستندات رسمی Aspose.PSD مراجعه کنید برای اطلاعات بیشتر درباره نحوه‌ی نصب و استفاده از کتابخانه.

لطفاً مثال کامل را چک کنید.

## **نمونه**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-create-psd-psb-images-from-scratch.py" >}}
