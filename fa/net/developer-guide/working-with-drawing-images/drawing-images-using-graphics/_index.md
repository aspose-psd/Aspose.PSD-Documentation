---
title: رسم تصاویر با استفاده از گرافیک
type: docs
weight: 20
url: /fa/net/drawing-images-using-graphics/
---

## **رسم تصاویر با استفاده از گرافیک**
با کتابخانه Aspose.PSD می‌توانید شکل‌های ساده مانند خطوط، مستطیل‌ها و دایره‌ها را رسم کنید، همچنین شکل‌های پیچیده مانند چند‌ضلعی، منحنی‌ها، خم‌ها و شکل‌های بزیر را نیز. کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) که در فضای‌نام Aspose.PSD قرار دارد، این اشکال را ایجاد می‌کند. اشیاء گرافیکی مسئول انجام عملیات رسم مختلف روی تصویر هستند و در نتیجه سطح تصویر را تغییر می‌دهند. کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) از انواع اشیای کمکی برای بهبود اشکال استفاده می‌کند:

·         Pens، برای رسم خطوط، خطوط حاشیه ای یا بیان شکل‌های هندسی دیگر.

·         Brushes، برای تعریف نحوه پرشدن مناطق.

·         Fonts، برای تعریف شکل حروف متن.


### **رسم با استفاده از کلاس گرافیک**
در زیر، مثال کد نشان داده شده است که استفاده از کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) را نشان می‌دهد. کد منبع مثال به چند بخش تقسیم شده است تا ساده و آسان برای دنبال کردن باشد. گام‌به‌گام، مثال‌ها نشان می‌دهند چگونه باید:

1. تصویری ایجاد کنید.
2. یک شی از کلاس گرافیک بسازید و مقدماتی کنید.
3. سطح را پاک کنید.
4. یک بیضی بکشید.
5. یک چندضلعی پر شده بکشید و تصویر را ذخیره کنید.


### **نمونه‌های برنامه‌نویسی**
#### **ایجاد یک تصویر**
شروع به ایجاد یک تصویر کنید با استفاده از هر یک از روش‌های توصیف شده در ایجاد فایل‌ها.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

#### **ساخت و مقدماتی کردن یک شی از کلاس گرافیک**
سپس یک شی از کلاس گرافیک را با گذراندن شیء Image به سازنده‌اش، ایجاد و مقدماتی کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingArc-DrawingArc.cs" >}}

#### **پاک کردن سطح**
سطح گرافیک را با فراخوانی متد Clear کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) پاک کنید و رنگ را به عنوان پارامتر منتقل کنید. این متد سطح گرافیک را با رنگی که به عنوان آرگومان منتقل شده است پر کرده.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

#### **بکشیدن یک بیضی**
ممکن است توجه کنید که کلاس [Graphics](https://reference.aspose.com/psd/net/aspose.psd/graphics) تعداد بسیاری از متدها برای رسم و پر کردن اشکال اکتشاف کرده است. در مرجع API Aspose.PSD برای .NET لیست کامل متدها را پیدا خواهید کرد. چند نسخه از متد‌های DrawEllipse توسط کلاس گرافیک ارائه شده است. تمام این متدها یک شیء Pen را به عنوان اولین آرگومان خود می‌پذیرند. پارامترهای بعدی برای تعریف مستطیل محاط قایم دور بیضی منتقل می‌شوند. به منظور این مثال، از نسخه‌ای که یک شیء Rectangle را با عنوان دومین پارامتر برای رسم یک بیضی با استفاده از شیء Pen رنگی که مدنظر شماست استفاده کنید.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-CoreDrawingFeatures-CoreDrawingFeatures.cs" >}}

#### **بکشیدن یک چندضلعی پر شده**
سپس، یک چندضلعی با استفاده از LinearGradientBrush و یک آرایه از نقاط بکشید. کلاس گرافیک چندین نسخه از متد FillPolygon را بروز کرده است. همه‌ی این‌ها یک شیء Brush را به عنوان اولین آرگومان خود قبول می‌کنند که ویژگی‌های پر کردن را تعریف می‌کند. پارامتر دوم یک آرایه از نقاط است. توجه داشته باشید که هر دو نقطه متوالی در آرایه یک طرف چندضلعی را مشخص می‌کنند.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

### **رسم تصاویر با استفاده از گرافیک : منبع کامل**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-DrawingImages-DrawingUsingGraphics-DrawingUsingGraphics.cs" >}}

تمام کلاس‌هایی که IDisposable پیاده سازی می‌کنند و به منابع غیرمدیریت شده دسترسی دارند، در یک بیانیه Using نهاده می‌شوند تا اطمینان حاصل شود که به درستی کاهش داده‌اند.
