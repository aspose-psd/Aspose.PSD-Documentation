---
title: تغییر دادن تصاویر JPEG
type: docs
weight: 30
url: /fa/net/manipulating-jpeg-images/
---

## **استفاده از کلاس ExifData برای خواندن و تغییر برچسب‌های EXIF تصاویر JPEG**
تقریباً تمام دوربین‌های دیجیتال (شامل گوشی‌های هوشمند)، اسکنرها و دیگر سیستم‌هایی که تصاویر را ذخیره می‌کنند، اطلاعات EXIF (تبادل فایل تصویری) در تصاویر را ذخیره می‌کنند. تنظیمات دوربین و اطلاعات صحنه توسط دوربین در فایل تصویر ضبط می‌شود. داده‌های EXIF شامل همچنین سرعت شاتر، تاریخ و زمانی که عکس گرفته شده است، فاصله کانونی، جبران اکسپوژر، الگوی اندازه‌گیری و اگر از فلاش استفاده شده باشد. APIهای Aspose.Imaging به توانایی استخراج اطلاعات EXIF از تصویر داده شده را به یک شیوه بسیار آسان و ساده فراهم کرده‌اند. توسعه‌دهندگان می‌توانند همچنین داده‌های EXIF را به تصاویر بنویسند یا اطلاعات موجود را به دلخواه خود تغییر دهند. Aspose.PSD کلاس [ExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/exifdata) برای خواندن، نوشتن و تغییر داده‌های EXIF را فراهم کرده است، جایی که فضای نام [Aspose.PSD.Exif.Enums](https://reference.aspose.com/psd/net/aspose.psd.exif.enums) حاوی شمارش‌های مربوطه استفاده شده در این فرایند می‌باشد.
### **خواندن داده‌های EXIF**
APIهای Aspose.PSD امکان خواندن داده‌های EXIF از یک تصویر داده شده را فراهم می‌کنند. مراحل زیر نشان می‌دهند چگونگی استفاده از کلاس ExifData برای خواندن اطلاعات EXIF از یک تصویر.

- تصویر PSD را با استفاده از متد Load فابریک بارگیری کنید.
- بین منابع PSD، تصویر کوچک Jpeg را پیدا کنید.
- یک نمونه از کلاس ExifData استخراج کنید.

اطلاعات مورد نیاز را دریافت کرده و آن‌ها را به کنسول بنویسید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.cs" >}}

در صورت نیاز، توسعه‌دهندگان می‌توانند نیز اطلاعات خاص را با استفاده از قطعه کد زیر دریافت کنند.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.cs" >}}
### **نوشتن و تغییر داده‌های EXIF**
با استفاده از APIهای Aspose.PSD، توسعه‌دهندگان می‌توانند اطلاعات EXIF جدید را نوشته و داده‌های EXIF موجود تصویر را تغییر دهند. هر دو فرآیند (نوشتن و تغییر) نیازمند بارگیری تصویر و گرفتن داده‌های EXIF به یک نمونه از کلاس ExifData می‌باشد. سپس می‌توانید به ویژگی‌های کلاس ExifData دسترسی پیدا کرده و آن‌ها را مطابق با نیازهای خود تنظیم نمایید. لطفاً توجه داشته باشید که تصاویر برای تغییر باید تصاویر Jpeg یا Tiff باشند که معمولاً تصاویر کوچک PSD هستند. کد نمونه برای نشان دادن استفاده به شرح زیر است:




{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.cs" >}}
## **استخراج تصاویر کوچک از منابع PSD**
تصاویر کوچک نسخه‌های کوچک‌تر از عکس‌ها هستند که برای نمایش یک بخش مهم از عکس به جای فریم کامل استفاده می‌شوند. برخی از فایل‌های تصویر (مخصوصاً فایل‌هایی که با یک دوربین دیجیتال گرفته شده‌اند) دارای تصویر کوچک هستند که در فایل تصاویر جای داده شده‌است. API Aspose.PSD امکان استخراج تصویر کوچک منابع PSD را فراهم می‌کند و آن را جداگانه بر روی دیسک ذخیره می‌کند. منبع تصاویر کوچک [ExifData.Thumbnail](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata/properties/thumbnail) دارای صفت thumbnail است که می‌تواند اطلاعات تصویر کوچک را بازیابی نماید. قطعه کد زیر نشان می‌دهد چگونه از آن استفاده کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


از رویکرد مطرح شده برای ذخیره تصویر کوچک در سایر فرمت‌های پشتیبانی شده استفاده کنید. اگر می‌خواهید اطلاعات تصویر کوچک را به سایر فرمت‌های تصویری مانند BMP و PNG صادر کنید، لطفاً از گزینه‌های صادر کردن تصویر دیگر استفاده کنید. 

### **استخراج تصاویر کوچک از بخش‌های JFIF**
امکاناً استخراج تصاویر کوچک از بخش ExifData یا JFIF منابع PSD تصویر وجود دارد. کد زیر نشان می‌دهد چگونه استخراج اطلاعات تصویر کوچک از بخش JFIF یا ExifData انجام می‌شود:




{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.cs" >}}


از رویکرد مطرح شده برای ذخیره تصویر کوچک در سایر فرمت‌های پشتیبانی شده استفاده کنید. اگر می‌خواهید اطلاعات تصویر کوچک را به سایر فرمت‌های تصویری مانند BMP و PNG صادر کنید، لطفاً از گزینه‌های صادر کردن تصویر دیگر استفاده کنید.
### **افزودن تصویر کوچک به بخش JFIF**
قطعه کد زیر نشان می‌دهد چگونه از خاصیت JFIF.Thumbnail برای افزودن تصویر کوچک به بخش JFIF تصویر PSD بارگذاری شده استفاده شود.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.cs" >}}


تصاویر کوچک با سایر داده‌های بخش نمی‌توانند بیش از ۶۵٬۵۴۵ بایت را اشغال کنند به دلیل مشخصات فرمت JPEG. 
در مواقعی که تصاویر بزرگ به عنوان یک تصویر کوچک تنظیم شوند، ممکن است استثناء ایجاد شود.

### **افزودن تصویر کوچک به بخش EXIF**
قطعه کد زیر نشان می‌دهد چگونه از خاصیت ExifData.Thumbnail برای افزودن تصویر کوچک به بخش EXIF تصویر PSD بارگذاری شده استفاده شود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}


در این حالت، API Aspose.PSD قادر به اندازه تصویر کوچک تخمین زده نمی‌شود، اما اندازه بخش داده‌های EXIF کلی را می‌توان بررسی کرد. این نباید بیشتر از ۶۵٬۵۳۵ بایت باشد.
## **استفاده از کلاس JpegExifData برای خواندن و تغییر برچسب‌های EXIF تصاویر JPEG**
APIهای Aspose.PSD کلاس [JpegExifData](https://reference.aspose.com/psd/net/aspose.psd.exif/jpegexifdata) را فراهم کرده‌اند که برای فرمت‌های تصویر Jpeg به منظور بازیابی و به‌روزرسانی اطلاعات EXIF اختصاصی استفاده می‌شود. این مقاله استفاده از کلاس JpegExifData را برای رسیدن به همان موارد نشان داده است. کلاس Aspose.PSD.Exif.JpegExifData به عنوان کانتینر داده‌های EXIF برای تصاویر Jpeg عمل کرده و به معنای بازیابی برچسب‌های استاندارد EXIF تصاویر Jpeg است.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.cs" >}}
### **فهرست کاملی از برچسب‌های EXIF**
قطعه کد فوق تعدادی از برچسب‌های EXIF را با استفاده از خصوصیت‌های ارائه شده توسط کلاس Aspose.PSD.Exif.JpegExifData خوانده است. فهرست کامل این خصوصیت‌ها اینجا در دسترس است. کد زیر تمام برچسب‌های EXIF را با استفاده از کلاس [System.Reflection.PropertyInfo](https://docs.microsoft.com/en-us/dotnet/api/system.reflection.propertyinfo?view=net-5.0) خواهد خواند.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.cs" >}}
## **تصحیح خودکار جهت تصاویر JPEG**


عکس‌ها ممکن است به آن‌ها به زاویه ۹۰ درجه، ۱۸۰ درجه، ۲۷۰ درجه یا بدون تغییر (جهت طبیعی) با یک دوربین گرفته شوند. بیشتر دوربین‌های دیجیتال اطلاعات جهت همراه با داده‌های تصویر به عنوان برچسب‌های EXIF تصاویر JPEG ذخیره می‌کنند. این اطلاعات می‌تواند برای انجام چرخش اتوماتیک بر روی تصاویر به منظور تصحیح جهت استفاده شود. API Aspose.PSD متد AutoRotate را برای کلاس JpegImage برای تصحیح خودکار جهت تصاویر JPEG فراهم می‌کند. در ادامه نحوه استفاده از متد AutoRotate با API Aspose.PSD برای .NET نش
