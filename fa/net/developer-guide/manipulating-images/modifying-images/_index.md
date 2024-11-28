---
title: تغییر تصاویر
type: مستندات
weight: 50
url: /fa/net/modifying-images/
---

## **راینش کردن برای تصاویر رستر**
راینش یک تکنیک برای ایجاد حس خلق رنگ‌ها و سایه‌های جدید با تغییر الگوی نقاطی است که در واقع تصویری ایجاد می‌کنند. این راینش بیشترین وسیله‌ای است که برای کاهش بردار رنگی تصاویر به 256 (یا کمتر) رنگ استفاده می‌شود. Aspose.PSD پشتیبانی از راینش برای کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) را با معرفی روش Dither فراهم می‌کند که دو پارامتر را می‌پذیرد. اولین پارامتر از نوع DitheringMethod است که با دو گزینه ممکن FloydSteinbergDithering و ThresholdDithering کاربرد دارد. پارامتر دوم به روش [Dither](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/dither) مقدار نرمال‌اینتجر را می‌پذیرد. BitCount اندازه نمونه‌برداری برای نتیجه راینش را تعریف می‌کند. مقدار پیش‌فرض 1 است که سیاه و سفید را نشان می‌دهد، در حالی که مقادیر مجاز 1، 4، 8 برای ایجاد پالت با 2، 4 و 256 رنگ به ترتیب هستند.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-DitheringforRasterImages-DitheringforRasterImages.cs" >}}
## **تنظیم روشنایی، کنتراست و گاما**
تنظیمات رنگی در تصاویر دیجیتال یکی از ویژگی‌های اصلی است که اکثر کتابخانه‌های پردازش تصاویر ارائه می‌دهند. تنظیمات رنگی می‌توانند به شکل زیر دسته‌بندی شوند.

1. روشنایی به نوری یا تاریکی یک رنگ اطلاق می‌گردد. افزایش روشنایی یک تصویر باعث روشنتر شدن همه رنگ‌ها می‌شود در حالی که کاهش روشنایی تاریک‌تر شدن همه رنگ‌ها را فراهم می‌کند.
1. کنتراست به واضح‌تر کردن اشیاء یا جزئیات در یک تصویر اشاره دارد. افزایش کنتراست تصویر اختلاف بین ناحیه‌های روشن و تاریک را بیشتر می‌کند به طوری که ناحیه‌های روشنتر روشن‌تر و ناحیه‌های تاریک تاریک‌تر شوند. کاهش کنتراست باعث می‌شود که نواحی روشن و تاریک تقریباً همان عملکردی را داشته باشند ولی تصویر به طور کلی یکنواخت‌تر می‌شود.
1. گاما به بهینه‌سازی کنتراست و روشنایی نور غیر مستقیمی است که یک شی را در تصویر روشن قرار داده است.

### **تنظیم روشنایی**
API Aspose.PSD برای .NET روش [AdjustBrightness](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustbrightness) را برای کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ارائه می‌دهد که می‌توان برای تنظیم روشنایی تصویر از آن با ارسال مقدار صحیح به عنوان پارامتر استفاده کرد. ارزش بالاترین پارامتر به تصویر روشنتر اشاره دارد. اینجا تصویر اصلی و تصویر نتیجه برای مقایسه آورده شده است.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingBrightness-AdjustingBrightness.cs" >}}


### **تنظیم کنتراست**
روش [AdjustContrast](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustcontrast) که توسط کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) فراهم شده است، برای تنظیم کنتراست تصویر با گذر دادن یک مقدار شناور به عنوان پارامتر استفاده می‌شود.

مقدار بالاترین پارامتر کنتراست بیشتری را در تصویر داده می‌شود. اینجا تصویر اصلی و تصویر نتیجه برای مقایسه آورده شده است.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingContrast-AdjustingContrast.cs" >}}
### **تنظیم گاما**
روش [AdjustGamma](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/adjustgamma) که توسط کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ارائه شده است دو نسخه دارد. یکی از اضافه بارها یک مقدار شناور را قبول می‌کند و اصلاح گاما برای ضرایب کانال قرمز، آبی و سبز را انجام می‌دهد. در حالی که اضافه بارها دیگر سه پارامتر شناور را قبول می‌کند که هرکدام نشان‌دهنده ضریب رنگ جداگانه است. کد انتقال زیر نشان می‌دهد که چگونه بر روی یک تصویر گاما را تنظیم کنید.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-AdjustingGamma-AdjustingGamma.cs" >}}
## **مات کردن یک تصویر**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای .NET برای اعمال اثر مات بر روی یک تصویر استفاده کنید. API های Aspose.PSD متداول و آسان برای استفاده را برای این هدف ارائه کرده است. Aspose.PSD برای .NET کلاس [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) را برای ایجاد اثر مات روی تصاویر فراهم کرده است. کلاس [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) برای ایجاد اثر مات روی یک تصویر نیاز به مقادیر شعاع و سیگما دارد. مراحل انجام تغییران بسیار ساده هستند:

