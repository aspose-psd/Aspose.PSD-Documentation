---
title: برش، چرخش و تغییر اندازه تصاویر
type: docs
weight: 40
url: /fa/net/crop-rotate-and-resize-images/
---

## **برش تصاویر**
برش تصویر معمولا به حذف بخش‌های خارجی تصویر برای بهبود چارچوب اشاره دارد. برش همچنین ممکن است برای بریدن بخشی از تصویر برای افزایش تمرکز بر یک ناحیه خاص استفاده شود. رابط کاربری Aspose.PSD دو روش مختلف برای برش تصویر پشتیبانی می‌کند: با شیفت و مستطیل.
### **برش با شیفت**
کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) نسخه پر تنظیم متد Crop را فراهم می‌کند که 4 مقدار integer را به عنوان چپ، راست، بالا و پایین قبول می‌کند. بر اساس این چهار مقدار، متد Crop حدود تصویر را به سمت مرکز تصویر حرکت می‌دهد در حالی که بخش خارجی را دور می‌نگارد. کد زیر نشان می‌دهد چگونه تصویر را با شیفت برش دهیم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyShifts-CroppingbyShifts.cs" >}}
### **برش با مستطیل**
کلاس [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage) نسخه دیگری از متد Crop دارد که یک نمونه از کلاس Rectangle را قبول می‌کند. شما می‌توانید هر بخشی از تصویر را با تعیین مرزهای مورد نظر به شیء Rectangle ببرید. کد زیر نشان می‌دهد چگونه می‌توان به هر تصویری با مستطیل برش داد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-CroppingbyRectangle-CroppingbyRectangle.cs" >}}
## **چرخش و برگرداندن تصویر**
Aspose.PSD برای .NET یک کتابخانه آسان برای استفاده است زیرا روش‌های ساده‌ای برای انجام عملیات پیچیده فراهم می‌کند. به عنوان مثال، Aspose.PSD برای .NET متد RotateFlip را برای کلاس پایه خود Image ارائه کرده است اگر یک برنامه نیاز به چرخش یک تصویر داشته باشد. بدون توجه به قالب تصویر، این کتابخانه می‌تواند عملیات خاص چرخه و برگردان را بر روی آن انجام دهد.
### **چرخش تصویر**
متد Image.RotateFlip می‌تواند برای چرخش تصویر به 90/180/270 درجه و برگرداندن تصویر به صورت افقی یا عمودی استفاده شود. متد Image.RotateFlip پارامتری از جنس RotateFlipType را قبول می‌کند که نوع چرخه و برگرداندن مورد نظر برای اعمال به تصویر را مشخص می‌کند. مراحل انجام چرخش و برگرداندن به سادگی به شرح زیر است:

1. بارگذاری تصویر با استفاده از متد کارخانه Load کلاس Image.
1. فراخوانی متد Image.RotateFlip هنگام مشخص کردن RotateFlipType مناسب.
1. ذخیره نتایج.

