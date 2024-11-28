---
title: تلاط JPEG تصاویر
type: docs
weight: 20
url: /fa/java/manipulating-jpeg-images/
---

## **استفاده از کلاس ExifData برای خواندن و ویرایش تگ‌های EXIF تصاویر JPEG**


تقریباً همه دوربین‌های دیجیتال (شامل گوشی‌های هوشمند)، اسکنرها و سایر سیستم‌هایی که با تصاویر سروکار دارند، تصاویر را با اطلاعات EXIF (تبادل فایل تصویر) ذخیره می‌کنند. تنظیمات دوربین و اطلاعات صحنه توسط دوربین به فایل تصویر ضبط می‌شوند. اطلاعات EXIF شامل سرعت شاتر، تاریخ و زمان تاریخ‌گرفتن عکس، فاصله کانونی، جبران اشعه، الگوی اندازه‌گیری و اگر از چراغ فلش استفاده شده باشد را نیز شامل می‌شود. APIهای Aspose.Imaging امکان استخراج اطلاعات EXIF از یک تصویر داده شده را به صورت بسیار آسان و ساده فراهم کرده‌اند. توسعه‌دهندگان ممکن است اطلاعات EXIF را به تصاویر بنویسند یا اطلاعات موجود را براساس نیاز خود تغییر دهند. Aspose.Imaging کلاس ExifData را برای خواندن، نوشتن و تغییر داده‌های EXIF فراهم کرده است، در حالی که فضای نام Aspose.PSD.Exif.Enums، شامل تعریف‌های ضروری استفاده شده در این فرایند، می‌باشد.
### **خواندن اطلاعات EXIF**
APIهای Aspose.PSD، امکان خواندن اطلاعات EXIF از یک تصویر داده شده را فراهم می‌کنند. مراحل ارائه شده زیر نشان می‌دهند چگونگی استفاده از کلاس ExifData برای خواندن اطلاعات EXIF از یک تصویر.

- تصویر PSD را با استفاده از متد کارخانه Load بارگذاری کنید.
- بین منابع PSD، تصویر بندانگشتی JPEG را پیدا کنید.
- یک نمونه از کلاس ExifData استخراج نمایید.

اطلاعات مورد نیاز را به دست آورید و آن را در کنسول نویسی کنید.




