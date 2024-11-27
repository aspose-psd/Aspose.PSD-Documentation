---
title: تغییر تصاویر TIFF
type: docs
weight: 50
url: /fa/net/manipulating-tiff-images/
---

## **افزودن قاب ها با تنظیمات مختلف**
TIFF یک فرمت بسیار انعطاف پذیر است و امکان افزودن قاب‌های مختلف با ابعاد، فشرده‌سازی و سایر تنظیمات متفاوت را فراهم می‌کند. API‌های Aspose.PSD به شما امکان اضافه کردن هر قاب TIFF به هر اندازه‌ای را می‌دهند که به ایجاد اسناد پیچیده کمک می‌کند. اگر نیاز به تنظیم مجدد قاب‌ها در طول فرآیند افزودن به منظور تطبیق آنها برای تمامیت داشته باشید، مراحل زیر را انجام دهید:

- یک قاب خالی جدید با گزینه‌های موردنظر ایجاد کنید یا قاب منبع را با گزینه‌های خروجی مشخص‌شده با استفاده از متد CreateFrameFrom کپی کنید.
- قاب/تصویر منبع را به ابعاد موردنظر با استفاده از متد Resize تغییر اندازه دهید.
- پیکسل‌های قاب/تصویر منبع را به قاب جدید اضافه کنید.
- قاب جدید را به تصویر TIFF خروجی اضافه کنید.

## **صدور لایه‌های تصویر PSD به فرمت فایل Tiff صفحه چندگانه**
گاهی اوقات نیاز به صدور لایه‌های تصویر PSD به فرمت فایل TIFF چند صفحه‌ای است. این مقاله نشان می‌دهد چگونه می‌توان با استفاده از API Aspose.PSD برای .NET این کار را انجام داد. ابتدا تصویر PSD را از دیسک بارگیری کنیم. سپس بر روی لایه‌های تصویر PSD حرکت می‌کنیم و TiffFrame از لایه‌های مربوطه ایجاد می‌کنیم. در نهایت، تصویر Tiff حاصل را در یک فایل تکی بر روی دیسک ذخیره می‌کنیم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-ExportToMultiPageTiff-ExportToMultiPageTiff.cs" >}}

## **پیکربندی گزینه‌های Tiff**
توسعه‌دهندگان می‌توانند ویژگی‌های مختلف کلاس [TiffOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions) را تنظیم کنند تا نتایج موردنظر را دریافت کنند. در این مستند، به 4 ویژگی اصلی که کنترل ویژگی‌های تصویر نهایی را تعیین می‌کند، تمرکز خواهیم کرد.

این ویژگی‌ها در زیر لیست شده‌اند.

1. [TiffOptions.Photometric](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/photometric)
1. [TiffOptions.Compression](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/compression)
1. [TiffOptions.BitsPerSample](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/bitspersample)
1. [TiffOptions.Predictor](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/tiffoptions/properties/predictor)

هرگاه یک ساختار TiffOptions خالی را مقدماتی می‌سازیم، هر گزینه به مقدار پیش‌فرض خود تنظیم می‌شود، به عنوان مثال فشرده‌سازی به مقدار هیچ، BitsPerSample به 1 و Photometric به MinIsWhite تنظیم می‌شود. ذخیره در این فرمت باعث سیاه و سفید شدن تصویر نهایی می‌شود و این رفتار مورد انتظار برای چنین ترکیب‌های گزینه‌هاست. برای به دست آوردن نتایج رنگی باید تمام ویژگی‌های فوق را با مقادیری که مطابق با فضای رنگ موردنظر هستند تنظیم کنید یا ساختار TiffOptions را با تنظیمات پیش‌فرض که در این مقاله بعدا بحث خواهد شد، مقدماتی کنید. در زیر جدولی آورده شده است که مقادیر پارامترهای مورد انتظار را که باید برای دستیابی به نتایج موردنظر تنظیم کنید، توضیح می‌دهد. لطفا توجه داشته باشید، شما باید همه 4 ستون را از طریق TiffOptions تنظیم کنید تا بتوانید هر تصویر بارگیری شده/ایجاد شده را به فرمت TIFF ذخیره کنید.

