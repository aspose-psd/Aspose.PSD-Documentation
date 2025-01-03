---
title: تلاش برای تصاویر PNG
type: docs
weight: 30
url: /fa/java/manipulating-png-images/
---

## **تعیین شفافیت برای تصاویر PNG**
یکی از مزایای ذخیره تصاویر در قالب PNG این است که PNG می‌تواند پس زمینه شفاف داشته باشد. Aspose.PSD برای Java امکان تعیین شفافیت برای کلاس‌های PngImage و RasterImage را ارائه می‌دهد که در بخش زیر نشان داده شده است. از Aspose.PSD برای جاوا می‌توان برای تعیین هر رنگی به عنوان شفاف هنگام ایجاد تصاویر PNG جدید یا تبدیل تصاویر موجود به فرمت PNG استفاده کرد. به این منظور، Aspose.PSD API برای جاوا خاصیت TransparentColor و شمارش PngColorType را ارائه کرده است که می‌تواند برای تعیین هر رنگی که به عنوان شفاف در تصویر PNG نمایش داده شود، تنظیم شود. کد قطعه زیر نشان می‌دهد چگونه با استفاده از سازنده overloaded PngImage و مشخص کردن رنگ مورد نظر به عنوان شفاف، یک تصویر PSD موجود را به تصویر PNG تبدیل کنیم.

## **تنظیم وضوح برای تصاویر PNG**
Aspose.PSD برای Java کلاس ResolutionSetting را ارائه می‌دهد که می‌توان از آن برای تنظیم وضوح برای تمام فرمت‌های تصویر شامل PNG استفاده کرد. این مقاله نحوه استفاده از Aspose.PSD برای Java API برای تنظیم پارامترهای وضوح افقی و عمودی برای فرمت تصویر PNG را نشان می‌دهد. قطعه کد زیر یک تصویر PSD موجود را بارگذاری می‌کند و آن را به فرمت PNG تبدیل می‌کند و همچنین وضوح را تغییر می‌دهد.

## **فشرده‌سازی فایل‌های PNG**
قالب Portable Network Graphic (PNG) یک فرمت فشرده‌سازی بدون از دست دادن برای ارسال یک نقطه نظر راهبردی از شبکه‌ها می‌باشد. هنگامی که یک تصویر را در برنامه‌ای به عنوان یک فایل PNG ذخیره می‌کنید، ممکن است بخواهید یک سطح فشرده‌سازی را در محدوده از 0 تا حداکثر انتخاب کنید. تنظیم این مقدار به واقعیت اندازه فایل را فشرده می‌کند و کیفیت تصویر را کاهش نمی‌دهد. این مقاله توضیح می‌دهد که چگونه API‌های Aspose.PSD به شما امکان می‌دهند که اندازه فایل PNG را کنترل کنید. API‌های Aspose.PSD برای تنظیم سطح‌های فشرده‌سازی برای فرمت فایل PNG از کلاس PngOptions استفاده می‌کنند که شامل خاصیت نوع فشرده‌سازی از نوع int است. این خاصیت یک مقدا را از 0 تا 9 که 9 حداکثر فشرده‌سازی است، می‌پذیرد. قطعه کد زیر نشان می‌دهد چگونه سطوح فشرده‌سازی را با استفاده از API Aspose.PSD برای Java تنظیم کنیم.

## **تعیین عمق بیت برای تصاویر PNG**
عمق بیت در تصویربرداری تعداد بیت‌های استفاده شده برای نشان دادن رنگ یک پیکسل تنها در یک تصویر Bitmap است. مانند سایر فرمت‌های bitmap دیگر، عمق رنگ PNG نیز به بیت نشان داده می‌شود مانند ۱-بیت (2 رنگ)، ۲-بیت (۴ رنگ)، ۴-بیت (۱۶ رنگ) و ۸-بیت (۲۵۶ رنگ). API Aspose.PSD برای جاوا برای تنظیم عمق بیت برای تصاویر PNG با استفاده از خاصیت BitDepth که توسط کلاس PngOptions ارائه شده است، استفاده می‌کند. در حال حاضر تنها خاصیت BitDepth را می‌توان برای نوع‌های رنگ خاکستری و رنگ‌های نمایه‌ای به ۱، ۲، ۴ یا ۸ بیت تنظیم کرد. کد قطعه زیر نشان می‌دهد چگونه بت‌های عمق رنگ PNG را تعیین کنیم.

## **اعمال روش‌های فیلتر بر تصاویر PNG**
Aspose.PSD برای Java از شمارش PngFilterType استفاده می‌کند که می‌توان از آن برای تنظیم نوع فیلتر برای تصویر PNG استفاده کرد. قطعه کد زیر نشان می‌دهد که چگونه فیلتری را بر روی یک فایل PSD موجود به تصویر PNG با استفاده از PngFilterType  اعمال کرد.

## **تغییر رنگ پس‌زمینه تصویر PNG شفاف**
تصاویر فرمت PNG می‌توانند پس‌زمینه شفاف داشته باشند. Aspose.PSD برای Java امکان تغییر رنگ پس‌زمینه تصویر PNG دارای پس‌زمینه شفاف را فراهم می‌کند. API Aspose.PSD برای Java برای تنظیم/تغییر رنگ یک تصویر PNG شفاف استفاده می‌شود. قطعه کد زیر نشان می‌دهد چگونه رنگ پس‌زمینه یک تصویر PNG شفاف را تعیین/تغییر می‌دهد.
