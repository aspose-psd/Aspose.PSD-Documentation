---
title: تبدیل فضای رنگی برای JPEG از طریق پروفایل‌های ICC
type: docs
weight: 60
url: /fa/net/color-space-conversion-for-jpeg-through-icc-profiles/
---

## **مدیریت رنگ برای فرمت JPEG**

این مقاله درباره استفاده از پروفایل‌های ICC برای انجام مدیریت فضای رنگی در هنگام بررسی فرمت JPEG با استفاده از API‌های Aspose.PSD صحبت می‌کند. فضای رنگی داخلی JPEG، YCbCr است، با این حال این [فرمت](https://reference.aspose.com/psd/net/aspose.psd/pixelformat) قادر است که فضاهای Grayscale، RGB، CMYK و YCCK را هم پذیرفته و در فضای متادیت تصویر ذخیره کند. API‌های Aspose.PSD عمدتاً در فضای رنگی RGB عمل می‌کنند بنابراین API باید تبدیل فضای رنگی به‌وازه و از وازه به رنگ را انجام دهد تا بتواند به درستی با فایل‌های JPEG برخورد کند. تبدیل‌های Grayscale به RGB و YCbCr به RGB با استفاده از تبدیل‌های ریاضی قابل انجام است، اما فضاهای CMYK و YCCK به راحتی به فضای رنگی RGB تبدیل نمی‌شوند.

API‌های Aspose.PSD باید تبدیل مستقیم از RGB به CMYK برای تصاویر JPEG دارای فضای رنگی CMYK انجام داد. از طرف دیگر، تصاویر دارای فضای رنگ YCCK نیازمند تبدیل از RGB به CMYK به YCCK است، که تبدیل CMYK به YCCK از تبدیل [ITU-R BT.601](https://wikipedia.org/wiki/Rec._601) استفاده می‌کند که برای کانال‌های اول تا سوم اعمال می‌شود و کانال k بدون تغییر باقی می‌ماند. به طور خلاصه، API‌های Aspose.PSD باید تبدیل‌های متقابل از فضاهای رنگی RGB و CMYK برای هر دو تصویر CMYK و YCCK انجام دهند و اینگونه تبدیل‌ها با کمک پروفایل‌های ICC که اساساً جدول‌های جستجو هستند که ویژگی‌های یک رنگ را توصیف کرده و در تبدیل‌های رنگی کمک می‌کنند انجام می‌شود.

## **پروفایل‌های ICC**
مکانیزم تبدیل ICC از "پروفایل‌ها" استفاده می‌کند که فضای رنگی منبع را به فضای رنگی مستقل از دستگاه CIELAB یا CIEXYZ نقشه‌برداری می‌کند. Aspose.PSD می‌تواند داده‌ها را به فضای رنگی دلخواه تبدیل کند تا وقتی از این دو فضای رنگی با پروفایل‌های اضافی استفاده نماید. بنابراین، برای تبدیل ICC، کاربر باید دو پروفایل - یک پروفایل RGB برای رسیدن به فضای رنگی داخلی CIE و یک پروفایل CMYK برای گرفتن ویژگی‌های رنگ CMYK - ارائه دهد. برای رسیدن به تبدیل CMYK به RGB، باید پروفایل‌ها را جابه‌جا کرد، یعنی؛ از پروفایل CMYK به‌عنوان پروفایل منبع استفاده کرد و از پروفایل RGB به‌عنوان پروفایل مقصد.

## **تبدیل رنگ برای JPEG از طریق پروفایل‌های ICC**
API‌های Aspose.PSD جزئیات را مخفی می‌کنند، امکان استفاده راحت از مکانیزم مشخص کردن پروفایل‌های ICC از طریق کلاس [JpegOptions](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions) فراهم می‌کنند. علاوه بر این، Aspose.PSD از پروفایل‌های نمونه SWOP، CMYK و sRGB که در هسته خود تعبیه شده است استفاده می‌کند بنابراین در اکثر موارد استفاده رایج، کاربر نیازی به جستجو برای هر پروفایل خاصی ندارد. یک معایب اینگونه اصلاحات وجود دارد، یعنی؛ این تبدیلات فضای رنگی برگشت‌ناپذیر هستند زیرا نمی‌توان انتظار داشت پس از تبدیل از RGB به CMYK و سپس از CMYK به RGB به رنگ یکسان برسیم به دلیل عدم تطابق فضاهای رنگی و پروفایل‌های رنگ متفاوت. شیوه زیر کد نشان می‌دهد که از API Aspose.PSD برای .NET برای مشخص کردن پروفایل‌های رنگی RGB و CMYK برای تصویر JPEG YCCK استفاده شده است. در مثال زیر پروفایل‌های رنگی RGB و CMYK تغییر می‌کنند و تصویر در فضای رنگی YCCK ذخیره می‌شود. توجه داشته باشید که این ویژگی‌های [RgbColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/rgbcolorprofile) و [CmykColorProfile](https://reference.aspose.com/psd/net/aspose.psd.imageoptions/jpegoptions/properties/cmykcolorprofile) برای تغییر داده‌های پیکسل برای فضای رنگی YCCK کار خواهد کرد. سایر فضاهای رنگی دیگر پروفایل‌های رنگی را برای بروزرسانی داده‌های رنگی با خود نخواهند آورد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingICCProfiles-ColorConversionUsingICCProfiles.cs" >}}

اگر پروفایل‌ها تنظیم نشده باشند، API Aspose.PSD برای .NET از پروفایل‌های پیش‌فرض استفاده خواهد کرد. مثال زیر از ویژگی‌های پروفایل‌های مقصد استفاده می‌کند که فضای رنگی مقصد را برای بیشتر تصاویر JPEG تغییر می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-Conversion-ColorConversionUsingDefaultProfiles-ColorConversionUsingDefaultProfiles.cs" >}}

