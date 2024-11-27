---
title: تبدیل تصاویر
type: docs
weight: 20
url: /fa/net/converting-images/
---

## **تبدیل تصاویر به سیاه و سفید و طیف خاکستری**
گاهی اوقات ممکن است نیاز داشته باشید تصاویر رنگی را به سیاه و سفید یا طیف خاکستری برای مقاصد چاپ یا بایگانی تبدیل کنید. این مقاله استفاده از رابط برنامه نویسی Aspose.PSD برای .NET را برای رسیدن به این هدف با استفاده از دو روشی که در زیر آورده شده انجام می‌دهد.

- دودویی‌سازی
- طیف‌خاکستری
### **دودویی‌سازی**
برای درک مفهوم دودویی‌سازی، اهمیت دارد تا تصویر دودویی را تعریف کنیم؛ یعنی تصویر دیجیتالی که می‌تواند فقط دو مقدار ممکن برای هر پیکسل داشته باشد. معمولاً، دو رنگی که برای یک تصویر دودویی استفاده می‌شوند، سیاه و سفید هستند اگرچه هر دو رنگ ممکن است استفاده شود. دودویی‌سازی فرآیند تبدیل یک تصویر به بیسطح است که به معنای این است که هر پیکسل به عنوان یک بیت تبدیل می‌شود (0 یا 1) جایی که 0 عدم وجود رنگ را نشان می‌دهد و 1 به معنای وجود رنگ است. API Aspose.PSD برای .NET در حال حاضر از دو روش دودویی‌سازی پشتیبانی می‌کند.
#### **دودویی‌سازی با آستانه ثابت**
کد مثال زیر نحوه استفاده از دودویی‌سازی با آستانه ثابت را به شما نشان می‌دهد.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithFixedThreshold-BinarizationWithFixedThreshold.cs" >}}


#### **دودویی‌سازی با آستانه اتوسو**
کد مثال زیر نشان می‌دهد که نحوه اعمال دودویی‌سازی با آستانه اتوسو به تصویر چگونه است.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-BinarizationWithOtsuThreshold-BinarizationWithOtsuThreshold.cs" >}}


### **طیف‌خاکستری**
تبدیل به طیف‌خاکستری فرآیند تبدیل تصویر دست‌رسی به یک تصویر با رنگ‌های خاکستری ناپیوسته است. کد مثال زیر نشان می‌دهد که نحوه استفاده از تبدیل به طیف‌خاکستری چگونه است.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-Grayscaling-Grayscaling.cs" >}}


## **تبدیل لایه‌های تصویر GIF به تصویر TIFF**
گاهی اوقات لازم است لایه‌های یک تصویر PSD را به یک فرمت تصویر تخته رنگی دیگر تبدیل کرد تا نیاز برنامه‌ای را برآورده سازد. API Aspose.PSD از قابلیت برداشتن و تبدیل لایه‌های یک تصویر PSD به فرمت تصویر تخته رنگی دیگر پشتیبانی می‌کند. ابتدا یک نمونه تصویر ایجاد می‌کنیم و تصویر PSD را از دیسک محلی بارگذاری می‌کنیم، سپس هر لایه را در ویژگی لایه‌ها تکرار می‌کنیم. سپس بلوک را به تصویر TIFF تبدیل می‌کنیم. کد مثال زیر نشان می‌دهد که چگونه لایه‌های تصویر PSD را به تصاویر TIFF تبدیل کنیم.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-GIFImageLayersToTIFF-GIFImageLayersToTIFF.cs" >}}


## **تبدیل PSD CMYK به TIFF CMYK**
با استفاده از Aspose.PSD برای .NET، توسعه‌دهندگان می‌توانند فایل CMYK PSD را به فرمت TIFF CMYK تبدیل کنند. این مقاله نشان می‌دهد که چگونه فایل CMYK PSD را به فرمت TIFF CMYK صادر/تبدیل کنیم با Aspose.PSD. با استفاده از Aspose.PSD برای .NET می‌توانید تصویر‌های PSD را بارگذاری کرده و سپس می‌توانید از [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) کلاس مختلفی تنظیم کنید و تصویر را ذخیره یا صادر کنید. کد مثال زیر نشان می‌دهد که چگونه این قابلیت را دستیابی کنیم.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-CMYKPSDtoCMYKTiff-CMYKPSDtoCMYKTiff.cs" >}}


