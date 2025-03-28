---
title: پردازش داده‌های خام
type: docs
weight: 50
url: /fa/net/raw-data-processing/
---

## **پردازش داده‌های خام**
برای بهبود عملکرد Aspose.PSD API، ما یک روش برای پردازش داده‌های خام با نسخه 2.4.0 معرفی کرده‌ایم. این پردازش داده‌های خام در حال حاضر داخلی استفاده می‌شود و دارای یک API خارجی است تا بتواند از خارج از کتابخانه استفاده شود و عملکرد کلی را بهبود بخشد. گاهی اوقات پردازش یکم پیچیده است و به توضیحاتی نیاز دارد. در حال حاضر پردازش داده‌های خام تنها برای فرمت BMP در دسترس است.

برای کمک به توسعه دهندگان برای بهبود عملکرد بهتر، API Aspose.PSD سیستمی برای پردازش داده‌های خام ارائه می‌دهد که دارای یک API خارجی برای سفارشی‌سازی است. توسعه دهندگان با فراخوانی متد‌های [LoadRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/loadrawdata/index) و [SaveRawData](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/saverawdata) می‌توانند از پردازش داده‌های خام استفاده کنند. این متد‌ها نیازمند تنظیم فرمت داده‌های خام مورد نظر هستند که با استفاده از کلاس [RawDataSettings](https://reference.aspose.com/psd/net/aspose.psd/rawdatasettings) قابل تعیین است. کلاس RawDataSettings به توسعه دهندگان امکان تعیین هر فرمت داده‌ی خام را می‌دهد. با این حال، برای به دست آوردن بهترین عملکرد باید از فرمت داده‌های خامی استفاده کنید که داده در آن ذخیره شده است. RawDataSettings تعریف شده در کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) به تعیین فرمت خام تصویر کمک می‌کند. هنگام گذراندن نمونه RawDataSettings به متد LoadRawData، داده به عنوان چیزی بدون هر گونه تبدیل باز می‌گردد و ممکن است باعث بهبود عملکرد شود. از سوی دیگر، شما باید از تمامی فرمت‌های مختلف داده‌های خام که گاهی به مقداری پیچیده هستند، مراقبت کنید.

برای سهولت در اجرای فرایند، با هزینه‌ی کمی از جریمه‌ی عملکرد، ممکن است فرمت RawDataSettings مورد نظر را با نمونه‌دهی و مقداردهی کلاس مورد نظر تعیین کنید. در برخی موارد امکان بازگرداندن داده‌های خام در فرمت مشخص نیست (برای مثال تبدیل از فضای رنگ CMYK به RGB در نسخه 2.4.0 در دسترس نیست). علاوه بر این، ممکن است مواردی وجود داشته باشد که پردازش داده‌های خام برای یک فرمت تصویر در دسترس نباشد. برای تشخیص اینکه آیا می‌توانید از خانواده متد‌های LoadRawData و SaveRawData استفاده کنید یا خیر، باید ویژگی [IsRawDataAvailable](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/israwdataavailable) را استعلام کنید.
### **بینایی**
برای فرمت داده‌های Pixel RGB فرمت‌های داده‌های خام مبتنی بر نمونه و مبتنی بر RGB موجود است. فرمت‌های داده‌های خام نمونه دار حاوی شاخص‌های ورودی پالت در محدوده 0..(2^تعداد بیت - 1) هستند. فرمت‌های داده‌های خام نمونه‌ای، 1، 2، 4 و 8 بیت در هر پیکسل هستند. بقیه فرمت‌های داده‌های خام مبتنی بر RGB هستند. هنگام بارگذاری داده‌های خام، مراقب باشید که باید کافی باشد بایت‌ها برای بارگذاری داده موجود باشد، در غیر این صورت یک استثناء مناسب پرتاب خواهد شد. می‌توانید به راحتی اندازه‌ی آرایه بایت را با ضرب اندازه خط تخمین بزنید تا خطاهای مورد نیاز را بدست آورید. اندازه‌ی خط می‌تواند متغیر باشد و به فرمت ذخیره‌سازی داده‌های خام بستگی دارد.

برای به دست آوردن بهترین عملکرد همیشه اندازه خط داده‌های خام را برابر با [RasterImage.RawLineSize](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawlinesize) قرار دهید. با این حال، گاهی اوقات ممکن است نیاز به اضافه کردن اندازه‌گیری دیگر به سطرهای داده‌های خام داشته باشید، یا کمتر کردن آن، و زمانی که این اتفاق می‌افتد اندازه‌گیری متفاوت ممکن است استفاده شود. اگر نیاز به زیرمجموعه ای از یک مستطیل تصویر وجود داشته باشد، آنگاه باید به شیفت‌های بیتی توجه داشته باشید که در فرمت پیکسل رنگ RGB نقش می‌بندد. برای مثال، فرض کنید یک تصویر با ابعاد 100x100 پیکسل و فرمت داده که 1 بیت در هر پیکسل دارد. می‌خواهید یک مستطیل داده‌های خام با موقعیت (7,0) و ابعاد (2,1)، یعنی دو پیکسل از x=7 و y=0 را بخواهید. در این حالت، شما باید ترتیب داده‌ها را به صورت زیر دریافت کنید:




![todo:image_alt_text](raw-data-processing_1.png)

این به این معناست که شما 2 بایت دریافت می‌کنید که بایت اول حاوی 7 پیکسل غیر مطلوب، سپس یک پیکسل مطلوب و بایت دوم حاوی یک پیکسل مطلوب و سپس 7 پیکسل غیرمطلوب است. ممکن است بپرسید چرا ما داده‌ها را شیفت نداده‌ایم و آن دو پیکسل را در یک بایت ترکیب نکردیم؟ پاسخ ساده است: برای حفظ عملکرد بالا. همه‌ی پردازش داخلی معمولاً با تمامی داده‌ها شروع شده از اولین پیکسل و تمام موجودیت‌ها تا انتهای آخرین پیکسل در حالت دسترسی است. وقتی به شیفت‌ها نیازی نداریم، عملکرد کاهش می‌یابد و کد زیادتر و بی‌دلیل پیچیده می‌شود. همیشه اندازه‌گیری کنید که بیت صحیح (نیازی به تعیین بایت صحیح نیست چرا که داده‌ها همواره با اولین بایت پر می‌شوند) که پیکسل‌های مطلوب آغاز می‌شود را محاسبه کنید. برای محاسبه بیت صحیح یک فرمول ساده ممکن است استفاده شود: (rect.Left * تعداد بیت) % 8.
### **تبدیل رنگ RGB فهرستی**
برای به دست آوردن بالاترین عملکرد ممکن، همیشه از تنظیم‌های منبع و مقصد داده‌های خام، فرمت‌های پیکسل و اندازه‌های خط یکسان استفاده کنید. با این حال، گاهی اوقات ممکن است نیاز به انجام تبدیل داده‌ها باشد. به عنوان مثال، ممکن است یک تصویر RGB 1 بیت در هر پیکسل را بارگذاری کنید و آن را با 2 بیت در هر پیکسل ذخیره کنید، یا یک تصویر RGB 4 بیت را بارگذاری کرده و محدوده رنگی آن را تا 2 بیت در هر پیکسل کاهش دهید. در هر دو مورد، باید یک تبدیل رنگ اعمال شود. تبدیل تصاویر RGB فهرستی گاهی پیچیده است و باید بدون تنظیمات انجام گردد. باید تعیین کنیم چگونه محدوده رنگ منبع به فضای رنگ مقصد نگاشت داده می‌شود. برای انجام این کار، ما داریم:

- تطابق پالت (DitheringMethods.PaletteConversion)
- نقشه داده‌های خام (DitheringMethods.PaletteIgnore)
- تبدیل سفارشی (DitheringMethods.CustomConverter)

در صورت استفاده از تبدیل پالت، فضای رنگ منبع سعی می‌کند تا بهترین تطابق را با فضای رنگ مقصد داشته باشد. به عنوان مثال فرض کنید یک تصویر 4 بیتی با رنگ‌های زیر داشته باشیم:
[0] RGB=0, 0, 0
[1] RGB=17, 17, 17
[2] RGB=34, 34, 34
[3] RGB=51, 51, 51
[4] RGB=68, 68, 68
[5] RGB=85, 85, 85
[6] RGB=102, 102, 102
[7] RGB=119, 119, 119
[8] RGB=136, 136, 136
[9] RGB=153, 153, 153
[10] RGB=170, 170, 170
[11] RGB=187, 187, 187
[12] RGB=204, 204, 204
[13] RGB=221, 221, 221
[14] RGB=238, 238, 238
[15] RGB=255, 255, 255

تصویر منبع به صورت زیر است:




![todo:image_alt_text](raw-data-processing_2.png)

و ما تصویر 4 بیتی را به تصویر 1 بیتی با رنگ پالت مشخص زیر تبدیل می‌کنیم:

[0] RGB = 0, 0, 0
[1] RGB = 255, 255, 255

در حالت تبدیل پالت، مبدل رنگ منبع رنگ منبع را می‌خواند و با استفاده از متد [GetNearestColorIndex](https://reference.aspose.com/psd/net/aspose.psd/icolorpalette/methods/getnearestcolorindex/index) پالت مقصد مشخص می‌کند. مقدار ویژگی [RasterImage.RawFallbackIndex](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/properties/rawfallbackindex) زمانی استفاده می‌شود که متد GetNearestColorIndex پالت مقصد شاخص خارج از محدوده‌ی داده است. این تبدیل رنگ‌های منبع را به رنگ‌های مقصد نزدیک به حالت انتقالی. می‌توانید نتیجه‌ی زیر را مشاهده کنید:


![todo:image_alt_text](raw-data-processing_3.png)

در حالت نقشه داده‌های خام، یک سناریو متفاوت استفاده می‌شود. پالت‌های رنگ منبع و مقصد به طور ساده نادیده گرفته می