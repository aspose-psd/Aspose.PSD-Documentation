---
title: پشتیبانی از لایه‌های پر شده
type: docs
weight: 50
url: /fa/java/support-of-fill-layers/
---

## **پشتیبانی از لایه‌های پر شده با رنگ**
این مقاله نشان می‌دهد چگونه می‌توان یک لایه PSD را با رنگ پر کرد. لطفا از کلاس Aspose.PSD.FileFormats.Psd.Layers.FillLayer برای اضافه کردن رنگ به لایه PSD استفاده کنید. کد‌های زیر یک فایل PSD را بارگذاری می‌کند، به کلاس Filllayer دسترسی پیدا می‌کند و رنگ را با استفاده از ویژگی FillLayer.FillSettings تنظیم می‌کند.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-ColorFillLayer-ColorFillLayer.java" >}}
## **پشتیبانی از لایه‌های پر شده با افقی**
این مقاله نحوه استفاده از پرکردن افقی برای پر کردن لایه PSD را نشان می‌دهد. API‌های Aspose.PSD روش‌های کارآمد و آسان را برای رسیدن به این هدف ارائه کرده‌اند. Aspose.PSD کلاس‌های GradientColorPoint و GradientTransparencyPoint را برای افزودن اثر افقی به یک لایه ارائه کرده است.

مراحل پر کردن لایه PSD با پر افقی به سادگی زیر هستند:

- یک فایل PSD را به عنوان یک تصویر با استفاده از متد Load ارائه شده توسط کلاس Image بارگذاری کنید.
- ویژگی‌های تنظیمات شی FillLayer را تنظیم کنید.
- لیستی از ColorPoints با رنگ‌ها و موقعیت رنگ مورد نیاز ایجاد کنید.
- لیستی از transparencyPoints با شفافیت مورد نیاز و موقعیت نقطه شفافیت ایجاد کنید.
- متد FillLayer.Update را فرا خوانی کنید.
- نتایج را ذخیره کنید.

کد زیر به شما نشان می‌دهد چگونه می‌توانید پر افقی را به لایه PSD اضافه کنید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-GradientFillLayer-GradientFillLayer.java" >}}


## **اثر ضربه با پر شدن رنگ**
این مقاله نحوه اعمال اثر ضربه با پر کردن رنگ را نشان می‌دهد. اثر Stroke برای اضافه کردن ضربه‌ها و حاشیه‌ها به لایه‌ها و اشکال استفاده می‌شود. این می‌تواند برای ایجاد خطوط رنگی جامد، افقی رنگارنگ، و همچنین حاشیه‌های الگویی استفاده شود.

مراحل اعمال اثر ضربه با پر کردن رنگ به سادگی زیر هستند:

- ویژگی LoadEffectsResource را تنظیم کنید.
- یک فایل PSD را به عنوان یک تصویر با استفاده از متد Load ارائه شده توسط کلاس Image بارگذاری کنید و PsdLoadOptions را تعریف کنید.
- ویژگی‌های تنظیمات شی ColorFillSetting را تنظیم کنید.
- نتایج را ذخیره کنید.

کد زیر به شما نشان می‌دهد چگونه می‌توانید اثر ضربه با پر کردن رنگ را اعمال کنید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-StrokeEffectWithColorFill-StrokeEffectWithColorFill.java" >}}

