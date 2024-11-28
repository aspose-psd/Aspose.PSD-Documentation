---
title: استفاده از لایه تنظیم برای بهبود‌های PSD
weight: 100
type: docs
description: نمونه‌های استفاده از لایه‌های تنظیم از طریق Aspose.PSD برای C#
keywords: [لایه تنظیم, بهبود عکس, تنظیم منحنی‌ها, افزایش سطوح, برعکس کردن, فیلتر عکس, رابط برنامه نویسی اس‌دی, C#, سی‌شارپ, نمونه کد]
url: fa/net/adjustment-layer-enhancement/
---

## مرور

در این مقاله، ما قصد داریم ویرایش لایه‌های تنظیمی را در Aspose.PSD برای C# بررسی کنیم. لایه‌های تنظیم ویژگی‌های قدرتمندی در ویرایش تصویر دارند که به شما امکان می‌دهند تغییرات غیر مخربی در تصاویر خود اعمال کنید. Aspose.PSD مجموعه جامعی از کلاس‌های لایه تنظیم ارایه کرده است که می‌توانید از آنها برای تغییرات مختلفی در تصاویرتان استفاده کنید.

برای نمایش ویرایش لایه‌های تنظیم، ما از یک قطعه کد نمونه در انتهای صفحه استفاده خواهیم کرد که یک تصویر PSD را بارگیری می‌کند و تغییرات مختلفی را در لایه‌های آن اعمال می‌کند.

در قطعه کد زیر، ما با بارگیری تصویر PSD با استفاده از متد `PsdImage.Load()` شروع می‌کنیم. سپس گزینه‌ها برای ذخیره فایل‌های PNG خروجی را تنظیم می‌کنیم. کلاس `PngOptions` به ما امکان می‌دهد تا نوع رنگ برای تصویر خروجی را مشخص کنیم.

سپس، ما از روی هر لایه در تصویر PSD عبور می‌کنیم و نوع آن را با استفاده از متد `IsAssignable()` بررسی می‌کنیم. اگر لایه از نوع خاصی باشد، ما آن را به آن نوع تبدیل کرده و تنظیم مورد نظر را اعمال می‌کنیم. به عنوان مثال، ما روشنایی و تضاد یک `BrightnessContrastLayer` را تنظیم می‌کنیم، سطح‌های یک `LevelsLayer` را تغییر می‌دهیم، نقطه‌ای به یک `CurvesLayer` اضافه می‌کنیم و غیره.

شما می‌توانید کد اضافی برای اعمال تغییرات دیگر به لایه‌های مربوطه اضافه کنید. Aspose.PSD مجموعه گسترده‌ای از کلاس‌های لایه تنظیم ارایه می‌دهد مانند [ExposureLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer), [HueSaturationLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/huesaturationlayer), [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/colorbalanceadjustmentlayer), [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/blackwhiteadjustmentlayer), [PhotoFilterLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/photofilterlayer), [ChannelMixerLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/channelmixerlayer), [InvertAdjustmentLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/invertadjustmentlayer), [PosterizeLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/posterizelayer), [ThresholdLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/thresholdlayer), [SelectiveColorLayer](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.adjustmentlayers/selectivecolorlayer)، و غیره.

در نهایت، تصویر تغییر یافته را با استفاده از متد `Save()` کلاس `PsdImage` ذخیره می‌کنیم.

این کد یک مرور ابتدایی از چگونگی ویرایش لایه‌های تنظیم در Aspose.PSD برای C# ارایه می‌دهد. شما می‌توانید تنظیمات را مطابق با نیازهای خود سفارشی کنید و گزینه‌های مختلفی که در اسناد رابط برنامه نویسی موجود هستند را بررسی کنید.

## مثال

در زیر یک نمونه کد ارایه شده که نشان می‌دهد چگونه از لایه‌های تنظیم با استفاده از Aspose.PSD برای C# استفاده کنید:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "UsingAdjustmentLayers-UsingAdjustmentLayers.cs" >}}

برای اطلاعات و مثال‌های بیشتر، لطفا به [مستندات Aspose.PSD برای C#](https://docs.aspose.com/psd/net/) مراجعه کنید.

