---
title: تلاش‌های PNG
type: docs
weight: 40
url: /fa/net/manipulating-png-images/
---

## **مشخص کردن شفافیت برای تصاویر PNG**
یکی از مزایای ذخیره تصاویر به فرمت PNG این است که PNG می‌تواند پس زمینه شفاف داشته باشد. Aspose.PSD برای .NET امکان مشخص کردن شفافیت برای تصاویر PNG و تصاویر رستر را فراهم می‌کند که به‌صورت روشن در بخش زیر نشان داده شده است. می‌توان از API Aspose.PSD برای .NET برای تنظیم هر رنگ به عنوان شفاف هنگام ایجاد تصاویر PNG جدید یا تبدیل تصاویر موجود به فرمت PNG استفاده کرد. به این منظور، API Aspose.PSD برای .NET خاصیت [TransparentColor](https://reference.aspose.com/psd/net/aspose.psd/ipsdcolorpalette/properties/transparentcolor) و شماره شناسه PngColorType که می‌تواند تنظیم شود تا هر رنگی که در تصویر PNG شفاف باشد مشخص شود را ارائه داده است. کد ارائه‌شده زیر نمایش می‌دهد که چگونه یک تصویر PSD موجود را به تصویر PNG تبدیل کنیم و رنگ مورد‌نظر را به عنوان شفاف مشخص کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyTransparency-SpecifyTransparency.cs" >}}
## **تنظیم وضوح برای تصاویر PNG**
Aspose.PSD برای .NET کلاس ResolutionSetting را ارائه می‌دهد که می‌توان از آن برای تنظیم وضوح برای همه فرمت‌های تصویر از جمله PNG استفاده کرد. این مقاله نشان می‌دهد چگونه از API Aspose.PSD برای .NET برای تنظیم پارامترهای افقی و عمودی وضوح برای فرمت تصویر PNG استفاده شود. کد زیر یک تصویر PSD موجود را بارگذاری و به فرمت PNG تبدیل می‌کند و همچنین وضوح را تغییر می‌دهد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SettingResolution-SettingResolution.cs" >}}
## **فشرده‌سازی فایل‌های PNG**
فرمت تصویر شبکه‌ای قابل حمل (PNG) یک فرمت فشرده‌سازی بدون از دست دادن اطلاعات برای انتقال تصویر روی شبکه‌ها است. وقتی یک تصویر را به عنوان یک فایل PNG در هر برنامه ذخیره می‌کنید، ممکن است از شما بخواهد که یک سطح فشرده‌سازی به انتخاب کنید از 0 تا سطح بیشینه. تنظیم این مقدار در واقع اندازه فایل را فشرده‌سازی می‌کند و کیفیت تصویر را کاهش نمی‌دهد. این مقاله توضیح می‌دهد که API Aspose.PSD چگونه به شما اجازه می‌دهد تا اندازه فایل‌های PNG را کنترل کنید. API‌های Aspose.PSD برای تنظیم سطوح فشرده‌سازی برای فرمت فایل PNG از کلاس PngOptions استفاده می‌کنند که دارای خاصیت int type [CompressionLevel](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions/properties/compressionlevel) است. این خاصیت یک مقدار از 0 تا 9 را که 9 حداکثر فشرده‌سازی است قبول می‌کند. کد ارائه‌شده زیر نشان می‌دهد که چگونه از طریق API Aspose.PSD برای .NET سطوح فشرده‌سازی را تعیین کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-CompressingFiles-CompressingFiles.cs" >}}
## **مشخص کردن عمق بیت برای تصاویر PNG**
عمق بیت در تصویربرداری تعداد بیت‌های استفاده شده برای نشان دادن رنگ یک پیکسل تنها در یک تصویر بیتمپ است. مانند سایر فرمت‌های بیتمپ، عمق رنگ PNG نیز به بیت ارایه شده است مانند 1-بیت (2 رنگ)، 2-بیت (4 رنگ)، 4-بیت (16 رنگ) و 8-بیت (256 رنگ). به کمک خاصیت BitDepth که توسط کلاس PngOptions ارائه شده است، API Aspose.PSD برای .NET می‌تواند برای تصاویر PNG از عمق بیت استفاده کند. در حال حاضر، خاصیت BitDepth می‌تواند برای انواع رنگی با کدوم 1، 2، 4 یا 8 بیت برای خاک‌انگاشت و اندیس‌سازی تنظیم شود. برای سایر انواع رنگی تنها 8 بیت پشتیبانی می‌شود. کد ارائه‌شده زیر نشان می‌دهد که چگونه عمق بیت را برای یک تصویر PNG تنظیم کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-SpecifyBitDepth-SpecifyBitDepth.cs" >}}
## **اعمال روش‌های فیلتر بر روی تصاویر PNG**
عمق بیت در تصویربرداری تعداد بیت‌های استفاده شده برای نشان دادن رنگ یک پیکسل تنها در یک تصویر بیتمپ است. مانند سایر فرمت‌های بیتمپ، عمق رنگ PNG نیز به بیت ارایه شده است مانند 1-بیت (2 رنگ)، 2-بیت (4 رنگ)، 4-بیت (16 رنگ) و 8-بیت (256 رنگ). از BitDepth که توسط کلاس PngOptions ارائه شده است می‌توان برای تصاویر PNG استفاده کرد. در حال حاضر، خاصیت BitDepth برای انواع رنگ‌های خاکی و اندیس شده می‌تواند به 1، 2، 4 یا 8 بیت تنظیم شود. برای سایر انواع رنگ‌ها تنها 8 بیت پشتیبانی می‌شود. کد ارائه‌شده زیر نشان می‌دهد که چگونه عمق بیت را برای یک تصویر PNG تنظیم کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ApplyFilterMethod-ApplyFilterMethod.cs" >}}
## **تغییر رنگ پس‌زمینه تصویر PNG شفاف**
تصاویر فرمت PNG می‌توانند پس‌زمینه شفاف داشته باشند. Aspose.PSD برای .NET امکان تغییر رنگ پس‌زمینه تصویر PNG دارد که پس‌زمینه شفاف دارد. API Aspose.PSD برای .NET می‌تواند برای تنظیم/تغییر رنگ یک تصویر PNG شفاف استفاده شود. کد ارائه‌شده زیر نشان می‌دهد که چگونه رنگ پس‌زمینه تصویر PNG شفاف را تنظیم/تغییر دهیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PNG-ChangeBackgroundColor-ChangeBackgroundColor.cs" >}}
