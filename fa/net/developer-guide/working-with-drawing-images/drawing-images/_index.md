---
title: رسم تصاویر
type: docs
weight: 10
url: /fa/net/drawing-images/
---

## **رسم خطوط**
در این مثال از کلاس [گرافیک](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم اشکال خطی روی سطح تصویر استفاده می‌شود. برای نشان دادن عملیات، مثال یک تصویر جدید ایجاد می‌کند و خطوط را روی سطح تصویر با استفاده از متد [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) ارائه شده توسط کلاس گرافیک رسم می‌کند. ابتدا، ما یک PsdImage ایجاد می‌کنیم و ارتفاع و عرض آن را مشخص می کنیم.

هنگامی که تصویر ایجاد شد، از متد Clear ارائه شده توسط کلاس گرافیک برای تنظیم رنگ پس‌زمینه آن استفاده می‌کنیم. متد [DrawLine](https://reference.aspose.com/psd/net/aspose.psd/graphics/methods/drawline/index) کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم یک خط روی یک تصویر بین دو ساختار نقطه استفاده می‌شود. این متد چندین نسخه دارد که نمونه از کلاس Pen و جفت‌های مختلفی از نقاط یا ساختارهای Point/PointF را به عنوان آرگومان‌ها می‌پذیرد. کلاس Pen یک شی را برای رسم خطوط، منحنی‌ها و اشکال تعریف می‌کند. کلاس Pen چندین سازنده overloaded دارد که برای رسم خطوط با رنگ، عرض و قلم تعیین شده استفاده می‌شوند. کلاس SolidBrush برای رسم به صورت پیوسته با رنگ خاص استفاده می‌شود. در نهایت، تصویر به فرمت فایل bmp صدور می‌شود. کد مثال زیر نحوه رسم اشکال خطی روی سطح تصویر را نمایش می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingLines-DrawingLines.cs" >}}

## **رسم بیضی**
مثال رسم بیضی دوم در مجموعه رسم اشکال است. ما از کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم اشکال بیضی روی سطح تصویر استفاده خواهیم کرد. برای نشان دادن عملیات، مثال یک تصویر جدید ایجاد می‌کند و با استفاده از متد DrawEllipse ارائه شده توسط [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)، شکل بیضی را روی سطح تصویر رسم می‌کند. ابتدا، ما یک PsdImage ایجاد می‌کنیم و ارتفاع و عرض آن را مشخص می کنیم.

پس از ایجاد تصویر، یک شیء کلاس گرافیک ایجاد و مقداردهی می‌کنیم و رنگ پس‌زمینه تصویر را با استفاده از متد Clear کلاس گرافیک تنظیم می‌کنیم. متد DrawEllipse کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم شکل بیضی روی سطح تصویر مشخص شده توسط ساختار مستطیل استفاده می‌شود. این متد چندین نسخه دارد که نمونه‌های کلاس Pen و Rectangle/RectangleF یا جفتی از مختلفی از مختصات به عنوان آرگومان‌ها را بپذیر می‌کند. کلاس Pen یک شیء برای رسم خطوط، منحنی‌ها و اشکال تعریف می‌کند. کلاس Pen چندین سازنده overloaded دارد که برای رسم خطوط با رنگ، عرض و قلم تعیین شده استفاده می‌شوند. کلاس Rectangle یک مجموعه از چهار عدد صحیح است که مکان و اندازه یک مستطیل را نشان می‌دهد. کلاس Rectangle چندین سازنده overloaded دارد برای رسم ساختار مستطیل با اندازه و مکان مشخص شده. کلاس SolidBrush برای رسم به صورت پیوسته با رنگ خاص استفاده می‌شود. در نهایت، تصویر به فرمت فایل bmp صدور می‌شود. کد مثال زیر نحوه رسم شکل بیضی روی سطح تصویر را نشان می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingEllipse-DrawingEllipse.cs" >}}

## **رسم مستطیل**
در این مثال، ما شکل مستطیل را روی سطح تصویر رسم می کنیم. برای نشان دادن عملیات، مثال یک تصویر جدید ایجاد کرده و شکل مستطیل را روی سطح تصویر با استفاده از متد DrawRectangle ارائه شده توسط [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) کلاس رسم می‌کند. ابتدا، ما یک PsdImage ایجاد می‌کنیم و ارتفاع و عرض آن را مشخص می کنیم. سپس، با استفاده از متد Clear کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics)، رنگ پس‌زمینه تصویر را تنظیم می‌کنیم.

متد DrawRectangle کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم شکل مستطیل روی سطح تصویر مشخص شده توسط ساختار مستطیل استفاده می‌شود. این متد چندین نسخه دارد که نمونه‌های کلاس Pen و Rectangle/RectangleF یا جفتی از مختلفی از مختصات به عنوان آرگومان‌ها را بپذیر می‌کند. کلاس Rectangle یک مجموعه از چهار عدد صحیح است که مکان و اندازه یک مستطیل را نشان می‌دهد. کلاس Rectangle چندین سازنده overloaded دارد که برای رسم ساختار مستطیل با اندازه و مکان مشخص شده استفاده می‌کند. در نهایت، تصویر به فرمت فایل bmp صدور می‌شود. کد مثال زیر نحوه رسم شکل مستطیل روی سطح تصویر را نشان می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingRectangle-DrawingRectangle.cs" >}}

## **رسم قوس**
در این بخش از مجموعه رسم اشکال، قوس را روی سطح تصویر رسم خواهیم کرد. ما از متد DrawArc کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای نشان دادن عملیات بر روی تصویر BMP استفاده خواهیم کرد. ابتدا، ما یک PsdImage ایجاد می‌کنیم و ارتفاع و عرض آن را مشخص می کنیم. هنگامی که تصویر ایجاد شد، از متد Clear ارائه شده توسط کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای تنظیم رنگ پس‌زمینه آن استفاده می‌کنیم.

متد DrawArc کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم شکل قوس روی سطح تصویر استفاده می‌شود. DrawArc یک قسمت از یک بیضی را نشان می‌دهد که توسط ساختار مستطیل و یا جفتی از مختلفی از نقاط تعیین شده است. این متد چندین نسخه دارد که نمونه‌های کلاس‌های Pen و ساختارهای Rectangle / RectangleF یا جفتی از مختلفی از نقاط، یک عرض و یک ارتفاع را به عنوان آرگومان‌ها می‌پذیرند. در نهایت، تصویر به فرمت فایل bmp صدور می‌شود. کد مثال زیر نحوه رسم شکل قوس روی سطح تصویر را نشان می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}

