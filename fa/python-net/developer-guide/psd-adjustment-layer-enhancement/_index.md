---
title: استفاده از لایه تنظیم برای بهبود‌های PSD
weight: 100
type: docs
description: نمونه‌های استفاده از لایه تنظیم از طریق Aspose.PSD برای Python
keywords: [لایه تنظیم، بهبود تصویر، تنظیم منحنی، بهبود سطوح، معکوس کردن، فیلتر تصویر،  api psd, python, نمونه کد]
url: fa/python-net/adjustment-layer-enhancement/
---

## **بررسی کلی**

در این مقاله، ما قصد داریم ویرایش لایه‌های تنظیمی در Aspose.PSD برای Python را بررسی کنیم. لایه‌های تنظیمی یک قابلیت قدرتمند در ویرایش تصویر هستند که به شما امکان می‌دهند تغییراتی غیر ازخراب‌کننده برای تصاویر خود اعمال کنید. Aspose.PSD یک مجموعه جامع از کلاس‌های لایه تنظیمی فراهم کرده است که می‌توانید برای تغییر جوانب مختلف تصاویر خود استفاده کنید.

برای نشان دادن ویرایش لایه‌های تنظیمی، ما از یک قسمت کد نمونه استفاده خواهیم کرد که در انتهای صفحه یک تصویر PSD را بارگذاری کرده و تغییرات مختلفی را به لایه‌های آن اعمال خواهیم کرد.

در قسمت کد نمونه زیر، ما با شروع به بارگذاری تصویر PSD از طریق متد PsdImage.load() شروع می‌کنیم. سپس تنظیمات ذخیره کردن پرونده‌های PNG خروجی را تنظیم می‌کنیم. کلاس PngOptions به ما این امکان را می‌دهد که نوع رنگ برای تصویر خروجی را مشخص کنیم.

سپس، ما از طریق هر لایه در تصویر PSD حرکت کرده و نوع آن را با استفاده از متد is_assignable() بررسی می‌کنیم. اگر لایه از نوع خاصی باشد، آن را به آن نوع تبدیل و تنظیم مورد نظر را اعمال می‌کنیم. به عنوان مثال، ما روی روشنایی و کنتراست یک BrightnessContrastLayer تنظیم می‌کنیم، سطوح یک LevelsLayer را تغییر می‌دهیم، یک نقطه منحنی به یک CurvesLayer اضافه می‌کنیم و غیره.

شما می‌توانید کد اضافی اضافه کنید تا تنظیمات دیگری را برای لایه‌های مربوطه اعمال کنید. Aspose.PSD یک مجموعه وسیعی از کلاس‌های لایه تنظیمی ارائه می‌دهد مانند [ExposureLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/exposurelayer)، [HueSaturationLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/HueSaturationLayer)، [ColorBalanceAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ColorBalanceAdjustmentLayer)، [BlackWhiteAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/BlackWhiteAdjustmentLayer)، [PhotoFilterLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PhotoFilterLayer)، [ChannelMixerLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ChannelMixerLayer)، [InvertAdjustmentLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/InvertAdjustmentLayer)، [PosterizeLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/PosterizeLayer)، [ThresholdLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/ThresholdLayer)، [SelectiveColorLayer](https://reference.aspose.com/psd/python-net/aspose.psd.fileformats.psd.layers.adjustmentlayers/SelectiveColorLayer) و غیره.

سرانجام، ما تصویر ویرایش شده را با استفاده از متد save() کلاس PsdImage ذخیره می‌کنیم.

این کد یک بررسی اولیه از نحوه ویرایش لایه‌های تنظیم را در Aspose.PSD برای Python ارائه می‌دهد. شما می‌توانید تنظیمات خود را به توجه به نیازهای خود سفارشی‌سازی کرده و گزینه‌های مختلف موجود در مستندات API را بررسی کنید.

لطفاً مثال کامل را بررسی کنید.

## **مثال**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-adjustment-layer-enhancement.py" >}}