مثال کد زیر نشان می‌دهد چگونه خاصیت RotateFlip یک Image و شماره‌گذاری RotateFlipType انجام می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImage-RotatinganImage.cs" >}}
## **چرخش تصویر به زاویه خاص**
API Aspose.PSD برای .NET متد [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate را برای کاربران خود که می‌خواهند یک تصویر را به یک زاویه خاص چرخاندن ارائه دهند. برخلاف متد [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).RotateFlip، متد [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate سه پارامتر را قبول می‌کند:

1. زاویه چرخش: یک پارامتر از نوع float که زاویه چرخش تصویر را مشخص می‌کند. مقدار مثبت تصویر را به صورت ساعتگرد چرخانده و مقدار منفی چرخه‌ای در جهت عقربه‌های ساعت انجام می‌دهد.
1. تغییر اندازه به نسبت: یک پارامتر از نوع Boolean که مشخص می‌کند آیا اندازه تصویر باید بر اساس پروژکشن‌های مستطیل چرخه‌ای (نقاط چنگال) چرخش یابد یا خیر. اگر بر روی نادرست تنظیم شود، ابعاد تصویر نامتماس خواهند بود و فقط محتویات داخلی تصویر چرخه‌ای می‌شوند.
1. رنگ پس‌زمینه: یک پارامتر از نوع Color که رنگی که در پس‌زمینه تصویر چرخه‌ای پر شود را مشخص می‌کند.

کد زیر نشان می‌دهد چگونه از متد [RasterImage](https://reference.aspose.com/psd/net/aspose.psd/rasterimage).Rotate استفاده کنیم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-RotatinganImageonaSpecificAngle-RotatinganImageonaSpecificAngle.cs" >}}
## **تغییر اندازه تصاویر**
این مقاله نحوه استفاده از Aspose.PSD برای .NET برای انجام عملیات Resize بر روی تصویر را نشان می‌دهد. این API‌ها روش‌های موثر و آسان برای دستیابی به این هدف ارائه کرده‌اند. Aspose.PSD برای .NET تمد Resize را برای کلاس Image ارائه کرده است که می‌توان از آن برای تغییر اندازه تصاویر موجود به صورت پویا استفاده کرد. دو نسخه از Resize وجود دارد تا نیازهای برنامه را منطبق سازد.
### **تغییر اندازه ساده**
مراحل اجرای Resize به شرح زیر است:

1. بارگذاری تصویر با استفاده از متد کارخانه Load کلاس Image.
1. فراخوانی متد Image.Resize در هنگام مشخص کردن ارتفاع و عرض جدید.
1. ذخیره نتایج.

مثال کد زیر نشان می‌دهد چگونه یک تصویر را تغییر اندازه دهیم.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-SimpleResizing-SimpleResizing.cs" >}}
### **تغییر اندازه با شماره‌گذاری ResizeType**
API Aspose.PSD شماره‌گذاری ResizeType را ارائه داده است که با Image.Resize برای دستیابی به نتایج مطلوب استفاده می‌شود. مثال کد ارائه شده در زیر استفاده از شماره‌گذاری ResizeType را نشان می‌دهد، در حالی که جزئیات اعضای شماره‌گذاری ResizeType می‌تواند در پایین این صفحه پیدا شود.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizingwithResizeTypeEnumeration-ResizingwithResizeTypeEnumeration.cs" >}}



اگر قصد دارید بعد از اعمال تغییر اندازه نتیجه با کیفیتی را بدست آورید، پیشنهاد می‌شود همواره از ResizeType.LanczosResample استفاده کنید زیرا نتایج بسیار کیفیتی ارائه می‌دهد اما ممکن است کار کندتر از ResizeType.NearestNeighbourResample. به علاوه، الگوریتم ResizeType.NearestNeighbourResample به طور خاص برای تغییر اندازه سریع استفاده می‌شود اما به همراه کاهش کیفیت تصویر. این روش ممکن است برای تولید تصویر انگشتی به‌صورت زمان واقعی یا پردازش‌های مشابه که نیاز به عملکرد دارد، مفید باشد.
## **تغییر اندازه تصویر به صورت واگذاری**
شما می‌توانید تصاویر را با گذر دادن مقادیر ارتفاع و عرض جدید به متد Image.Resize تغییر اندازه دهید اما در این صورت باید نسبت ابعاد را خودتان محاسبه کنید. این به این دلیل است که هنگامیکه عرض یا ارتفاع تصویر تغییر می‌کند، تصویر یا به مقدار بزرگ یا به اندازه کوچک تعیین شده به منظور پر کردن اندازه جدید اسکال یا تورق خواهد شد. اگر تغییرات ارتفاع و عرض تصویر در نسبت نباشد ممکن است به نتیجه کشیده و خواصیده منتج شود. این مقاله نحوه استفاده از API Aspose.PSD برای .NET برای تغییر اندازه تصاویر با گذاشتن ارتفاع یا عرض جدید را نشان می‌دهد درحالیکه به API اجازه حساب کردن مقدار متناسب دیگر را می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingAndFormattingImages-ResizeImageProportionally-ResizeImageProportionally.cs" >}}
### **شماره‌گذاری ResizeType**
شماره‌گذاری ResizeType نوع تغییر اندازه انجام شده بر اساس فیلتر انتخاب‌شده را مشخص می‌کند.

اعضای شماره‌گذاری [ResizeType](https://reference.aspose.com/psd/net/aspose.psd/resizetype)

|**نام عضو**|**مقدار**|**توضیحات**|
| :- | :- | :- |
|LeftTopToLeftTop|0|نقطه بالا چپ تصویر جدید با نقطه بالا چپ تصویر اصلی هم‌خوانی خواهد داشت. اگر لازم باشد بریده خواهد شد.|
|RightTopToRightTop|1|نقطه بالا راست تصویر جدید با نقطه بالا راست تصویر اصلی هم‌خوانی خواهد داشت. اگر لازم باشد بریده خواهد شد.|
|RightBottomToRightBottom|2|نقطه پایین راست تصویر جدید با نقطه پایین راست تصویر اصلی هم‌خوانی خواهد داشت. اگر لازم باشد بریده خواهد شد.|
|LeftBottomToLeftBottom|3|نقطه پایین چپ تصویر جدید با نقطه پایین چپ تصویر اصلی هم‌خوانی خواهد داشت. اگر لازم باشد بریده خواهد شد.|
|CenterToCenter|4|مرکز تص