1. بارگذاری تصویر با استفاده از متد کارخانه Load کلاس تصویر.
1. تبدیل تصویر به [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).
1. ایجاد یک نمونه از کلاس [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) با سازنده پیش‌فرض یا ارایه مقادیر شعاع و سیگما در سازنده.
1. فراخوانی متد [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Filter هنگامی که مستطیل را به عنوان مرز تصویر و شیی [GaussianBlurFilterOptions](https://reference.aspose.com/psd/net/aspose.psd.imagefilters.filteroptions/gaussianblurfilteroptions) را مشخص می‌کنید.
1. ذخیره نتایج.

کد زیر نشان می‌دهد چگونه می‌توان یک اثر مات بر روی تصویر ایجاد کرد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-BluranImage-BluranImage.cs" >}}
## **تأیید شفافیت تصویر**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای .NET برای بررسی شفافیت تصاویر استفاده کنید. مراحل بررسی شفافیت تصویر به شکل زیر است:

1. بارگذاری تصویر با استفاده از متد فابریکی [Load](https://reference.aspose.com/psd/net/aspose.psd/image/load/methods/2) کلاس [Image](https://reference.aspose.com/psd/net/aspose.psd/image).
1. بررسی شفافیت تصویر اگر شفافیت صفر باشد تصویر شفاف است.
1. کد زیر نشان می‌دهد چگونه می‌توان بررسی کرد که آیا تصویر شفاف است یا خیر.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-VerifyImageTransparency-VerifyImageTransparency.cs" >}}
## **پیاده‌سازی فشرده‌ساز GIF با از دست دادن**
با استفاده از Aspose.PSD برای .NET، توسعه‌دهندگان می‌توانند یک تفاوت پیکسل را تنظیم کنند. فشرده‌سازی GIF بر اساس یک "لغت‌نامه" از رشته‌هایی از پیکسل‌هاست که دیده شده است. کدگذار عادی در لغت‌نامه برای بلندترین رشته‌های پیکسلی که دقیقاً با پیکسل‌های تصویر مطابقت دارند، جستجو می‌کند. کدگذار از دست داده بلندترین رشته پیکسل‌ها را انتخاب می‌کند که "به اندازه کافی مشابه" پیکسل‌های تصویر هستند. کد نمونه زیر این عملکرد را نشان می‌دهد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementLossyGIFCompressor-ImplementLossyGIFCompressor.cs" >}}
## **پیاده‌سازی تجدید نمونه Bicubic**
تجدید نمونه به معنای تغییر ابعاد پیکسلی یک تصویر است. هنگامی که داونزمپل می‌کنید، شما پیکسل‌ها را حذف کرده و در نتیجه اطلاعات و جزئیات از تصویر خود پاک می‌کنید. وقتی اپ‌سمپل می‌کنید، پیکسل‌ها را اضافه می‌کنید. فتوشاپ این پیکسل‌ها را با استفاده از اینترپولیشن اضافه می‌کند. این مقاله نشان می‌دهد که چگونه می‌توان کار تجدید نمونه Bicubic را با استفاده از Aspose.PSD برای .NET انجام داد.

کد زیر نشان می‌دهد چگونه می‌توان تجدید نمونه Bicubic را ایجاد کرد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ImplementBicubicResampler-ImplementBicubicResampler.cs" >}}
## **لایه تنظیم تعادل رنگی**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای .NET برای انجام **لایه تنظیم تعادل رنگی** بر روی یک تصویر استفاده کنید. لایه تنظیم تعادل رنگ، امکان انجام تنظیمات روی رنگ‌های تصاویر را به شما می‌دهد. این لایه تنظیم تعادل رن
