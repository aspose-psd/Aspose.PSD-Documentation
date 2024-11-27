---
title: تأثیر ضربه با پر کردن رنگ
type: docs
weight: 60
url: /fa/net/stroke-effect-with-color-fill/
---

## **تأثیر ضربه با پر کردن رنگ**
این مقاله نحوه رندر کردن تأثیر ضربه با پر کردن رنگ را نشان می‌دهد. تأثیر ضربه برای افزودن ضربه‌ها و حاشیه‌ها به لایه‌ها و اشکال استفاده می‌شود. این می‌تواند برای ایجاد خطوط رنگی جامد، انتقالات رنگارنگ، و همچنین حاشیه‌های الگویی استفاده شود.

مراحل رندر کردن تأثیر ضربه با پرکردن رنگ به شرح زیر است:
- ویژگی‌ [**LoadEffectsResource**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions/properties/loadeffectsresource) را تنظیم کنید.
- فایل PSD را به عنوان یک تصویر با استفاده از متد کارخانه Load ارائه شده توسط کلاس Image بارگیری کنید و [**PsdLoadOptions**](https://reference.aspose.com/psd/net/aspose.psd.imageloadoptions/psdloadoptions) را تعریف کنید.
- ویژگی‌های تنظیمات [**ColorFillSetting.**](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.fillsettings/colorfillsettings) را تنظیم کنید.
- نتایج را ذخیره کنید.

کد زیر نشان می‌دهد چطور تأثیر ضربه با پر کردن رنگ را رندر کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.cs" >}}