|**TiffOptions.Photometric**|**TiffOptions.Compression**|**TiffOptions.BitsPerSample**|**TiffOptions.Predictor**|
| :- | :- | :- | :- |
|پالت|LZW/بدون‌فشرده‌سازی|1/4/8/16 (حالت پالت، حالت رنگ) تنها کانال تکی|هیچ|
|MinIsWhite/MinIsBlack|LZW/بدون‌فشرده‌سازی|1/4/8/16 (حالت سطح خاکستری) تنها کانال تکی|هیچ|
|پالت|LZW/بدون‌فشرده‌سازی|8 (حالت پالت، حالت رنگ) تنها کانال تکی|افقی (فشرده‌سازی بیشتر برای LZW الگوهای مشابه)|
|MinIsWhite/MinIsBlack|LZW/بدون‌فشرده‌سازی|8 (حالت سطح خاکستری) تنها کانال تکی|افقی (فشرده‌سازی بیشتر برای LZW الگوهای مشابه)|
|RGB|LZW/بدون‌فشرده‌سازی|[8,8,8] (3 کانال RGB)|هیچ/افقی|
|RGB|LZW/بدون‌فشرده‌سازی|[8,8,8,8] (3 کانال RGB و یک کانال افزوده آلفا ممکن است از طریق TiffOptions.AlphaStorage تنظیم شود) در واقع تعداد هر کانال اضافی پشتیبانی می‌شود اما هر کانال باید به اندازه 8 بیتی باشد مانند [8,8,8,8,8,8]|هیچ/افقی|
همه 4 خاصیت باید از طریق TiffOptions تنظیم شوند تا هر فرمت تصویری را به فرمت Tiff ذخیره کنید. با استفاده از ترکیبات مختلف، برخی از مشاهده‌کنندگان (شامل نمایشگر عکس ویندوز) ممکن است به نمایش تصویر نهایی ارائه شده ابتدائی چون حمایت محدود آن‌ها، انکارکننده‌اند. در چنین مواردی، لطفا برای آزمایش‌های خود نمایشگر متفاوتی انتخاب نمایید.
### **تنظیمات پیش‌فرض برای کلاس TiffOptions**
برای تسهیل کاربران و جلوگیری از اشتباه تنظیم‌کردن نمونه TiffOptions، API Aspose.PSD برای .NET یک سازنده دیگر را آشکار ساخته است که یک پارامتر از نوع [TiffExpectedFormat](https://reference.aspose.com/psd/net/aspose.psd.fileformats.tiff.enums/tiffexpectedformat) را قبول می‌کند. بر اساس مقدار انتخابی از شمارشک(TiffExpectedFormat) ، API تمام ویژگی‌های اجباری برای نمونه TiffOptions را به منظور تولید نتایج موردنظر پیکربندی می‌کند. قبل از اینکه به کد نمونه برویم، اینجا جزییات فیلدها TiffExpectedFormat و مقادیر آن برای درک بهتر استفاده آورده شده است.


- TiffExpectedFormat.Default: تنظیم این فیلد به حالت پیش‌فرض مشابه ساختنگر پیش‌فرض کلاس TiffOptions با فشرده‌سازی تنظیم نشده و تعداد بیت در هر پیکسل (BitsPerPixel) به 1 تنظیم شود تا نتیجه سیاه و سفید ایجاد شود. توصیه می‌شود برای استفاده از این فیلد هنگامی که قرار است دیگر ویژگی‌های خاص فرمت تنظیم شود.
- TiffExpectedFormat.TiffCcitRle: اختصاص دادن این فیلد به RLE در حالی که نتیجه را در فرمت TIFF با 1 BitsPerPixel (سیاه و سفید) ذخیره می‌کند.
- TiffExpectedFormat.TiffCcittFax3: نسبت به رمزگذاری CCITT Fax3 در حین ذخیره نتیجه در فرمت TIFF با 1 BitsPerPixel (سیاه و سفید) خاص است.
- TiffExpectedFormat.TiffCcittFax4: نسبت به رمزگذاری CCITT Fax4 در حین ذخیره نتیجه در فرمت TIFF با 1 BitsPerPixel (سیاه و سفید) خاص است.
- TiffExpectedFormat.TiffDeflateBW: نسبت به فشرده‌سازی Deflate در حالی که نتیجه را در فرمت TIFF با 1 BitsPerPixel (سیاه و سفید) ذخیره می‌کند.
- TiffExpectedFormat.TiffDeflateRGB: نسبت به فشرده‌سازی Deflate در حالی که نتیجه را در فرمت TIFF با رنگ RGB ذخیره می‌کند.
- TiffExpectedFormat.TiffJpegRGB: نسبت به فشرده‌سازی Jpeg در حالی که نتیجه را در فرمت TIFF با رنگ RGB ذخیره می‌کند.
- TiffExpectedFormat.TiffJpegYCBCR: نسبت به فشرده‌سازی Deflate در حالی که نتیجه را در فرمت TIFF با رنگ YCBCR ذخیره می‌کند.
- TiffExpectedFormat.TiffLzwBW: نسبت به فشرده‌سازی LZW در حالی که نتیجه را در فرمت TIFF با 1 BitsPerPixel (سیاه و سفید) ذخیره می‌کند.
- TiffExpectedFormat.TiffLzwRGB: نسبت به فشرده‌سازی LZW در حالی که نتیجه را در فرمت TIFF با رنگ RGB ذخیره می‌کند.
- TiffExpectedFormat.TiffLzwRGBA: نسبت به فشرده‌سازی LZW در حالی که نتیجه را در فرمت TIFF با RGBA (رنگ با شفافیت) ذخیره می‌کند.
- TiffExpectedFormat.TiffNoCompressionBW: نسبت به فرمت TIFF بدون‌فشرده‌سازی در حالی که نتیجه را با 1 BitsPerPixel (سیاه و سفید) ذخیره می‌کند.
- TiffExpectedFormat.TiffNoCompressionRGB: نسبت به فرمت TIFF بدون‌فشرده‌سازی در حالی که نتیجه را با رنگ RGB ذخیره می‌کند.
- TiffExpectedFormat.TiffNoCompressionRGBA: نسبت به فرمت TIFF بدون‌فشرده‌سازی در حالی که نتیجه را با RGBA (رنگ با شفافیت) ذخیره می‌کند.

برای ایجاد یک نمونه از کلاس TiffOptions، کد زیر نحوه استفاده از فیلدهای TiffExpectedFormat را توضیح می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-TIFF-TiffOptionsConfiguration-TiffOptionsConfiguration.cs" >}}

## **پشتیبانی از فشرده‌سازی Deflate و Adobe Deflate**
فرمت فایل TIFF (Tagged Image File Format) انواع مختلفی از فشرده‌سازی را پشت