## **صادره کردن تصاویر**
علاوه بر یک مجموعه غنی از روش‌های پردازش تصویر، Aspose.PSD کلاس‌های ویژه‌ای برای تبدیل فرمت‌های فایل PSD به فرمت‌های دیگر ارائه می‌دهد. با استفاده از این کتابخانه، تبدیل تصاویر PSD بسیار ساده و بصورت غیرضعیف است. کلاس‌های ویژه‌ای برای این هدف در فضای‌نام [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) وجود دارد.

- [BmpOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/bmpoptions)
- [GifOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/gifoptions)
- [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions)
- [Jpeg2000Options](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpeg2000options)
- [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions)
- [PngOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/pngoptions)

صادره کردن تصاویر با Aspose.PSD برای .NET API بسیار آسان است. تنها چیزی که نیاز دارید، یک شیء از کلاس مناسب از فضای‌نام [ImageOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions) باشید. با استفاده از این کلاس‌ها، می‌توانید به راحتی هر تصویری که با Aspose.PSD برای .NET ساخته، ویرایش یا فقط بارگذاری شده است، به هر فرمت پشتیبانی‌شده دیگری صادر کنید.
## **ترکیب تصاویر**
این مثال از کلاس Graphics استفاده می‌کند و نشان می‌دهد چگونه دو یا چند تصویر را در یک تصویر کامل ترکیب کنیم. برای نشان دادن این عمل، این مثال یک PsdImage جدید ایجاد کرده و تصاویر را روی سطح کانونی با استفاده از متد افزوده شده Draw Image از کلاس Graphics رسم می‌کند. با استفاده از کلاس Graphics می‌توان دو یا چند تصویر را به گونه‌ای ترکیب کرد که تصویر حاصل به عنوان یک تصویر کامل بدون فضایی بین بخش‌های تصویر و بدون صفحه‌ها به نظر برسد. اندازه کانوس باید برابر با اندازه تصویر حاصل باشد. مثال کد زیر نحوه استفاده از متد [DrawImage](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawimage/index) از کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) را نشان می‌دهد تا چگونه تصاویر را در یک تصویر ترکیب کنیم.



{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CombiningImages-CombiningImages.cs" >}}

## **گسترش و قطع تصاویر**
API Aspose.PSD به شما امکان گسترش یا قطع تصویر در طول فرآیند تبدیل تصویر را می‌دهد. توسعه‌دهنده باید یک مستطیل با مختصات X و Y ایجاد کند و عرض و ارتفاع جعبه مستطیل را مشخص کند. مختصات X، Y و عرض، ارتفاع مستطیل، گسترش یا قطع تصویر بارگذاری شده را نشان می‌دهد. اگر در طول فرآیند تبدیل تصویر نیاز به گسترش یا قطع تصویر باشد، مراحل زیر را انجام دهید:

1. یک نمونه از کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) ایجاد کنید و تصویر موجود را بارگذاری کنید.
1. نمونه آبجکت کلاس ImageOption بسازید.
1. یک نمونه از کلاس [Rectangle](https://reference.aspose.com/psd/net/aspose.psd/rectangle) بسازید و مختصات X,Y و عرض، ارتفاع مستطیل را مقدمه دهید
1. متد [Save](https://reference.aspose.com/psd/net/aspose.psd/rasterimage/methods/save/index) کلاس RasterImage را فراخوانی کنید هنگامی که نام فایل خروجی، گزینه‌های تصویر و آبجکت مستطیل به عنوان پارامترها را منتقل می‌کنید.


{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ExpandandCropImages-ExpandandCropImages.cs" >}}

## **خواندن و نوشتن دیتای XMP به تصاویر**
XMP (Extensible Metadata Platform) استاندارد ISO است. XMP یک مدل داده، یک فرمت سریالیزاسیون و خواص اصلی برای تعریف و پردازش دیتای قابل انگشت‌نریزی را استاندارد می‌کند. همچنین رهنمودهایی برای جاسازی اطلاعات XMP به یک تصویر محبوب مانند JPEG ارائه می‌کند بدون اینکه خوانایی آنها توسط برنامه‌هایی که از XMP پشتیبانی نمی‌کنند را تخریب کند. با استفاده از Aspose.PSD برای .NET API توسعه‌دهندگان می‌توانند XMP metadata را از تصاویر بخوانند یا دیتای XMP را در تصاویر بنویسند. این مقاله نشان می‌دهد که چگونه می‌توان از داده‌های XMP خواند و آنها را در تصاویر نوشت.
### **ایجاد داده‌ی XMP، نوشتن آن و خواندن از فایل**
با کمک فضای‌نام Xmp، توسعه‌دهندگان می‌توانند یک شیء داده‌های XMP ایجاد و آن را در یک تصویر نوشت. کد مثال زیر نشان می‌دهد چگونه از
