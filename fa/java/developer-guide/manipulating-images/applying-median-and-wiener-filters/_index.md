---
title: اعمال فیلترهای میانگین و وینر
type: docs
weight: 10
url: /fa/java/applying-median-and-wiener-filters/
---

## **اعمال فیلترهای میانگین و وینر**
فیلتر میانگین یک تکنیک فیلترینگ دیجیتال غیرخطی است که اغلب برای حذف نویز استفاده می‌شود. این کاهش نویز یک مرحله پیش‌پردازش معمولی برای بهبود نتایج پردازش‌های بعدی است. فیلتر وینر فیلتر بهینه MSE (خطا مربعات میانگین) خطی و ایستان برای تصاویری است که توسط نویز افزایشی و ابهام‌زایی دچار تغییر شده اند. با استفاده از Aspose.PSD برای توسعه‌دهندگان API جاوا، امکان اعمال فیلتر میانگین برای حذف نویز تصویر و اعمال فیلتر وینر گاوس بر روی تصاویر وجود دارد. این مقاله نشان می‌دهد که چگونه فیلتر میانگین و فیلتر گاوس وینر روی تصاویر قابل اعمال است.

### **اعمال فیلتر میانگین**
Aspose.PSD کلاس MedianFilterOptions را برای اعمال فیلتر بر روی یک RasterImage ارائه می‌دهد. تکه کد زیر نشان می‌دهد چگونه می‌توان فیلتر میانگین را بر روی یک تصویر راستری اعمال کرد.


{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMedianAndWienerFilters-ApplyMedianAndWienerFilters.java" >}}
### **اعمال فیلتر گاوس وینر**
Aspose.PSD کلاس GaussWienerFilterOptions را برای اعمال فیلتر بر روی RasterImage فراهم می‌کند. تکه کد زیر نشان می‌دهد چگونه می‌توان فیلتر گاوس وینر را بر روی یک تصویر راستری اعمال کرد.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFilters-ApplyGausWienerFilters.java" >}}
### **اعمال فیلتر گاوس وینر بر روی تصویر رنگی**
Aspose.PSD برای تصاویر رنگی هم GaussWienerFilterOptions را ارائه می‌دهد. تکه کد زیر نشان می‌دهد چگونه می‌توان فیلتر گاوس وینر را بر روی یک تصویر رنگی اعمال کرد.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyGausWienerFiltersForColorImage-ApplyGausWienerFiltersForColorImage.java" >}}
### **اعمال فیلتر موشن وینر**
Aspose.PSD کلاس MotionWienerFilterOptions را برای اعمال فیلتر بر روی یک RasterImage فراهم می‌کند. تکه کد زیر نشان می‌دهد چگونه می‌توان فیلتر موشن وینر را بر روی یک تصویر راستری اعمال کرد.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyMotionWienerFilters-ApplyMotionWienerFilters.java" >}}
## **اعمال فیلتر اصلاحی بر روی یک تصویر**
این مقاله نشان می‌دهد چگونه از Aspose.PSD برای جاوا برای انجام فیلترهای اصلاحی بر روی یک تصویر استفاده کنید. API‌های Aspose.PSD متداول و ساده برای دست‌یابی به این هدف ارائه کرده‌اند. Aspose.PSD برای جاوا کلاس‌ BilateralSmoothingFilterOptions و SharpenFilterOptions را برای اعمال فیلتر به تصاویر فراهم کرده است. کلاس BilateralSmoothingFilterOptions نیاز به یک عدد صحیح به عنوان اندازه دارد. مراحل انجام تغییرات به سادگی به صورت زیر است:

1. تصویر را با استفاده از متد کارخانه Load کلاس Image بارگذاری کنید.
1. تصویر را به RasterImage تبدیل کنید.
1. نمونه‌هایی از BilateralSmoothingFilterOptions و SharpenFilterOptions بسازید.
1. متدFilter کلاس RasterImage را با مشخص کردن مستطیل به عنوان مرزهای تصویر و نمونه کلاس BilateralSmoothingFilterOptions فراخوانی کنید.
1. متدFilter کلاس RasterImage را با مشخص کردن مستطیل به عنوان مرزهای تصویر و نمونه کلاس SharpenFilterOptions فراخوانی کنید.
1. کنتراست را تنظیم کنید.
1. روشنایی را تنظیم کنید.
1. نتایج را ذخیره کنید.

تکه کد زیر نشان می‌دهد چگونه می‌توان فیلتر اصلاحی را اعمال کرد.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-ApplyCorrectionFilterOnImage-ApplyCorrectionFilterOnImage.java" >}}
## **استفاده از الگوریتم آستانه Bradley**
آستانه‌گذاری تصویر در برنامه‌های گرافیکی استفاده می‌شود. هدف از آستانه‌گذاری تصویر، طبقه‌بندی پیکسل‌ها به عنوان "تاریک" یا "روشن" است. API Aspose.PSD به شما امکان استفاده از آستانه‌گذاری Bradley را هنگام تبدیل تصاویر می‌دهد. تکه کد زیر نشان می‌دهد چگونه می‌توانید مقدار آستانه را تعریف کرده و سپس الگوریتم آستانه Bradley را فراخوانی کنید.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Conversion-Bradleythreshold-Bradleythreshold.java" >}}
