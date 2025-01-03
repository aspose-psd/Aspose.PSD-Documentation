---
title: مروری بر فرمت PSD
type: docs
weight: 60
url: /fa/net/psd-format-overview/
---

## **توضیحات**
PSD، یا سند فتوشاپ، نشان دهنده فرمت فایل اصلی فتوشاپ Adobe برای طراحی و توسعه گرافیک می‌باشد.

## **مشخصات فرمت فایل**
داده‌ها در یک فایل PSD به صورت بایت‌های big-endian ذخیره می‌شود. این به این معناست که در هنگام خواندن یا نوشتن در پلتفرم ویندوز، باید صحیح و long integer ها را جابجا کنید. فرمت فایل فتوشاپ به پنج بخش اصلی تقسیم شده است. این فرمت دارای نشانگرهای طول مختلفی است که می‌توانند برای حرکت از یک بخش به بخش بعدی استفاده شوند. نشانگرهای طول عادتاً با بایت‌ها پر می‌شوند تا به نزدیک‌ترین فاصله 2 یا 4 بایتی برسند. پنج بخش اصلی عبارتند از:

- هدر فایل
- اطلاعات حالت رنگ
- منابع تصویر
- اطلاعات لایه و ماسک
- داده‌ی تصویر

برای پیروی از استاندارد، داده باید به تمام این فیلدها در بخش نوشته شود، زیرا فتوشاپ ممکن است سعی کند کل بخش را بخواند. این همچنین به این معناست که باید صفرها به فیلدهای رد شده نوشته شوند در هنگام نوشتن به یک فایل. فیلد طول در بخش‌های طول-محدود باید برای تصمیم‌گیری در مورد کیفیت خواندن استفاده شود. در اغلب موارد، فیلد طول تعداد بایت‌ها را نشان می‌دهد، نه رکورد‌ها که دنبال می‌شوند. موارد زیر باید در هنگام خواندن یک فایل‌ به یاد داشته شود.

- مقادیر در ستون "طول" در تمام جدول‌ها به بایت‌ها می‌باشند.
- همه مقادیر تعریف شده به عنوان رشته یونیکد از شامل میشود: 
- فیلد طول 4 بایتی، نشان‌دهنده تعداد کاراکترها در رشته است (نه بایت).
- رشته‌ای از مقادیر یونیکد، دو بایت برای هر کاراکتر.

## **ویژگی‌های فرمت**
فایل‌های PSD ممکن است شامل لایه‌های تصویر، لایه‌های تنظیم، ماسک‌های لایه، حاشیه نویسی، اطلاعات فایل، کلمات کلیدی و سایر عناصر خاص فتوشاپ باشند. فایل‌های فتوشاپ دارای پسوند پیش‌فرض .PSD بوده و ارتفاع و عرض حداکثر ۳۰٬۰۰۰ پیکسل و حداکثر طول ۲ گیگابایت را دارا هستند.

## **نحوه استفاده‌ی این فرمت**
1. ابزار برای برش PSD
1. [تبدیل PSD](psd/fa/net/converting-psd-image-to-raster-format/) به HTML
1. استفاده از [PSD به عنوان یک قالب](psd/fa/net/using-psd-files-as-templates-for-automation-business-cards-case/) برای ایمیل
1. PSD به HTML CMS خاص
1. Identikit در فایل PSD (اسکچ پلیس)
1. ایجاد تصاویر پیش‌نمایش شبیه‌سازی شده ۳D با استفاده از اشیاء هوشمند برای اجناسی مانند بطری، فناج، تیشرت و غیره
1. ویرایش سریع PSD: خودکار تن، پیش‌تنظیمات، اشیاء هوشمند، برش تصویر لایهٔ متن

و بسیاری دیگر. اگر با Aspose.PSD کار بزرگی انجام داده‌اید، لطفاً مطالعه‌ی موردی خود را با [انجمن‌های Aspose](https://forum.aspose.com/) به اشتراک گذارید.

می‌توانید از مثال‌های دیگر نیز یاد بگیرید:

- [مطالعات موردی](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [نمونه‌کارها](psd/fa/net/showcases-html/)
