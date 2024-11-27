---
title: افزودن یک علامت‌گذاری به تصویر
type: docs
weight: 30
url: /fa/net/adding-a-watermark-to-an-image/
---

## **افزودن یک علامت‌گذاری به تصویر**
این سند توضیح می‌دهد چگونه از Aspose.PSD برای افزودن یک علامت‌گذاری به یک تصویر استفاده کنید. افزودن یک علامت‌گذاری به یک تصویر نیاز متداولی در برنامه‌های پردازش تصویر است. این مثال از کلاس Graphics برای رسم یک رشته بر روی سطح تصویر استفاده می‌کند.

### **افزودن یک علامت‌گذاری**
برای نمایش عمل، یک تصویر BMP از دیسک بارگذاری کرده و یک رشته به عنوان علامت‌گذاری در سطح تصویر با استفاده از متد DrawString کلاس Graphics رسم خواهیم کرد. سپس تصویر را با استفاده از کلاس PngOptions به فرمت PNG ذخیره خواهیم کرد. کد زیر نحوه افزودن یک علامت‌گذاری به یک تصویر را نشان می‌دهد. کد منبع مثال به بخش‌هایی تقسیم شده است تا دنبال کردن آن آسان شود. گام به گام، مثال‌ها نحوه:

1. تصویر را [بارگذاری](https://reference.aspose.com/psd/net/aspose.psd.image/load/methods/2) کنید.
1. یک شی از کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) ایجاد و مقداردهی کنید.
1. یک شی از فونت و [SolidBrush](https://reference.aspose.com/psd/net/aspose.psd.brushes/solidbrush) ایجاد و مقداردهی کنید.
1. یک رشته به عنوان علامت‌گذاری با استفاده از متد [DrawString](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawstring) کلاس Graphics رسم کنید.
1. تصویر را به فرمت PNG ذخیره کنید.

کد زیر نحوه افزودن یک علامت‌گذاری به تصویر را نشان می‌دهد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddWatermark-AddWatermark.cs" >}}

### **افزودن یک علامت‌گذاری مورب**
افزودن یک علامت‌گذاری مورب به یک تصویر مشابه افزودن یک علامت‌گذاری افقی است که در بالا بحث شد، با تعدادی تفاوت. برای نشان دادن عمل، یک تصویر JPG را از دیسک بارگذاری کرده، تبدیل‌ها با استفاده از یک شی از کلاس [Matrix](https://reference.aspose.com/psd/net/aspose.psd/matrix) اضافه کرده و یک رشته به عنوان علامت‌گذاری در سطح تصویر با استفاده از متد DrawString کلاس Graphics رسم خواهیم کرد. کد زیر نحوه افزودن یک علامت‌گذاری مورب به تصویر را نشان می‌دهد. کد منبع مثال به بخش‌هایی تقسیم شده است تا دنبال کردن آن آسان شود. گام به گام، مثال‌ها نحوه:

1. تصویر را بارگذاری کنید.
1. یک شی از کلاس Graphics ایجاد و مقداردهی کنید.
1. یک شی از [Font](https://reference.aspose.com/psd/net/aspose.psd/font) و SolidBrush ایجاد و مقداردهی کنید.
1. اندازه تصویر را در شی SizeF بدست آورید.
1. یک نمونه از کلاس Matrix ایجاد کرده و تبدیلات ترکیبی انجام دهید.
1. تبدیل را به شی Graphics اختصاص دهید.
1. یک شی از کلاس [StringFormat](https://reference.aspose.com/psd/net/aspose.psd/stringformat) ایجاد و مقداردهی کنید.
1. یک رشته به عنوان علامت‌گذاری با استفاده از متد DrawString کلاس Graphics رسم کنید.
1. تصویر نتیجه‌ای را ذخیره کنید.

کد زیر نحوه افزودن یک علامت‌گذاری مورب را نشان می‌دهد.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-AddDiagnolWatermark-AddDiagnolWatermark.cs" >}}