{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTags-ReadAllEXIFTags.java" >}}



به علاوه، توسعه‌دهندگان می‌توانند اطلاعات معین را با استفاده از قطعه کد زیر دریافت کنند.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadSpecificEXIFTagsInformation-ReadSpecificEXIFTagsInformation.java" >}}
### **نوشتن و تغییر داده‌های EXIF**
با استفاده از APIهای Aspose.PSD، توسعه‌‌دهندگان می‌توانند اطلاعات EXIF جدید بنویسند و داده‌های موجود EXIF یک تصویر را تغییر دهند. هر دو فرایند (نوشتن و تغییر) نیازمند بارگذاری یک تصویر و گرفتن داده‌های EXIF به یک نمونه از کلاس ExifData هستند. سپس می‌توان به خصوصیاتی که توسط کلاس ExifData ارائه شده‌اند دسترسی پیدا کرد و آن‌ها را به شکل مورد نظر خود تغییر داد. لطفاً توجه داشته باشید که تصاویر برای تلاطر کردن باید تصاویر JPEG یا TIFF باشند که معمولاً بنگاه‌نامه‌های PSD هستند. کد نمونه برای نشان دادن استفاده به صورت زیر است:




{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-WritingAndModifyingEXIFData-WritingAndModifyingEXIFData.java" >}}
## **استخراج بنگاه‌نامه‌ها از منابع PSD**
بنگاه‌نامه‌ها نسخه‌های کوچک‌تر تصاویر هستند، برای نمایش یک بخش مهم از تصویر به جای قاب کامل استفاده می‌شوند. برخی از پرونده‌های تصویر (به ویژه آن‌هایی که با دوربین دیجیتال گرفته شده‌اند) شامل یک تصویر بنگاه‌نامه‌ای درون فایل هستند. API Aspose.PSD اجازه استخراج بنگاه‌نامه‌ها از منابع PSD را می‌دهد و این امکان را فراهم می‌کند که جداگانه در دیسک ذخیره شوند. منابع بنگاه‌نامه حاوی خصوصیت ExifData.Thumbnail هستند که می‌تواند داده‌های بنگاه‌نامه را بازیابی کند. فقره کد زیر نشان می‌دهد چگونه از آن استفاده کنیم.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



از روش بالا برای ذخیره بنگاه‌نامه در سایر فرمت‌های پشتیبانی شده استفاده کنید. اگر بخواهید داده‌های بنگاه‌نامه را به سایر فرمت‌های تصویری مانند BMP و PNG صدور کنید، لطفاً از گزینه‌های صدور تصویر دیگر استفاده کنید.


### **استخراج بنگاه‌نامه‌ها از بخش‌های JFIF**
همچنین امکان استخراج بنگاه‌نامه‌ها از بخش ExifData یا JFIF منابع بنگاه‌نامه‌ی PSD وجود دارد. کد زیر نشان می‌دهد چگونه استخراج داده‌های بنگاه‌نامه از بخش JFIF یا ExifData: 



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ExtractThumbnailFromPSD-ExtractThumbnailFromPSD.java" >}}



از روش بالا برای ذخیره بنگاه‌نامه در سایر فرمت‌های پشتیبانی شده استفاده کنید. اگر بخواهید داده‌های بنگاه‌نامه را به سایر فرمت‌های تصویری مانند BMP و PNG صدور کنید، لطفاً از گزینه‌های صدور تصویر دیگر استفاده کنید.
### **افزودن بنگاه‌نامه به بخش JFIF**
قطعه‌کد زیر نشان می‌دهد چگونه از خصوصیت JFIF.Thumbnail برای افزودن یک تصویر بنگاه‌نامه به بخش JFIF یک تصویر PSD بارگذاری شده استفاده کنیم.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToJFIFSegment-AddThumbnailToJFIFSegment.java" >}}

تصاویر بنگاه‌نامه با دیگر داده‌های بخش نمی‌توانند بیشتر از 65،545 بایت را داشته باشند به دلیل مشخصات فرمت JPEG. در مواردی که تصاویر بزرگ به عنوان بنگاه‌نامه تنظیم شوند، ممکن است استثناء ایجاد شود.


### **افزودن بنگاه‌نامه به بخش EXIF**
قطعه کد زیر نشان می‌دهد چگونه از خصوصیت ExifData.Thumbnail برای افزودن یک تصویر بنگاه‌نامه به بخش EXIF یک تصویر PSD بارگذاری شده استفاده کنیم.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}

در این حالت، API Aspose.PSD نمی‌تواند اندازه تصویر بنگاه‌نامه را تخمین بزند، اما می‌تواند اندازه بخش داده‌های کل نمایشگر EXIF را بررسی کند. این نمی‌تواند بیشتر از 65،535 بایت باشد.
## **استفاده از کلاس JpegExifData برای خواندن و ویرایش تگ‌های EXIF تصاویر JPEG**
APIهای Aspose.PSD کلاس JpegExifData را ارائه داده‌اند که اختصاصاً برای فرمت تصاویر JPEG به منظور بازیابی و به‌روزرسانی اطلاعات EXIF طراحی شده است. این مقاله استفاده از کلاس JpegExifData را برای دستیابی به همان نتیجه نشان می‌دهد. کلاس Aspose.PSD.Exif.JpegExifData به عنوان یک ظرف اطلاعات EXIF برای تصاویر JPEG عمل می‌کند، و روش‌های بازیابی تگ‌های استاندارد EXIF JPEG همانند زیر نشان داده شده است:




{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AddThumbnailToEXIFSegment-AddThumbnailToEXIFSegment.java" >}}
### **لیست کامل تگ‌های EXIF**
قطعه کد بالا چندین تگ EXIF را با استفاده از خصوصیت‌های ارائه شده توسط کلاس Aspose.PSD.Exif.JpegExifData خوانده است. لیست کامل این خصوصیت‌ها اینجا موجود است. کد زیر تمام تگ‌های EXIF را با استفاده از کلاس System.Reflection.PropertyInfo خواهد خواند.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-ReadAllEXIFTagList-ReadAllEXIFTagList.java" >}}
## **خودکار تنظیم جهت تصاویر JPEG**
عکس‌ها ممکن است با دوربین به 90°، 180°، 270° یا بدون چرخش (جهت عادی) گرفته شوند. اکثر دوربین‌های دیجیتال اطلاعات جهت گردان را به همراه داده‌های تصویر به عنوان تگ‌های EXIF تصاویر JPEG ذخیره می‌کنند. این اطلاعات می‌تواند برای انجام چرخش خودکار بر روی تصاویر به منظور تصحیح جهت استفاده شود. APIهای Aspose.PSD متد AutoRotate برای کلاس JpegImage برای انجام خودکار تصحیح جهت تصاویر JPEG فراهم می‌کند. اینجا نحوه استفاده از متد AutoRotate با API Aspose.PSD برای زبان جاوا آورده شده است.



{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-JPEG-AutoCorrectOrientationOfJPEGImages-AutoCorrectOrientationOfJPEGImages.java" >}}
## **پشتیبانی از JPEG-LS با CMYK و YCCK**


API Aspose.PSD برای زبان جاوا امکان ارائه پش