## **رسم بیزیر**
در این مثال از کلاس [گرافیک](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم شکل بیزیر روی سطح تصویر استفاده می‌شود. برای نشان دادن عملیات، مثال یک تصویر جدید ایجاد می‌کند و شکل بیزیر روی سطح تصویر با استفاده از متد DrawBezier ارائه شده توسط [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) کلاس رسم می‌کند. ابتدا، ما یک PsdImage ایجاد می‌کنیم و ارتفاع و عرض آن را مشخص می کنیم. هنگامی که تصویر ایجاد شد، از متد Clear ارائه شده توسط کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای تنظیم رنگ پس‌زمینه آن استفاده می‌کنیم.

متد DrawBezier کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) برای رسم شکل بیزیه بر روی سطح تصویر تعریف شده توسط چهار ساختار نقطه استفاده می‌شود. این متد چندین نسخه دارد که نمونه‌های کلاس Pen و چهار جفت مرتب‌شده از مختلفی از مختصات یا چهار ساختار Point/PointF یا آرایه از ساختارهای Point/PointF را به عنوان آرگومان‌ها می‌پذیرند. کلاس Pen یک شیء برای رسم خطوط، منحنی‌ها و اشکال تعریف می‌کند. کلاس Pen چندین سازنده overloaded دارد که برای رسم خطوط با رنگ، عرض و قلم تعیین شده استفاده می‌شوند. در نهایت، تصویر به فرمت فایل bmp صدور می‌شود. کد مثال زیر نحوه رسم شکل بیزیر روی سطح تصویر را نشان می‌دهد.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingBezier-DrawingBezier.cs" >}}

## **رسم تصاویر با استفاده از قابلیت‌های اصلی**
Aspose.PSD یک کتابخانه است که امکانات ارزشمندی را ارائه می‌دهد از جمله ایجاد تصاویر از ابتدا. رسم با استفاده از قابلیت‌های اصلی مانند تلاطم اطلاعات بیتمپ تصویر، یا استفاده از قابلیت‌های پیشرفته مانند کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) و [GraphicsPath](https://reference.aspose.com/psd/net/aspose.psd/graphicspath) برای رسم اشکال بر روی سطح تصویر با کمک قلم‌ها و مدادهای م
