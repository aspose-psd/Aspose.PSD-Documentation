---
title: اعمال فیلتر های میانه و وینر
type: docs
weight: 10
url: /fa/net/applying-median-and-wiener-filters/
---

## **اعمال فیلتر های میانه و وینر**
فیلتر میانه یک تکنیک فیلترینگ دیجیتال غیرخطی است که اغلب برای حذف نویز استفاده می شود. این کاهش نویز مرحله پیش‌پردازشی معمولی است که باعث بهبود نتایج پردازش های بعدی می شود. فیلتر وینر فیلتر اختیاری خطی بهینه MSE (خطای مربع متوسط) برای تصاویری است که توسط نویز افزوده شده و خوشه دار شده اند. با استفاده از Aspose.PSD برای توسعه دهندگان API .NET می توانید یک فیلتر میانه برای حذف نویز تصویر و یا یک فیلتر ویینر گاوس روی تصاویر اعمال کنید. این مقاله نشان می دهد چگونه فیلتر میانه و فیلتر گاوس وینر بر روی تصاویر اعمال می شوند.
### **اعمال فیلتر میانه**
Aspose.PSD کلاس [MedianFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/medianfilteroptions) را برای اعمال فیلتر روی یک [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ارائه می دهد. قطعه کد زیر نشان می دهد چگونه می توان فیلتر میانه را بر روی یک تصویر خانه اعمال نمود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.cs" >}}


### **اعمال فیلتر گاوس وینر**
Aspose.PSD کلاس [GaussWienerFilterOptions](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions) را برای اعمال فیلتر روی یک [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ارائه می دهد. قطعه کد زیر نشان می دهد چگونه می توان فیلتر گاوس وینر را بر روی یک تصویر خانه اعمال نمود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.cs" >}}


### **اعمال فیلتر گاوس وینر برای تصویر رنگی**
Aspose.PSD کلاس [GaussWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/gausswienerfilteroptions)برای تصاویر رنگی نیز موجود است. قطعه کد زیر نشان می دهد چگونه می توان فیلتر گاوس وینر را بر روی تصویر رنگی خانه اعمال نمود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.cs" >}}


### **اعمال فیلتر وینر حرکتی**
Aspose.PSD کلاس [MotionWienerFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/motionwienerfilteroptions)را برای اعمال فیلتر روی یک [RasterImage](https://reference.aspose.com/net/psd/aspose.psd/rasterimage) ارائه می دهد. قطعه کد زیر نشان می دهد چگونه می توان فیلتر وینر حرکتی را بر روی یک تصویر خانه اعمال نمود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.cs" >}}


## **اعمال فیلتر اصلاحی بر روی یک تصویر**
این مقاله نشان می دهد چگونه از Aspose.PSD برای .NET استفاده کرد تا فیلترهای اصلاحی را بر روی یک تصویر اعمال کند. API های Aspose.PSD روش‌های موثر و آسان برای دستیابی به این هدف ارائه کرده اند. Aspose.PSD برای .NET کلاس [BilateralSmoothingFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/bilateralsmoothingfilteroptions)و [SharpenFilterOptions ](https://reference.aspose.com/net/psd/aspose.psd.imagefilters.filteroptions/sharpenfilteroptions)را برای فیلتراسیون فراهم کرده است. کلاس BilateralSmoothingFilterOptions نیازمند یک عدد صحیح به عنوان اندازه است. مراحل انجام تغییرات ساده هستند:

1. تصویر را با استفاده از متد کارخانه Load ارائه شده توسط Image class بارگیری کنید.
1. تصویر را به RasterImage تبدیل نمایید.
1. نمونه ای از BilateralSmoothingFilterOptions و SharpenFilterOptions ایجاد نمایید.
1. متد [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) را صدا بزنید در حالیکه مستطیل های مشخصی را به عنوان محدوده تصویر و نمونه کلاس BilateralSmoothingFilterOptions اعلام می کنید.
1. متد [RasterImage.Filter](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/filter) را صدا بزنید در حالیکه مستطیل های مشخصی را به عنوان محدوده تصویر و نمونه کلاس SharpenFilterOptions اعلام می کنید.
1. کنتراست را تنظیم کنید.
1. روشنایی را تنظیم کنید.
1. نتایج را ذخیره کنید.


## **استفاده از الگوریتم آستانه Bradley**
تعیین آستانه تصویر در برنامه های گرافیکی استفاده می شود. هدف از تعیین آستانه تصویر، دسته بندی پیکسل ها به عنوان "تاریک" یا "روشن" است. API Aspose.PSD به شما امکان استفاده از تعیین آستانه Bradley را هنگام تبدیل تصاویر می دهد. قطعه کد زیر نشان می دهد چگونه مقدار آستانه را تعریف کرده و سپس الگوریتم آستانه Bradley را فراخوانی کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Bradleythreshold-Bradleythreshold.cs" >}}
